---
article_id: CCT-05-02
title: "Menghitung kebutuhan channel dan ruang ekspansi recorder"
slug: "channel-dan-ekspansi-recorder-cctv"
description: "Size and evaluate recorders, storage, retention, redundancy, playback, and export."
status: draft
publication_date: "2025-08-24"
publication_date_basis: editorial_backfill
date_modified: null
parent_topic: CCT-05
primary_intent: "Size recorder channels with documented growth headroom."
reader_community: "Tukang.co.id"
reader_address: "Teman Tukang.co.id"
final_route: "/artikel/channel-dan-ekspansi-recorder-cctv.html"
technical_review: required
writing_contract_version: "native-id-v2"
sources:
  - "https://webstore.iec.ch/en/publication/7353"
  - "https://www.onvif.org/profiles/profile-t/"
  - "https://www.onvif.org/"
  - "https://csrc.nist.gov/pubs/ir/8259/r1/final"
  - "https://pages.nist.gov/IoT-Device-Cybersecurity-Requirement-Catalogs/technical/"
  - "https://peraturan.bpk.go.id/Details/229798/uu-no-27-tahun-2022"
---

# Menghitung kebutuhan channel dan ruang ekspansi recorder

Halo, Teman Tukang.co.id! Recorder tidak dipilih dari jumlah kamera hari ini saja. Hitung semua kanal yang benar-benar akan dipakai, lalu sisakan kanal kosong untuk pertumbuhan yang sudah masuk akal dalam rencana proyek. Jika daftar kamera, tipe stream, dan target ekspansi belum disahkan, keputusan final masih memerlukan data proyek [NEEDS PROJECT CAMERA SCHEDULE AND APPROVED GROWTH HORIZON].

Rumusnya: **kanal minimum = jumlah stream kamera aktif + stream tambahan yang diwajibkan**. Pilih recorder dengan kapasitas di atas angka itu dan dokumentasikan kanal yang sengaja dikosongkan. Kapasitas hard disk, retensi, dan bandwidth adalah pemeriksaan berbeda.

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

![Ilustrasi CCTV Merk ZKTECO](/wp-content/uploads/2023/08/CCTV-Merk-ZKTECO.jpg)


*Aset lokal situs; gambar ini bukan dokumentasi proyek tertentu.*

## Definisi dan batas objek

Channel adalah slot input atau stream yang dapat diterima dan dikelola recorder. Kamera dengan dua stream, audio, metadata, atau PTZ harus dicocokkan dengan kemampuan model dan lisensinya. IEC 62676-4 menempatkan tujuan adegan, pemilihan, pemasangan, pengujian, dan evaluasi objektif sebagai bagian dari perencanaan; megapiksel atau demo produk saja tidak cukup ([IEC 62676-4](https://webstore.iec.ch/en/publication/7353)).

Artikel ini berfokus pada kapasitas kanal dan ruang ekspansi, bukan retensi hard disk atau trafik jaringan. Teman Tukang.co.id, batas ini mencegah proposal memakai angka kanal sebagai pengganti perhitungan lain.

## Cara kerjanya

Mulai dari daftar kamera bernomor: tujuan, resolusi, mode rekam, serta kebutuhan audio, metadata, atau PTZ. Pisahkan kamera terpasang, tahap berikutnya yang disetujui, dan kemungkinan yang belum diputuskan.

1. Jumlahkan stream yang wajib direkam.
2. Tambahkan ekspansi dengan pemilik, lokasi perkiraan, dan waktu keputusan.
3. Cocokkan kapasitas input, incoming bandwidth, decoding, codec, dan lisensi recorder.
4. Tetapkan kanal cadangan dan tulis alasannya.
5. Uji kamera masuk, rekaman, pencarian, playback, serta ekspor dengan hak akses yang benar.

ONVIF Profile T mencakup streaming, imaging, event, metadata, PTZ, HTTPS, dan audio, tetapi profil atau logo tidak menjamin semua fitur opsional berjalan pada kombinasi kamera–recorder ([ONVIF Profile T](https://www.onvif.org/profiles/profile-t/); [panduan produk conformant ONVIF](https://www.onvif.org/)). Verifikasi model, firmware, peran profil, dan hasil uji.

## Faktor yang mengubah hasil

- **Jenis stream:** pastikan datasheet menyebut kapasitas input untuk codec dan resolusi yang dipilih.
- **Live view dan playback:** uji jumlah panel serta operator yang memutar rekaman bersamaan.
- **Fitur tambahan:** audio, metadata, analitik, atau PTZ dapat memerlukan dukungan dan lisensi tersendiri.
- **Pertumbuhan fisik:** kanal kosong harus disertai jalur kabel, daya, switch, rak, dan titik pemasangan.
- **Siklus produk:** NIST menekankan inventaris, konfigurasi aman, perlindungan data, pembaruan, pemantauan, dan penghentian perangkat sebagai kemampuan yang perlu diverifikasi ([NISTIR 8259 Rev. 1](https://csrc.nist.gov/pubs/ir/8259/r1/final); [katalog IoT NIST](https://pages.nist.gov/IoT-Device-Cybersecurity-Requirement-Catalogs/technical/)).

Jika rekaman memuat orang, ekspor dan playback memerlukan tujuan, pemilik, otorisasi, dan aturan penghapusan yang ditinjau untuk konteks aktual ([UU No. 27 Tahun 2022](https://peraturan.bpk.go.id/Details/229798/uu-no-27-tahun-2022)).

## Contoh keputusan praktis

Misalkan ada 12 kamera aktif dan 4 kamera tahap kedua yang disetujui. Angka desainnya 16 kanal. Jika proyek menyepakati dua kanal cadangan, pilih recorder minimal 18 kanal, dengan syarat input, decoding, lisensi, dan alur uji mendukungnya. Kanal cadangan bukan izin menambah kamera tanpa revisi.

Jika empat kamera belum punya lokasi atau pemilik anggaran, buat skenario 12 kanal dan tandai [NEEDS APPROVAL: 4 FUTURE CAMERAS].

Dokumen sizing sebaiknya memisahkan tiga kolom: kondisi terpasang, kondisi yang disetujui, dan opsi. Catat nomor kanal yang dipakai, nama kamera, stream utama atau tambahan, serta alasan kanal cadangan. Saat terjadi perubahan denah, perbarui tabel sebelum teknisi menarik kabel. Dengan cara ini, orang yang memeriksa di lapangan dapat membandingkan label fisik, alamat perangkat, dan konfigurasi recorder tanpa mengandalkan ingatan.

Untuk tahap pengadaan, minta penjual menunjukkan batas input per codec dan resolusi, jumlah decoding bersamaan, kebutuhan lisensi, serta prosedur pemulihan konfigurasi. Mintalah model dan firmware ditulis pada penawaran; nama seri saja belum cukup untuk audit perubahan. Bila pekerjaan berlanjut ke pemasangan di lokasi tertentu, gunakan halaman layanan lokal seperti [pemasangan CCTV di Yosowilangun](/kota/jual-pasang-cctv-yosowilangun/) atau [pemasangan CCTV di Wuluhan](/kota/jual-pasang-cctv-wuluhan/) hanya setelah kebutuhan kanal dan ruang ekspansi disetujui.

Pada serah terima, simpan daftar akun dan peran, waktu pengujian, hasil setiap kamera, contoh file ekspor, serta catatan kegagalan. Bukti ini membantu membedakan masalah kanal dari masalah jaringan, penyimpanan, atau hak akses. Jika ada kamera yang hanya tampil tetapi tidak masuk rekaman, hentikan klaim siap operasi sampai penyebab dan tindakan korektif dicatat.

Tambahkan kolom “pemicu perubahan” pada lembar sizing. Isinya dapat berupa pembukaan area baru, perubahan tujuan pengamatan, atau keputusan menambah kamera. Pemicu membuat tim tahu kapan angka kanal harus dihitung ulang. Sertakan juga batas pemilik keputusan: siapa yang menyetujui kamera baru, siapa yang memeriksa kompatibilitas, dan siapa yang menandatangani uji. Tanpa pembagian ini, kanal cadangan sering dipakai spontan dan dokumentasi tertinggal.

Saat membandingkan dua recorder, jangan hanya membandingkan jumlah kanal pada label. Bandingkan cara perangkat menangani stream utama dan tambahan, jumlah sesi playback, ekspor bersamaan, pembaruan firmware, serta pemulihan konfigurasi. Minta bukti tertulis untuk fitur yang menjadi syarat, lalu catat fitur yang belum diuji sebagai batas penerimaan. Pendekatan ini menjaga keputusan tetap dapat ditelusuri ketika kebutuhan berubah.

| Pertanyaan | Bukti | Konsekuensi |
|---|---|---|
| Stream wajib saat serah terima? | Daftar kamera disetujui | Kapasitas dasar |
| Ekspansi punya rencana nyata? | Tahap, pemilik, lokasi, waktu | Kanal cadangan |
| Kombinasi kompatibel? | Datasheet dan uji ONVIF | Mencegah gagal merekam |
| Playback dan ekspor berfungsi? | Skenario uji dan matriks akses | Mencegah gagal saat insiden |

## Kesalahan umum dan cara memeriksanya

Jangan membeli recorder 16 kanal hanya karena denah menunjukkan 16 kamera. Stream tambahan atau lisensi dapat mengubah kebutuhan. Periksa definisi kanal pada datasheet, lalu tulis jumlah kanal kosong dan pemilik persetujuan ekspansi.

Jangan menguji tampilan langsung saja. Kawan Tukang.co.id, minta uji penerimaan dari kamera masuk sampai ekspor dan pembukaan file hasil ekspor. Simpan versi firmware dan konfigurasi saat uji. Merek sama juga bukan bukti kompatibilitas.

## Jalan pintas yang tampak murah

Membeli kapasitas terbesar lalu mengisi kamera belakangan dapat mengunci anggaran pada fitur yang tidak diperlukan, sementara decoding, lisensi, firmware, atau jalur fisik belum terjawab. Gunakan lembar sizing berisi stream, tahap ekspansi, kanal cadangan, kompatibilitas teruji, dan kriteria penerimaan.

## Penutup

Kebutuhan channel recorder adalah stream yang disahkan ditambah ruang ekspansi yang dapat dijelaskan, lalu diverifikasi terhadap input, decoding, lisensi, kompatibilitas, dan uji playback/export. Sobat Tukang.co.id, sebelum memesan, minta daftar kamera bernomor, spesifikasi model dan firmware, jumlah kanal kosong, serta berita acara uji.

Angka ini adalah metode, bukan persetujuan desain. Jika data atau kriteria uji belum lengkap, pertahankan [NEEDS PROJECT TECHNICAL REVIEW] dan jangan menyatakan recorder sudah memadai.
