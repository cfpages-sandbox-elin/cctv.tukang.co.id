---
article_id: CCT-07-03
writing_contract_version: "native-id-v2"
title: "Menghitung durasi UPS untuk CCTV"
slug: "durasi-ups-untuk-cctv"
description: "Panduan memperkirakan waktu cadangan UPS untuk CCTV dengan memeriksa beban, baterai, tegangan, proteksi, dan uji lapangan."
status: draft
publication_date: "2025-10-16"
publication_date_basis: editorial_backfill
date_modified: null
parent_topic: CCT-07
primary_intent: "Estimate backup runtime with load, efficiency, battery, and aging assumptions."
reader_community: "Tukang.co.id"
reader_address: "Kawan Tukang.co.id"
final_route: "/artikel/durasi-ups-untuk-cctv.html"
technical_review: required
sources:
  - "https://www.ilo.org/topics-and-sectors/occupational-safety-and-health-guide-labour-inspectors-and-other/how-can-occupational-safety-and-health-be-managed/controlling-risks"
  - "https://webstore.iec.ch/en/publication/7353"
  - "https://peraturan.bpk.go.id/Details/145984/permenaker-no-12-tahun-2015"
  - "https://peraturan.bpk.go.id/Details/351282/permenaker-no-11-tahun-2026"
  - "https://webstore.iec.ch/en/publication/63699"
---

# Menghitung durasi UPS untuk CCTV

Halo, Kawan Tukang.co.id! Durasi UPS untuk CCTV tidak bisa ditentukan hanya dari angka VA pada kardus UPS atau jumlah kamera. Perkiraan yang masuk akal dimulai dari beban nyata yang tetap menyala, energi baterai yang tersedia, efisiensi konversi, dan kondisi baterai. Hasil akhirnya masih perlu dicocokkan dengan tabel runtime dari produsen dan diuji pada konfigurasi yang akan dipakai.

Secara konsep, hitung energi baterai yang dapat dipakai, lalu bagi dengan daya beban. Bentuk sederhananya adalah: **runtime perkiraan = energi baterai nominal × faktor pemakaian × efisiensi ÷ daya beban**. “Faktor pemakaian” mencakup batas pelepasan baterai dan pengaruh usia; nilainya harus berasal dari data pabrikan atau hasil uji, bukan tebakan. Jika beban, tegangan, kabel, ventilasi, atau mode UPS berubah, runtime ikut berubah. Karena itu artikel ini memberi cara menyiapkan perhitungan dan pertanyaan verifikasi, bukan janji berapa jam UPS akan bertahan.

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

Ilustrasi umum dari aset lokal Tukang.co.id; bukan dokumentasi proyek tertentu.

## Definisi dan batas objek

Yang dihitung adalah waktu sejak sumber listrik padam sampai UPS mencapai batas operasi yang ditetapkan, sementara kamera, perekam, jaringan, dan aksesori yang dipilih tetap berfungsi sesuai kebutuhan. Tentukan lebih dahulu apa yang harus bertahan: hanya kamera, atau juga NVR/DVR, switch PoE, modem, monitor, pemanas kamera, dan perangkat penyimpanan. Perangkat yang tidak masuk daftar beban tidak boleh diam-diam dianggap gratis.

Perhitungan ini berbeda dari penentuan kualitas gambar atau cakupan adegan. IEC 62676-4 menempatkan tujuan adegan, pemilihan, pemasangan, commissioning, pemeliharaan, pengujian, dan evaluasi objektif sebagai hal yang perlu dibuktikan terpisah. [Baca panduan aplikasi sistem CCTV menurut IEC 62676-4](https://webstore.iec.ch/en/publication/7353) untuk memahami mengapa runtime saja tidak membuktikan rekaman berguna.

Batas keselamatannya juga tegas. Artikel ini tidak menetapkan ukuran kabel, setelan proteksi, metode kerja bertegangan, desain grounding, atau persetujuan instalasi. Penerapan kewajiban K3 bergantung pada tempat kerja, aktivitas, orang, peralatan, dan aturan yang berlaku; kepastian untuk proyek tertentu memerlukan telaah kompeten dan sumber hukum terkini. [NEEDS TECHNICAL REVIEW: identitas sistem, desain kelistrikan, dan kewajiban lokasi belum tersedia]

## Cara kerjanya

Mulai dengan lembar beban. Catat identitas model, tegangan masukan/keluaran, arus atau daya terukur, mode operasi, serta perangkat yang benar-benar terhubung. Pisahkan beban kontinu dari beban yang hanya sesekali aktif. Untuk PoE, minta data konsumsi kamera beserta margin yang diizinkan switch; jangan mengganti data itu dengan jumlah port.

Berikutnya, ambil data baterai dari label dan manual: tegangan rangkaian, kapasitas, konfigurasi, batas pelepasan, kurva runtime, serta kondisi pengujian. Kapasitas nominal tidak sama dengan energi yang dapat dipakai pada setiap beban. UPS online, line-interactive, dan jenis lain juga dapat memiliki efisiensi serta perilaku perpindahan yang berbeda. Gunakan nilai efisiensi dan runtime pada dokumen model yang sama.

Masukkan faktor koreksi yang dapat dibuktikan: temperatur, usia baterai, pengisian, resistansi kabel, dan perubahan beban. Bila produsen hanya menyediakan tabel runtime, gunakan titik beban yang paling mendekati konfigurasi aktual dan nyatakan bahwa hasil tersebut adalah estimasi. Jangan mengekstrapolasi melampaui rentang tabel tanpa persetujuan teknis.

Uji berurutan setelah desain diperiksa: rekam kondisi awal, ukur beban, simulasikan padam sesuai prosedur yang disetujui, catat tegangan dan alarm, lalu kembalikan sistem dengan aman. Sumber identifikasi, isolasi, verifikasi tidak bertegangan, grounding/proteksi, kondisi lingkungan, dan otorisasi adalah bukti yang berbeda; semuanya tidak dapat digantikan oleh label “UPS terpasang”. Prinsip pengendalian risiko ILO menekankan pengenalan bahaya, penilaian, pengendalian, dan peninjauan ulang yang mengikuti kondisi nyata ([ILO—controlling risks](https://www.ilo.org/topics-and-sectors/occupational-safety-and-health-guide-labour-inspectors-and-other/how-can-occupational-safety-and-health-be-managed/controlling-risks)).

## Faktor yang mengubah hasil

**Beban dan mode kerja.** IR illuminator, pemanas, kipas, disk yang aktif menulis, dan komunikasi jaringan dapat mengubah konsumsi. Periksa beban puncak serta arus masuk, bukan hanya angka rata-rata. Jika sebagian kamera memakai suplai lokal dan sebagian melalui PoE, petakan keduanya agar tidak dihitung dua kali atau terlewat.

**Tegangan dan kompatibilitas.** Cocokkan tegangan keluaran UPS dengan catu kamera, NVR/DVR, dan switch. Rentang tegangan yang salah dapat membuat perangkat restart meskipun baterai masih menyimpan energi. IEC 60364-1 mengingatkan bahwa batas mains, SELV, PoE, proteksi, pembumian, jalur kabel, UPS, dan verifikasi merupakan bagian yang saling terkait, bukan satu angka runtime ([IEC 60364-1](https://webstore.iec.ch/en/publication/63699)).

**Surge, petir, dan grounding.** Proteksi lonjakan dan pembumian memengaruhi keselamatan serta keandalan, tetapi tidak boleh diasumsikan dari keberadaan UPS. Minta diagram satu garis, identitas perangkat proteksi, hasil verifikasi, dan penjelasan antarmuka. Jangan melakukan pekerjaan bertegangan atau mengubah proteksi tanpa orang berwenang dan metode yang disetujui; rujuk persyaratan kompetensi dan pengendalian energi pada aturan ketenagakerjaan yang berlaku ([Permenaker No. 12 Tahun 2015](https://peraturan.bpk.go.id/Details/145984/permenaker-no-12-tahun-2015) dan [Permenaker No. 11 Tahun 2026](https://peraturan.bpk.go.id/Details/351282/permenaker-no-11-tahun-2026)).

**Baterai dan lingkungan.** Temperatur, ventilasi, umur, siklus, terminal, dan jadwal penggantian memengaruhi kemampuan aktual. Simpan tanggal pemasangan, hasil inspeksi, alarm, dan penggantian. Catatan ini adalah rekaman kondisi, bukan bukti bahwa runtime tertentu selalu tercapai.

## Contoh keputusan praktis

Bayangkan daftar beban sudah berisi kamera, perekam, switch PoE, dan jaringan. Jangan langsung memilih UPS dari total VA yang tertulis di brosur. Buat tiga skenario: beban kontinu normal, beban saat inframerah atau aksesori aktif, dan beban setelah baterai menua sesuai batas yang disarankan produsen. Untuk tiap skenario, tulis daya terukur, titik runtime pada tabel pabrikan, alarm yang diharapkan, dan beban mana yang boleh dimatikan.

Jika kebutuhan hanya menjaga perekaman sampai generator atau teknisi mengambil alih, keputusan dapat berupa UPS dengan runtime tabel yang memenuhi jendela tersebut, lalu diverifikasi melalui uji. Jika tidak ada sumber pengganti dan sistem harus terus merekam, kebutuhan itu menjadi persoalan desain daya dan kontinuitas yang lebih luas; jangan menyimpulkan cukup hanya karena hasil rumus tampak panjang. Kawan Tukang.co.id, minta pemilik sistem menyetujui prioritas: kamera mana yang wajib hidup, berapa lama toleransi kehilangan rekaman, dan siapa yang mengambil tindakan saat alarm baterai muncul.

## Kesalahan umum dan cara memeriksanya

- Mengalikan voltase dan ampere-jam lalu menganggap seluruh energi tersedia. Periksa batas pelepasan, efisiensi, dan kurva runtime model yang sama.
- Menggunakan konsumsi kamera saja. Cocokkan daftar aktual dengan NVR/DVR, switch PoE, jaringan, penyimpanan, dan aksesori.
- Mengandalkan angka “hingga” pada kemasan. Minta kondisi uji, beban, baterai, dan edisi manual; klaim pemasaran tidak membuktikan sistem terpasang.
- Mengabaikan penuaan dan temperatur. Tetapkan pemantauan, inspeksi, serta kriteria penggantian berbasis catatan.
- Menguji dengan mencabut kabel sembarangan. Susun metode, otorisasi, titik isolasi, komunikasi, dan pemulihan; pekerjaan kelistrikan memerlukan kompetensi dan pengawasan yang sesuai.
- Menganggap grounding atau surge protector otomatis memperpanjang runtime. Keduanya adalah bagian proteksi yang perlu desain dan verifikasi tersendiri.

Gunakan checklist ringkas: identitas model dan firmware; diagram beban; daya kontinu dan puncak; data baterai dan tanggalnya; tabel runtime; tegangan serta kompatibilitas; proteksi dan grounding; kondisi ruang; prosedur uji; hasil uji; alarm; pemilik tindakan korektif. Siklus penilaian risiko sebaiknya ditinjau ulang saat beban, perangkat, lokasi, atau metode berubah, bukan hanya saat jadwal administrasi tiba.

## Jalan pintas yang tampak menarik

Jalan pintas yang sering dipilih adalah membeli UPS dengan kapasitas VA terbesar yang terjangkau, lalu menganggap durasi otomatis aman. Cara ini dapat gagal karena VA bukan energi baterai yang dapat digunakan, beban nyata bisa berubah, dan konfigurasi keluaran mungkin tidak cocok. Alternatif yang lebih dapat dipertanggungjawabkan adalah mengunci identitas beban, meminta data pabrikan, menghitung dengan asumsi yang ditulis, lalu melakukan uji terkontrol. Sobat Tukang.co.id, bila salah satu data penting tidak tersedia, tandai kekosongan itu dan minta review teknis—jangan mengisinya dengan angka perkiraan.

## Kesimpulan

Durasi UPS untuk CCTV diperkirakan dari beban aktual, energi baterai yang dapat dipakai, efisiensi, faktor usia/lingkungan, dan data runtime produsen; rumus hanya titik awal. Kumpulkan diagram beban, manual, kondisi baterai, persyaratan tegangan, proteksi, grounding, dan catatan uji sebelum menetapkan keputusan. Minta orang berkompeten memeriksa desain serta metode pengujian, terutama ketika melibatkan sumber listrik, pekerjaan bertegangan, atau perubahan proteksi.

Teman Tukang.co.id, aturan operasinya sederhana: **tanpa identitas sistem, asumsi tertulis, dan hasil uji yang sesuai, jangan menjanjikan runtime**. [NEEDS TECHNICAL REVIEW: persetujuan desain dan penerimaan proyek tetap diperlukan sebelum dipakai sebagai dasar operasi.]

Untuk menyiapkan pertanyaan dan peninjauan lanjutan, mulai dari [halaman utama Tukang.co.id](/) dan, bila lokasi Anda sesuai, lihat [layanan jual-pasang CCTV di Dau](/kota/jual-pasang-cctv-dau/) sebagai jalur kontak proyek. Ketersediaan tenaga, ruang lingkup, dan persetujuan tetap harus dikonfirmasi langsung.
