---
article_id: CCT-02-02
title: "Dome, bullet, fixed, dan PTZ: memilih bentuk kamera"
slug: "bentuk-kamera-dome-bullet-fixed-ptz"
description: "Panduan memilih bentuk kamera, memahami hubungan kamera dengan recorder, dan menyusun spesifikasi awal sistem."
status: draft
writing_contract_version: "native-id-v2"
publication_date: "2025-06-12"
publication_date_basis: editorial_backfill
date_modified: null
parent_topic: CCT-02
primary_intent: "Match camera form and movement to an operating need."
reader_community: "Tukang.co.id"
reader_address: "Teman Tukang.co.id"
final_route: "/artikel/bentuk-kamera-dome-bullet-fixed-ptz.html"
technical_review: required
sources:
  - "https://webstore.iec.ch/en/publication/7353"
  - "https://www.onvif.org/profiles/profile-t/"
  - "https://www.onvif.org/"
  - "https://peraturan.bpk.go.id/Details/229798/uu-no-27-tahun-2022"
---

# Dome, bullet, fixed, dan PTZ: memilih bentuk kamera

Halo, Teman Tukang.co.id! Bentuk kamera bukan penentu tunggal bahwa satu sistem lebih bagus dari yang lain. Dome, bullet, dan fixed pada dasarnya mengubah cara kamera dipasang dan diarahkan; PTZ (pan-tilt-zoom) menambah kemampuan bergerak. Pilihannya harus mengikuti adegan yang perlu dipantau, apakah sudut pandang harus tetap, dan siapa atau apa yang akan mengoperasikan perubahan arah itu.

Jawaban singkatnya: gunakan fixed ketika area pantauan sudah jelas dan bukti harus konsisten; pilih dome atau bullet setelah mempertimbangkan ruang, akses fisik, dan lingkungan pemasangan; pertimbangkan PTZ hanya jika ada alasan operasional untuk berpindah pandangan dan kamera itu akan dipantau atau dipicu dengan prosedur yang nyata. Tidak ada bentuk yang otomatis menghasilkan identifikasi, rekaman utuh, atau notifikasi yang berguna. Persyaratan adegan, pencahayaan, penyimpanan, recorder, dan pengujian penerimaan dapat mengubah keputusan.

![Ilustrasi CCTV Merk ZKTECO](/wp-content/uploads/2023/08/CCTV-Merk-ZKTECO.jpg)

Ilustrasi umum dari aset lokal cctv.tukang.co.id; bukan dokumentasi proyek tertentu.

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

Istilah **fixed** berarti arah pandang kamera ditetapkan setelah pemasangan. “Dome” dan “bullet” terutama menunjuk keluarga bentuk rumah kamera, bukan jaminan kualitas gambar atau kelas ketahanan tertentu. Sebuah dome dapat berisi kamera fixed, sementara bullet juga dapat memiliki lensa dan fitur berbeda-beda. **PTZ** adalah kamera yang dapat mengubah arah horizontal (pan), vertikal (tilt), dan pembesaran optik (zoom) melalui kendali atau aturan tertentu.

Karena itu, artikel ini membahas bentuk, gerak, bahasa spesifikasi, dan hubungan kamera dengan recorder. Detail sudut pemasangan, ketinggian, jalur kabel, dan pekerjaan mounting perlu keputusan proyek tersendiri. Artikel ini juga bukan persetujuan desain, penentuan kepatuhan, atau pengganti uji di lokasi. Untuk area yang merekam orang, pemilik sistem perlu memeriksa dasar pemrosesan, akses, dan retensi data dengan tinjauan privasi yang sesuai UU Pelindungan Data Pribadi; artikel ini tidak menetapkan kewajiban hukum untuk lokasi tertentu ([UU No. 27 Tahun 2022](https://peraturan.bpk.go.id/Details/229798/uu-no-27-tahun-2022)).

## Cara kerjanya

Mulailah dari **tujuan adegan**, bukan dari katalog bentuk. Tulis apakah kamera diperlukan untuk melihat alur orang, mengenali wajah, membaca plat, memantau pintu, atau meninjau kejadian setelah laporan. Tujuan itu menentukan bidang pandang, detail yang dibutuhkan, perilaku cahaya, dan berapa lama rekaman harus dapat dicari. Panduan aplikasi CCTV IEC 62676-4 menempatkan persyaratan, pemilihan, pemasangan, commissioning, pemeliharaan, pengujian, serta evaluasi objektif sebagai rangkaian yang saling terkait; jumlah megapiksel atau demo produk saja tidak membuktikan adegan akan berguna ([IEC 62676-4](https://webstore.iec.ch/en/publication/7353)).

Setelah tujuan jelas, pilih perilaku arah pandang:

| Kebutuhan operasional | Bentuk yang masuk shortlist | Alasan yang perlu diuji |
| --- | --- | --- |
| Satu pintu, kasir, koridor, atau jalur tetap | Fixed, dalam rumah dome atau bullet | Rekaman konsisten dan lebih mudah dibandingkan antarwaktu |
| Ruang dengan akses fisik yang perlu dibatasi atau tampilan yang ingin lebih menyatu | Dome fixed | Bentuknya dapat sesuai ruang, tetapi tetap periksa akses servis dan refleksi penutup lensa |
| Arah pandang memanjang atau pemasangan yang memerlukan badan kamera mudah diarahkan saat instalasi | Bullet fixed | Orientasi mudah dipahami, namun jangan menyimpulkan performa lingkungan dari bentuk saja |
| Area luas dengan kejadian yang berpindah dan operator yang siap mengendalikan | PTZ | Gerak dan zoom dapat mengikuti kejadian, tetapi area di luar arah saat itu tidak otomatis terekam |

Kamera lalu terhubung ke recorder atau client. Cocokkan jenis stream, resolusi, codec, audio bila digunakan, event, metadata, daya, jaringan, waktu sistem, serta cara pemutaran dan ekspor bukti. ONVIF Profile T mencakup kemampuan streaming, imaging, event, metadata, PTZ, dan komunikasi aman pada peran perangkat tertentu. Namun logo ONVIF atau kotak centang protokol tidak membuktikan semua fitur opsional, kecocokan recorder, firmware, atau alur kerja yang Anda perlukan; verifikasi model dan workflow yang benar-benar diuji di [panduan produk konforman ONVIF](https://www.onvif.org/) dan [Profile T](https://www.onvif.org/profiles/profile-t/).

Urutan praktisnya adalah: rumuskan adegan, pilih fixed atau bergerak, tetapkan bentuk yang masuk akal untuk ruang dan akses, cocokkan kamera-recorder, lalu uji siang/malam dan kondisi operasi yang relevan. Jika salah satu mata rantai belum memiliki bukti, simpulan masih berupa shortlist, bukan spesifikasi final.

## Faktor yang mengubah hasil

**Perilaku kejadian.** Jika kejadian selalu berada pada satu area, fixed biasanya memberi baseline yang stabil. PTZ berguna ketika perpindahan pandangan memang menjadi bagian dari respons: operator menerima alarm, mengarahkan kamera, dan merekam atau menandai kejadian sesuai prosedur. Tanpa operator, preset, atau aturan yang teruji, zoom PTZ dapat hanya memperbesar area yang kebetulan sedang dilihat.

**Cahaya dan gerakan.** Silau, lampu latar, malam, hujan, kabut, serta objek bergerak mengubah hasil lebih besar daripada nama bentuk. Minta contoh rekaman dari adegan serupa dan tentukan kriteria lulus: misalnya detail yang harus terlihat pada titik tertentu, bukan sekadar gambar “jernih”. Jangan mengisi angka jarak, lux, frame rate, atau retensi sebelum ada datasheet model dan pengukuran lokasi ([IEC 62676-4](https://webstore.iec.ch/en/publication/7353)).

**Akses dan gangguan fisik.** Rumah kamera memengaruhi kemudahan orang menyentuh, menggeser, atau menghalangi lensa; tetapi bentuk dome tidak otomatis anti-vandalisme dan bullet tidak otomatis cocok untuk luar ruang. Periksa kelas perlindungan, bahan, bracket, jalur kabel, dan akses servis pada dokumen model yang sama. Detail geometri pemasangan tetap perlu penanggung jawab pekerjaan.

**Recorder dan jaringan.** Dua kamera yang sama-sama bertuliskan “IP” dapat berbeda pada codec, profil, event, bitrate, daya, atau metode autentikasi. Pastikan recorder dapat menerima stream dan event yang dibutuhkan, merekam pada beban yang direncanakan, dan mengekspor klip dengan waktu yang benar. Uji bukan hanya tampilan langsung; coba playback, pencarian, ekspor, pemulihan setelah koneksi terputus, dan pembaruan firmware. [NEEDS MODEL/RECORDER WORKFLOW TEST: exact camera, firmware, recorder, client, and acceptance evidence are not provided.]

**Kewenangan dan data.** Tentukan siapa yang boleh melihat live view, mengubah arah PTZ, mengekspor rekaman, dan menghapus atau mempertahankan data. Pisahkan akun operator dari akun administrasi, catat perubahan konfigurasi, dan batasi area pantauan sesuai tujuan yang disetujui. Dasar hukum, retensi, akses subjek data, dan respons insiden memerlukan tinjauan organisasi serta hukum yang aktual; jangan menyimpulkan kepatuhan hanya dari fitur kamera ([UU No. 27 Tahun 2022](https://peraturan.bpk.go.id/Details/229798/uu-no-27-tahun-2022)).

## Contoh keputusan praktis

Bayangkan tiga kebutuhan berikut. Ini contoh bersyarat, bukan klaim hasil proyek.

1. **Pintu masuk dengan arah lalu lintas tetap.** Mulai dari fixed. Pilih dome atau bullet berdasarkan akses servis, kemungkinan gangguan, dan ruang yang tersedia. Uji adegan saat siang dan malam; pastikan recorder menyimpan stream serta waktu yang dapat dicari.
2. **Halaman yang sering berubah titik perhatiannya.** PTZ masuk shortlist hanya bila ada petugas atau otomasi yang sudah ditentukan untuk menerima pemicu, mengarahkan kamera, dan menandai rekaman. Tambahkan kamera fixed bila area yang tidak sedang dituju tetap harus menjadi bukti.
3. **Ruang sempit dengan beberapa arah penting.** Jangan menganggap PTZ sebagai pengganti beberapa sudut tetap. Bandingkan satu atau lebih fixed dengan kebutuhan detail tiap arah, kapasitas recorder, dan beban review. Bentuk dome/bullet dipilih setelah batas fisik dan akses ditetapkan.

Pada lembar shortlist, tulis setidaknya: tujuan adegan, titik yang harus terlihat, fixed atau PTZ, bentuk kandidat, lensa dan stream dari datasheet, recorder/client yang diuji, aturan akun, kondisi cahaya, hasil playback-ekspor, serta siapa yang menyetujui. Kolom kosong berarti keputusan belum siap dibeli atau dipasang.

## Kesalahan umum dan cara memeriksanya

**Memilih dari foto casing.** Foto tidak memberitahu bidang pandang, perilaku malam, atau kompatibilitas. Minta datasheet dan nomor model lengkap, lalu cocokkan dengan unit dan firmware yang akan dikirim.

**Menganggap PTZ mencakup semuanya.** PTZ hanya merekam arah yang sedang dilihat. Tanyakan area yang boleh luput, siapa pengendalinya, apa pemicunya, dan bagaimana bukti dari gerak kamera ditinjau.

**Menyamakan megapiksel dengan identifikasi.** Detail bergantung pada adegan, lensa, cahaya, gerak, kompresi, dan posisi. Tetapkan kriteria observasi/identifikasi dan lakukan uji penerimaan di kondisi nyata ([IEC 62676-4](https://webstore.iec.ch/en/publication/7353)).

**Memakai logo ONVIF sebagai jaminan.** Verifikasi profil, peran perangkat, fitur wajib/bersyarat, sertifikat konformansi, dan workflow pada recorder yang dipilih. Jika belum diuji, tulis sebagai risiko terbuka, bukan sebagai “pasti kompatibel” ([ONVIF Profile T](https://www.onvif.org/profiles/profile-t/)).

**Mengabaikan tata kelola rekaman.** Kamera yang merekam area publik atau pekerja memerlukan keputusan akses dan retensi. Buat register pemilik data, akun, masa simpan, ekspor, dan penghapusan; minta review privasi/hukum sebelum operasi.

## Jangan tergoda jalan pintas “yang penting bentuknya bagus”

Shortcut membeli dome untuk semua indoor, bullet untuk semua outdoor, atau PTZ untuk menggantikan seluruh kamera fixed terlihat sederhana karena mengurangi pertanyaan. Ia gagal ketika bentuk dipakai sebagai pengganti tujuan adegan dan pengujian. Alternatif yang lebih dapat dipertanggungjawabkan adalah membuat shortlist kecil, meminta bukti model-recorder, dan menolak klaim fitur yang belum diuji. Sobat Tukang.co.id, lebih baik menunda keputusan pada satu kolom yang belum terbukti daripada mengunci sistem yang tidak dapat menampilkan bukti saat diperlukan.

## Kesimpulan dan langkah berikutnya

Dome dan bullet adalah pilihan rumah kamera; fixed menetapkan arah; PTZ menambah gerak yang harus dioperasikan dan diuji. Pilih berdasarkan adegan, cahaya, akses, recorder, jaringan, serta tata kelola rekaman—bukan nama bentuk atau jumlah megapiksel. Kawan Tukang.co.id, sebelum meminta harga, buat lembar kebutuhan untuk setiap titik dan minta vendor mengisi nomor model, firmware, kompatibilitas recorder, skenario uji, serta batas fitur yang belum dibuktikan.

Jika model, lokasi, atau dampak privasinya signifikan, mintalah tinjauan teknis dan privasi yang berwenang. Terapkan aturan kerja ini: tidak ada kamera yang dianggap “terpilih” sampai tujuan adegan, alur recorder, akses data, dan hasil uji penerimaan tercatat; [NEEDS TECHNICAL REVIEW: coordinator must review the unresolved model/recorder and site-specific evidence before publication.]

Untuk menyiapkan pertanyaan sebelum survei, gunakan [beranda cctv.tukang.co.id](/) sebagai titik mulai dan baca [informasi tentang pengelola situs](/about/) bila Anda perlu memahami konteks penerbitnya.
