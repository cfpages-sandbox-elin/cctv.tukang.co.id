---
article_id: CCT-04-02
title: "Pixel density CCTV: menghitung lalu membuktikan di lokasi"
slug: "pixel-density-cctv-dan-uji-lokasi"
description: "Judge whether a proposed camera and configuration can produce useful images in the target scene."
status: draft
writing_contract_version: "native-id-v2"
publication_date: "2025-08-01"
publication_date_basis: editorial_backfill
date_modified: null
parent_topic: CCT-04
primary_intent: "Estimate image detail and validate it with target-scene evidence."
reader_community: "Tukang.co.id"
reader_address: "Sobat Tukang.co.id"
final_route: "/artikel/pixel-density-cctv-dan-uji-lokasi.html"
technical_review: required
sources:
  - "https://webstore.iec.ch/en/publication/7353"
  - "https://webstore.iec.ch/en/publication/59704"
---

# Pixel density CCTV: menghitung lalu membuktikan di lokasi

Halo, Sobat Tukang.co.id!

Pixel density CCTV membantu menjawab pertanyaan yang sering tertukar: apakah kamera yang diusulkan benar-benar memberi detail yang berguna pada jarak dan lebar area sasaran? Jawabannya tidak cukup dari angka megapiksel. Hitung perkiraan jumlah piksel yang jatuh pada satu meter area sasaran, lalu buktikan dengan rekaman uji dari posisi, cahaya, dan konfigurasi yang akan dipakai.

Perhitungan hanya menyaring kandidat. Lensa, sudut pemasangan, kompresi, gerak objek, pencahayaan, dan cara operator mengambil bukti dapat mengubah hasil. Pedoman aplikasi CCTV IEC 62676-4 menempatkan kebutuhan scene, pemilihan, pemasangan, commissioning, pengujian, dan evaluasi objektif sebagai rangkaian yang saling terkait ([IEC 62676-4](https://webstore.iec.ch/en/publication/7353)). Jadi, jangan menyebut seseorang “teridentifikasi” hanya karena hasil rumus terlihat tinggi. Jika kriteria penerimaan belum disepakati untuk tugas Anda, tinggalkan penanda **[NEEDS TECHNICAL REVIEW: tetapkan target detail dan metode uji sebelum menyimpulkan identifikasi]**.

![Ilustrasi CCTV Merk ZKTECO](/wp-content/uploads/2023/08/CCTV-Merk-ZKTECO.jpg)

*Ilustrasi umum dari aset lokal Tukang.co.id; ini bukan dokumentasi proyek tertentu.*

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

## Definisi dan batas objek

Pixel density adalah kepadatan piksel pada lebar scene tertentu, biasanya dinyatakan sebagai piksel per meter (px/m). Lebar scene di sini berarti lebar area yang benar-benar ingin dinilai pada jarak objek, bukan lebar seluruh halaman spesifikasi kamera. Semakin banyak piksel yang jatuh pada objek, semakin banyak detail spasial yang tersedia untuk ditinjau; itu bukan jaminan bahwa wajah, tulisan, atau tindakan pasti dapat dikenali.

Artikel ini membahas estimasi detail dan uji penerimaan pada scene sasaran. Ia tidak menetapkan ambang universal untuk “deteksi”, “observasi”, atau “identifikasi”, tidak menggantikan desain pencahayaan, dan tidak membuktikan kepatuhan hukum atau keberhasilan suatu produk. IEC 62676-6 juga menekankan bahwa klasifikasi objek atau aktivitas perlu skenario, lingkungan, konsekuensi salah positif/salah negatif, dan metode penerimaan yang jelas ([IEC 62676-6](https://webstore.iec.ch/en/publication/59704)).

Dengan batas itu, keputusan yang sehat berbunyi: “konfigurasi ini memenuhi tugas yang didefinisikan pada scene dan kondisi uji tertentu.” Kalimat tersebut lebih dapat diaudit daripada “kamera ini pasti mengenali orang.”

## Cara kerjanya

Mulailah dari tugas operasional. Tulis apakah kamera dipakai untuk melihat keberadaan orang, membaca nomor kendaraan, meninjau arah gerak, atau menyediakan potongan rekaman untuk pemeriksaan setelah kejadian. Tugas berbeda memerlukan detail dan cara uji berbeda. Catat juga bidang sasaran: pintu selebar berapa meter, jalur kendaraan sepanjang berapa meter, atau zona yang harus terlihat.

Untuk estimasi awal, gunakan urutan berikut.

1. Catat resolusi horizontal efektif kamera (P), dalam piksel. Gunakan angka stream yang akan direkam, bukan hanya resolusi sensor maksimum.
2. Perkirakan lebar scene pada jarak sasaran (W), dalam meter. Lebar ini berasal dari kombinasi sensor, focal length, tinggi, kemiringan, dan jarak; ia bukan angka yang boleh ditebak dari megapiksel saja.
3. Hitung perkiraan pixel density: **PD = P ÷ W (px/m)**.
4. Ulangi pada beberapa jarak atau posisi penting. Sebuah pintu mungkin memiliki PD memadai di garis tengah tetapi turun di tepi karena sudut pandang dan distorsi.
5. Rekam kondisi yang sama dengan rencana operasional: resolusi, frame rate, codec, bitrate, shutter, fokus, WDR, infrared atau lampu tambahan, serta jarak objek.

Rumus tersebut adalah alat perencanaan, bukan klausa ambang dari standar. Saat commissioning, ambil cuplikan uji dengan objek atau aktivitas yang memang menjadi tugas. Simpan gambar asli, waktu, posisi kamera, pengaturan, kondisi cahaya, dan keputusan penilai. Jika hasil perlu dipakai sebagai bukti, catat siapa yang menilai dan versi konfigurasi yang diuji.

## Faktor yang mengubah hasil

Resolusi horizontal yang lebih tinggi dapat menaikkan PD hanya jika lebar scene tidak ikut melebar dan detail lain tidak hilang. Lensa dengan focal length berbeda mengubah lebar scene pada jarak sama. Digital zoom tidak menambah informasi yang tidak direkam; ia hanya memperbesar piksel yang sudah ada.

Fokus dan kedalaman bidang penting ketika kamera dipasang tetap tetapi sasaran bergerak mendekat. Motion blur dari gerakan objek atau shutter terlalu lambat dapat menghapus detail walaupun rumus tampak baik. Kompresi, bitrate rendah, dan jaringan yang menjatuhkan frame juga mengubah rekaman yang akhirnya diterima operator.

Cahaya latar, kontras, hujan, debu, pantulan kaca, dan infrared yang tidak merata membuat detail efektif berubah sepanjang hari. WDR dapat membantu rentang terang-gelap, tetapi pengaruhnya harus diuji pada pintu atau jalur yang sebenarnya. Untuk fungsi analitik, kepadatan piksel hanyalah satu masukan; sudut objek, oklusi, kerumunan, ambang perangkat lunak, serta tindakan operator menentukan hasil akhir. IEC 62676-6 memperingatkan bahwa contoh klip atau angka deteksi vendor tidak otomatis mewakili cuaca, crowd, lighting, dan alur respons di scene Anda ([IEC 62676-6](https://webstore.iec.ch/en/publication/59704)).

Sobat Tukang.co.id, perlakukan perubahan kecil sebagai perubahan konfigurasi. Memindahkan kamera beberapa meter, mengganti lensa, mengaktifkan stream berbeda, atau menambah lampu berarti perhitungan dan uji perlu diulang. Jangan menyalin hasil uji siang untuk menyatakan kinerja malam.

## Contoh keputusan praktis

Bayangkan area pintu selebar 4 m menggunakan stream horizontal 2.560 piksel. Estimasi awalnya 640 px/m (2.560 ÷ 4). Angka ini hanya menunjukkan pembagian piksel pada lebar tersebut. Tim masih harus memeriksa apakah subjek berada pada jarak itu, wajah menghadap kamera, gerak tidak blur, dan rekaman mempertahankan detail.

Gunakan tabel keputusan sederhana berikut ketika membandingkan proposal:

| Temuan | Keputusan sementara | Bukti lanjutan |
|---|---|---|
| PD rendah pada seluruh zona tugas | Jangan lanjut ke klaim detail; ubah lebar scene, lensa, posisi, atau kamera | Denah, jarak, dan simulasi ulang |
| PD memadai di tengah tetapi turun di tepi | Batasi zona tugas atau uji beberapa titik | Cuplikan dari tepi dan tengah |
| PD memadai siang, gagal saat backlight/malam | Pisahkan persyaratan siang dan malam | Uji pada jam dan pencahayaan sasaran |
| Rumus baik, cuplikan berulang blur/terkompresi | Tahan penerimaan; periksa fokus, shutter, stream, dan jaringan | File asli serta log konfigurasi |
| Cuplikan memenuhi tugas yang disepakati | Terima hanya untuk scene, kondisi, dan versi yang diuji | Berita acara uji dan tanggal review |

Contoh di atas sengaja tidak memberi angka ambang identifikasi. Ambang harus disepakati bersama pemilik proses dan penilai kompeten berdasarkan tugas, konsekuensi kesalahan, dan metode uji yang terdokumentasi. **[NEEDS TECHNICAL REVIEW: validasi bahwa kriteria penerimaan, sampel scene, dan penilai sudah ditetapkan untuk proyek ini.]**

## Kesalahan umum dan cara memeriksanya

Kesalahan pertama adalah menganggap megapiksel sebagai bukti identifikasi. Periksa resolusi stream aktual dan lebar scene di titik sasaran; minta keduanya tertulis dalam lembar desain.

Kesalahan kedua adalah menghitung dari gambar demo vendor. Demo dapat memakai jarak, cahaya, bitrate, dan objek yang dipilih khusus. Minta uji pada lokasi atau lingkungan yang merepresentasikan lokasi, lalu simpan file tanpa hanya mengandalkan tangkapan layar dashboard.

Kesalahan ketiga adalah mengabaikan perubahan setelah serah terima. Firmware, profil kompresi, fokus, sudut kamera, dan pencahayaan dapat berubah. Cantumkan versi, tanggal, dan pemicu pengujian ulang dalam catatan pemeliharaan.

Kesalahan keempat adalah memperlakukan label analitik sebagai fakta. Tanyakan tugas yang dilabeli, corpus atau scene uji, definisi salah positif dan salah negatif, serta siapa yang meninjau hasil. Dokumentasikan kondisi ketika label boleh memicu tindakan dan kapan manusia harus memeriksa ulang.

Kawan Tukang.co.id, gunakan pertanyaan berhenti berikut sebelum menandatangani penerimaan: “Di mana tepatnya objek diuji? Dengan stream dan cahaya apa? File asli mana yang mendukung keputusan? Apa yang berubah sejak uji terakhir?” Jika satu jawaban tidak tersedia, hasilnya adalah gap bukti, bukan nilai performa.

## Jalan pintas yang tampak menarik

Jalan pintas yang umum ialah memilih kamera dengan megapiksel terbesar lalu memasangnya agar seluruh halaman masuk satu frame. Cara ini memang menyederhanakan jumlah perangkat, tetapi memperlebar W dan menurunkan PD pada bagian yang paling membutuhkan detail. Perbesaran digital setelah kejadian tidak memulihkan informasi yang tidak pernah direkam.

Alternatif yang lebih dapat dipertanggungjawabkan adalah memecah kebutuhan: tetapkan zona dan tugas, hitung PD per zona, lalu uji konfigurasi pada jarak dan cahaya nyata. Bila kepadatan di satu bagian tidak cukup, pertimbangkan perubahan lensa atau kamera untuk bagian itu—setelah ditinjau dari sudut pandang, privasi, jaringan, penyimpanan, dan keselamatan pemasangan. IEC 62676-4 menyediakan kerangka aplikasi yang menghubungkan kebutuhan, penempatan, instalasi, commissioning, dan evaluasi, bukan sekadar pilihan resolusi ([IEC 62676-4](https://webstore.iec.ch/en/publication/7353)).

## Kesimpulan dan langkah berikutnya

Pixel density CCTV menjawab “berapa banyak piksel per meter yang diperkirakan jatuh pada sasaran”; uji lokasi menjawab “apakah detail itu tetap berguna dalam kondisi kerja.” Keduanya harus berjalan bersama. Hitung dari resolusi stream dan lebar scene, nyatakan asumsi, kemudian rekam uji pada posisi, cahaya, gerak, dan konfigurasi yang benar-benar akan dipakai.

Teman Tukang.co.id, langkah berikutnya adalah membuat lembar uji satu halaman: tugas, zona, jarak, P, W, PD, pengaturan kamera, kondisi lingkungan, file asli, penilai, hasil, dan tanggal pengulangan. Untuk menindaklanjuti pemeriksaan pemasangan, Anda dapat melihat [layanan jual-pasang CCTV di Dau](/kota/jual-pasang-cctv-dau/) atau [layanan jual-pasang CCTV di Bae](/kota/jual-pasang-cctv-bae/) sesuai wilayah. Minta tinjauan teknis sebelum menyebut hasil sebagai identifikasi atau sebelum mengubahnya menjadi persyaratan kontrak. Aturan operasionalnya sederhana: **angka adalah perkiraan; hanya bukti scene yang diuji dan terdokumentasi yang boleh menjadi dasar penerimaan—dan bukti itu tetap tidak menjamin identifikasi di setiap kejadian.**
