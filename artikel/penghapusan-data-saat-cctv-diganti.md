---
article_id: CCT-09-06
writing_contract_version: "native-id-v2"
title: "Menghapus data dan kredensial saat CCTV diganti"
slug: "penghapusan-data-saat-cctv-diganti"
description: "Reduce unauthorized access and insecure remote connectivity across the device lifecycle."
status: draft
publication_date: "2025-12-13"
publication_date_basis: editorial_backfill
date_modified: null
parent_topic: CCT-09
primary_intent: "Decommission cameras, recorders, media, apps, and cloud accounts safely."
reader_community: "Tukang.co.id"
reader_address: "Teman Tukang.co.id"
final_route: "/artikel/penghapusan-data-saat-cctv-diganti.html"
technical_review: required
sources:
  - "https://csrc.nist.gov/pubs/ir/8259/r1/final"
  - "https://pages.nist.gov/IoT-Device-Cybersecurity-Requirement-Catalogs/technical/"
  - "https://peraturan.bpk.go.id/Details/229798/uu-no-27-tahun-2022"
  - "https://www.ilo.org/topics-and-sectors/occupational-safety-and-health-guide-labour-inspectors-and-other/how-can-occupational-safety-and-health-be-managed/controlling-risks"
---

# Menghapus data dan kredensial saat CCTV diganti

Halo, Teman Tukang.co.id! Mengganti kamera tanpa menutup akses lama dapat meninggalkan rekaman, akun administrator, atau koneksi jarak jauh pada perangkat yang sudah keluar dari lokasi. Jawaban singkatnya: lakukan inventaris, amankan bukti yang memang masih berwenang disimpan, cabut akses, hapus atau sanitasi media, lalu verifikasi bahwa perangkat dan akun lama tidak lagi dapat terhubung.

Jangan menganggap menekan tombol *factory reset* sudah cukup. Reset dapat mengembalikan konfigurasi, tetapi tidak otomatis mencabut sesi aplikasi, akun cloud, salinan rekaman, kartu memori, atau kredensial yang tersimpan pada layanan lain. Rincian langkah berubah menurut model, firmware, arsitektur cloud, dan kewenangan pemilik data. Karena itu, hasil penghapusan harus dicatat dan diperiksa oleh pihak yang berwenang; artikel ini tidak menentukan masa simpan atau izin pemusnahan rekaman.

![Ilustrasi CCTV Merk ZKTECO](/wp-content/uploads/2023/08/CCTV-Merk-ZKTECO.jpg)

Ilustrasi umum dari aset lokal Tukang.co.id; bukan dokumentasi proyek tertentu.

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

## Data dan kredensial apa saja yang harus ditangani?

Objeknya lebih luas daripada kamera di plafon. Petakan kamera, perekam (NVR/DVR), hard disk atau kartu memori, komputer pemantau, aplikasi seluler, akun cloud, gateway jaringan, dan perangkat lunak pihak ketiga. Untuk tiap objek, catat pemilik, nomor aset atau identitas perangkat, lokasi, akun yang terhubung, media penyimpanan, serta status penggantian.

Pisahkan tiga jenis bahan. Pertama, data video dan audio, termasuk ekspor insiden, foto tangkapan layar, dan cadangan otomatis. Kedua, kredensial dan token: nama pengguna, kata sandi, kunci API, kode pemulihan, sesi browser, serta akun berbagi. Ketiga, metadata konfigurasi seperti alamat jaringan, daftar pengguna, aturan notifikasi, dan pasangan perangkat. Katalog kapabilitas keamanan IoT NIST menempatkan identitas perangkat, perlindungan data, kontrol akses, konfigurasi aman, operasi, dan pensiun perangkat sebagai kebutuhan yang berbeda; mengganti satu kata sandi tidak membuktikan seluruhnya sudah ditutup ([NISTIR 8259 Rev. 1](https://csrc.nist.gov/pubs/ir/8259/r1/final), [katalog kapabilitas NIST](https://pages.nist.gov/IoT-Device-Cybersecurity-Requirement-Catalogs/technical/)).

Batas artikel ini adalah sanitasi teknis. Persetujuan retensi, dasar pemrosesan, permintaan akses, *legal hold*, dan berita acara pemusnahan harus mengikuti register organisasi serta tinjauan privasi yang berlaku. UU Pelindungan Data Pribadi menjadi rujukan untuk menentukan kapan penanganan data pribadi memerlukan keputusan dan dokumentasi khusus, bukan izin otomatis untuk menghapus semua rekaman ([UU No. 27 Tahun 2022](https://peraturan.bpk.go.id/Details/229798/uu-no-27-tahun-2022)).

## Urutan kerja yang dapat diverifikasi

Mulai dengan penetapan kewenangan. Pemilik sistem atau pengelola data menetapkan rekaman mana yang masih harus dipertahankan dan siapa yang boleh menyetujui penghapusan. Jika statusnya belum jelas, hentikan penghapusan dan tandai `[NEEDS RETENTION AUTHORIZATION]`. Siklus penilaian risiko ILO menganjurkan identifikasi bahaya, penilaian, pengendalian, dan peninjauan; gunakan pola yang sama untuk risiko akses tertinggal, bukan sekadar mengejar kecepatan bongkar ([ILO—controlling risks](https://www.ilo.org/topics-and-sectors/occupational-safety-and-health-guide-labour-inspectors-and-other/how-can-occupational-safety-and-health-be-managed/controlling-risks)).

Berikutnya, buat daftar sumber akses. Periksa konsol kamera dan perekam, aplikasi ponsel setiap administrator, portal cloud, akun email pemulihan, integrasi jaringan, dan layanan notifikasi. Simpan bukti konfigurasi hanya jika berwenang dan lindungi salinan tersebut. Nonaktifkan pengguna lama, cabut sesi atau token, hapus perangkat dari akun cloud, dan ubah kredensial yang dipakai bersama sistem lain. Kerjakan pencabutan sebelum perangkat dibawa pergi agar koneksi jarak jauh tidak tetap aktif.

Setelah akses dikendalikan, amankan data yang sah. Ekspor hanya rekaman yang memiliki tujuan dan persetujuan jelas, beri identitas versi, dan simpan pada lokasi dengan akses terbatas. Jangan menyalin seluruh disk sebagai kebiasaan. Jika data tidak lagi diperlukan dan kewenangan sudah ada, gunakan fungsi sanitasi yang didukung produsen atau prosedur organisasi untuk media tersebut. Perhatikan bahwa menu, dukungan firmware, dan kemampuan penghapusan berbeda antar-model; jangan menyatakan media sudah bersih tanpa verifikasi hasil.

Lepaskan perangkat dari jaringan, kemudian kembalikan konfigurasi pabrik sesuai petunjuk model. Untuk perekam, perlakukan hard disk internal dan media lepas-pasang sebagai objek terpisah. Jika media akan dipakai ulang, minta metode sanitasi dan uji baca-tulis dari pengelola TI; jika akan diserahkan atau dihancurkan, ikuti prosedur pemusnahan organisasi. Pekerjaan fisik di area bertegangan atau ketinggian tetap memerlukan otorisasi dan pengendalian K3 setempat.

Terakhir, lakukan verifikasi dari sisi pengguna dan jaringan. Coba akses dengan akun pengganti, pastikan akun lama ditolak, pastikan perangkat lama tidak muncul di portal, dan periksa bahwa notifikasi tidak lagi menuju penerima sebelumnya. Dokumentasikan tanggal, pelaksana, objek, metode, hasil, dan penyimpangan. Catatan itu membuktikan apa yang diperiksa—bukan jaminan bahwa semua salinan di luar inventaris otomatis hilang.

## Faktor yang mengubah hasil

Arsitektur menjadi faktor pertama. Sistem lokal dengan NVR memusatkan risiko pada perekam, disk, dan akun lokal; sistem cloud menambah portal vendor, aplikasi, email pemulihan, dan token. Sistem hibrida membutuhkan kedua jalur. Firmware yang sudah tidak didukung juga dapat membatasi pilihan sanitasi, sehingga pengelola perlu meminta bukti kemampuan resmi sebelum perangkat dipindahkan.

Jenis media dan cara penggunaannya ikut menentukan. Kartu memori yang pernah dipindahkan, ekspor ke laptop, rekaman pada NAS, atau cadangan otomatis dapat berada di luar menu kamera. Inventaris yang hanya mencatat nomor kamera akan melewatkan salinan itu. Sebaliknya, menghapus bukti insiden yang masih ditahan secara sah dapat menimbulkan masalah lain. Sobat Tukang.co.id, bila pemilik data tidak dapat menjawab “siapa yang menyetujui penghapusan ini?”, jangan lanjut ke langkah pemusnahan.

Perubahan personel dan vendor juga penting. Akun teknisi sementara, kode QR pemasangan, akses dukungan jarak jauh, dan grup berbagi sering dibuat untuk pekerjaan awal lalu terlupakan. Minta daftar pengguna aktif dari pemilik sistem, bukan hanya melihat akun yang tampak di satu aplikasi. Untuk pekerjaan yang melibatkan banyak pihak, tetapkan satu pemegang keputusan dan satu pemeriksa independen dari pelaksana bila memungkinkan.

Kondisi lapangan memengaruhi keselamatan urutan kerja. Pencabutan kabel, pemindahan perekam, atau pembongkaran di area publik dapat menambah risiko listrik, jatuh, dan gangguan operasi. Rencanakan isolasi energi dan pengamanan area melalui prosedur K3 proyek; sanitasi data tidak menghapus kewajiban keselamatan kerja.

## Contoh keputusan praktis

| Kondisi yang ditemukan | Keputusan aman berikutnya | Bukti minimum |
|---|---|---|
| Rekaman tidak memiliki status retensi yang jelas | Tunda penghapusan dan minta persetujuan pemilik data | Nama pemberi persetujuan, ruang lingkup rekaman, tanggal |
| Kamera diganti tetapi akun cloud tetap dipakai | Cabut perangkat, sesi, dan token dari portal; ubah kredensial terkait | Tangkapan status perangkat dan uji penolakan akun lama |
| NVR dikembalikan, disk tetap di dalam | Perlakukan disk sebagai media berisi data; sanitasi atau serahkan melalui prosedur resmi | Identitas disk, metode, hasil verifikasi |
| Teknisi lama masih tercantum sebagai administrator | Nonaktifkan akses dan periksa integrasi pemulihan | Daftar pengguna sebelum/sesudah dan pemeriksa |
| Vendor tidak menjelaskan kemampuan penghapusan | Jangan mengklaim bersih; eskalasi ke TI atau pemilik sistem | Respons vendor, model/firmware, keputusan tertulis |

Contoh ini bersifat kondisional, bukan bukti bahwa konfigurasi tertentu sudah aman. Jika satu baris tidak dapat dibuktikan, statusnya adalah “belum terverifikasi”, bukan “selesai”.

## Kesalahan umum dan cara memeriksanya

Kesalahan pertama adalah hanya menekan reset. Tanyakan: apakah akun cloud, aplikasi, token, dan media cadangan sudah dicabut atau diperiksa? Kesalahan kedua adalah mengganti kata sandi kamera tetapi mempertahankan kata sandi yang sama pada email pemulihan atau layanan jaringan. Tanyakan: apakah kredensial bersama pernah dipakai di sistem lain dan sudah diganti di sana?

Kesalahan ketiga adalah menganggap disk kosong karena daftar rekaman pada layar sudah hilang. Tanyakan: metode sanitasi apa yang didukung model, siapa yang menjalankannya, dan bagaimana hasilnya diverifikasi? Kesalahan keempat adalah membuat berita acara setelah fakta tanpa daftar objek. Gunakan inventaris bernomor agar pemeriksa dapat mencocokkan kamera, perekam, media, akun, dan hasil uji.

Shortcut yang paling menggoda adalah menyerahkan perangkat lama kepada vendor tanpa mencabut akses lebih dulu. Cara itu dapat memindahkan perangkat fisik tetapi membiarkan sesi dan akun tetap aktif. Alternatif yang lebih dapat dipertanggungjawabkan: cabut akses dari konsol, dokumentasikan statusnya, baru serahkan media melalui alur yang disetujui.

## Langkah berikutnya

Menghapus data dan kredensial saat CCTV diganti berarti menutup seluruh jejak akses—perangkat, media, aplikasi, cloud, dan integrasi—setelah status retensi disetujui. Buat satu lembar inventaris, minta pemilik data menyetujui objek yang boleh dihapus, lalu lakukan pencabutan dan sanitasi dengan pemeriksa yang dapat menguji penolakan akses lama.

Kawan Tukang.co.id, simpan catatan metode dan hasil tanpa memasukkan rahasia seperti kata sandi ke dalam berita acara. Jika Anda perlu menyiapkan penggantian berikutnya, gunakan [halaman utama Tukang.co.id](/) untuk memulai percakapan dan, bila lokasinya sesuai, lihat [layanan jual-pasang CCTV di Dau](/kota/jual-pasang-cctv-dau/) sambil membawa inventaris akses tadi. Untuk model atau arsitektur yang tidak menyediakan bukti sanitasi, tandai `[NEEDS TECHNICAL REVIEW]` dan eskalasi ke pengelola TI, vendor, atau profesional yang berwenang. Aturan operasionalnya sederhana: tidak ada bukti persetujuan, metode, dan verifikasi berarti perangkat belum boleh dianggap selesai dinonaktifkan.
