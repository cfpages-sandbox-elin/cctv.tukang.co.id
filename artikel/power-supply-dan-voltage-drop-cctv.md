---
article_id: CCT-07-02
title: "Power supply dan voltage drop pada kamera CCTV"
slug: "power-supply-dan-voltage-drop-cctv"
description: "Panduan memeriksa beban, cadangan daya, tegangan, surge, grounding, dan keselamatan listrik CCTV."
status: draft
writing_contract_version: "native-id-v2"
publication_date: "2025-10-13"
publication_date_basis: editorial_backfill
date_modified: null
parent_topic: CCT-07
primary_intent: "Check voltage, current, distance, conductor, and connector assumptions."
reader_community: "Tukang.co.id"
reader_address: "Teman Tukang.co.id"
final_route: "/artikel/power-supply-dan-voltage-drop-cctv.html"
technical_review: required
sources:
  - "https://www.ilo.org/topics-and-sectors/occupational-safety-and-health-guide-labour-inspectors-and-other/how-can-occupational-safety-and-health-be-managed/controlling-risks"
  - "https://www.ilo.org/publications/5-step-guide-employers-workers-and-their-representatives-conducting"
  - "https://peraturan.bpk.go.id/Details/145984/permenaker-no-12-tahun-2015"
  - "https://webstore.iec.ch/en/publication/63699"
  - "https://webstore.iec.ch/en/publication/7353"
---

# Power supply dan voltage drop pada kamera CCTV

Halo, Teman Tukang.co.id! Power supply CCTV tidak cukup dipilih dari tulisan “12 V” pada kamera. Anda perlu mencocokkan tegangan keluaran, arus total, jarak kabel, penampang dan material konduktor, konektor, kondisi lingkungan, serta perlindungan sisi sumber. **Voltage drop** adalah turunnya tegangan sepanjang penghantar saat arus mengalir; jika tegangan di ujung kamera terlalu rendah atau berfluktuasi, kamera dapat restart, infrared tidak stabil, atau berhenti bekerja. Nilai pastinya tidak boleh ditebak dari jarak saja.

Jawaban praktisnya: catat beban aktual tiap kamera dan aksesori, hitung atau verifikasi penurunan tegangan pada rute yang benar, ukur tegangan di sumber dan di ujung beban pada kondisi kerja, lalu cocokkan hasilnya dengan instruksi produk. Pemilihan adaptor, UPS, grounding, surge protection, dan perubahan jalur listrik tetap memerlukan desain serta pemeriksaan personel kompeten. [IEC 60364-1](https://webstore.iec.ch/en/publication/63699) menempatkan perlindungan, pembumian, verifikasi, dan perubahan instalasi sebagai hal yang harus dipertimbangkan bersama; halaman ini bukan persetujuan untuk bekerja pada bagian bertegangan.

![Ilustrasi CCTV Merk ZKTECO](/wp-content/uploads/2023/08/CCTV-Merk-ZKTECO.jpg)


*Aset lokal situs; gambar ini bukan dokumentasi proyek tertentu.*

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

Di sini “power supply” berarti rantai penyaluran daya tegangan rendah dari sumber, pengaman, kabel, sambungan, hingga terminal kamera. “Voltage drop” bukan spesifikasi kamera dan bukan pengganti pengukuran. Arus yang lebih besar, kabel yang lebih panjang atau lebih kecil, sambungan yang resistansinya meningkat, dan suhu atau kelembapan tertentu dapat memperbesar penurunan tegangan. Rute pergi-pulang harus dihitung sesuai topologi yang benar, bukan hanya panjang yang terlihat di denah.

Fokus artikel ini adalah kamera dengan catu daya rendah dan ketahanan pasokan: beban, cadangan, tegangan, surge (lonjakan sesaat), pembumian, dan pemeriksaan keselamatan. Perencanaan anggaran PoE berada pada pembahasan jaringan tersendiri, sehingga jangan mencampur angka PoE dengan keluaran adaptor DC biasa. Artikel ini juga tidak menentukan ukuran kabel, rating pengaman, kapasitas UPS, atau pengaturan proteksi untuk proyek tertentu. Semua itu masuk gate desain dan bukti lapangan.

## Cara kerjanya

Mulailah dari daftar beban. Untuk setiap kamera, tulis tegangan nominal, arus atau daya pada kondisi siang, malam, pemanas, iluminator, dan aksesori yang benar-benar terpasang. Bedakan beban normal, beban awal, dan beban terburuk yang diizinkan oleh lembar data. Jumlahkan beban pada satu sumber hanya setelah polaritas dan pembagian sirkuitnya jelas. Label adaptor atau klaim penjual tidak membuktikan bahwa model yang dikirim dan dipasang sama; verifikasi identitas serta kompatibilitas produk tetap diperlukan.

Secara konsep, penurunan tegangan mengikuti arus dan resistansi total penghantar: semakin besar arus atau resistansi, semakin besar drop. Resistansi dipengaruhi panjang rangkaian pergi-pulang, material, luas penampang, temperatur, dan kualitas sambungan. Karena itu, pemeriksaan yang berguna mencatat tegangan di terminal sumber dan terminal kamera ketika kamera sedang bekerja pada kondisi yang relevan. Pengukuran tanpa beban dapat menyembunyikan masalah yang baru muncul saat lampu inframerah atau aksesori aktif.

Urutan keputusan yang aman adalah: bekukan diagram satu garis dan rute; identifikasi sumber serta titik isolasi; verifikasi kondisi fisik dan sambungan; lakukan pengukuran oleh personel berwenang dengan alat yang sesuai; bandingkan hasil dengan instruksi pabrikan dan basis desain; dokumentasikan perubahan sebelum sistem dikembalikan. Identifikasi sumber, isolasi, verifikasi tidak adanya tegangan, pembumian/proteksi, dan otorisasi merupakan bukti yang berbeda. Jangan menganggap satu foto panel atau hasil continuity test sudah membuktikan semuanya. [Permenaker No. 12 Tahun 2015](https://peraturan.bpk.go.id/Details/145984/permenaker-no-12-tahun-2015) dapat menjadi rujukan awal untuk batas kompetensi dan pengendalian pekerjaan listrik; penerapan pada lokasi nyata harus ditinjau sesuai kondisi dan aturan terkini.

## Faktor yang mengubah hasil

Beberapa pertanyaan perlu dijawab sebelum menyimpulkan “adaptor cukup”.

- **Beban dan siklus operasi:** Berapa kamera, aksesori, dan beban awal yang berbagi sumber? Apakah mode malam mengubah arus? Apakah ada beban yang baru tersambung saat sistem sudah berjalan?
- **Jalur dan konduktor:** Berapa panjang pergi-pulang yang sebenarnya, bagaimana penampang dan material kabel, serta apakah ada terminal, coupler, atau sambungan tersembunyi? Rute baru atau sambungan tambahan mengubah perhitungan.
- **Sumber dan cadangan:** Apakah sumber memiliki keluaran dan proteksi yang sesuai dengan beban? Jika memakai UPS, berapa beban yang benar-benar dicadangkan, bagaimana perpindahan sumbernya, dan bukti uji apa yang tersedia? Label durasi UPS saja tidak membuktikan runtime pada sistem ini.
- **Lingkungan:** Apakah jalur berada di area basah, panas, berdebu, mudah terkena petir, atau berbagi jalur dengan rangkaian lain? Pemisahan, enclosure, dan perlindungan surge perlu dinilai dalam desain kelistrikan, bukan ditambahkan secara acak.
- **Bukti dan perubahan:** Apakah ada lembar data model yang terpasang, diagram satu garis, catatan pengukuran berbeban, foto sambungan, hasil inspeksi, dan catatan perubahan? [IEC 62676-4](https://webstore.iec.ch/en/publication/7353) menekankan bahwa pemilihan dan pemasangan CCTV perlu dihubungkan dengan tujuan, commissioning, pemeliharaan, pengujian, dan evaluasi objektif; angka resolusi atau demo produk saja tidak membuktikan hasil lapangan.

Kawan Tukang.co.id, perlakukan gejala “kamera kadang mati” sebagai sinyal untuk mengumpulkan bukti, bukan alasan langsung menaikkan tegangan. Menaikkan setelan sumber tanpa memastikan rating kamera, polaritas, isolasi, dan batas komponen dapat menambah risiko kerusakan.

## Contoh keputusan praktis

Gunakan tabel berikut sebagai penyaring awal, bukan pengganti desain.

| Temuan | Keputusan sementara | Bukti lanjutan |
| --- | --- | --- |
| Tegangan sumber sesuai label, tetapi ujung kamera turun saat beban malam aktif | Hentikan asumsi “adaptor rusak”; telusuri drop pada rute, sambungan, dan pembagian beban | Pengukuran berbeban di kedua ujung, identitas kabel, diagram rute |
| Tegangan ujung tampak baik tanpa beban, kamera restart ketika aksesori aktif | Anggap kondisi uji belum mewakili operasi | Catat arus/tegangan pada mode operasi yang memicu gejala dan cocokkan dengan datasheet |
| Banyak kamera berbagi satu sumber tanpa daftar beban | Jangan menambah kamera atau mengubah sekring berdasarkan perkiraan | Daftar beban, basis desain, rating sumber/pengaman, persetujuan kompeten |
| Ada bekas panas, korosi, isolasi rusak, atau sambungan longgar | Isolasi area sesuai prosedur dan serahkan pemeriksaan kepada personel berwenang | Catatan inspeksi, rencana perbaikan, verifikasi sebelum energisasi ulang |
| Sistem berada di area rawan petir atau sumber sering terganggu | Evaluasi koordinasi proteksi, pembumian, dan cadangan sebagai satu sistem | Desain kelistrikan aktual, kondisi tanah/instalasi, uji dan rekaman yang relevan |

Jika salah satu data kunci belum tersedia, tulis “[NEEDS SITE/DESIGN VERIFICATION]” pada lembar serah-terima internal dan jangan menyatakan kapasitas atau keandalan sudah terbukti. Untuk pekerjaan di lokasi berpenghuni atau dengan beberapa kontraktor, koordinasikan pemilik sumber, pelaksana, pengawas, dan pihak yang akan menerima sistem sebelum pengujian.

## Kesalahan umum dan cara memeriksanya

Kesalahan pertama adalah memilih adaptor berdasarkan voltase nominal saja. Periksa juga arus, mode beban, polaritas, konektor, ventilasi, dan bukti identitas model. Kedua, mengukur di panel lalu menyimpulkan kamera menerima nilai yang sama. Ukur titik yang relevan pada kondisi kerja, dengan metode dan alat yang disetujui.

Ketiga, mengabaikan jalur pergi-pulang atau menganggap kabel “tebal” tanpa identitas. Minta spesifikasi konduktor, panjang aktual, dan daftar sambungan. Keempat, menambah kapasitas sumber tanpa menilai pengaman, pembumian, enclosure, dan koordinasi dengan sistem lain. Kelima, menjadikan grounding sebagai obat untuk semua gejala. Pembumian adalah bagian dari skema perlindungan; ia tidak memperbaiki sambungan DC yang resistansinya tinggi atau desain sumber yang tidak cocok.

Sebelum serah-terima, minta paket bukti minimum: diagram satu garis bertanggal, daftar model dan beban, rute kabel, catatan tegangan sumber serta ujung beban pada kondisi uji, hasil inspeksi sambungan, pengaturan cadangan, catatan perubahan, dan nama kompetensi/otorisasi pemeriksa. Siklus risiko sebaiknya dimulai dari identifikasi bahaya, pengendalian pada sumber, verifikasi, lalu peninjauan ulang ketika kondisi berubah, sejalan dengan pendekatan [ILO tentang pengendalian risiko](https://www.ilo.org/topics-and-sectors/occupational-safety-and-health-guide-labour-inspectors-and-other/how-can-occupational-safety-and-health-be-managed/controlling-risks) dan [panduan lima langkah penilaian risiko](https://www.ilo.org/publications/5-step-guide-employers-workers-and-their-representatives-conducting).

## Jangan memilih adaptor hanya dari angka arus

“Kalau kamera 12 V, pasang adaptor 12 V berarus paling besar saja.” Shortcut ini gagal karena arus besar yang tersedia tidak menghapus drop pada kabel dan sambungan, tidak membuktikan kualitas proteksi, serta tidak memastikan setiap kamera menerima tegangan yang sesuai pada saat beban berubah. Alternatif yang lebih dapat dipertanggungjawabkan adalah mengunci daftar beban dan rute, memeriksa basis desain serta instruksi produk, mengukur pada titik sumber dan beban ketika beroperasi, lalu meminta review kelistrikan jika ada energi mains, area basah, surge, atau perubahan proteksi.

## Kesimpulan dan langkah berikutnya

Power supply dan voltage drop pada CCTV harus diputuskan dari beban, tegangan di ujung kamera saat bekerja, resistansi rute dan sambungan, serta bukti perlindungan dan cadangan—bukan dari label adaptor atau jarak perkiraan. Teman Tukang.co.id, langkah berikutnya adalah membuat lembar verifikasi per kamera dan meminta pemeriksaan personel kompeten untuk data yang belum terukur, terutama sumber, grounding, surge, dan isolasi. Jika Anda perlu mengatur survei lapangan, gunakan halaman [pemasangan CCTV di Dau](/kota/jual-pasang-cctv-dau/) atau [pemasangan CCTV di Bae](/kota/jual-pasang-cctv-bae/) sebagai titik kontak sesuai wilayah.

Aturan operasinya sederhana: bila identitas beban, rute, hasil pengukuran berbeban, atau otorisasi pekerjaan belum jelas, jangan menaikkan tegangan, mem-bypass pengaman, atau menganggap sistem siap. [NEEDS TECHNICAL REVIEW: site-specific electrical design, protection, grounding, surge, backup, and acceptance evidence]
