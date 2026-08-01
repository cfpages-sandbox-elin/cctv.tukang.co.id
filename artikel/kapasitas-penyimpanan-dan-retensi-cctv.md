---
article_id: CCT-05-03
title: "Menghitung kapasitas penyimpanan dan retensi CCTV"
slug: "kapasitas-penyimpanan-dan-retensi-cctv"
description: "Size and evaluate recorders, storage, retention, redundancy, playback, and export."
status: draft
publication_date: "2025-08-28"
publication_date_basis: editorial_backfill
date_modified: null
parent_topic: CCT-05
primary_intent: "Estimate storage from cameras, bitrate, schedule, and retention."
reader_community: "Tukang.co.id"
reader_address: "Teman Tukang.co.id"
final_route: "/artikel/kapasitas-penyimpanan-dan-retensi-cctv.html"
technical_review: required
writing_contract_version: "native-id-v2"
sources:
  - "https://webstore.iec.ch/en/publication/7353"
  - "https://www.onvif.org/profiles/profile-t/"
  - "https://www.onvif.org/"
  - "https://csrc.nist.gov/pubs/ir/8259/r1/final"
  - "https://pages.nist.gov/IoT-Device-Cybersecurity-Requirement-Catalogs/technical/"
  - "https://www.iso.org/standard/62542.html"
  - "https://peraturan.bpk.go.id/Details/229798/uu-no-27-tahun-2022"
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

# Menghitung kapasitas penyimpanan dan retensi CCTV

Halo, Teman Tukang.co.id! Kapasitas penyimpanan CCTV tidak bisa ditentukan dari jumlah kamera saja. Hitung kebutuhan data dari bitrate setiap kamera, berapa jam kamera merekam, jumlah hari retensi, lalu sisakan ruang untuk overhead, ekspor, dan pemulihan. Retensi yang tepat juga bukan angka universal: ia harus mengikuti tujuan pemantauan, kebutuhan pembuktian, dan keputusan pemilik sistem.

Rumus praktisnya: **kapasitas mentah (GB) = total bitrate (Mb/s) × 86.400 × jumlah hari ÷ 8.000**. Setelah itu tambahkan margin operasional dan cocokkan dengan kapasitas usable recorder, bukan kapasitas nominal pada label. Bitrate aktual, jadwal rekam, codec, audio, metadata, serta gerak di scene dapat mengubah hasil. IEC 62676-4 menekankan tujuan scene, kriteria kinerja, instalasi, pengujian penerimaan, dan peninjauan berkala—bukan demo produk atau megapiksel semata ([IEC 62676-4](https://webstore.iec.ch/en/publication/7353)).

![Ilustrasi CCTV Merk ZKTECO](/wp-content/uploads/2023/08/CCTV-Merk-ZKTECO.jpg)


*Aset lokal situs; gambar ini bukan dokumentasi proyek tertentu.*

## Jawaban singkat dan salah paham utama

Mulailah dari kejadian yang harus bisa diputar kembali. Jika delapan kamera masing-masing rata-rata 4 Mb/s merekam terus selama 14 hari, hitungan awalnya 8 × 4 × 86.400 × 14 ÷ 8.000, sekitar 4.838 GB sebelum margin. Ini contoh hitung, bukan kapasitas pembelian. Kamera berbasis gerak atau bitrate yang berubah dapat menghasilkan angka berbeda.

Salah paham yang mahal ialah menyamakan “hard disk 6 TB” dengan 6 TB yang seluruhnya siap direkam. Recorder membutuhkan ruang sistem, indeks, siklus tulis, ekspor, dan toleransi kegagalan. Periksa juga kemampuan menangani total incoming bitrate dan jumlah stream. Logo ONVIF membantu memeriksa interoperabilitas, tetapi tidak membuktikan semua fitur opsional dan alur playback pada kombinasi produk tertentu ([ONVIF Profile T](https://www.onvif.org/profiles/profile-t/), [panduan produk conformant ONVIF](https://www.onvif.org/)).

## Definisi dan batas objek

**Kapasitas** adalah ruang untuk rekaman; **retensi** adalah lama rekaman dipertahankan sebelum ditimpa. Keduanya berbeda dari resolusi, jumlah channel, dan kecepatan jaringan. Artikel ini memberi metode estimasi, bukan kebijakan masa simpan perkara atau kewajiban hukum lokasi tertentu. Karena otoritas kebijakan berada di luar cakupan, minta **[NEEDS RETENTION POLICY REVIEW: pemilik proses/legal menetapkan tujuan, masa simpan, akses, dan pengecualian]**.

Rekaman biasa, ekspor insiden, log akses, dan cadangan mempunyai pemilik serta risiko berbeda. ISO 15489-1 membahas pengelolaan rekod sepanjang siklus hidup; UU Pelindungan Data Pribadi membuat tujuan, akses, pengungkapan, dan penghapusan perlu ditinjau sesuai konteks ([ISO 15489-1](https://www.iso.org/standard/62542.html), [UU No. 27 Tahun 2022](https://peraturan.bpk.go.id/Details/229798/uu-no-27-tahun-2022)).

## Cara kerjanya

1. **Kumpulkan input per kamera.** Catat bitrate target atau hasil pengukuran recorder. Pisahkan kamera 24 jam, kamera berjendela waktu, dan kamera deteksi gerak. Masukkan audio serta stream tambahan bila disimpan.
2. **Ubah menjadi data harian.** Kalikan bitrate (Mb/s) dengan 86.400 detik, bagi 8.000 untuk pendekatan gigabyte desimal, lalu jumlahkan kamera dan kalikan hari retensi.
3. **Tambahkan margin yang dapat dijelaskan.** Sisihkan ruang untuk variasi bitrate, indeks, ekspor, rekaman yang ditahan, dan pemulihan. Besarnya margin harus berasal dari uji dan kebijakan setempat, bukan persentase universal.
4. **Cocokkan recorder dan media.** Periksa incoming throughput, jumlah disk, metode rekam, alarm, serta kapasitas nominal, usable, dan setelah redundansi.
5. **Uji alur bukti.** Putar pada jam sibuk, cari berdasarkan waktu, ekspor klip, dan buka hasilnya. Catat timestamp, zona waktu, audio, metadata, serta jejak siapa yang mengekspor.

## Faktor yang mengubah hasil

Bitrate dipengaruhi scene ramai, pencahayaan rendah, noise, dan perubahan codec. Jadwal 24 jam berbeda dari jadwal kerja; pre-record dan post-record menambah durasi. Audio dan metadata ikut dihitung bila dibutuhkan untuk kejadian.

Redundansi bukan cadangan. RAID atau disk ganda dapat membantu ketersediaan setelah kegagalan media, tetapi tidak otomatis melindungi dari penghapusan, ransomware, atau kesalahan operator. NIST memisahkan inventaris, akun/peran, perlindungan data, pembaruan, pemulihan, dan penghentian aman sebagai kemampuan yang perlu diverifikasi ([NISTIR 8259 Rev. 1](https://csrc.nist.gov/pubs/ir/8259/r1/final), [katalog kemampuan IoT NIST](https://pages.nist.gov/IoT-Device-Cybersecurity-Requirement-Catalogs/technical/)).

Kriteria scene juga menentukan retensi. Kamera pintu masuk mungkin memerlukan detail pada jam tertentu; kamera area umum mungkin cukup untuk mengetahui alur. Gunakan scene terukur, kriteria objektif, catatan instalasi, dan acceptance test sebelum mengurangi retensi hanya karena angka kapasitas terlihat besar.

## Contoh keputusan praktis

| Input | Contoh asumsi | Yang harus diverifikasi |
|---|---:|---|
| Jumlah kamera | 8 | Semua channel benar-benar merekam? |
| Bitrate rata-rata | 4 Mb/s/kamera | CBR/VBR dan jam sibuk |
| Jadwal | 24 jam/hari | Pre/post-record dan gerak |
| Retensi target | 14 hari | Disetujui pemilik proses |
| Hasil mentah | ±4.838 GB | Satuan dan ruang usable |

Buat skenario rendah, tengah, dan tinggi dengan angka dari datasheet serta pengukuran Anda. Bandingkan masing-masing dengan usable setelah margin dan redundansi. Sobat Tukang.co.id, keputusan pengadaan sebaiknya memakai skenario tinggi yang dapat dijelaskan, bukan bitrate terbaik di brosur.

Untuk ekspor, tentukan siapa yang boleh mengekspor, media tujuan, penamaan file, timestamp, dan masa simpan salinan insiden. Jika produk berbeda merek, uji playback dan ekspor pada kombinasi firmware yang akan dipasang; kesesuaian profil tidak menggantikan uji alur kerja.

Setelah tabel selesai, dokumentasikan asumsi dalam lembar serah-terima: nama kamera atau zona, sumber bitrate, jadwal, versi firmware, tanggal pengukuran, dan siapa yang menyetujui retensi. Dokumen ini memudahkan penghitungan ulang ketika kamera ditambah, scene berubah, atau recorder diganti. Jika Anda masih menyusun kebutuhan perangkat, gunakan [panduan layanan pemasangan CCTV di Wungu](/kota/jual-pasang-cctv-wungu/) sebagai konteks untuk menyiapkan pertanyaan teknis kepada penyedia; halaman tersebut bukan pengganti verifikasi kapasitas sistem Anda.

## Kesalahan umum dan cara memeriksanya

Jangan memakai resolusi sebagai pengganti bitrate. Ukur bitrate aktual pada scene yang mewakili. Jangan menjumlahkan kapasitas disk tanpa memisahkan nominal, usable, redundansi, dan ruang kerja ekspor. Jangan menganggap deteksi gerak selalu menghemat data; periksa false trigger dan pre/post-record.

Jangan menghapus otomatis semua rekaman saat umur retensi tercapai tanpa mekanisme penahanan insiden. Tetapkan proses hold dan pemilik persetujuannya. Shortcut “beli disk terbesar yang muat” juga bisa gagal bila recorder tidak mendukung kapasitas atau throughput, atau ekspor tidak pernah diuji. Alternatifnya adalah lembar input per kamera, uji rekam-playback-ekspor, alarm kegagalan, lalu tinjauan teknis dan privasi. Kawan Tukang.co.id, area publik, akses pihak ketiga, dan permintaan penghapusan data memerlukan tinjauan hukum aktual.

Saat meminta penawaran, kirimkan bukan hanya jumlah kamera, melainkan bitrate per stream, pola rekam, hari retensi, kebutuhan ekspor, dan kondisi jaringan. Tanyakan batas recorder, perilaku ketika disk penuh, pemberitahuan kegagalan, metode pemulihan, serta bukti uji pada firmware yang ditawarkan. Untuk lokasi lain, [opsi layanan pemasangan CCTV di Wuluhan](/kota/jual-pasang-cctv-wuluhan/) dapat menjadi rujukan langkah berikutnya, tetapi keputusan akhir tetap bergantung pada survei dan persetujuan proyek.

## Kesimpulan dan langkah berikutnya

Hitung **total bitrate × durasi rekam × hari retensi**, tambahkan margin yang dapat dipertanggungjawabkan, lalu cocokkan dengan usable, kemampuan recorder, redundansi, dan uji playback-ekspor. Retensi adalah keputusan pemilik proses tentang tujuan, akses, penahanan insiden, dan privasi—bukan sekadar jumlah hari.

Buat tabel per kamera berisi bitrate terukur, jadwal, audio/metadata, tiga skenario, usable, dan hasil ekspor. Minta persetujuan masa simpan dari pemilik sistem dan pemeriksaan profesional untuk desain, keamanan, serta kepatuhan spesifik lokasi. Tanpa input proyek dan kebijakan yang disetujui, metode ini hanya estimasi, bukan jaminan recorder memenuhi kebutuhan Anda.
