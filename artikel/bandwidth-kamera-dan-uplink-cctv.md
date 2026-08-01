---
article_id: CCT-06-02
title: "Menghitung bandwidth kamera dan uplink CCTV"
slug: "bandwidth-kamera-dan-uplink-cctv"
description: "Plan CCTV connectivity, addressing, bandwidth, time, segmentation, and network-delivered power."
status: draft
publication_date: "2025-09-18"
publication_date_basis: editorial_backfill
date_modified: null
parent_topic: CCT-06
primary_intent: "Estimate traffic per link with explicit bitrate and concurrency assumptions."
reader_community: "Tukang.co.id"
reader_address: "Teman Tukang.co.id"
final_route: "/artikel/bandwidth-kamera-dan-uplink-cctv.html"
technical_review: required
writing_contract_version: "native-id-v2"
sources:
  - "https://webstore.iec.ch/en/publication/7353"
  - "https://www.onvif.org/profiles/profile-t/"
  - "https://csrc.nist.gov/pubs/ir/8259/r1/final"
---

<!-- BEGIN MANAGED IMAGE PLAN
## Image plan

- **Image ID:** `LOCAL-001`
- **Source type:** `local`
- **Placement:** after the opening has answered the main question, before the first detailed H2
- **Exact Markdown to insert:** `![Ilustrasi CCTV Merk ZKTECO](/wp-content/uploads/2023/08/CCTV-Merk-ZKTECO.jpg)`
- **Caption/credit:** Aset lokal proyek; jangan klaim sebagai dokumentasi proyek tertentu.
- **Selection basis:** filename/source metadata identifies `CCTV Merk ZKTECO` as relevant content media; no pixels were inspected.
- **Hard boundary:** do not infer or describe unseen visual details, project ownership, location, people, brands, condition, performance, or outcome.
- **Substitution rule:** do not replace this image. If unavailable or provenance is incomplete, insert `[NEEDS IMAGE REVIEW: LOCAL-001]` and continue drafting the prose.
END MANAGED IMAGE PLAN -->

# Menghitung bandwidth kamera dan uplink CCTV

Halo, Teman Tukang.co.id! Bandwidth CCTV tidak ditentukan oleh jumlah kamera saja. Hitung bitrate aktual tiap stream, jumlah stream yang benar-benar melewati setiap link, lalu sisakan ruang untuk overhead dan lonjakan. Tanpa dua angka pertama itu, uplink yang tampak besar bisa tetap tersendat saat semua kamera aktif atau ketika operator membuka banyak tampilan.

Rumus awalnya sederhana: **total trafik link = jumlah stream aktif × bitrate per stream**. Bandingkan hasil dalam bit per detik dengan kapasitas link yang sama satuannya, kemudian uji pada kondisi terburuk yang masuk akal. Nilai pada lembar spesifikasi hanyalah asumsi sampai dikonfirmasi dari konfigurasi encoder dan pengukuran. [NEEDS SITE SURVEY AND MEASURED BITRATE: jumlah kamera, codec, resolusi, frame rate, pola gerak, serta stream yang melintasi tiap uplink belum diberikan.]

![Ilustrasi CCTV Merk ZKTECO](/wp-content/uploads/2023/08/CCTV-Merk-ZKTECO.jpg)


*Aset lokal situs; gambar ini bukan dokumentasi proyek tertentu.*

## Definisi dan batas objek

Bandwidth adalah laju data, biasanya Mbps atau Gbps; bukan kapasitas penyimpanan dalam TB. Kamera dapat memiliki main stream untuk rekaman dan substream untuk pratinjau. Keduanya dihitung terpisah bila keduanya aktif. Uplink adalah link antarswitch, dari switch ke server/NVR, atau dari lokasi ke jaringan lain. Satu kamera dapat menyumbang trafik berbeda pada masing-masing segmen.

Artikel ini membahas estimasi trafik, pemetaan jalur, concurrency (jumlah stream yang bersamaan), dan pemeriksaan sederhana. Ia tidak menetapkan desain final, rating kabel, konfigurasi VLAN, anggaran PoE, atau kapasitas penyimpanan tanpa data proyek. Panduan aplikasi CCTV IEC 62676-4 menekankan bahwa jumlah megapiksel atau demo produk saja tidak membuktikan hasil pengawasan yang berguna; kebutuhan adegan, pemasangan, pengujian, dan evaluasi objektif tetap diperlukan ([IEC 62676-4](https://webstore.iec.ch/en/publication/7353)).

## Cara kerjanya

Mulai dari daftar kamera. Catat identitas, codec, resolusi, frame rate, target bitrate (CBR atau VBR), main stream, substream, dan fitur tambahan seperti audio atau metadata. Jangan menjumlahkan angka penyimpanan harian untuk menggantikan bitrate jaringan; keduanya menjawab pertanyaan berbeda.

Selanjutnya gambar aliran datanya. Misalnya, kamera menuju access switch, lalu beberapa access switch menuju distribution switch, kemudian NVR. Untuk setiap link, hitung hanya stream yang melewatinya. Kamera di switch yang sama tidak otomatis membebani uplink sebelum datanya diteruskan ke NVR, workstation, cloud, atau lokasi lain. Tambahkan pula trafik playback, live view, event clip, sinkronisasi, dan administrasi bila jalurnya sama.

Gunakan langkah berikut:

1. Ubah semua bitrate ke Mbps (8 bit = 1 byte) dan tulis apakah angka itu rata-rata, puncak, atau batas konfigurasi.
2. Kalikan bitrate dengan jumlah stream aktif pada tiap jalur.
3. Tambahkan overhead protokol dan lonjakan VBR sebagai margin desain; tentukan margin itu bersama perancang jaringan, bukan dengan angka universal.
4. Cocokkan dengan kapasitas efektif port dan uplink, bukan label nominal saja.
5. Uji saat rekaman, live view, playback, dan event berjalan bersamaan.

ONVIF Profile T dapat menjadi petunjuk bahwa perangkat dan klien mendukung fungsi streaming tertentu, tetapi profil atau logo tidak membuktikan semua fitur opsional, kecocokan recorder, atau performa pada firmware yang Anda pilih ([ONVIF Profile T](https://www.onvif.org/profiles/profile-t/)). Verifikasi model, versi firmware, peran perangkat, dan alur yang benar-benar dipakai.

## Faktor yang mengubah hasil

Codec, detail gambar, cahaya, gerakan, dan pengaturan I-frame memengaruhi bitrate VBR. Dua kamera dengan resolusi sama dapat menghasilkan trafik berbeda. Audio, metadata analitik, dan stream tambahan juga menambah data. Saat banyak operator membuka tampilan, NVR bisa mengirim ulang stream ke beberapa klien; jalur NVR–switch, bukan hanya kamera–switch, yang kemudian menjadi titik padat.

Waktu juga penting. Rekaman terjadwal, deteksi gerak, dan event clip membuat concurrency berbeda. Tulis skenario normal dan skenario puncak: seluruh kamera merekam, sejumlah monitor menampilkan grid, satu operator melakukan playback, serta event mengirim klip. Jika sistem terhubung ke jaringan lain, hitung replikasi atau akses jarak jauh pada uplink tersebut.

Topologi, kecepatan port, duplex, antrian switch, dan jalur redundan mengubah kapasitas efektif. PoE menyelesaikan suplai daya, bukan otomatis menambah bandwidth. Kabel, terminasi, dan lingkungan yang tidak sesuai dapat memicu error atau retransmisi; angka throughput di atas kertas tidak menggantikan verifikasi fisik dan konfigurasi.

Pisahkan jaringan kamera dari akses umum sesuai kebutuhan, batasi layanan yang terbuka, dan catat akun serta jalur administrasi. NISTIR 8259 Rev. 1 menempatkan identitas perangkat, konfigurasi aman, perlindungan data, pembaruan, dan pengelolaan siklus hidup sebagai kemampuan yang perlu ditetapkan berdasarkan use case, bukan sekadar mengganti kata sandi bawaan ([NISTIR 8259 Rev. 1](https://csrc.nist.gov/pubs/ir/8259/r1/final)).

## Contoh keputusan praktis

Anggap ini contoh hitungan, bukan ukuran proyek: delapan kamera masing-masing dikonfigurasi 4 Mbps untuk main stream. Trafik menuju NVR adalah 8 × 4 = 32 Mbps sebelum overhead dan stream lain. Bila empat substream 0,8 Mbps melayani monitor pada jalur berbeda, jalur itu memerlukan 3,2 Mbps tambahan. Jika semua stream melewati satu uplink, jumlahkan 35,2 Mbps lalu masukkan margin dan trafik non-CCTV yang memang lewat di sana.

Gunakan tabel keputusan berikut saat menilai rancangan:

| Pertanyaan | Jika jawabannya “ya” | Konsekuensi pemeriksaan |
| --- | --- | --- |
| Apakah main stream dan substream melewati uplink yang sama? | Keduanya concurrency pada link itu. | Jumlahkan kedua bitrate, bukan jumlah kameranya saja. |
| Apakah live view memakai stream berbeda dari rekaman? | NVR atau klien dapat menggandakan trafik. | Hitung jalur keluar dari NVR dan jumlah monitor aktif. |
| Apakah bitrate VBR melonjak saat adegan ramai? | Nilai rata-rata meremehkan puncak. | Ambil log atau ukur pada adegan terpadat. |
| Apakah uplink membawa trafik kantor juga? | Kapasitas efektif terbagi. | Tetapkan prioritas dan ukur saat beban gabungan. |

Teman Tukang.co.id, simpan asumsi di lembar perhitungan: tanggal, konfigurasi encoder, jumlah klien, jalur stream, kapasitas port, dan skenario uji. Jika satu asumsi berubah, hitung ulang link yang terkena dampak; jangan mengubah angka total secara membabi buta.

## Kesalahan umum dan cara memeriksanya

Kesalahan pertama adalah mengalikan jumlah kamera dengan kapasitas port, misalnya menganggap sepuluh kamera pasti membutuhkan 10 × 100 Mbps. Port adalah batas kemampuan, sedangkan stream memakai bitrate yang dikonfigurasi. Kesalahan kedua adalah memakai total penyimpanan sebagai proksi bandwidth. Kesalahan ketiga adalah memeriksa kamera saat idle, lalu menyimpulkan jaringan aman ketika seluruh monitor dan event aktif.

Periksa counter interface untuk throughput, error, discard, dan retransmisi selama skenario yang disepakati. Bandingkan dengan log encoder dan log NVR agar Anda tahu apakah kemacetan berasal dari sumber, uplink, atau klien. Uji ulang setelah perubahan codec, frame rate, firmware, jumlah monitor, atau penambahan kamera. Hasil satu waktu tidak menjadi jaminan kapasitas seumur hidup.

Shortcut yang sering dipilih adalah membeli switch dengan uplink terbesar lalu menganggap masalah selesai. Itu bisa gagal bila concurrency tidak dipetakan, NVR menggandakan stream, atau port kamera dan kabel memiliki batas lain. Alternatif yang lebih dapat dipertanggungjawabkan adalah membuat matriks jalur, mengukur puncak, dan meminta review perancang jaringan untuk kapasitas, segmentasi, dan failover.

## Kesimpulan dan langkah berikutnya

Kawan Tukang.co.id, hitung bandwidth kamera dan uplink CCTV per link: jumlahkan bitrate semua stream yang benar-benar melintas pada skenario normal dan puncak, lalu verifikasi dengan pengukuran. Jangan memakai jumlah kamera, kapasitas port nominal, atau total penyimpanan sebagai pengganti bitrate dan concurrency.

Sebelum membeli atau mengubah konfigurasi, buat daftar kamera dan jalur, minta log bitrate puncak, jalankan uji gabungan rekaman–live view–playback, dan dokumentasikan hasilnya. [NEEDS TECHNICAL REVIEW: desain final, margin kapasitas, segmentasi, PoE, dan ketahanan link harus disetujui berdasarkan survei serta bukti perangkat dan instalasi yang aktual.] Aturan operasinya: setiap perubahan stream atau klien yang melewati uplink wajib memicu hitung ulang dan uji ulang.

Jika Anda membutuhkan survei lapangan, bawa matriks ini saat meminta [jual dan pasang CCTV di Yosowilangun](/kota/jual-pasang-cctv-yosowilangun/) atau [pendampingan pemasangan di Wungu](/kota/jual-pasang-cctv-wungu/); angka pada artikel tidak menggantikan pemeriksaan lokasi.
