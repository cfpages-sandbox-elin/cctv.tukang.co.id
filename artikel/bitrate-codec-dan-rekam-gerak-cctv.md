---
article_id: CCT-05-04
title: "Bitrate, codec, dan rekam gerak: dampak pada penyimpanan"
slug: "bitrate-codec-dan-rekam-gerak-cctv"
description: "Size and evaluate recorders, storage, retention, redundancy, playback, and export."
status: draft
writing_contract_version: "native-id-v2"
publication_date: "2025-08-31"
publication_date_basis: editorial_backfill
date_modified: null
parent_topic: CCT-05
primary_intent: "Understand variables that change recording volume and evidence quality."
reader_community: "Tukang.co.id"
reader_address: "Sobat Tukang.co.id"
final_route: "/artikel/bitrate-codec-dan-rekam-gerak-cctv.html"
technical_review: required
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

# Bitrate, codec, dan rekam gerak: dampak pada penyimpanan

Halo, Sobat Tukang.co.id! Rekaman CCTV cepat memenuhi hard disk bukan semata karena jumlah kameranya. Tiga pengungkit utamanya adalah bitrate (laju data), codec (cara kompresi), dan pola rekam—terus-menerus atau hanya saat ada gerakan. Bitrate lebih tinggi biasanya menyimpan lebih banyak detail tetapi menghasilkan data lebih besar; codec yang lebih efisien dapat mengecilkan data pada mutu yang sebanding; rekam gerak mengurangi jam rekam ketika adegan memang tenang.

Jawaban praktisnya: hitung kebutuhan dari bitrate aktual setiap kamera, durasi simpan, dan persentase waktu kamera aktif merekam. Setelah itu uji hasil playback pada adegan penting, bukan hanya melihat angka kapasitas. Nilai pasti bergantung pada model, firmware, adegan, pencahayaan, konfigurasi deteksi gerak, dan recorder terpilih. [NEEDS VERIFICATION: bitrate efektif, rasio gerak, dan mutu bukti harus diuji pada perangkat yang dipilih.]

![Ilustrasi CCTV Merk ZKTECO](/wp-content/uploads/2023/08/CCTV-Merk-ZKTECO.jpg)


*Aset lokal situs; gambar ini bukan dokumentasi proyek tertentu.*

## Definisi dan batas objek

Bitrate adalah banyaknya bit yang dialirkan tiap detik dari kamera ke recorder. Codec adalah algoritme yang menyusun gambar menjadi aliran data lebih ringkas. Rekam gerak (motion recording) menyimpan ketika aturan gerak terpenuhi, sering dengan jeda sebelum dan sesudah pemicu. Ketiganya memengaruhi volume penyimpanan, tetapi tidak sendirian menentukan apakah wajah, tulisan, atau kejadian dapat dibaca.

Artikel ini membahas perencanaan volume, retensi, playback, ekspor, dan pemeriksaan kompatibilitas. Ia tidak menetapkan kapasitas untuk semua merek atau menjamin identifikasi objek. Pedoman aplikasi CCTV IEC menautkan tujuan adegan, pemilihan, pemasangan, komisioning, pemeliharaan, dan pengujian ke kebutuhan operasional; megapiksel atau demo saja tidak membuktikan hasil berguna ([IEC 62676-4](https://webstore.iec.ch/en/publication/7353)).

## Cara kerjanya

Untuk perkiraan awal, gunakan `bitrate (bit/detik) × detik rekam ÷ 8`. Kalikan dengan jumlah kamera dan proporsi waktu kamera benar-benar merekam. Contoh bersyarat: satu kamera pada 4 Mb/s selama 24 jam menghasilkan sekitar 43,2 GB data desimal per hari sebelum overhead. Jika pola gerak membuat kamera aktif separuh waktu, angka teoritisnya sekitar separuh—hanya jika pemicu, prarekaman, dan pascarekaman bekerja sesuai asumsi.

Codec tidak boleh dipilih hanya dari label “lebih hemat”. Codec dan profilnya harus didukung kamera, recorder, aplikasi playback, dan alat ekspor. ONVIF Profile T mencakup aliran video dan fungsi terkait, tetapi logo ONVIF tidak menjamin semua fitur opsional atau interoperabilitas setiap kombinasi perangkat. Verifikasi profil, peran perangkat, firmware, dan alur yang diuji pada [ONVIF Profile T](https://www.onvif.org/profiles/profile-t/) dan [panduan produk konforman ONVIF](https://www.onvif.org/).

Petakan alur kamera → jaringan → recorder → media → playback → ekspor. Kegagalan satu antarmuka dapat terlihat seperti “hard disk kurang”, padahal penyebabnya koneksi putus, jam meleset, indeks rusak, atau codec tidak bisa diputar aplikasi tujuan.

## Faktor yang mengubah hasil

Resolusi dan frame per detik menaikkan data, tetapi adegan juga berpengaruh. Dinding hampir tidak berubah dapat dikompresi berbeda dari lalu lintas ramai, hujan, atau daun bergerak. Pencahayaan rendah dan noise sering membuat aliran lebih sulit dipadatkan. Karena itu, bitrate brosur bukan pengganti pengukuran pada sudut pandang dan waktu operasi sebenarnya.

Pada rekam gerak, ukuran zona, sensitivitas, objek pemicu, prarekaman, dan pascarekaman menentukan durasi klip. Bayangan, pantulan, serangga, atau perubahan cahaya dapat memicu klip berlebih; gerakan penting di luar zona dapat terlewat. Simpan log konfigurasi dan uji siang-malam dengan kejadian yang sengaja dibuat.

Retensi bukan sekadar “berapa hari muat”. Tentukan kejadian yang harus dapat dicari, siapa yang boleh mengakses, kapan klip dikunci, dan bagaimana salinan diekspor. Pengelolaan rekod mendorong pengendalian versi, akses, distribusi, retensi, dan pemusnahan berdasarkan konteks ([ISO 15489-1](https://www.iso.org/standard/62542.html)). Jika gambar memuat orang, tujuan, cakupan bidang pandang, masa simpan, akses, dan penghapusan perlu ditinjau terhadap UU Pelindungan Data Pribadi ([UU No. 27 Tahun 2022](https://peraturan.bpk.go.id/Details/229798/uu-no-27-tahun-2022)).

Kawan Tukang.co.id, masukkan overhead recorder, sistem berkas, metadata, dan ruang degradasi media ke lembar hitung. Jangan mengisi seluruh kapasitas nominal sebelum kebutuhan retensi dan pemulihan disepakati.

## Contoh keputusan praktis

| Kondisi terukur | Pilihan awal | Pemeriksaan wajib |
|---|---|---|
| Adegan ramai, detail penting | Bitrate/kualitas lebih tinggi, kontinu atau gerak ketat | Uji keterbacaan siang-malam; hitung ulang retensi |
| Adegan tenang, kejadian sporadis | Rekam gerak dengan prarekaman dan zona tertata | Uji pemicu palsu dan kejadian singkat |
| Kamera dan recorder beda merek | Codec/profil yang sama-sama didukung | Uji live view, rekam, pencarian, dan ekspor |
| Retensi wajib, kapasitas terbatas | Ubah variabel setelah tujuan bukti diprioritaskan | Dokumentasikan keputusan dan persetujuan |

Jika targetnya menemukan urutan kejadian, kontinuitas waktu dan sinkronisasi jam bisa lebih penting daripada kompresi maksimum. Jika targetnya membaca detail di satu pintu, area itu mungkin memerlukan profil berbeda dari kamera pemantau umum. Ini hipotesis desain, bukan jaminan; penerimaan harus memakai adegan dan kriteria terdokumentasi.

## Kesalahan umum dan cara memeriksanya

Jangan membagi kapasitas hard disk dengan jumlah kamera lalu menyebut hasilnya retensi. Periksa bitrate per kamera, jam rekam aktual, overhead, dan konfigurasi gerak. Jangan menganggap H.265 otomatis menggandakan hari simpan; bandingkan klip adegan sama pada perangkat dan firmware sama, lalu pastikan playback dan ekspor dapat dibuka pihak tujuan.

Jangan mematikan rekam kontinu tanpa menguji pemicu. Jalankan skenario masuk-keluar, gerakan cepat, cahaya berubah, dan jaringan terputus. Catat apakah klip muncul, durasi prarekaman, dan apakah cap waktu bertahan saat diekspor. Keamanan recorder juga perlu inventaris perangkat, akun, pembaruan, perlindungan data, pencatatan, dan pembuangan aman; mengganti kata sandi bawaan saja tidak membuktikan kontrol lengkap ([NISTIR 8259 Rev. 1](https://csrc.nist.gov/pubs/ir/8259/r1/final), [katalog kapabilitas IoT NIST](https://pages.nist.gov/IoT-Device-Cybersecurity-Requirement-Catalogs/technical/)).

Shortcut membeli hard disk terbesar lalu menurunkan mutu sampai ruang terasa cukup dapat menghilangkan detail, melewatkan gerak, atau membuat ekspor gagal. Alternatifnya adalah lembar kebutuhan berisi tujuan tiap kamera, bitrate uji, pola rekam, retensi, hak akses, metode ekspor, dan hasil uji penerimaan. Jika data belum ada, tandai `[NEEDS SITE TEST]` dan jangan menjanjikan hari simpan tertentu.

Untuk langkah lapangan, siapkan daftar pertanyaan dan minta penyedia menjelaskan metode uji, bukan hanya menawarkan kapasitas. Anda dapat membandingkan ruang lingkup layanan pada halaman [jual-pasang CCTV di Wuluhan](/kota/jual-pasang-cctv-wuluhan/) dan [jual-pasang CCTV di Yosowilangun](/kota/jual-pasang-cctv-yosowilangun/), lalu tetap meminta spesifikasi serta hasil uji perangkat yang benar-benar dipilih. Tautan lokasi bukan bukti performa; ia hanya titik awal untuk meminta pemeriksaan.

## Penutup: ubah angka menjadi bukti yang bisa dipakai

Bitrate menentukan laju data, codec mengubah efisiensi penyandian, dan rekam gerak mengubah lama aliran disimpan. Dampaknya pada penyimpanan hanya dapat dinilai bersama adegan, konfigurasi, retensi, kompatibilitas, dan hasil playback-ekspor. Sobat Tukang.co.id, sebelum membeli atau mengubah setelan, minta lembar uji dari perangkat yang tepat: bitrate efektif per kamera, persentase rekam, perhitungan kapasitas, contoh klip siang-malam, hasil pencarian, dan ekspor.

Jadikan angka itu dasar persetujuan dan jadwal peninjauan, bukan janji universal. Performa final tetap memerlukan verifikasi teknis di lokasi serta tinjauan privasi dan operasional sesuai penggunaan sebenarnya.
