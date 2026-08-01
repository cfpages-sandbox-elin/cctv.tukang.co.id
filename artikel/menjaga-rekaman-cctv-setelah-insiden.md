---
article_id: CCT-18-04
title: "Menjaga rekaman CCTV setelah insiden"
slug: "menjaga-rekaman-cctv-setelah-insiden"
description: "Take control of the system, understand warranty conditions, preserve incident material, and close the data lifecycle."
status: draft
writing_contract_version: "native-id-v2"
publication_date: "2026-07-16"
publication_date_basis: editorial_backfill
date_modified: null
parent_topic: CCT-18
primary_intent: "Preserve original material, metadata, access records, copies, and authorization."
reader_community: "Tukang.co.id"
reader_address: "Teman Tukang.co.id"
final_route: "/artikel/menjaga-rekaman-cctv-setelah-insiden.html"
technical_review: required
sources:
  - "https://www.ilo.org/topics-and-sectors/occupational-safety-and-health-guide-labour-inspectors-and-other/how-can-occupational-safety-and-health-be-managed/controlling-risks"
  - "https://www.iso.org/standard/62542.html"
  - "https://peraturan.bpk.go.id/Details/229798/uu-no-27-tahun-2022"
  - "https://csrc.nist.gov/pubs/ir/8259/r1/final"
  - "https://www.onvif.org/profiles/profile-t/"
  - "https://bnsp.go.id/"
---

# Menjaga rekaman CCTV setelah insiden

Halo, Teman Tukang.co.id! Setelah insiden, jangan langsung mematikan recorder, mencabut hard disk, atau mengirim potongan video lewat grup chat. Langkah pertama adalah membatasi perubahan pada sistem: tunjuk satu orang yang berwenang, catat waktu dan kondisi awal, lalu amankan salinan kerja tanpa menghapus materi asli. Rekaman yang masih utuh, metadata waktunya, dan catatan siapa yang mengaksesnya jauh lebih berguna daripada video pendek yang tidak jelas asalnya.

Urutan sederhananya: hentikan perubahan yang tidak perlu, dokumentasikan identitas sistem dan jam, simpan rekaman asli secara read-only bila fitur tersedia, buat salinan terverifikasi untuk pemeriksaan, dan batasi distribusi. Apa yang harus disimpan, berapa lama, dan kepada siapa boleh diberikan bergantung pada tujuan insiden, kebijakan organisasi, kontrak, serta aturan privasi yang berlaku. Karena itu artikel ini bukan penetapan keabsahan alat bukti; **[NEEDS LEGAL/PRIVACY REVIEW: konfirmasi dasar pemrosesan, retensi, permintaan akses, dan pengungkapan untuk kasus aktual]**.

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

## Jawaban singkat dan salah paham utama

Menjaga rekaman berarti menjaga **materi asli, konteks, dan jejak pengelolaannya**. Materi asli adalah berkas atau segmen yang dihasilkan recorder; konteks mencakup kamera, kanal, zona waktu, pengaturan, dan rentang waktu; jejak pengelolaan mencakup siapa menyalin, kapan, dengan alat apa, dan ke mana salinan disimpan. Memotong video agar mudah dibagikan boleh dilakukan sebagai salinan kerja, tetapi jangan menggantikannya dengan sumber asli.

Salah paham yang sering merugikan adalah mengira satu file MP4 sudah cukup. Ekspor dapat menghilangkan metadata, mengubah zona waktu, atau tidak menunjukkan apakah file berasal dari kamera yang benar. Prinsip pengelolaan rekaman menuntut informasi yang dapat ditemukan, dipahami, dan dipertahankan sepanjang siklus hidupnya; kerangka [ISO 15489-1](https://www.iso.org/standard/62542.html) membantu melihat rekaman sebagai objek yang memiliki konteks, kontrol akses, retensi, dan pemusnahan terdokumentasi.

## Definisi dan batas objek

Objek yang dibahas ialah rekaman insiden pada kamera dan recorder yang benar-benar berada dalam penguasaan Anda, beserta metadata, log akses, salinan, dan keputusan retensinya. “Asli” di sini berarti salinan pertama yang diekspor atau media sumber yang tidak diedit; bukan klaim bahwa isinya otomatis sah atau benar. “Retensi” berarti masa simpan yang ditetapkan berdasarkan tujuan dan risiko, bukan angka universal untuk semua lokasi.

Artikel ini tidak menentukan siapa yang bersalah, memastikan video dapat diterima di pengadilan, menginstruksikan penyitaan perangkat, atau menetapkan kewajiban hukum organisasi. Rekaman CCTV dapat memuat data pribadi. [UU Pelindungan Data Pribadi](https://peraturan.bpk.go.id/Details/229798/uu-no-27-tahun-2022) mengharuskan penilaian atas tujuan, akses, pengungkapan, keamanan, dan penghapusan; penerapannya harus dicocokkan dengan peran pengendali/prosesor dan kondisi kasus. Bila insiden melibatkan pekerja, pelanggan, atau area publik, minta peninjauan hukum dan privasi sebelum membagikan materi.

## Cara kerjanya

Gunakan alur berikut dan catat setiap perpindahan:

1. **Tunjuk pengendali awal.** Satu operator mencatat siapa yang melapor, kapan insiden diketahui, kamera atau kanal yang diduga relevan, serta siapa yang diberi otorisasi. Jangan membuat akun bersama. Praktik identitas dan akses yang tertib sejalan dengan panduan keamanan perangkat IoT [NISTIR 8259 Rev. 1](https://csrc.nist.gov/pubs/ir/8259/r1/final).
2. **Bekukan konteks, bukan seluruh operasi tanpa alasan.** Catat jam recorder, zona waktu, status penyimpanan, perubahan konfigurasi terakhir, dan apakah sistem sedang menimpa rekaman lama. Jika perlu mengisolasi perangkat untuk mencegah penghapusan, lakukan sesuai prosedur organisasi dan instruksi vendor; jangan mencabut daya secara serampangan karena dapat merusak data atau menghilangkan log.
3. **Tentukan rentang waktu dan kamera.** Simpan beberapa menit sebelum dan sesudah kejadian agar urutan sebab-akibat tidak dipotong. Catat kanal, nama kamera, resolusi yang diekspor, format, dan metode ekspor. Jika sistem mendukung metadata atau watermark, simpan juga berkas pendampingnya.
4. **Buat salinan kerja terpisah.** Simpan salinan asli pada media dengan akses terbatas. Buat hash (sidik digital berkas) bila organisasi memiliki alat dan prosedur yang tervalidasi, lalu catat nilai hash, nama berkas, ukuran, waktu, dan operator. Hash membantu mendeteksi perubahan; ia tidak membuktikan isi video atau keabsahan hukum.
5. **Catat perpindahan dan pemeriksaan.** Setiap akses, penyalinan, pemutaran, atau pengiriman dicatat dalam log sederhana: identitas, waktu, tujuan, media, dan tindakan. Pemeriksaan risiko yang baik memang perlu membedakan kondisi awal, kontrol, dan tindakan lanjutan, bukan sekadar mengumpulkan formulir ([ILO, controlling risks](https://www.ilo.org/topics-and-sectors/occupational-safety-and-health-guide-labour-inspectors-and-other/how-can-occupational-safety-and-health-be-managed/controlling-risks)).
6. **Tutup siklusnya.** Setelah kebutuhan insiden, kewajiban retensi, dan permintaan yang sah berakhir, dokumentasikan keputusan penghapusan atau anonimisasi. Jangan menyimpan salinan di ponsel pribadi atau cloud pribadi hanya karena lebih cepat.

## Faktor yang mengubah hasil

Hasil ekspor dan keputusan retensi dipengaruhi oleh jam sistem, zona waktu, sinkronisasi, mode perekaman, kapasitas penyimpanan, overwrite, dan kesehatan media. Kamera yang benar pada kanal yang salah dapat membuat pencarian menyesatkan. Fitur interoperabilitas juga tidak otomatis menjamin hasil yang sama pada setiap recorder; klaim dukungan harus dicek terhadap model, firmware, peran, dan fitur yang benar-benar diuji, bukan sekadar logo protokol ([ONVIF Profile T](https://www.onvif.org/profiles/profile-t/)).

Kondisi akses mengubah risiko. Kata sandi bersama, akun mantan operator, port yang terbuka, atau ekspor melalui perangkat tak terenkripsi memperluas kemungkinan perubahan dan kebocoran. Sobat Tukang.co.id, perlakukan kredensial, log, dan video sebagai satu paket pengendalian: cabut akses yang tidak lagi diperlukan, aktifkan autentikasi yang tersedia, dan simpan daftar siapa yang masih berwenang. Jangan mengubah konfigurasi saat investigasi kecuali perubahan itu dicatat dan memang diperlukan untuk mencegah kehilangan.

Tujuan penggunaan juga menentukan masa simpan. Permintaan dari korban, perusahaan asuransi, regulator, atau aparat dapat memiliki prosedur berbeda. Kebijakan internal tidak boleh dipakai untuk mengabaikan permintaan yang sah, tetapi permintaan lisan pun jangan langsung dipenuhi tanpa memeriksa identitas, ruang lingkup, dan otorisasinya. **[NEEDS CASE-SPECIFIC REVIEW: tentukan retensi, dasar pengungkapan, dan respons permintaan untuk lokasi serta pihak yang terlibat]**.

## Contoh keputusan praktis

Misalkan operator melihat kejadian pada pukul 14.10 dari kamera gerbang. Ia tidak tahu apakah jam recorder tepat dan sistem menimpa data setiap hari. Keputusan yang aman bukan langsung mengirim potongan 30 detik, melainkan:

| Pertanyaan | Jika jawabannya belum jelas | Keputusan sementara |
| --- | --- | --- |
| Jam recorder dan zona waktu sudah dicatat? | Belum | Foto layar status, catat waktu rujukan, lalu minta pemeriksaan teknis. |
| Rentang sebelum-sesudah kejadian tersedia? | Tidak | Bekukan media dan eskalasi; jangan menyimpulkan urutan dari potongan pendek. |
| File asli, metadata, dan log ekspor tersimpan? | Tidak | Buat ekspor ulang sesuai prosedur, simpan salinan terpisah, dan catat kegagalan. |
| Peminta memiliki otorisasi? | Tidak jelas | Tahan pengiriman, verifikasi identitas dan dasar permintaan. |
| Sistem masih menimpa rekaman? | Ya | Aktifkan langkah preservasi yang disetujui pemilik sistem; jangan melakukan tindakan listrik atau forensik tanpa kompetensi. |

Jika polisi atau penasihat hukum meminta perangkat asli, catat serah-terima dan minta instruksi tertulis tentang ruang lingkupnya. Jika hanya perlu meninjau, berikan salinan kerja yang diberi label, bukan mengubah media sumber. Untuk pengelola yang memakai operator bersertifikat, verifikasi identitas, ruang lingkup, dan masa berlaku melalui penerbit atau catatan resmi; situs [BNSP](https://bnsp.go.id/) adalah titik awal verifikasi, bukan bukti bahwa seseorang otomatis berwenang pada sistem Anda.

Jika Anda membutuhkan pemeriksaan atau penggantian perangkat setelah preservasi selesai, mulai dari [halaman utama Tukang.co.id](/) untuk menjelaskan kebutuhan dan batas akses. Untuk lokasi yang memang berada di Dau, Anda dapat melihat [opsi jual-pasang CCTV di Dau](/kota/jual-pasang-cctv-dau/) sebagai langkah mencari penyedia; rute itu bukan bukti bahwa penyedia tertentu menangani atau menilai insiden Anda.

## Kesalahan umum dan cara memeriksanya

- **Memotong lalu menghapus sumber.** Tanyakan: di mana file sebelum dipotong, siapa menyimpannya, dan apakah checksum atau catatan ekspor tersedia?
- **Mengandalkan timestamp layar.** Bandingkan jam recorder dengan sumber waktu yang dicatat dan dokumentasikan selisihnya; jangan memperbaiki timestamp dengan edit video.
- **Menggunakan flashdisk atau akun pribadi.** Periksa pemilik media, izin akses, enkripsi yang tersedia, serta rencana pengembaliannya.
- **Mengubah password tanpa mencatat dampak.** Catat akun yang dinonaktifkan, waktu perubahan, dan apakah perubahan memutus akses pemantauan yang masih diperlukan.
- **Menganggap kamera yang sama selalu menghasilkan file yang sama.** Verifikasi model, firmware, format ekspor, dan keberadaan metadata pada sistem aktual.
- **Menyimpan selamanya.** Tetapkan pemilik keputusan retensi, tanggal tinjau, dasar penyimpanan, dan cara penghapusan yang dapat dicatat.

Kawan Tukang.co.id, bila salah satu jawaban itu “tidak tahu”, tandai sebagai ketidakpastian. Jangan menutup celah dengan narasi yakin atau menyebut video “pasti valid”. Minta pemeriksaan teknis, hukum, atau privasi sesuai jenis celahnya.

## Jalan pintas yang perlu dihindari

Shortcut yang paling menggoda adalah mengirim video lewat aplikasi pesan agar semua pihak segera melihatnya. Cara itu memang cepat, tetapi dapat membuat banyak salinan tanpa kendali, menghapus konteks, dan meninggalkan data pribadi di perangkat yang tidak dikelola. Alternatifnya: simpan sumber dan salinan kerja pada lokasi yang dikendalikan organisasi, kirim tautan berizin dengan masa berlaku bila tersedia, dan catat penerima serta tujuan pengiriman. Kecepatan tetap bisa dicapai tanpa kehilangan jejak.

## Langkah penutup

Menjaga rekaman CCTV setelah insiden berarti mengamankan sumber, konteks, metadata, log akses, salinan, dan keputusan retensi secara berurutan. Hari ini, tunjuk pengendali, catat status recorder dan jamnya, ekspor rentang yang relevan tanpa mengedit sumber, simpan salinan terbatas, lalu minta tinjauan teknis serta hukum/privasi untuk kasus nyata. Aturan operasionalnya sederhana: **jangan hapus, ubah, atau bagikan sebelum asal, otorisasi, tujuan, dan masa simpan setiap salinan tercatat**.
