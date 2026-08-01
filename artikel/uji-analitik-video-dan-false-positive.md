---
article_id: CCT-13-03
title: "Menguji analitik video dan false positive CCTV"
slug: "uji-analitik-video-dan-false-positive"
description: "Design usable monitoring, alert-response, display, analytics, and integration workflows."
status: draft
writing_contract_version: "native-id-v2"
publication_date: "2026-03-13"
publication_date_basis: editorial_backfill
date_modified: null
parent_topic: CCT-13
primary_intent: "Run a representative trial and record misses and false positives."
reader_community: "Tukang.co.id"
reader_address: "Teman Tukang.co.id"
final_route: "/artikel/uji-analitik-video-dan-false-positive.html"
technical_review: required
sources:
  - "https://webstore.iec.ch/en/publication/7353"
  - "https://webstore.iec.ch/en/publication/59704"
  - "https://www.ilo.org/topics-and-sectors/occupational-safety-and-health-guide-labour-inspectors-and-other/how-can-occupational-safety-and-health-be-managed/controlling-risks"
  - "https://csrc.nist.gov/pubs/ir/8259/r1/final"
  - "https://pages.nist.gov/IoT-Device-Cybersecurity-Requirement-Catalogs/technical/"
  - "https://peraturan.bpk.go.id/Details/229798/uu-no-27-tahun-2022"
  - "https://www.onvif.org/profiles/profile-t/"
  - "https://www.onvif.org/"
---

# Menguji analitik video dan false positive CCTV

Halo, Teman Tukang.co.id! Analitik video CCTV baru layak dipakai untuk keputusan operasional setelah diuji pada adegan, pencahayaan, cuaca, dan alur respons yang benar-benar akan dihadapi. Demo vendor atau satu klip yang terlihat bagus belum menjawab dua pertanyaan penting: apakah kejadian yang dicari terdeteksi, dan apakah alarm yang muncul cukup jarang sehingga operator masih mau menindaklanjutinya?

Uji yang berguna membandingkan kejadian yang sengaja dibuat secara aman dengan kejadian yang memang terjadi, lalu mencatat deteksi benar, kejadian terlewat (*false negative*), alarm keliru (*false positive*), waktu tinjau, dan tindakan operator. Kesimpulan hanya berlaku untuk kondisi uji yang terdokumentasi. Jika kamera, sudut, aturan analitik, firmware, atau pola aktivitas berubah, hasilnya harus diuji ulang. [NEEDS representative test conditions and privacy authorization before any field trial]

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

*Ilustrasi umum dari aset lokal cctv.tukang.co.id; bukan dokumentasi proyek tertentu.*

## Definisi dan batas objek

Dalam artikel ini, analitik video berarti aturan perangkat lunak yang menilai aliran gambar untuk tugas tertentu—misalnya mendeteksi orang melewati garis, berada di zona, atau memasuki area pada jam tertentu. *False positive* adalah alarm yang memenuhi aturan mesin tetapi tidak memenuhi kejadian yang dimaksud pengguna. Kebalikannya, *false negative*, adalah kejadian yang seharusnya terdeteksi tetapi luput.

Jangan mencampur tiga lapisan penilaian. Pertama, kemampuan kamera atau server menghasilkan metadata. Kedua, kemampuan perekam dan klien menerima event serta menampilkannya. Ketiga, kemampuan organisasi memeriksa alarm dan melakukan tindakan. IEC 62676-4 menekankan bahwa resolusi, jumlah megapiksel, atau jumlah kamera saja tidak membuktikan kegunaan sistem; kebutuhan adegan, pemasangan, pengujian penerimaan, dan pemeliharaan tetap harus dinilai ([IEC 62676-4](https://webstore.iec.ch/en/publication/7353)).

Batasnya juga penting: pengujian ini bukan audit kepatuhan, bukan pembuktian bahwa produk tertentu selalu akurat, dan bukan izin merekam orang. Untuk penggunaan yang memproses data pribadi, tujuan, cakupan, akses, penyimpanan, pengungkapan, dan penghapusan perlu ditetapkan oleh pengendali/penanggung jawab yang berwenang sesuai konteks aktual ([UU No. 27 Tahun 2022](https://peraturan.bpk.go.id/Details/229798/uu-no-27-tahun-2022)).

## Cara kerjanya

Mulai dari keputusan yang ingin dibuat, bukan dari nama fitur. Tulis satu kalimat seperti: “Alarm ini memicu pemeriksaan operator ketika seseorang masuk zona terbatas pada rentang waktu tertentu.” Kalimat tersebut menetapkan objek, zona, waktu, dan tindakan; tanpa itu, angka akurasi tidak punya arti.

Susun uji dalam urutan berikut.

1. **Tetapkan skenario dan kriteria.** Tentukan adegan yang termasuk kejadian, adegan yang mirip tetapi bukan kejadian, serta kapan alarm harus diabaikan. Definisikan metrik sejak awal: jumlah kejadian benar, luput, alarm keliru, durasi tinjau, dan tindakan yang diambil. IEC 62676-6 mengingatkan bahwa klasifikasi objek/aktivitas harus dikaitkan dengan skenario, lingkungan, tujuan waktu nyata atau forensik, serta metode penerimaan ([IEC 62676-6](https://webstore.iec.ch/en/publication/59704)).
2. **Bekukan konfigurasi.** Catat model, firmware, lensa, posisi, sudut, resolusi, zona, garis, jadwal, sensitivitas, *debounce* atau penundaan, server analitik, perekam, dan versi aplikasi. Jika event diteruskan lewat perangkat berbeda, catat format dan perannya. Logo atau kotak centang ONVIF tidak menjamin semua fitur opsional, kompatibilitas klien, atau dukungan sepanjang siklus hidup; verifikasi produk dan alur yang benar-benar diuji ([ONVIF Profile T](https://www.onvif.org/profiles/profile-t/), [panduan produk conformant ONVIF](https://www.onvif.org/)).
3. **Siapkan korpus uji.** Ambil rentang kondisi yang mewakili operasi: siang/malam, perubahan cahaya, hujan atau kabut bila relevan, objek diam/bergerak, jumlah orang berbeda, dan latar yang mudah memicu alarm. Tandai waktu referensi dan kejadian sebenarnya oleh pengamat yang berwenang. Jangan menggunakan wajah atau area yang tidak perlu; persetujuan dan pembatasan akses harus selesai sebelum perekaman.
4. **Jalankan uji terkontrol.** Untuk setiap skenario, jalankan beberapa pengulangan dengan prosedur sama. Jangan mengubah aturan di tengah satu set lalu menyebut hasilnya sebanding. Simpan klip sumber, event, konfigurasi, dan catatan pengamat dengan identitas versi. Siklus risiko yang ringkas—identifikasi, kendalikan, periksa, lalu perbaiki—lebih berguna daripada menumpuk formulir ([ILO, controlling risks](https://www.ilo.org/topics-and-sectors/occupational-safety-and-health-guide-labour-inspectors-and-other/how-can-occupational-safety-and-health-be-managed/controlling-risks)).
5. **Uji respons manusia.** Berikan alarm kepada operator melalui tampilan dan kanal yang akan dipakai. Catat apakah operator melihat kamera yang tepat, memahami alasan alarm, menandai hasil, dan melakukan eskalasi sesuai prosedur. Alarm yang benar tetapi tidak ditindaklanjuti belum menjadi kontrol yang efektif.
6. **Bekukan hasil dan keputusan.** Setelah satu set selesai, hitung hasil berdasarkan definisi awal. Pisahkan temuan perangkat, jaringan, antarmuka, dan prosedur. Putuskan: diterima untuk tujuan terbatas, perlu penyetelan dan uji ulang, atau tidak cocok untuk skenario tersebut.

## Faktor yang mengubah hasil

Kondisi gambar sering mengubah ambang keputusan. Cahaya dari belakang, pantulan, bayangan bergerak, lensa kotor, hujan, dan perubahan posisi kamera dapat membuat objek terlihat berbeda dari korpus uji. Kepadatan orang, pakaian yang mirip latar, kendaraan, atau hewan juga dapat menambah alarm keliru. Karena itu, tulis kondisi setiap pengulangan; jangan menyatukan “siang cerah” dengan “malam berpenerangan sebagian” menjadi satu angka.

Aturan analitik dan tujuan juga berpengaruh. Aturan untuk investigasi setelah kejadian boleh menoleransi peninjauan manual lebih lama daripada alarm yang harus segera memanggil petugas. Ambang yang terlalu rendah biasanya menaikkan alarm keliru; ambang terlalu tinggi dapat menambah kejadian terlewat. Tidak ada angka ambang universal yang dapat dipindahkan dari satu lokasi ke lokasi lain tanpa uji.

Rantai integrasi merupakan sumber kegagalan tersendiri. Kamera dapat membuat event, tetapi perekam mungkin tidak menyimpan metadata, aplikasi mungkin tidak menampilkan alasan alarm, atau jaringan dapat memutus klip. Profil dan peran perangkat yang sesuai perlu diperiksa pada firmware yang dipakai, termasuk kredensial, enkripsi, pembaruan, log, dan proses pemulihan. NIST menempatkan identitas perangkat, konfigurasi aman, perlindungan data, kontrol akses, pembaruan, dan pembuangan sebagai kemampuan yang perlu direncanakan—bukan sekadar mengganti kata sandi bawaan ([NISTIR 8259 Rev. 1](https://csrc.nist.gov/pubs/ir/8259/r1/final), [katalog kemampuan teknis NIST](https://pages.nist.gov/IoT-Device-Cybersecurity-Requirement-Catalogs/technical/)).

Terakhir, manusia dan tata kelola menentukan makna hasil. Operator yang lelah, definisi “kejadian benar” yang berubah, atau akses rekaman yang terlalu luas dapat merusak uji. Tetapkan pemilik data, siapa yang boleh meninjau, berapa lama bukti disimpan, serta bagaimana salinan dan penghapusan ditangani. Hal ini perlu disesuaikan dengan penilaian hukum dan privasi setempat, bukan disimpulkan dari artikel ini.

## Contoh keputusan praktis

Bayangkan aturan “orang memasuki zona pintu belakang setelah jam tertentu”. Ini bukan hasil proyek, melainkan contoh cara mencatat keputusan. Gunakan tabel seperti berikut untuk setiap set uji.

| Temuan | Pertanyaan verifikasi | Keputusan bersyarat |
|---|---|---|
| Alarm benar dan operator melihat klip | Apakah waktu, kamera, dan alasan event jelas? | Lanjutkan hanya untuk tujuan dan kondisi yang diuji. |
| Alarm keliru berulang saat bayangan bergerak | Apakah perubahan cahaya termasuk korpus uji? | Ubah zona/jadwal atau nyatakan kondisi sebagai pengecualian, lalu uji ulang. |
| Orang masuk tetapi tidak ada event | Apakah objek tertutup, keluar bingkai, atau jaringan putus? | Hentikan klaim cakupan; perbaiki penyebab dan ulangi skenario. |
| Event ada, tetapi klip/metadata tidak sampai ke operator | Apakah perekam, jaringan, dan aplikasi menyimpan jejak yang sama? | Perlakukan sebagai kegagalan alur, bukan sekadar masalah akurasi analitik. |

Teman Tukang.co.id, perhatikan bahwa keputusan “diterima” selalu memiliki ekor kalimat: diterima **untuk adegan apa, kondisi apa, dan tindakan siapa**. Catat batas itu di lembar penerimaan agar tidak berubah menjadi klaim umum tentang sistem.

## Kesalahan umum dan cara memeriksanya

Kesalahan pertama adalah menguji satu klip promosi lalu menganggapnya mewakili lokasi. Periksa sumber klip, kondisi cahaya, sudut, dan apakah kejadian luput juga dicari. Kesalahan kedua adalah menghitung persentase tanpa denominator. Tulis jumlah kejadian yang benar-benar terjadi, jumlah yang terdeteksi, dan jumlah kesempatan alarm keliru; jika pengamat tidak dapat menentukan acuan, tandai datanya tidak cukup.

Kesalahan ketiga adalah menyetel sensitivitas sampai grafik tampak bagus tanpa menguji respons operator. Tanyakan berapa alarm yang dapat ditinjau per giliran, apakah alasan alarm terlihat, dan apa prosedur ketika bukti tidak lengkap. Kesalahan keempat adalah menyamakan kompatibilitas protokol dengan keamanan. Periksa akun dan peran, paparan jaringan, pembaruan firmware, log, pencadangan, serta rencana menonaktifkan perangkat saat pensiun.

Kesalahan kelima adalah menyimpan rekaman uji tanpa batas atau membagikannya melalui kanal pribadi. Batasi bidang pandang dan data, tetapkan otorisasi, masa simpan, ekspor, dan penghapusan sebelum uji. Jika kebutuhan berubah, lakukan peninjauan ulang; jangan memperluas tujuan secara diam-diam.

## Jalan pintas yang perlu dihindari

Shortcut yang sering terdengar adalah, “Aktifkan deteksi manusia dengan ambang default; kalau terlalu banyak alarm, operator tinggal mengabaikannya.” Ini gagal karena mengubah beban ketidakakuratan menjadi beban manusia. Alarm keliru yang berulang dapat menurunkan perhatian, sementara kejadian terlewat tetap tidak terlihat. Alternatif yang lebih dapat dipertanggungjawabkan adalah menetapkan skenario, menguji kondisi pemicu dan nonpemicu, mengukur respons, lalu menyetel aturan secara terdokumentasi dan mengulang set uji yang sama.

## Kesimpulan

Menguji analitik video dan *false positive* CCTV berarti membuktikan alur lengkap—adegan, aturan, event, rekaman, tampilan, dan tindakan operator—pada kondisi yang dinyatakan, bukan mengejar satu angka demo. Sobat Tukang.co.id, buat lembar uji berisi konfigurasi versi, korpus skenario, definisi kejadian, hasil benar/luput/keliru, waktu respons, dan batas penggunaan.

Sebelum dipakai operasional, minta penanggung jawab teknis dan privasi meninjau otorisasi perekaman, akses, retensi, keamanan integrasi, serta bukti penerimaan. Untuk langkah lapangan, Anda dapat mulai dari [halaman utama Tukang.co.id](/) dan, bila lokasinya sesuai, [informasi jual-pasang CCTV di Dau](/kota/jual-pasang-cctv-dau/) sebagai konteks peninjauan pemasangan—bukan sebagai bukti hasil uji artikel ini. Jika kondisi lapangan atau tujuan berubah, kembali ke skenario dan uji ulang. Aturan akhirnya sederhana: jangan menyebut analitik “andal” di luar kondisi yang benar-benar diuji dan dapat ditelusuri.
