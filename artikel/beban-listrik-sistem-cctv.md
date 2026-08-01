---
article_id: CCT-07-01
title: "Menghitung beban listrik sistem CCTV"
slug: "beban-listrik-sistem-cctv"
description: "Panduan memperkirakan beban listrik CCTV dan menyiapkan data untuk pemeriksaan tenaga listrik."
status: draft
publication_date: "2025-10-09"
publication_date_basis: editorial_backfill
date_modified: null
parent_topic: CCT-07
primary_intent: "Estimate system load and identify circuits needing professional verification."
reader_community: "Tukang.co.id"
reader_address: "Sobat Tukang.co.id"
final_route: "/artikel/beban-listrik-sistem-cctv.html"
technical_review: required
writing_contract_version: "native-id-v2"
sources:
  - "https://www.ilo.org/topics-and-sectors/occupational-safety-and-health-guide-labour-inspectors-and-other/how-can-occupational-safety-and-health-be-managed/controlling-risks"
  - "https://www.ilo.org/publications/5-step-guide-employers-workers-and-their-representatives-conducting"
  - "https://peraturan.bpk.go.id/Details/47614/uu-no-1-tahun-1970"
  - "https://peraturan.bpk.go.id/Details/145984/permenaker-no-12-tahun-2015"
  - "https://webstore.iec.ch/en/publication/7353"
  - "https://webstore.iec.ch/en/publication/63699"
---

# Menghitung beban listrik sistem CCTV

Halo, Sobat Tukang.co.id! Beban listrik CCTV tidak cukup dihitung dari jumlah kamera. Jumlahkan kebutuhan daya kamera, perekam, jaringan, penyimpanan, layar, dan aksesori yang benar-benar menyala bersamaan. Setelah itu ubah total watt menjadi arus pada tegangan yang digunakan, lalu periksa apakah sirkuit, proteksi, pembumian, serta cadangan dayanya memang cocok.

Rumus perencanaan dasarnya sederhana: **daya total (W) = jumlah daya tiap perangkat (W)**, **arus perkiraan (A) = daya total (W) ÷ tegangan (V)**, dan **energi cadangan (Wh) = daya (W) × waktu yang diinginkan (jam)**. Angka pada label hanyalah titik awal. Model perangkat, mode malam, beban PoE, panjang kabel, suhu, kondisi sumber, dan kebutuhan rekaman dapat mengubah hasil. Karena itu, hasil di halaman ini bukan izin untuk mengubah panel atau mengerjakan instalasi bertegangan.

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

Yang dihitung adalah beban listrik peralatan CCTV pada kondisi operasi yang disepakati: kamera, NVR/DVR, switch atau injektor PoE, modem/router, monitor, hard disk, pemanas atau iluminator jika memang ada, serta UPS bila dipasang. Beban siaga dan beban puncak sebaiknya dicatat terpisah. Kamera yang sama dapat menarik daya berbeda saat iluminator aktif, sedangkan switch PoE dapat menanggung beban kamera sekaligus konsumsi elektroniknya sendiri.

Yang tidak bisa diputuskan dari rumus umum ini adalah ukuran MCB, jenis RCD/RCBO, ukuran penghantar, kemampuan panel, nilai tahanan pembumian, koordinasi proteksi, penempatan stopkontak, dan ketahanan terhadap petir atau surja. Semua itu bergantung pada instalasi nyata, lingkungan, aturan yang berlaku, serta rancangan tenaga listrik. Undang-Undang Keselamatan Kerja menempatkan keselamatan sebagai kewajiban yang penerapannya mengikuti tempat kerja dan kegiatannya; artikel ini tidak dapat menetapkan kepatuhan untuk lokasi tertentu ([UU No. 1 Tahun 1970](https://peraturan.bpk.go.id/Details/47614/uu-no-1-tahun-1970)).

Untuk proyek nyata, tandai dulu **[NEEDS SITE SURVEY AND ELECTRICAL DESIGN REVIEW: kondisi sumber, jalur, proteksi, pembumian, lingkungan, dan pihak berwenang belum tersedia]**. Tanpa data itu, angka total hanya estimasi awal.

## Cara kerjanya

Mulailah dari daftar beban, bukan dari kapasitas UPS yang kebetulan tersedia. Minta lembar data atau foto label untuk setiap perangkat. Catat tegangan masukan, daya atau arus nominal, apakah angka itu per unit atau per port, serta kondisi maksimum yang dinyatakan pembuat. Untuk perangkat DC, gunakan watt yang sudah tercantum atau kalikan volt dan ampere pada keluaran DC. Untuk adaptor AC, jangan menjumlahkan angka keluaran DC lalu menganggapnya sama persis dengan konsumsi dari jaringan; rugi konversi dan mode siaga perlu dikonfirmasi.

Buat tabel kerja berikut.

| Kelompok | Data yang dicatat | Pertanyaan verifikasi |
| --- | --- | --- |
| Kamera | jumlah, daya siang dan malam, tegangan | Apakah iluminator atau pemanas menaikkan beban? |
| Perekam dan disk | daya NVR/DVR dan konfigurasi disk | Apakah semua disk aktif bersamaan? |
| PoE/jaringan | kapasitas port dan konsumsi switch | Apakah anggaran PoE mencakup kondisi puncak? |
| Tampilan dan aksesori | monitor, modem, kipas, lampu bantu | Mana yang wajib hidup saat listrik padam? |
| Cadangan | target waktu dan beban prioritas | Apakah runtime dihitung dari beban terukur dan kondisi baterai? |

Jumlahkan kolom daya untuk kondisi normal dan kondisi puncak. Jika beberapa perangkat memakai adaptor terpisah, kelompokkan berdasarkan sirkuit dan tegangan, bukan hanya berdasarkan fungsi CCTV. Untuk sisi AC satu fasa, arus perkiraan diperoleh dari watt dibagi volt; faktor daya, efisiensi, dan arus awal dapat membuat arus aktual berbeda. Jangan memakai hasil bagi itu untuk menetapkan rating proteksi tanpa perhitungan tenaga listrik lengkap.

Untuk cadangan, tentukan dahulu beban prioritas: biasanya kamera, perekam, dan jaringan; monitor mungkin tidak perlu terus menyala. Kalikan beban prioritas dengan durasi target untuk memperoleh Wh teoritis. Kapasitas UPS yang tertulis tidak otomatis menjadi durasi pakai karena dipengaruhi efisiensi, batas pengosongan, umur baterai, suhu, dan pola beban. Durasi harus dikonfirmasi dari dokumentasi model dan uji yang disetujui, bukan dari label semata.

Pendekatan bertahap ini sejalan dengan prinsip pengendalian risiko: kenali bahaya, nilai kondisi, pilih pengendalian, lalu tinjau kembali setelah ada perubahan ([ILO, controlling risks](https://www.ilo.org/topics-and-sectors/occupational-safety-and-health-guide-labour-inspectors-and-other/how-can-occupational-safety-and-health-be-managed/controlling-risks); [ILO, panduan lima langkah penilaian risiko](https://www.ilo.org/publications/5-step-guide-employers-workers-and-their-representatives-conducting)).

## Faktor yang mengubah hasil

Pertama, bedakan angka label dari beban terukur. Kamera malam, pemanas, IR, motor pan-tilt-zoom, atau analitik lokal dapat meningkatkan konsumsi. NVR dengan lebih banyak disk dan proses tampilan juga berbeda dari unit kosong. Perubahan firmware atau konfigurasi bisa mengubah pola beban, jadi simpan versi konfigurasi bersama tabel.

Kedua, perhatikan jalur dan lingkungan. Kabel panjang menambah rugi tegangan; bundel rapat, ruang panas, area lembap, dan jalur bersama kabel tenaga lain memerlukan tinjauan tersendiri. PoE membantu distribusi daya, tetapi anggaran PoE, batas panjang, pemisahan jalur, dan perlindungan tetap harus dibuktikan untuk konfigurasi aktual. IEC 60364-1 menempatkan perlindungan, pembumian, verifikasi, dan perubahan instalasi dalam rancangan kelistrikan; catatan ini tidak menggantikan edisi standar dan desain kompeten ([IEC 60364-1](https://webstore.iec.ch/en/publication/63699)).

Ketiga, pisahkan listrik dari keamanan gambar. Daya yang cukup tidak membuktikan cakupan, identifikasi, rekaman, atau alarm yang berguna. Tujuan adegan, pemilihan, penempatan, commissioning, pemeliharaan, dan evaluasi objektif perlu ditetapkan untuk sistem CCTV ([IEC 62676-4](https://webstore.iec.ch/en/publication/7353)).

Keempat, petir dan surja bukan sekadar tambahan watt. Perlu ditinjau jalur masuk, bonding, pembumian, perangkat proteksi, serta koordinasinya dengan bangunan dan jaringan. Jangan menghubungkan penghantar pembumian atau memasang pelindung surja berdasarkan diagram umum tanpa pemeriksaan tenaga listrik di lokasi. Permenaker tentang keselamatan dan kesehatan kerja listrik juga menuntut perhatian pada identifikasi sumber, isolasi, verifikasi tidak bertegangan, kondisi lingkungan, dan kompetensi; pekerjaan tersebut harus ditangani personel berwenang ([Permenaker No. 12 Tahun 2015](https://peraturan.bpk.go.id/Details/145984/permenaker-no-12-tahun-2015)).

## Contoh keputusan praktis

Bayangkan Anda memiliki daftar kamera dengan dua angka daya: operasi biasa dan operasi malam. Jangan memilih angka biasa hanya karena siang hari lebih lama. Hitung dua skenario: semua perangkat normal, lalu kamera malam aktif bersama perekam, switch PoE, dan jaringan. Skenario kedua menjadi dasar pemeriksaan kapasitas dan cadangan. Jika sebagian kamera hanya menyala pada jadwal tertentu, tuliskan jadwal itu sebagai asumsi yang dapat berubah, bukan sebagai fakta permanen.

Gunakan keputusan berikut setelah tabel terisi:

| Hasil pemeriksaan | Keputusan perencanaan |
| --- | --- |
| Data label lengkap, sirkuit dan jalur belum diverifikasi | Hentikan pada estimasi; minta survei dan desain listrik. |
| Total watt berubah besar antara siang dan malam | Gunakan skenario puncak untuk kapasitas; minta konfirmasi inrush dan PoE. |
| Beban prioritas dan target durasi sudah jelas, tetapi baterai/model belum | Hitung Wh teoritis saja; minta data runtime model dan uji penerimaan. |
| Ada gejala panas, trip, koneksi longgar, air, atau surja | Jangan menambah beban; isolasi area sesuai prosedur dan panggil personel berwenang. |

Kawan Tukang.co.id, minta setiap asumsi diberi pemilik dan tanggal: siapa yang mengonfirmasi jumlah kamera, mode malam, durasi cadangan, dan sirkuit yang dipakai. Jika pekerjaan berlangsung di lokasi aktif atau melibatkan kontraktor lain, koordinasikan perubahan dan serah-terima secara tertulis.

## Kesalahan umum dan cara memeriksanya

Kesalahan pertama adalah mengalikan jumlah kamera dengan satu angka iklan. Periksa apakah angka tersebut termasuk iluminator, pemanas, audio, atau hanya konsumsi tipikal. Kesalahan kedua adalah menjumlahkan watt DC untuk menentukan kebutuhan stopkontak AC tanpa memperhitungkan adaptor. Minta data masukan AC atau ukur dengan alat yang sesuai dan personel kompeten.

Kesalahan ketiga adalah memilih UPS dari VA terbesar yang tersedia. VA, watt, runtime, bentuk gelombang, kompatibilitas, dan kondisi baterai adalah pertanyaan berbeda. Minta lembar data model, beban prioritas, metode uji, serta batas penggantian baterai. Kesalahan keempat adalah menganggap kontinuitas gambar berarti instalasi aman. Catat hasil verifikasi proteksi, pembumian, jalur kabel, dan perubahan konfigurasi sebagai dokumen terpisah.

Kesalahan kelima adalah bekerja pada panel atau konduktor hidup demi “sekadar mengecek”. Jangan melakukan pekerjaan live, switching, pengujian, atau perubahan grounding dari panduan ini. Identifikasi sumber, isolasi, verifikasi tidak bertegangan, dan izin kerja memerlukan metode lokasi, alat, serta otorisasi yang dapat diaudit. **[NEEDS COMPETENT PERSON REVIEW: metode kerja, isolasi, proteksi, pembumian, dan pengujian aktual]**

## Jalan pintas yang berisiko

Shortcut yang sering dipilih adalah memasang UPS lebih besar agar semua ketidakpastian dianggap selesai. Itu bisa gagal bila beban puncak belum dihitung, jalur listrik tidak sesuai, baterai tidak kompatibel, atau sistem tetap kehilangan rekaman karena jaringan dan perekam tidak berada pada beban prioritas. Alternatif yang lebih dapat dipertanggungjawabkan adalah menetapkan beban prioritas, menghitung skenario normal dan puncak, memeriksa sumber serta proteksi, lalu menguji runtime dan failover dengan rencana yang disetujui.

## Kesimpulan

Jadi, cara menghitung beban listrik sistem CCTV adalah menjumlahkan daya semua perangkat pada skenario operasi yang relevan, mengubahnya menjadi arus pada tegangan yang dipakai, lalu menghitung energi cadangan untuk beban prioritas. Hasil itu hanya dasar perencanaan. Sobat Tukang.co.id, siapkan daftar model, label daya, mode operasi, rute kabel, target durasi, dan asumsi lingkungan untuk ditinjau teknisi listrik yang berwenang.

Minta dokumen desain satu garis, pemeriksaan proteksi dan pembumian, verifikasi jalur/PoE, serta uji penerimaan yang sesuai lokasi. Untuk mencari tindak lanjut pemasangan di wilayah yang tercantum, Anda dapat melihat [layanan pasang CCTV di Yosowilangun](/kota/jual-pasang-cctv-yosowilangun/) atau [layanan pasang CCTV di Wungu](/kota/jual-pasang-cctv-wungu/). Jika data aktual, aturan yang berlaku, atau kompetensi pelaksana belum jelas, pertahankan status **[NEEDS TECHNICAL REVIEW BEFORE INSTALLATION]**. Aturan operasinya: jangan menambah beban atau mengubah instalasi berdasarkan hitungan watt saja.
