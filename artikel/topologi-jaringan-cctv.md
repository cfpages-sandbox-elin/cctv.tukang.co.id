---
article_id: CCT-06-01
writing_contract_version: "native-id-v2"
title: "Membuat topologi jaringan khusus CCTV"
slug: "topologi-jaringan-cctv"
description: "Plan CCTV connectivity, addressing, bandwidth, time, segmentation, and network-delivered power."
status: draft
publication_date: "2025-09-13"
publication_date_basis: editorial_backfill
date_modified: null
parent_topic: CCT-06
primary_intent: "Document devices, links, uplinks, and network dependencies."
reader_community: "Tukang.co.id"
reader_address: "Sobat Tukang.co.id"
final_route: "/artikel/topologi-jaringan-cctv.html"
technical_review: required
sources:
  - "https://www.onvif.org/profiles/profile-t/"
  - "https://www.onvif.org/"
  - "https://csrc.nist.gov/pubs/ir/8259/r1/final"
  - "https://pages.nist.gov/IoT-Device-Cybersecurity-Requirement-Catalogs/technical/"
  - "https://webstore.iec.ch/en/publication/63699"
  - "https://www.ilo.org/topics-and-sectors/occupational-safety-and-health-guide-labour-inspectors-and-other/how-can-occupational-safety-and-health-be-managed/controlling-risks"
---

# Membuat topologi jaringan khusus CCTV

Halo, Sobat Tukang.co.id! Kesalahan paling mahal saat membuat topologi CCTV biasanya bukan salah memilih kamera, melainkan menyambungkan semua perangkat ke jaringan kantor tanpa peta aliran data. Akibatnya, kamera berebut uplink, alamat IP bertabrakan, rekaman terputus ketika satu switch mati, atau daya PoE habis sebelum semua kamera menyala.

Jawaban singkatnya: gambar dulu perangkat dan hubungan logisnya, lalu tetapkan zona jaringan, skema alamat, jalur uplink, kebutuhan bandwidth, sumber waktu, dan anggaran daya. Topologi yang layak bukan sekadar gambar kamera menuju NVR; ia menunjukkan dependensi dari kamera, switch PoE, switch inti, NVR/VMS, penyimpanan, akses operator, serta koneksi waktu dan layanan yang benar-benar diperlukan. Nilai kapasitas, jarak, jumlah kamera, durasi retensi, dan kondisi listrik harus berasal dari survei proyek—bukan asumsi artikel ini. **[NEEDS PROJECT EVIDENCE: inventaris perangkat, beban trafik, kapasitas uplink, dan anggaran PoE belum tersedia.]**

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

## Definisi dan batas objek

Topologi jaringan khusus CCTV adalah rancangan hubungan antarperangkat dan aliran layanan: kamera mengirim stream ke perekam atau VMS (video management system), operator mengakses tampilan, dan perangkat memperoleh alamat serta waktu yang konsisten. “Khusus” tidak selalu berarti jaringan fisik yang sepenuhnya terpisah. Yang penting adalah batas logis dan jalur yang dapat dijelaskan—misalnya VLAN kamera, VLAN manajemen, dan jalur akses operator yang dikendalikan.

Halaman ini membahas arsitektur dan dependensi. Pilihan jenis kabel, jalur fisik, dan detail pathway berada pada lingkup artikel CCT-08. Penguatan keamanan rinci—akun, firewall, pembaruan, dan pemantauan—berada pada CCT-09. Jangan menganggap satu diagram arsitektur sebagai persetujuan desain listrik atau keselamatan kerja; pekerjaan nyata tetap memerlukan survei dan peninjauan kompeten.

## Cara kerjanya

Mulailah dengan daftar fungsi, bukan merek. Catat setiap kamera, switch PoE, switch distribusi/inti, NVR atau server VMS, penyimpanan, workstation, gateway, sumber waktu, dan jalur servis. Untuk tiap perangkat, tulis pemilik, lokasi logis, antarmuka yang dipakai, serta layanan yang harus berbicara dengannya. Diagram kemudian memiliki panah yang bermakna: stream kamera menuju perekam, metadata atau event menuju klien, dan sinkronisasi waktu menuju sumber waktu.

Pisahkan tiga lapisan keputusan berikut.

1. **Akses kamera.** Kamera berada pada segmen yang tidak menjadi tempat laptop umum. Port aksesnya menuju switch PoE yang ditetapkan, bukan ke soket acak pada switch kantor.
2. **Distribusi dan uplink.** Switch akses mengirim trafik ke switch distribusi atau inti melalui uplink yang kapasitasnya dibuktikan dari perhitungan. Bila ada dua jalur, gambar tujuan failover dan perilaku saat satu jalur gagal; jangan menyebutnya redundan tanpa uji.
3. **Layanan dan operator.** NVR/VMS, penyimpanan, konsol operator, DNS atau sumber waktu ditempatkan pada zona yang jelas. Akses pemantauan diberikan melalui jalur yang diperlukan saja.

Untuk interoperabilitas, dokumentasikan peran perangkat dan fitur yang benar-benar diuji. ONVIF Profile T mendeskripsikan kemampuan streaming, imaging, event, metadata, PTZ, HTTPS, dan audio tertentu; logo ONVIF saja tidak membuktikan semua fitur opsional pada kombinasi kamera, firmware, dan klien Anda ([ONVIF Profile T](https://www.onvif.org/profiles/profile-t/), [panduan produk konforman ONVIF](https://www.onvif.org/)). Tuliskan model dan firmware yang akan diuji pada daftar desain, bukan hanya “mendukung ONVIF”.

Sinkronisasi waktu juga bagian dari topologi. Pilih sumber waktu yang dapat dijangkau kamera, NVR/VMS, dan klien; tentukan zona waktu serta siapa yang berwenang mengubahnya. Tanpa waktu konsisten, urutan kejadian antar kamera sulit dibandingkan. Sumber waktu proyek dan jalur keluar jaringan harus ditetapkan secara tertulis.

## Faktor yang mengubah hasil

Jumlah kamera hanyalah salah satu variabel. Resolusi, frame rate, codec, pola gerak, audio, event, dan apakah stream utama serta stream rendah dikirim bersamaan memengaruhi trafik. Hitung beban per kamera dari spesifikasi dan konfigurasi yang benar-benar direncanakan, jumlahkan pada setiap switch, lalu tambahkan ruang untuk overhead dan perubahan yang disetujui. Uplink yang tampak cukup pada kondisi diam belum tentu cukup saat semua kamera mengirim stream utama.

Pisahkan tiga angka yang sering tercampur: kapasitas port, kapasitas uplink, dan kapasitas tulis/baca perekam. Ketiganya harus melewati perhitungan dan pengujian masing-masing. Retensi rekaman juga mengubah kebutuhan penyimpanan, tetapi durasi retensi dan resolusi adalah keputusan pemilik sistem, bukan angka baku dari artikel ini.

PoE adalah dependensi daya sekaligus jaringan. Buat tabel kamera, kebutuhan daya nominal dan maksimum dari lembar data, anggaran port switch, serta cadangan yang disepakati. Periksa perilaku saat kamera inframerah, pemanas, atau aksesori aktif. Label “PoE” tidak membuktikan kompatibilitas atau daya tersedia. Batas mains, SELV, PoE, UPS, pembumian, proteksi, dan verifikasi harus ditangani perancang listrik kompeten dengan kondisi aktual; IEC 60364-1 menempatkan persyaratan instalasi dan verifikasi dalam konteks sistem yang nyata ([IEC 60364-1](https://webstore.iec.ch/en/publication/63699)).

Segmentasi perlu menjawab “siapa boleh berbicara dengan siapa”. Kamera umumnya hanya perlu menuju perekam, layanan waktu, dan layanan manajemen yang disetujui. Akses operator dan pemeliharaan dibuat sebagai jalur terpisah dengan aturan yang dapat ditinjau. NIST menekankan identitas perangkat, konfigurasi aman, perlindungan data, kontrol akses, pembaruan, dan operasi aman sebagai kapabilitas yang perlu ditentukan menurut use case ([NISTIR 8259 Rev. 1](https://csrc.nist.gov/pubs/ir/8259/r1/final), [katalog kapabilitas IoT NIST](https://pages.nist.gov/IoT-Device-Cybersecurity-Requirement-Catalogs/technical/)). Itu menjadi masukan untuk CCT-09, bukan alasan untuk menjejalkan konfigurasi keamanan detail di sini.

Kawan Tukang.co.id, jangan lupa dependensi non-jaringan: ruang rak, akses teknisi, jalur listrik, perubahan pekerjaan lain, dan kondisi lokasi. Siklus pengendalian risiko yang baik dimulai dari kondisi dan bahaya aktual, lalu memilih pengendalian dan meninjau ulang setelah perubahan—bukan mengandalkan matriks generik ([ILO, controlling risks](https://www.ilo.org/topics-and-sectors/occupational-safety-and-health-guide-labour-inspectors-and-other/how-can-occupational-safety-and-health-be-managed/controlling-risks)).

## Contoh keputusan praktis

Gunakan tabel keputusan berikut sebagai kerangka, bukan angka siap pakai.

| Pertanyaan | Jika jawabannya “ya” | Keputusan arsitektur |
| --- | --- | --- |
| Kamera berada di zona atau bangunan berbeda? | Jalur antar-zona memiliki dependensi sendiri. | Gambar switch akses per zona, uplink, titik terminasi, dan dampak putusnya uplink. |
| Trafik gabungan mendekati kapasitas uplink? | Ada risiko antrean dan kehilangan stream. | Naikkan kapasitas setelah perhitungan, kurangi stream yang tidak perlu, atau bagi zona; validasi dengan uji. |
| Semua kamera membutuhkan PoE bersamaan? | Beban daya puncak dapat melampaui anggaran switch. | Cocokkan maksimum per port dan total switch; dokumentasikan cadangan serta sumber listrik. |
| NVR/VMS adalah titik tunggal kegagalan? | Gangguan perekam menghentikan rekaman terpusat. | Catat konsekuensi, kebutuhan pemulihan, dan keputusan pemilik; jangan menyebut failover tanpa desain dan pengujian. |
| Operator perlu akses dari jaringan umum? | Permukaan akses bertambah. | Buat jalur dan aturan akses yang disetujui; detail hardening diteruskan ke CCT-09. |

Contoh alur yang aman untuk dibahas pada rapat desain adalah: setiap zona memiliki switch PoE; uplink menuju distribusi; distribusi menuju NVR/VMS; klien operator berada pada zona manajemen. Jika satu zona membutuhkan dua uplink, catat apakah keduanya aktif, siaga, atau hanya jalur servis. Status itu harus dibuktikan oleh konfigurasi dan uji penerimaan.

## Kesalahan umum dan cara memeriksanya

Kesalahan pertama adalah menggambar garis tanpa arah layanan. Periksa setiap panah: siapa pengirim, siapa penerima, protokol atau fungsi apa yang diperlukan, dan apa yang terjadi ketika jalur itu putus. Kesalahan kedua adalah memakai alamat IP dari kebiasaan lama. Buat rencana subnet, gateway, reservasi atau DHCP yang disetujui, nama perangkat, dan catatan konflik; jangan menyalin alamat produksi ke proyek baru.

Kesalahan ketiga adalah menyamakan angka di brosur dengan performa sistem. Tanda ONVIF, label PoE, kapasitas port, atau demo satu kamera tidak membuktikan kombinasi perangkat, firmware, trafik puncak, dan retensi bekerja. Minta bukti identitas model, versi firmware, konfigurasi, hasil uji stream, dan catatan batasannya.

Kesalahan keempat adalah menaruh semua layanan pada satu segmen “agar mudah”. Mudah saat pemasangan dapat menjadi sulit saat gangguan atau perubahan. Tanyakan siapa pemilik setiap VLAN, siapa yang menyetujui akses, dan bagaimana perubahan dicatat. Teman Tukang.co.id, jika jawaban itu belum ada, arsitektur belum siap diserahkan.

## Jalan pintas yang perlu ditolak

Jalan pintas yang sering dipilih adalah membeli switch PoE dengan jumlah port sama dengan jumlah kamera lalu menganggap masalah selesai. Jumlah port tidak menjawab total daya, uplink, kapasitas perekam, jalur waktu, atau konsekuensi ketika switch mati. Alternatif yang lebih dapat dipertanggungjawabkan adalah membuat lembar beban: daftar perangkat, stream, alamat, port, kebutuhan daya, uplink, layanan, pemilik, dan bukti pengujian. Jika salah satu kolom masih berupa tebakan, tandai dan minta data proyek sebelum memesan.

## Kesimpulan

Membuat topologi jaringan khusus CCTV berarti mendokumentasikan perangkat, hubungan, alamat, aliran bandwidth, sumber waktu, segmentasi, dan daya PoE beserta titik gagal dan pemiliknya. Mulailah dari survei dan kebutuhan operasi, hitung kapasitas tiap lapisan, verifikasi kompatibilitas perangkat serta kondisi listrik, lalu uji jalur yang akan diterima.

Langkah berikutnya: minta pemilik sistem menyetujui diagram versi, daftar alamat, matriks layanan, tabel beban bandwidth/PoE, dan skenario gangguan. Untuk menindaklanjuti survei, Anda dapat mulai dari [halaman utama Tukang.co.id](/) atau meminta koordinasi [layanan pasang CCTV di Dau](/kota/jual-pasang-cctv-dau/) bila lokasinya sesuai. Serahkan perhitungan listrik, jalur fisik, dan hardening kepada disiplin yang berwenang. **[NEEDS TECHNICAL REVIEW: persetujuan desain, kapasitas terukur, dan hasil uji lapangan belum tersedia.]** Aturan praktisnya: tidak ada garis pada diagram yang boleh tanpa pengirim, penerima, kapasitas, pemilik, dan bukti verifikasi.
