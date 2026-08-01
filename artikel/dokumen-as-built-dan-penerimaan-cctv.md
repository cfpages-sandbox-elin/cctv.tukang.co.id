---
article_id: CCT-12-06
writing_contract_version: "native-id-v2"
title: "Dokumen as-built dan berita acara penerimaan CCTV"
slug: "dokumen-as-built-dan-penerimaan-cctv"
description: "Test the installed system against documented requirements before sign-off."
status: draft
publication_date: "2026-03-02"
publication_date_basis: editorial_backfill
date_modified: null
parent_topic: CCT-12
primary_intent: "Assemble approved drawings, settings, tests, defects, and sign-off records."
reader_community: "Tukang.co.id"
reader_address: "Sobat Tukang.co.id"
final_route: "/artikel/dokumen-as-built-dan-penerimaan-cctv.html"
technical_review: required
sources:
  - "https://webstore.iec.ch/en/publication/7353"
  - "https://www.onvif.org/profiles/profile-t/"
  - "https://www.onvif.org/"
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

# Dokumen as-built dan berita acara penerimaan CCTV

Halo, Sobat Tukang.co.id! Sistem CCTV belum layak ditandatangani hanya karena kamera menyala di monitor. Penerimaan yang dapat dipertanggungjawabkan membandingkan kondisi terpasang dengan kebutuhan yang disetujui, lalu menyimpan bukti pengujian, daftar kekurangan, dan keputusan siapa menerima apa.

Paket minimumnya terdiri dari gambar as-built (gambar yang sudah diperbarui sesuai kondisi terpasang), daftar perangkat dan konfigurasi, hasil uji commissioning, daftar punch list, serta berita acara penerimaan yang menyebut status terbuka atau tertutup. Kesimpulannya berubah bila gambar belum disetujui, identitas firmware tidak cocok, uji belum mewakili adegan operasi, atau kewajiban privasi dan akses rekaman belum diputuskan. Karena data proyek tidak tersedia di artikel ini, keputusan akhir tetap memerlukan review pemilik, penyedia, dan tenaga kompeten.

![Ilustrasi CCTV Merk ZKTECO](/wp-content/uploads/2023/08/CCTV-Merk-ZKTECO.jpg)


*Aset lokal situs; gambar ini bukan dokumentasi proyek tertentu.*

## Definisikan kebutuhan sebelum meminta harga

Mulailah dari fungsi yang harus dibuktikan, bukan dari jumlah kamera. Tulis area dan adegan yang perlu dipantau, tujuan observasi (melihat kejadian atau mengenali orang), kondisi cahaya, akses pengguna, kebutuhan rekaman dan ekspor, serta antarmuka ke jaringan atau sistem lain. Panduan aplikasi IEC 62676-4 menempatkan tujuan adegan, pemilihan, penempatan, instalasi, commissioning, pengujian, dan evaluasi objektif sebagai satu rangkaian; megapiksel atau demo vendor saja tidak membuktikan hasil di lokasi ([IEC 62676-4](https://webstore.iec.ch/en/publication/7353)).

Bekukan persyaratan dalam dokumen yang memiliki nomor revisi dan persetujuan. Sertakan asumsi yang masih menunggu survei: sudut pandang, pencahayaan malam, jalur kabel, kapasitas penyimpanan, dan siapa yang boleh mengakses. Sobat Tukang.co.id, bila satu asumsi berubah setelah pemasangan, tandai sebagai perubahan dan jangan diam-diam mengoreksi gambar lama.

## Buat penawaran benar-benar sebanding

Minta setiap penawaran memakai struktur yang sama: lingkup perangkat, pekerjaan instalasi, konfigurasi, pengujian, dokumentasi as-built, pelatihan serah terima, eksklusi, dan asumsi akses lokasi. Pisahkan item yang disediakan pemilik, seperti jaringan, listrik, rak, atau koneksi internet. Dengan begitu, harga lebih rendah tidak menyembunyikan pengujian atau pembaruan gambar yang hilang.

Tanyakan juga kondisi penerimaan: apakah pembayaran terakhir bergantung pada seluruh kamera teruji, atau hanya barang tiba. Jika ada pekerjaan tertunda karena area belum siap, catat sebagai ketergantungan dengan pemilik dan tanggal pemeriksaan ulang. Artikel ini tidak menetapkan harga, kapasitas, garansi, atau waktu respons; semua itu harus berasal dari catatan komersial proyek yang bertanggal.

## Dokumen yang membuktikan hal berbeda

Jangan menumpuk semua berkas dalam satu folder tanpa fungsi. Gunakan matriks sederhana berikut.

| Dokumen | Yang dibuktikan | Yang belum terbukti |
| --- | --- | --- |
| Gambar as-built bernomor revisi | Rute kabel, lokasi perangkat, label, dan perubahan dari desain | Kinerja gambar atau cakupan adegan tanpa uji lapangan |
| Daftar perangkat dan konfigurasi | Model, serial, alamat jaringan, versi firmware, profil, dan akun yang diserahkan | Kesesuaian fitur opsional atau keamanan konfigurasi |
| Laporan commissioning | Metode, tanggal, alat, saksi, hasil tiap skenario, dan deviasi | Kinerja di luar skenario dan kondisi yang diuji |
| Punch list | Kekurangan, pemilik tindakan, tenggat, dan status | Bukti bahwa tindakan sudah efektif sebelum ditutup |
| Berita acara penerimaan | Pihak, ruang lingkup, tanggal, status, pengecualian, dan tanda tangan | Pengganti untuk pemeliharaan atau garansi berkelanjutan |

Untuk interoperabilitas, minta identitas profil dan peran perangkat yang benar-benar diuji. ONVIF Profile T menjelaskan kemampuan streaming, imaging, event, metadata, HTTPS, dan audio tertentu, tetapi logo ONVIF atau kotak centang protokol tidak menjamin semua fitur opsional, kecocokan firmware, atau dukungan sepanjang umur sistem ([Profile T](https://www.onvif.org/profiles/profile-t/); [panduan produk konforman ONVIF](https://www.onvif.org/)).

## Pertanyaan wajib kepada penyedia

Ajukan pertanyaan yang dapat dijawab dengan rekaman, bukan janji:

- Versi gambar dan daftar perangkat mana yang menjadi baseline penerimaan?
- Serial, firmware, profil ONVIF, alamat jaringan, dan peran tiap perangkat apa yang dicatat?
- Skenario apa yang diuji untuk live view, rekam, pencarian, playback, ekspor, waktu sistem, dan notifikasi?
- Adegan mana yang belum diuji karena cahaya, akses, jaringan, atau area belum siap?
- Siapa menyaksikan uji, alat apa yang dipakai, dan di mana file asli hasil uji disimpan?
- Setiap punch list memiliki pemilik, tenggat, bukti penutupan, dan uji ulang atau tidak?
- Akun admin, kredensial awal, kunci enkripsi, dan prosedur penggantian diserahkan melalui kanal apa?
- Perubahan setelah tanda tangan akan diperlakukan sebagai change order, revisi gambar, atau uji penerimaan ulang?

Kawan Tukang.co.id, jawaban “sudah standar” belum cukup. Minta identitas produk dan ruang lingkup bukti yang dapat ditelusuri; catatan sertifikasi atau cuplikan uji tidak otomatis membuktikan model terpasang dan sistem yang diterima.

## Tanda risiko dan biaya yang sering tersembunyi

Waspadai penawaran yang hanya menyebut “pasang CCTV lengkap”, gambar satu garis tanpa label, hasil uji berupa satu foto monitor, atau berita acara yang menyatakan “diterima baik” tanpa daftar pengecualian. Red flag lain adalah serial dan firmware tidak dicatat, akun bawaan tidak diganti, atau penyedia meminta tanda tangan sebelum area dan jaringan siap.

Biaya tersembunyi biasanya muncul sebagai kunjungan ulang, waktu tunggu akses, pemindahan kabel karena jalur tidak sesuai gambar, ekspor ulang karena waktu sistem keliru, dan pekerjaan menutup punch list. Itu bukan alasan untuk mengarang angka; masukkan asumsi dan pemicu biayanya ke penawaran. Jika deviasi menyentuh listrik, struktur, privasi, atau jaringan produksi, hentikan penerimaan bagian tersebut sampai disiplin yang berwenang meninjau.

## Penerimaan, serah terima, dan keputusan akhir

Lakukan pemeriksaan berurutan. Pertama, cocokkan ruang lingkup dan revisi gambar dengan kondisi fisik serta label perangkat. Kedua, verifikasi konfigurasi, waktu sistem, akun, jaringan, dan pengaturan yang disetujui. Ketiga, jalankan skenario uji yang disepakati dan simpan log atau file asli. Keempat, buka punch list untuk setiap deviasi, tetapkan pemilik dan tenggat, lalu lakukan uji ulang setelah perbaikan. Terakhir, terbitkan berita acara dengan status: diterima, diterima dengan pengecualian terdaftar, atau belum diterima.

Simpan paket final dalam repositori terkendali: file sumber, PDF bertanda tangan, identitas versi bila dipakai, daftar distribusi, dan catatan perubahan. Prinsip pengelolaan rekaman ISO 15489 menekankan keaslian, keandalan, integritas, dan keterpakaian; Undang-Undang Pelindungan Data Pribadi juga membuat pengaturan akses dan penyimpanan rekaman perlu ditinjau sesuai konteks organisasi ([ISO 15489-1](https://www.iso.org/standard/62542.html); [UU No. 27 Tahun 2022](https://peraturan.bpk.go.id/Details/229798/uu-no-27-tahun-2022)). Detail retensi, dasar pemrosesan, dan siapa boleh melihat video harus diputuskan oleh pemilik dan peninjau hukum/privasi, bukan ditebak dari artikel.

Jangan mencampur serah terima dengan O&M atau garansi. Paket ini membuktikan keadaan dan pengujian pada tanggal penerimaan; pemeliharaan, pemantauan, dan klaim setelahnya memerlukan proses serta catatan tersendiri.

## Mengapa live view saja tidak cukup

Jalan pintasnya adalah menandatangani berita acara berdasarkan live view: semua gambar muncul, maka sistem dianggap selesai. Cara ini gagal karena live view tidak menguji pencarian rekaman, ekspor, ketepatan waktu, adegan sulit, akun, atau perilaku saat jaringan terganggu. Alternatif yang lebih aman adalah memakai daftar skenario, merekam hasil dan deviasi, lalu menandatangani hanya lingkup yang benar-benar dibuktikan.

## Kesimpulan

Dokumen as-built menunjukkan apa yang terpasang; laporan uji menunjukkan apa yang terjadi saat skenario dijalankan; punch list menunjukkan yang belum selesai; berita acara menyatakan keputusan dan pengecualiannya. Empat lapis bukti itu harus merujuk pada baseline persyaratan dan revisi yang sama.

Langkah berikutnya: minta penyedia mengirim paket berindeks, pilih saksi penerimaan, dan jadwalkan uji ulang untuk setiap item terbuka. Untuk meminta konteks pekerjaan berikutnya, Anda dapat mulai dari [halaman utama Tukang.co.id](/) atau melihat [layanan jual dan pasang CCTV di Dau](/kota/jual-pasang-cctv-dau/) sambil tetap meminta dokumen proyek yang spesifik. **[NEEDS PROJECT REVIEW: EG-01, EG-02, EG-03, EG-09, EG-10, EG-12 — survei aktual, desain/konfigurasi, metode uji, identitas produk, kewajiban hukum, dan ketentuan komersial belum tersedia dalam artikel ini.]** Teman Tukang.co.id, jangan nyatakan sistem diterima penuh sebelum pemilik proyek menyetujui bukti dan batas pengecualiannya secara tertulis.
