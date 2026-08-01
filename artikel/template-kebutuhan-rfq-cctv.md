---
article_id: CCT-16-01
title: "Template kebutuhan untuk RFQ CCTV yang bisa dibandingkan"
slug: "template-kebutuhan-rfq-cctv"
description: "Susun permintaan penawaran CCTV yang setara, periksa bukti, pahami pemicu biaya, dan kendalikan perubahan lingkup."
status: draft
writing_contract_version: "native-id-v2"
publication_date: "2026-05-13"
publication_date_basis: editorial_backfill
date_modified: null
parent_topic: CCT-16
primary_intent: "Request comparable scope, evidence, tests, documentation, and options from vendors."
reader_community: "Tukang.co.id"
reader_address: "Teman Tukang.co.id"
final_route: "/artikel/template-kebutuhan-rfq-cctv.html"
technical_review: required
sources:
  - "https://webstore.iec.ch/en/publication/7353"
  - "https://www.onvif.org/profiles/profile-t/"
  - "https://www.onvif.org/"
  - "https://csrc.nist.gov/pubs/ir/8259/r1/final"
  - "https://pages.nist.gov/IoT-Device-Cybersecurity-Requirement-Catalogs/technical/"
  - "https://peraturan.bpk.go.id/Details/45288/uu-no-8-tahun-1999"
  - "https://peraturan.bpk.go.id/Details/229798/uu-no-27-tahun-2022"
  - "https://www.iso.org/standard/62542.html"
  - "https://www.ilo.org/topics-and-sectors/occupational-safety-and-health-guide-labour-inspectors-and-other/how-can-occupational-safety-and-health-be-managed/controlling-risks"
---

# Template kebutuhan untuk RFQ CCTV yang bisa dibandingkan

Halo, Teman Tukang.co.id! Penawaran CCTV sering tampak mudah dibandingkan karena semua vendor menulis jumlah kamera dan harga total. Masalahnya, angka itu bisa mewakili cakupan, kondisi lokasi, pengujian, dan dokumen yang berbeda. Template RFQ (request for quotation, yaitu permintaan penawaran) yang baik memaksa setiap penyedia menjawab pertanyaan yang sama.

Jawaban singkatnya: kirim satu lembar kebutuhan yang menetapkan tujuan tiap area, batas pekerjaan, asumsi akses dan jaringan, bukti produk, pengujian penerimaan, serta format perubahan. Minta harga dipisahkan per komponen dan tandai pilihan wajib, opsional, dan yang belum diketahui. Harga terendah baru bermakna setelah baris-baris itu sebanding. Kriteria teknis tetap harus disesuaikan dengan lokasi dan ditinjau pihak yang kompeten; artikel ini adalah input pengadaan, bukan security brief atau persetujuan proyek.

![Ilustrasi CCTV Merk ZKTECO](/wp-content/uploads/2023/08/CCTV-Merk-ZKTECO.jpg)

*Ilustrasi umum dari aset lokal Tukang.co.id; bukan dokumentasi proyek tertentu.*

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

## Definisikan kebutuhan sebelum meminta harga

Mulailah dengan fungsi, bukan merek. Untuk setiap area, tulis kejadian yang perlu ditinjau, siapa yang melihat rekaman, dan berapa lama bukti perlu tersedia. Bedakan kebutuhan melihat situasi umum dari kebutuhan mengenali wajah, membaca plat nomor, atau mengikuti pergerakan. Panduan aplikasi IEC 62676-4 menempatkan tujuan adegan, pemilihan, penempatan, commissioning, pemeliharaan, dan pengujian sebagai bagian dari evaluasi; jumlah megapiksel saja tidak membuktikan hasil yang berguna ([IEC 62676-4](https://webstore.iec.ch/en/publication/7353)).

Gunakan tabel kebutuhan berikut sebagai lampiran RFQ:

| Kolom | Isi yang harus ditulis |
|---|---|
| Area dan tujuan | Lokasi, kejadian yang dicari, tingkat detail yang dibutuhkan |
| Kondisi | Pencahayaan, cuaca, jam operasi, akses, dan gangguan yang sudah diketahui |
| Perangkat | Kamera, lensa, dudukan, recorder, penyimpanan, lisensi, dan akses klien |
| Antarmuka | Jaringan, daya, integrasi, akun, dan pihak pemilik sistem |
| Batas kerja | Jalur kabel, pekerjaan sipil, konfigurasi, pelatihan, dokumentasi, dan pembersihan |
| Penerimaan | Adegan yang diuji, bukti hasil, format berita acara, dan penanggung jawab |

Nyatakan kuantitas hanya jika dasar pengukurannya jelas. Jika survei belum dilakukan, minta vendor menuliskan asumsi dan opsi survei terpisah—jangan menyamarkan ketidakpastian sebagai jumlah final. Sobat Tukang.co.id, lampirkan denah atau foto yang memang boleh dibagikan, tetapi minta penyedia mengonfirmasi apa yang belum dapat disimpulkan dari lampiran itu.

Untuk area dengan orang yang dapat diidentifikasi, tambahkan tujuan penggunaan, pihak yang mendapat akses, dan perkiraan masa simpan. UU Pelindungan Data Pribadi mengharuskan kebutuhan dan pengelolaan aktual ditinjau sesuai peran pengendali/prosesor dan konteksnya; tanda peringatan atau kontrak cloud saja tidak membuktikan seluruh pengendalian telah terpenuhi ([UU PDP](https://peraturan.bpk.go.id/Details/229798/uu-no-27-tahun-2022)).

## Buat penawaran benar-benar sebanding

Kirim format harga yang sama kepada semua penyedia. Pisahkan setidaknya: perangkat, lisensi, material pemasangan, tenaga kerja, konfigurasi, pekerjaan jaringan atau daya, survei, pengujian, pelatihan, dokumentasi, pajak, transportasi, dan pekerjaan yang dikecualikan. Minta subtotal per area dan total, bukan hanya satu angka paket.

Tetapkan tiga label pada setiap baris: **wajib**, **opsional**, atau **menunggu verifikasi**. Untuk baris menunggu verifikasi, minta harga satuan atau rumus penyesuaian dan batas persetujuannya. Tulis juga keadaan sementara: pekerjaan malam, akses bertahap, area tetap berpenghuni, atau menunggu listrik dan jaringan. Dengan begitu biaya tunggu, mobilisasi ulang, dan perlindungan area tidak muncul sebagai kejutan.

Lampirkan template jawaban: model dan firmware, jumlah unit, satuan harga, waktu pengadaan yang harus dikonfirmasi, masa dukungan, garansi yang benar-benar ditawarkan, asumsi, eksklusi, serta risiko yang vendor lihat. Jangan mengisi ketersediaan, harga, atau masa dukungan dari brosur lama. Jika sebuah fitur bergantung pada recorder atau klien tertentu, minta skenario dan batas kompatibilitasnya.

Kesetaraan juga berarti pengujian yang sama. Tetapkan adegan uji, kondisi cahaya yang dicatat, akses live dan playback, ekspor bukti, sinkronisasi waktu, notifikasi, serta bukti serah terima. Profil ONVIF Profile T mencakup kemampuan tertentu untuk streaming, imaging, event, metadata, PTZ, HTTPS, dan audio, tetapi logo atau centang protokol tidak membuktikan semua fitur opsional bekerja pada kombinasi perangkat Anda ([Profile T](https://www.onvif.org/profiles/profile-t/), [panduan produk konforman ONVIF](https://www.onvif.org/)).

## Dokumen yang membuktikan hal berbeda

Buat matriks bukti, bukan folder berisi logo. Lembar data membuktikan spesifikasi yang dinyatakan untuk model tertentu. Daftar produk konforman dan sertifikat harus dicocokkan dengan model, peran, firmware, dan tanggal yang ditawarkan. Laporan uji harus menyebut metode, konfigurasi, kondisi, hasil, dan batasnya. Metode pemasangan menjelaskan cara kerja yang diusulkan; itu bukan bukti pekerjaan telah dilakukan dengan benar.

Pisahkan pula bukti pengalaman, garansi, dan persetujuan. Referensi proyek tidak otomatis membuktikan kesamaan lokasi atau hasil. Gambar sertifikat tidak mengautentikasi pemegangnya; bila kompetensi personel menentukan pekerjaan, minta identitas skema, penerbit, ruang lingkup, masa berlaku, dan cara verifikasi. Bukti harus dapat ditelusuri ke objek yang ditawarkan. Prinsip ini sejalan dengan perlindungan konsumen: klaim penawaran harus dapat dipertanggungjawabkan, bukan sekadar rating atau frasa “sesuai standar” ([UU Perlindungan Konsumen](https://peraturan.bpk.go.id/Details/45288/uu-no-8-tahun-1999)).

Untuk keamanan siber, minta inventaris model, akun dan peran, protokol yang terbuka, konfigurasi awal, mekanisme pembaruan, pencatatan log, pemulihan cadangan, dan rencana penghentian layanan. NIST menempatkan identitas perangkat, konfigurasi aman, perlindungan data, kontrol akses, pembaruan, kesadaran keadaan, dan pengelolaan siklus hidup sebagai kapabilitas yang perlu diprofilkan sesuai penggunaan—mengganti kata sandi bawaan saja tidak cukup ([NISTIR 8259 Rev. 1](https://csrc.nist.gov/pubs/ir/8259/r1/final), [katalog kapabilitas IoT](https://pages.nist.gov/IoT-Device-Cybersecurity-Requirement-Catalogs/technical/)).

## Pertanyaan wajib kepada penyedia

Masukkan pertanyaan ini dan minta jawaban tertulis per nomor:

1. Tujuan adegan apa yang Anda asumsikan untuk tiap kamera, dan informasi apa yang tidak dapat dijamin tanpa survei?
2. Model, lensa, firmware, recorder, lisensi, dan akses klien apa yang termasuk? Apa alternatif setara dan dampaknya?
3. Fitur mana yang wajib, kondisional, atau memerlukan perangkat lunak tambahan? Tunjukkan bukti kompatibilitas pada kombinasi yang ditawarkan.
4. Pekerjaan apa yang termasuk dan dikecualikan—termasuk jalur kabel, jaringan, daya, pekerjaan sipil, akses ketinggian, kerja malam, dan proteksi area berpenghuni?
5. Adegan, kondisi cahaya, playback, ekspor, waktu, notifikasi, dan integrasi apa yang akan diuji? Siapa menyediakan alat dan siapa menandatangani hasil?
6. Dokumen apa yang diserahkan: gambar akhir, daftar aset, konfigurasi, akun, manual, lisensi, log uji, pelatihan, dan prosedur pemulihan?
7. Bagaimana akun awal, pembaruan firmware, kerentanan, backup, akses jarak jauh, dan penghapusan data dikelola selama serta setelah dukungan?
8. Apa asumsi akses, jadwal, izin, keselamatan, dan koordinasi pihak lain? Apa pemicu biaya atau waktu tambahan?
9. Bagaimana perubahan scope diajukan, dihargai, disetujui, dan dicatat sebelum pekerjaan berubah?
10. Siapa kontak teknis dan pengambil keputusan selama penerimaan, dan berapa lama respons yang ditawarkan—jika memang ditawarkan?

Jangan meminta jawaban “ya” saja. Minta kolom bukti, pemilik tindakan, tanggal berlaku, dan batasan. Kawan Tukang.co.id, jawaban yang jujur “belum dapat dipastikan sebelum survei” lebih berguna daripada kepastian tanpa dasar.

## Tanda bahaya dan biaya yang sering tersembunyi

Red flag pertama adalah total paket tanpa kuantitas, satuan, asumsi, atau eksklusi. Red flag berikutnya adalah model tidak lengkap, fitur hanya dibuktikan lewat demo merek yang sama, sertifikat tanpa jalur verifikasi, dan garansi tanpa objek serta proses klaim. Tanda lain: vendor menolak menyebut siapa yang menguji atau menganggap jaringan, daya, akun, dan pembersihan “sudah termasuk” tanpa definisi.

Biaya yang lazim tersembunyi bukan hanya perangkat: survei ulang, akses di luar jam biasa, menunggu area dibuka, mobilisasi kedua, material tambahan, penyesuaian jaringan, lisensi per kanal, penyimpanan dan ekspor, pelatihan, pemindahan akun, serta perbaikan setelah uji gagal. Minta setiap risiko diberi pemilik dan mekanisme persetujuan. Jangan menyetujui pekerjaan tambahan melalui percakapan lisan saja.

Jika perubahan terjadi karena kondisi lapangan, hentikan perbandingan lama: terbitkan revisi yang menandai baris berubah, alasan, dampak harga/waktu, dan bukti yang masih berlaku. Untuk area kerja atau pemasangan yang memiliki risiko keselamatan, pengendalian harus ditentukan dari kondisi aktual dan metode yang kompeten; matriks generik atau PPE-first tidak menggantikan penilaian risiko yang sesuai ([ILO—controlling risks](https://www.ilo.org/topics-and-sectors/occupational-safety-and-health-guide-labour-inspectors-and-other/how-can-occupational-safety-and-health-be-managed/controlling-risks)).

## Penerimaan, serah terima, dan keputusan akhir

Sebelum memilih, tetapkan paket penerimaan satu halaman. Untuk tiap area tulis siapa memeriksa pemasangan fisik, siapa menguji fungsi, siapa memeriksa akses dan data, serta bukti apa yang disimpan. Bukti dapat berupa daftar aset dan firmware, foto titik yang boleh didokumentasikan, hasil playback dan ekspor, catatan sinkronisasi waktu, daftar akun yang diserahkan melalui kanal aman, log isu, dan berita acara dengan status lulus, gagal, atau ditunda.

Penerimaan bukan berarti semua klaim produk terbukti. Ia hanya menyatakan bahwa kriteria yang disepakati telah diuji pada kondisi yang dicatat. Tautkan setiap kegagalan ke tindakan, pemilik, tenggat, dan uji ulang. Simpan versi RFQ, penawaran, klarifikasi, perubahan, hasil uji, dan keputusan agar asal-usul bukti dapat ditelusuri; rekaman memiliki pemilik, akses, masa simpan, dan sensitivitas yang berbeda ([ISO 15489-1](https://www.iso.org/standard/62542.html)).

Shortcut yang sering dipilih adalah menerima penawaran termurah lalu “menyetel detail belakangan”. Itu gagal ketika detail tersebut—jalur kabel, lisensi, integrasi, retensi, atau uji adegan—ternyata mengubah scope dan biaya. Alternatif yang lebih aman adalah meminta dua atau tiga penawaran menjawab template identik, menormalkan asumsi, lalu menyimpan daftar pertanyaan terbuka sebagai syarat keputusan.

## Kesimpulan

Template RFQ CCTV yang dapat dibandingkan berisi tujuan per area, kondisi dan batas scope, format biaya terurai, bukti model dan kompetensi, skenario uji, pengelolaan data serta keamanan, aturan perubahan, dan paket serah terima. Langkah berikutnya: isi tabel kebutuhan, tandai fakta yang belum terverifikasi, kirim ke penyedia dengan format jawaban yang sama, lalu minta peninjauan teknis dan hukum untuk kondisi proyek nyata.

Teman Tukang.co.id, pilih penawaran hanya setelah setiap selisih punya penjelasan dan bukti yang dapat ditelusuri. Untuk langkah layanan berikutnya, Anda dapat mulai dari [beranda Tukang.co.id](/) atau melihat [opsi jual-pasang CCTV di Dau](/kota/jual-pasang-cctv-dau/) setelah scope internal disetujui. Jika tujuan, kondisi, atau kewajiban proyek belum jelas, pertahankan `[NEEDS PROJECT REVIEW]` dan jangan mengubahnya menjadi janji harga, performa, atau kepatuhan.
