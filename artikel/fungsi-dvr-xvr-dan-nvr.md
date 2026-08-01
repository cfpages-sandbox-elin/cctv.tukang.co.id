---
article_id: CCT-05-01
writing_contract_version: "native-id-v2"
title: "DVR, XVR, dan NVR: fungsi dan batas masing-masing"
slug: "fungsi-dvr-xvr-dan-nvr"
description: "Panduan memilih kelas recorder berdasarkan arsitektur, penyimpanan, retensi, redundansi, playback, dan ekspor."
status: draft
publication_date: "2025-08-20"
publication_date_basis: editorial_backfill
date_modified: null
parent_topic: CCT-05
primary_intent: "Choose a recorder class based on system architecture."
reader_community: "Tukang.co.id"
reader_address: "Teman Tukang.co.id"
final_route: "/artikel/fungsi-dvr-xvr-dan-nvr.html"
technical_review: required
sources:
  - "https://webstore.iec.ch/en/publication/7353"
  - "https://www.onvif.org/profiles/profile-t/"
  - "https://www.onvif.org/"
  - "https://csrc.nist.gov/pubs/ir/8259/r1/final"
  - "https://pages.nist.gov/IoT-Device-Cybersecurity-Requirement-Catalogs/technical/"
  - "https://peraturan.bpk.go.id/Details/229798/uu-no-27-tahun-2022"
  - "https://www.iso.org/standard/62542.html"
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

# DVR, XVR, dan NVR: fungsi dan batas masing-masing

Halo, Teman Tukang.co.id! Memilih recorder bukan sekadar mencari kotak dengan channel paling banyak. DVR, XVR, dan NVR berbeda pada tempat sinyal diproses, jenis kamera yang diterima, serta cara rekaman disimpan dan diakses. Karena itu, recorder yang tampak lebih mahal atau lebih baru belum tentu cocok dengan arsitektur CCTV Anda.

Jawaban singkatnya: DVR umumnya menerima kamera analog melalui kabel koaksial dan mengubahnya menjadi rekaman digital; NVR menerima aliran video jaringan dari kamera IP; XVR berada di tengah, biasanya dirancang untuk menerima beberapa keluarga sinyal analog dan, pada model tertentu, sebagian kamera jaringan. Batas yang menentukan keputusan adalah dukungan persis pada model dan firmware, bandwidth, codec, kapasitas penyimpanan, serta kebutuhan bukti saat diputar atau diekspor. Kamera yang “bisa tampil” di demo belum otomatis menjamin fitur, stabilitas, atau hasil identifikasi di lokasi. Pedoman aplikasi CCTV juga menekankan bahwa resolusi atau jumlah kamera saja tidak membuktikan cakupan dan hasil yang berguna ([IEC 62676-4](https://webstore.iec.ch/en/publication/7353)).

![Ilustrasi CCTV Merk ZKTECO](/wp-content/uploads/2023/08/CCTV-Merk-ZKTECO.jpg)

Ilustrasi umum dari aset lokal cctv.tukang.co.id; bukan dokumentasi proyek tertentu.

## Definisi dan batas objek

Recorder adalah titik yang menerima, mengatur, menyimpan, dan mengeluarkan kembali rekaman. Ia bukan pengganti kamera, kabel, jaringan, monitor, atau prosedur pengelolaan bukti. Istilah berikut membantu membatasi pilihan:

- **DVR (Digital Video Recorder)** menerima sinyal dari kamera analog melalui jalur koaksial, lalu melakukan digitalisasi dan kompresi di recorder. Jalur kamera dan jalur jaringan biasanya dipisahkan secara fungsi.
- **NVR (Network Video Recorder)** menerima stream (aliran video) dari kamera IP melalui jaringan. Sebagian proses, seperti kompresi dan metadata, berlangsung di kamera sebelum data dikirim ke NVR.
- **XVR** adalah recorder hibrida. Namanya tidak menetapkan satu daftar kemampuan universal; setiap model dapat membatasi tipe sinyal, resolusi, audio, event, atau jumlah kamera jaringan yang diterima.

Maka, “XVR mendukung semua kamera” atau “NVR pasti lebih bagus” adalah penyederhanaan yang berbahaya. Kompatibilitas harus dibaca dari lembar data model dan firmware yang akan dipasang, lalu diuji pada alur kerja yang benar-benar dibutuhkan. ONVIF Profile T, misalnya, mendeskripsikan kemampuan streaming, imaging, event, metadata, PTZ, HTTPS, dan audio pada peran produk tertentu; logo atau checkbox ONVIF sendiri tidak membuktikan semua fitur opsional bekerja pada kombinasi perangkat Anda ([Profile T](https://www.onvif.org/profiles/profile-t/), [panduan produk konforman ONVIF](https://www.onvif.org/)).

Di halaman ini, pembahasan dibatasi pada fungsi recorder, pilihan arsitektur, penyimpanan, retensi, redundansi, playback, dan ekspor. Pemilihan kamera yang tepat untuk sebuah scene adalah keputusan tersendiri; jangan menjadikan artikel ini sebagai pengganti uji kompatibilitas kamera tertentu.

## Cara kerjanya

Pada sistem DVR, kamera mengirim sinyal ke input recorder. DVR mendigitalisasi sinyal itu, memberi waktu dan konfigurasi kanal, kemudian menulis potongan rekaman ke media penyimpanan. Jika salah satu jalur koaksial, catu daya, atau input bermasalah, kanal tersebut dapat hilang sementara kanal lain tetap berjalan. Integrasi jaringan tetap mungkin ada untuk akses jarak jauh, tetapi sumber video utamanya adalah input yang didukung DVR.

Pada sistem NVR, kamera IP mengirim stream melewati switch dan jaringan menuju NVR. Setiap kamera menggunakan alamat, akun, dan parameter jaringan. Akibatnya, kapasitas switch, uplink, bandwidth, latensi, dan pengaturan keamanan menjadi bagian dari rantai rekaman. Putus jaringan antara kamera dan NVR dapat memengaruhi rekaman meskipun kamera masih menyala. Fitur edge recording atau penyimpanan lokal kamera, bila tersedia dan diuji, bukan jaminan pemulihan otomatis tanpa prosedur sinkronisasi yang jelas.

XVR mengikuti pola hibrida: input analog diproses seperti DVR, sementara kamera jaringan masuk melalui port atau konfigurasi IP yang disediakan. “Jumlah channel” dapat berarti gabungan beberapa tipe input, bukan jumlah kamera bebas tanpa syarat. Periksa tabel mode: berapa input analog aktif ketika kanal IP dipakai, resolusi dan frame rate yang diterima, serta apakah audio, event, atau playback serentak mengurangi kapasitas efektif.

Di ketiga kelas, alurnya tetap perlu dijelaskan sebagai: sumber video → transport/input → pemrosesan dan penandaan waktu → penyimpanan → pencarian/playback → ekspor dan pengamanan akses. Catat siapa yang boleh mengubah waktu, menghapus rekaman, menyalin file, atau mengakses jarak jauh. Praktik keamanan perangkat IoT mencakup identitas perangkat, konfigurasi aman, perlindungan data, kontrol akses, pembaruan, pemantauan, dan pensiun perangkat; mengganti kata sandi bawaan saja belum memenuhi seluruh kebutuhan itu ([NISTIR 8259 Rev. 1](https://csrc.nist.gov/pubs/ir/8259/r1/final), [katalog kemampuan teknis NIST](https://pages.nist.gov/IoT-Device-Cybersecurity-Requirement-Catalogs/technical/)).

## Faktor yang mengubah hasil

Pertama, petakan **arsitektur yang sudah ada**. Jika sebagian besar kabel dan kamera analog masih layak, DVR atau XVR dapat mengurangi perubahan jalur. Jika jaringan IP sudah dirancang dengan switch, VLAN, dan titik daya yang memadai, NVR mungkin lebih selaras. Kesimpulan ini berubah bila kamera campuran, jarak, lingkungan, atau rencana ekspansi menuntut rancangan berbeda.

Kedua, hitung **beban nyata**, bukan hanya jumlah kanal di brosur. Resolusi, frame rate, codec, bitrate, audio, metadata, event, dan jumlah stream saat live view atau playback memengaruhi throughput serta ruang simpan. Minta angka input bandwidth, decoding playback serentak, dan mode kanal gabungan dari datasheet model yang dipilih.

Ketiga, tetapkan **retensi dan pemulihan**. Lama simpan bergantung pada bitrate, jadwal rekam, jumlah stream, dan kapasitas media; tidak aman menjanjikan “sekian hari” tanpa parameter tersebut. Pisahkan kebutuhan rekaman harian dari salinan insiden. Redundansi—misalnya media cadangan, ekspor terkontrol, atau recorder pengganti—mengurangi dampak satu kegagalan, tetapi bukan berarti data pasti utuh. Uji restore dan playback dari salinan, termasuk suara, timestamp, watermark, dan format yang dapat dibuka oleh pihak penerima.

Keempat, periksa **akses dan privasi**. Rekaman dapat memuat wajah, aktivitas, atau area yang terhubung dengan orang tertentu. Tujuan, siapa yang mengakses, berapa lama disimpan, kapan diekspor, dan bagaimana dihapus perlu ditetapkan sesuai konteks pengendali/pemroses data; Undang-Undang Pelindungan Data Pribadi memerlukan tinjauan hukum aktual, bukan sekadar memasang tanda peringatan ([UU No. 27 Tahun 2022](https://peraturan.bpk.go.id/Details/229798/uu-no-27-tahun-2022)). Pengelolaan rekaman juga perlu jejak versi, pemilik, akses, dan masa simpan yang konsisten dengan kebijakan records management ([ISO 15489-1:2016](https://www.iso.org/standard/62542.html)).

Kelima, lihat **bukti penerimaan**. Sebelum serah terima, dokumentasikan model dan firmware, daftar kanal, sumber waktu, kondisi jaringan, hasil rekam, pencarian, playback, ekspor, akun, pembaruan, serta cara pemulihan. Kemampuan yang belum diuji tetap merupakan asumsi.

## Contoh keputusan praktis

Gunakan tabel ini sebagai penyaring awal, bukan persetujuan desain:

| Kondisi awal dan kebutuhan | Kelas yang layak diselidiki | Pertanyaan pengunci |
|---|---|---|
| Mayoritas kamera analog, jalur koaksial dipertahankan | DVR atau XVR | Apakah standar sinyal dan resolusi kamera benar-benar tercantum pada model? |
| Kamera baru dan lama harus berjalan bersama | XVR | Berapa kombinasi kanal analog/IP yang aktif pada mode yang dipilih? |
| Kamera IP, jaringan dan daya sudah dirancang | NVR | Berapa bandwidth kamera, uplink, dan decoding playback yang tersedia? |
| Rekaman harus dicari dan diekspor untuk insiden | Semua kelas | Apakah timestamp, format ekspor, integritas, dan hak akses sudah diuji? |
| Perlu memperpanjang masa simpan | Semua kelas | Parameter bitrate/jadwal apa yang dipakai untuk menghitung media dan backup? |

Contoh bersyarat: jika delapan kamera analog lama akan dipertahankan dan dua kamera IP ditambahkan, XVR baru masuk daftar pemeriksaan. Namun keputusan akhir menunggu tabel mode, bandwidth IP, kompatibilitas firmware, dan uji rekam-playback. Jika seluruh kamera akan diganti menjadi IP, membandingkan XVR dengan NVR berdasarkan harga kotak saja mengabaikan desain switch, segmentasi, dan pemeliharaan.

Teman Tukang.co.id, tulis keputusan itu dalam lembar verifikasi: sumber tiap kamera, jalur, mode input, beban stream, media, retensi yang disetujui, prosedur ekspor, dan pemilik akses. Dengan begitu, perubahan satu kamera tidak diam-diam mengurangi rekaman kanal lain.

## Kesalahan umum dan cara memeriksanya

**Menyamakan jumlah channel dengan kapasitas sistem.** Periksa catatan “analog + IP”, batas bandwidth, decoding, dan mode simultan; minta bukti uji untuk konfigurasi aktual.

**Menganggap ONVIF berarti pasti kompatibel.** Cocokkan profil, peran client/device, firmware, fitur wajib dan kondisional, lalu uji discovery, stream, event, audio, PTZ bila diperlukan. Panduan ONVIF sendiri mengarahkan verifikasi produk konforman, bukan sekadar klaim pemasaran.

**Menghitung retensi dari kapasitas hard disk saja.** Gunakan bitrate dan jadwal rekam yang disepakati, sisakan rencana untuk event dan salinan. Uji berapa lama rekaman benar-benar dapat dicari pada mode tersebut.

**Mengabaikan jam dan ekspor.** Uji sinkronisasi waktu, nama file, player, hash atau jejak salinan sesuai kebijakan, serta siapa yang mengesahkan ekspor. Rekaman yang ada tetapi tidak dapat ditemukan atau dipahami saat diperlukan belum memenuhi tujuan operasional.

**Membuka recorder ke internet secara langsung.** Kawan Tukang.co.id, perlakukan akses jarak jauh sebagai permukaan serangan: inventaris perangkat, akun dan peran, segmentasi, pembaruan, pencatatan akses, backup konfigurasi, dan prosedur insiden harus ditentukan. NIST menempatkan secure operation dan kemampuan memperbarui perangkat sebagai bagian dari profil penggunaan, bukan tambahan kosmetik.

**Mengklaim hasil scene dari spesifikasi kamera.** Megapixel, demo toko, atau rekaman siang hari tidak membuktikan identifikasi pada lokasi Anda. Tujuan scene, cahaya, posisi, dan kriteria penerimaan perlu diukur dan ditinjau sesuai pedoman aplikasi CCTV ([IEC 62676-4](https://webstore.iec.ch/en/publication/7353)).

## Jangan memilih hanya karena jalan pintas

Shortcut yang sering dipilih adalah membeli recorder dengan channel terbesar agar “aman untuk masa depan”. Itu dapat gagal karena channel gabungan, bandwidth, decoding, storage, firmware, atau jaringan tidak ikut membesar. Alternatif yang lebih dapat dipertanggungjawabkan adalah membuat skenario pertumbuhan: kamera dan stream yang direncanakan, ruang simpan dan retensi, port jaringan, lisensi atau batas perangkat, serta uji playback dan ekspor. Jika data model atau bukti uji belum ada, tandai sebagai [NEEDS TECHNICAL REVIEW: exact model/firmware compatibility, effective channel mode, bandwidth, storage-retention calculation, and export/restore test].

## Kesimpulan

DVR cocok diteliti ketika sumber utama adalah analog; NVR ketika sumber utama adalah kamera IP dan jaringan siap; XVR ketika sistem campuran memang membutuhkan jembatan—dengan syarat mode dan kompatibilitas model dibuktikan. Tidak satu pun kelas otomatis menjamin retensi, keamanan, atau bukti yang dapat dipakai.

Langkah berikutnya: buat lembar arsitektur untuk setiap kamera, minta datasheet dan firmware yang spesifik, hitung beban serta media dari parameter nyata, lalu lakukan uji rekam, pencarian, playback, ekspor, dan pemulihan sebelum serah terima. **Aturan operasinya: pilih recorder berdasarkan alur bukti yang harus dipertahankan dan hasil uji konfigurasi aktual, bukan berdasarkan label DVR/XVR/NVR atau jumlah channel semata.**

Jika Anda perlu menelusuri konteks layanan dan perangkat yang tersedia, mulai dari [halaman utama Tukang.co.id](/), lalu buka [ruang rujukan perangkat Dahua](/dahua/) hanya bila merek tersebut memang masuk daftar kandidat Anda.
