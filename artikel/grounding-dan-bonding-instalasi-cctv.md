---
article_id: CCT-07-05
title: "Grounding dan bonding pada instalasi CCTV"
slug: "grounding-dan-bonding-instalasi-cctv"
description: "Panduan memeriksa beban, cadangan daya, tegangan, surja, grounding, bonding, dan keselamatan listrik CCTV sebelum pekerjaan disetujui."
status: draft
writing_contract_version: "native-id-v2"
publication_date: "2025-10-24"
publication_date_basis: editorial_backfill
date_modified: null
parent_topic: CCT-07
primary_intent: "Understand interfaces that require code-compliant grounding review."
reader_community: "Tukang.co.id"
reader_address: "Teman Tukang.co.id"
final_route: "/artikel/grounding-dan-bonding-instalasi-cctv.html"
technical_review: required
sources:
  - "https://www.ilo.org/topics-and-sectors/occupational-safety-and-health-guide-labour-inspectors-and-other/how-can-occupational-safety-and-health-be-managed/controlling-risks"
  - "https://www.ilo.org/publications/5-step-guide-employers-workers-and-their-representatives-conducting"
  - "https://peraturan.bpk.go.id/Details/47614/uu-no-1-tahun-1970"
  - "https://peraturan.bpk.go.id/Details/145984/permenaker-no-12-tahun-2015"
  - "https://peraturan.bpk.go.id/Details/351282/permenaker-no-11-tahun-2026"
  - "https://webstore.iec.ch/en/publication/63699"
  - "https://webstore.iec.ch/en/publication/7353"
  - "https://bnsp.go.id/"
  - "https://www.iso.org/files/live/sites/isoorg/files/archive/pdf/en/iso_45001_-briefing_note.pdf"
---

# Grounding dan bonding pada instalasi CCTV

Halo, Teman Tukang.co.id! Grounding dan bonding pada instalasi CCTV bukan sekadar menancapkan kabel ke batang tanah. Keduanya perlu ditinjau bersama sumber listrik, beban, perangkat pelindung, jalur kabel, kondisi lingkungan, dan orang yang berwenang mengerjakannya. Grounding menyediakan jalur pelepasan gangguan ke bumi sesuai rancangan; bonding menyamakan potensial bagian logam yang dapat tersentuh. Salah sambung dapat membuat kamera tetap menyala tetapi casing, kabel, atau perangkat lain berbahaya saat terjadi gangguan.

Jawaban singkatnya: jangan menyetujui pemasangan hanya karena ada label “sudah di-grounding” atau hasil continuity test. Minta identitas sumber, diagram satu garis, data beban dan cadangan, metode proteksi surja, titik bonding, hasil verifikasi yang relevan, serta persetujuan tenaga listrik kompeten. Persyaratan akhirnya berubah menurut bangunan, sistem distribusi, jenis kamera (termasuk PoE), jalur luar ruang, dan aturan yang berlaku. **[NEEDS SITE-SPECIFIC ELECTRICAL REVIEW: EG-01, EG-02, EG-03, EG-05, EG-09, EG-10]**

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

Grounding (pembumian) menghubungkan bagian tertentu dari sistem ke bumi melalui rancangan proteksi. Bonding (penyamaan potensial) menghubungkan bagian logam yang semestinya berada pada potensial serupa, misalnya enclosure, rak, tray, atau pipa logam. Tujuannya mengurangi beda tegangan sentuh ketika terjadi arus gangguan. Koneksi data, shield kabel, dan konduktor pelindung tidak otomatis boleh diperlakukan sama; fungsi dan titik terminasi harus ditetapkan dalam desain.

Artikel ini adalah checklist pendidikan, bukan instruksi mengukur tahanan, memilih ukuran konduktor, menyetel proteksi, atau melakukan pekerjaan bertegangan. Undang-Undang Keselamatan Kerja menjadi landasan umum, tetapi penerapannya bergantung pada tempat kerja, peralatan, aktivitas, dan aturan pelaksana yang berlaku ([UU No. 1 Tahun 1970](https://peraturan.bpk.go.id/Details/47614/uu-no-1-tahun-1970)). Karena itu, angka tahanan, rating pemutus, ukuran kabel, atau jarak elektroda tidak boleh ditebak dari artikel umum.

## Cara kerjanya

Mulailah dari sumber. Identifikasi panel atau adaptor yang memasok kamera, switch PoE, NVR, monitor, dan UPS; catat tegangan nominal, jenis sistem (AC, DC, atau PoE), beban normal, arus awal, dan beban cadangan. Label UPS hanya menyatakan klaim pabrikan, bukan durasi nyata pada instalasi Anda. Data aktual harus diperiksa terhadap rancangan dan kondisi baterai.

Selanjutnya petakan antarmuka logam dan jalur kabel. Tentukan bagian yang harus dibonding, jalur konduktor pelindung, titik masuk dari area luar, serta pemisahan dari kabel daya atau sumber gangguan. Pada kamera PoE, daya dan data berjalan pada kabel jaringan; keberadaan PoE tidak menggantikan evaluasi pembumian, isolasi, perlindungan surja, dan kompatibilitas perangkat. Seri IEC 60364 mencakup prinsip instalasi listrik, termasuk perlindungan dan verifikasi, tetapi penerapan detail memerlukan desain dan edisi yang tepat ([IEC 60364-1:2025](https://webstore.iec.ch/en/publication/63699)).

Urutan kerjanya harus dapat ditelusuri: survei kondisi, desain, persetujuan, pengisolasian sumber oleh personel berwenang, pemasangan, pemeriksaan, pengujian, pelabelan, lalu serah terima. Panduan ILO menganjurkan identifikasi bahaya, penilaian risiko, penentuan pengendalian, pelaksanaan, dan peninjauan ulang; matriks generik tidak dapat menetapkan risiko sirkuit di lokasi tertentu ([ILO controlling risks](https://www.ilo.org/topics-and-sectors/occupational-safety-and-health-guide-labour-inspectors-and-other/how-can-occupational-safety-and-health-be-managed/controlling-risks), [ILO five-step guide](https://www.ilo.org/publications/5-step-guide-employers-workers-and-their-representatives-conducting)).

## Faktor yang mengubah hasil

Beberapa pertanyaan berikut mengubah keputusan grounding dan bonding:

- **Beban dan backup:** Berapa perangkat yang aktif bersamaan? Apakah switch PoE, NVR, dan UPS berada pada sirkuit yang sama? Apa yang terjadi saat satu sumber gagal?
- **Tegangan dan proteksi:** Apakah adaptor, PoE injector, UPS, pemutus, dan perangkat pelindung surja memiliki identitas model serta rating yang cocok? Bukti produk harus cocok dengan barang yang benar-benar dipasang; logo atau foto sertifikat saja tidak cukup.
- **Lingkungan:** Apakah kamera berada di luar, area lembap, dekat struktur logam, atau jalur yang berdekatan dengan instalasi petir dan kabel daya? Kondisi tersebut memengaruhi rute, enclosure, pemisahan, dan kebutuhan pemeriksaan.
- **Perubahan pekerjaan:** Apakah ada renovasi, genset, panel baru, atau kontraktor lain yang mengubah jalur dan sumber? Bonding yang benar pada satu fase dapat menjadi tidak memadai setelah perubahan.
- **Kompetensi dan izin:** Siapa yang merancang, mengisolasi, menguji, dan menyetujui pengembalian energi? Verifikasi kompetensi harus melihat lingkup, identitas, masa berlaku, konteks praktik, dan supervisi; situs BNSP hanya titik awal pemeriksaan, bukan pengesahan otomatis untuk pekerjaan tertentu ([BNSP](https://bnsp.go.id/)).

Sobat Tukang.co.id, minta dokumen yang menghubungkan setiap jawaban dengan bukti: gambar satu garis, daftar beban, lembar data perangkat, foto label setelah terpasang, catatan isolasi, hasil pemeriksaan, dan daftar perubahan. ISO 45001 menekankan peran, kompetensi, kendali operasional, serta evaluasi; dokumen tersebut membantu melihat siapa yang bertanggung jawab, bukan sekadar menambah kertas ([ISO 45001 briefing note](https://www.iso.org/files/live/sites/isoorg/files/archive/pdf/en/iso_45001_-briefing_note.pdf)).

## Contoh keputusan praktis

Gunakan tabel ini untuk memutuskan tindakan berikutnya, bukan untuk memberi persetujuan akhir.

| Temuan awal | Pertanyaan verifikasi | Keputusan sementara |
| --- | --- | --- |
| Kamera indoor, satu adaptor, jalur pendek | Apakah sumber, polaritas, proteksi, dan enclosure teridentifikasi? | Lanjutkan pemeriksaan desain; jangan menambah kabel bumi secara acak. |
| Kamera PoE melewati area luar | Apakah jalur masuk, shield, surja, dan bonding struktur sudah dirancang? | Tahan pemasangan sampai desain dan rute ditinjau tenaga kompeten. |
| NVR dan switch memakai UPS | Berapa beban terukur, mode bypass, dan skenario gagal sumber? | Minta perhitungan kapasitas serta uji failover yang terdokumentasi. |
| Tidak ada diagram atau label sirkuit | Dari panel mana energi berasal dan bagaimana isolasinya? | Hentikan pekerjaan listrik; lakukan identifikasi dan pengesahan terlebih dahulu. |

Contoh tersebut sengaja tidak menyebut ukuran kabel atau durasi UPS karena nilai itu bergantung pada data proyek. Untuk kebutuhan keamanan visual, IEC 62676-4 juga mengingatkan bahwa jumlah kamera atau demo produk tidak membuktikan cakupan, identifikasi, atau hasil operasional; kebutuhan adegan, pemasangan, commissioning, dan evaluasi objektif tetap harus ditetapkan ([IEC 62676-4](https://webstore.iec.ch/en/publication/7353)).

## Kesalahan umum dan cara memeriksanya

Kesalahan pertama adalah mengikat semua kabel ke benda logam terdekat. Tanyakan fungsi benda itu, kontinuitas jalurnya, dan apakah desain memang menetapkannya sebagai bagian bonding. Kesalahan kedua adalah menganggap continuity test membuktikan perlindungan lengkap. Tes tersebut tidak dengan sendirinya membuktikan kapasitas gangguan, koordinasi proteksi, ketahanan surja, atau keselamatan saat kondisi berubah.

Kesalahan ketiga adalah memakai adaptor atau UPS dengan spesifikasi yang “mirip”. Cocokkan model, tegangan, arus, polaritas, konektor, lingkungan, dan instruksi pabrikan dengan daftar material yang disetujui. Kesalahan keempat adalah melewati isolasi karena kamera bertegangan rendah. Sumber primer, kapasitor, dan jalur gabungan tetap perlu diidentifikasi dan diamankan; Permenaker terkait keselamatan listrik menempatkan identifikasi sumber, isolasi, verifikasi tidak bertegangan, perlindungan, kondisi lingkungan, dan otorisasi sebagai bukti yang berbeda ([Permenaker No. 12 Tahun 2015](https://peraturan.bpk.go.id/Details/145984/permenaker-no-12-tahun-2015), [Permenaker No. 11 Tahun 2026](https://peraturan.bpk.go.id/Details/351282/permenaker-no-11-tahun-2026)).

Kawan Tukang.co.id, periksa juga serah terima: label panel, as-built, daftar perangkat, hasil inspeksi, tanggal, pelaksana, dan batasan pengujian. Jika pekerjaan berada di Yosowilangun, Anda dapat menyiapkan pertanyaan teknis yang sama saat menghubungi layanan [jual dan pasang CCTV di Yosowilangun](/kota/jual-pasang-cctv-yosowilangun/). Jika ada temuan, tetapkan pemilik tindakan dan tanggal tinjau ulang. Jangan menutup temuan hanya karena kamera menampilkan gambar.

## Jalan pintas yang perlu dihindari

Shortcut yang sering dipilih adalah “tambahkan satu batang grounding lalu selesai”. Cara ini bisa gagal karena tidak menjawab sumber gangguan, bonding antarbagian logam, pemisahan jalur, perlindungan surja, atau koordinasi dengan sistem bangunan. Penambahan elektroda tanpa desain juga dapat menciptakan jalur arus yang tidak diinginkan.

Alternatif yang lebih aman adalah meminta paket verifikasi: survei kondisi, diagram satu garis, daftar beban dan sumber cadangan, rancangan grounding-bonding, identitas perangkat, metode isolasi, hasil pemeriksaan kompeten, dan persetujuan pengoperasian. Untuk proyek di Wungu, daftar ini juga membantu saat berdiskusi dengan penyedia [jual dan pasang CCTV di Wungu](/kota/jual-pasang-cctv-wungu/). Untuk risiko tinggi atau perubahan besar, libatkan ahli listrik dan penanggung jawab K3; artikel ini tidak dapat menggantikan keputusan mereka.

## Kesimpulan

Grounding dan bonding CCTV harus diputuskan sebagai bagian dari sistem listrik dan kondisi bangunan, bukan sebagai aksesori kamera. Sebelum pekerjaan diteruskan, kumpulkan diagram, data beban, jalur kabel, identitas proteksi, bukti kompetensi, serta hasil verifikasi yang relevan. Tandai bagian yang belum memiliki bukti dan minta tinjauan teknis untuk EG-01, EG-02, EG-03, EG-05, EG-09, dan EG-10. Aturan operasionalnya sederhana: bila sumber, jalur, proteksi, atau kewenangan tidak jelas, hentikan pekerjaan listrik dan minta penilaian profesional sebelum energi dinyalakan kembali.
