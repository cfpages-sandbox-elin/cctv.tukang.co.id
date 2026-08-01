---
article_id: CCT-06-05
title: "Alamat IP, DHCP, DNS, dan sinkronisasi waktu CCTV"
slug: "alamat-ip-dhcp-dns-dan-waktu-cctv"
description: "Plan CCTV connectivity, addressing, bandwidth, time, segmentation, and network-delivered power."
status: draft
writing_contract_version: "native-id-v2"
publication_date: "2025-09-30"
publication_date_basis: editorial_backfill
date_modified: null
parent_topic: CCT-06
primary_intent: "Establish stable addressing and trustworthy device time."
reader_community: "Tukang.co.id"
reader_address: "Sobat Tukang.co.id"
final_route: "/artikel/alamat-ip-dhcp-dns-dan-waktu-cctv.html"
technical_review: required
sources:
  - "https://www.onvif.org/profiles/profile-t/"
  - "https://www.onvif.org/"
  - "https://csrc.nist.gov/pubs/ir/8259/r1/final"
  - "https://pages.nist.gov/IoT-Device-Cybersecurity-Requirement-Catalogs/technical/"
  - "https://webstore.iec.ch/en/publication/63699"
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

# Alamat IP, DHCP, DNS, dan sinkronisasi waktu CCTV

Halo, Sobat Tukang.co.id! Jangan mulai dari mengganti kamera ketika rekaman tiba-tiba tidak bisa dibuka atau cap waktunya meleset. Mulailah dari peta jaringan: setiap kamera, perekam, dan komputer pemantau harus punya alamat yang dapat ditemukan, jalur komunikasi yang jelas, serta waktu yang berasal dari sumber tepercaya.

Jawaban singkatnya: gunakan rencana alamat IP yang terdokumentasi, pilih satu pengelola DHCP (Dynamic Host Configuration Protocol) atau tetapkan alamat statis/reservasi secara konsisten, sediakan DNS (Domain Name System) hanya bila nama perangkat memang dipakai, lalu sinkronkan kamera dan perekam ke sumber waktu yang sama. DHCP, DNS, dan NTP (Network Time Protocol) menyelesaikan masalah berbeda; salah satunya tidak dapat menggantikan yang lain. Pilihan final berubah menurut jumlah perangkat, rancangan VLAN, jalur internet, firmware, kebutuhan rekaman, dan bukti uji lapangan. **[NEEDS SITE/DESIGN REVIEW: EG-01, EG-02, EG-03, EG-09]**

![Ilustrasi CCTV Merk ZKTECO](/wp-content/uploads/2023/08/CCTV-Merk-ZKTECO.jpg)


*Aset lokal situs; gambar ini bukan dokumentasi proyek tertentu.*

## Definisi dan batas objek

Alamat IP adalah identitas logis pada jaringan. Alamat statis diisi pada perangkat dan tidak berubah kecuali diubah oleh administrator; reservasi DHCP membuat server DHCP memberikan alamat tertentu berdasarkan identitas perangkat. Keduanya bisa stabil, asalkan dicatat dan tidak saling tumpang tindih. DHCP sendiri hanya membagikan parameter seperti alamat, gateway, dan DNS; ia tidak menjamin kamera selalu hidup atau rekaman selalu tersimpan.

DNS menerjemahkan nama host menjadi alamat IP. Ia berguna bila operator memakai nama yang mudah diingat dan bila perubahan alamat perlu dikelola terpusat. Untuk sistem kecil, akses langsung dengan alamat yang terdokumentasi dapat lebih sederhana. NTP menyamakan jam perangkat dengan sumber waktu. Jam yang seragam penting saat mencari kejadian di beberapa kamera, tetapi sinkronisasi waktu tidak memperbaiki paket yang hilang, penyimpanan penuh, atau kamera yang terputus.

Artikel ini membahas konfigurasi operasional jaringan: pengalamatan, resolusi nama, waktu, segmentasi, koneksi perekam, dan hubungan PoE (Power over Ethernet) dengan jaringan. Kebijakan akun, kata sandi, hak akses, dan pengelolaan kredensial berada di ruang lingkup keamanan tersendiri. Perangkat tertentu mungkin memiliki menu dan kemampuan berbeda; identitas model, firmware, peran ONVIF, dan instruksi pabrikan harus diverifikasi sebelum perubahan.

## Cara kerjanya

Urutan yang mudah dirawat adalah sebagai berikut.

1. **Inventaris.** Catat kamera, NVR/VMS, switch, router, server waktu, jalur uplink, dan port PoE. Beri setiap aset nama, lokasi logis, alamat MAC, alamat IP, dan pemilik perubahan. Jangan mengisi kolom dengan tebakan; sisakan status “belum diverifikasi” bila survei belum dilakukan.
2. **Rancang ruang alamat.** Pisahkan jaringan CCTV dari jaringan kantor atau tamu bila analisis risiko dan perangkat jaringan mendukungnya. Tentukan subnet, rentang DHCP, rentang reservasi, alamat gateway, serta alamat manajemen switch. Hindari alamat statis yang berada di dalam pool DHCP tanpa reservasi karena konflik dapat muncul sewaktu-waktu.
3. **Terapkan satu sumber konfigurasi.** Jika DHCP dipilih, matikan layanan DHCP lain pada segmen yang sama. Jika sebagian perangkat statis, buat daftar pengecualian dan uji tidak ada duplikasi. Simpan perubahan dalam diagram dan tabel konfigurasi yang punya tanggal serta penanggung jawab.
4. **Uji konektivitas.** Dari NVR/VMS, periksa apakah kamera dapat dijangkau pada port layanan yang diperlukan. Uji juga arah sebaliknya yang memang dibutuhkan, bukan membuka semua akses. Profile T ONVIF mencakup kemampuan streaming, imaging, event, metadata, HTTPS, atau audio tertentu, tetapi dukungan opsional tetap harus dicocokkan dengan model dan firmware yang diuji ([ONVIF Profile T](https://www.onvif.org/profiles/profile-t/)). Logo atau centang ONVIF saja bukan bukti kompatibilitas penuh ([panduan ONVIF](https://www.onvif.org/)).
5. **Atur waktu.** Pilih sumber NTP internal yang dapat dijangkau kamera dan perekam; bila memakai sumber eksternal, dokumentasikan ketergantungan internet dan perilaku saat koneksi putus. Samakan zona waktu dan aturan musim waktu yang berlaku di perangkat. Lakukan uji dengan mencatat selisih jam sebelum dan sesudah sinkronisasi, bukan sekadar melihat ikon “connected”.
6. **Verifikasi PoE dan uplink.** PoE menyatukan daya dan data pada kabel, namun anggaran daya, kategori kabel, proteksi, jalur, dan pemisahan dari sumber lain tetap membutuhkan desain kompeten serta pengujian aktual. Rujukan IEC 60364-1 menekankan bahwa label anggaran atau uji kontinuitas saja tidak membuktikan keselamatan, bandwidth, retensi, atau ketahanan sistem ([IEC 60364-1](https://webstore.iec.ch/en/publication/63699)).

## Faktor yang mengubah hasil

Jumlah kamera bukan satu-satunya beban. Resolusi, frame rate, codec, audio, metadata, analitik, dan pola gerak memengaruhi lalu lintas. Uplink switch harus dinilai dari lalu lintas aktual dan cadangan yang disetujui, bukan dari jumlah port semata. Saat link penuh, gejalanya dapat berupa gambar patah, jeda, atau rekaman tidak lengkap meskipun alamat IP benar.

Topologi juga menentukan titik gagal. Satu switch atau satu jalur uplink membuat pemeliharaan lebih mudah tetapi dapat menjadi titik putus bersama. Segmentasi VLAN mengurangi ruang siar dan membatasi jalur, namun salah konfigurasi trunk, gateway, atau aturan firewall dapat membuat kamera tidak terlihat. Catat alur yang benar-benar diperlukan antara kamera, NVR/VMS, workstation, DNS, dan NTP.

Kawan Tukang.co.id, perhatikan waktu sebagai bukti operasional, bukan hiasan di layar. Sumber NTP yang tidak stabil, zona waktu berbeda, baterai jam yang lemah, atau reboot tanpa sinkronisasi dapat menggeser urutan kejadian. Tetapkan siapa yang memantau status sinkronisasi, kapan pemeriksaan dilakukan, dan apa tindakan jika sumber waktu tidak tersedia. Jangan menyimpulkan ketepatan waktu hanya dari satu tangkapan layar.

Faktor lain adalah siklus hidup perangkat. NIST mengelompokkan kebutuhan perangkat IoT ke identitas, konfigurasi aman, perlindungan data, kontrol akses logis, pembaruan, kesadaran keadaan, dan operasi aman ([NISTIR 8259 Rev. 1](https://csrc.nist.gov/pubs/ir/8259/r1/final)). Katalog kapabilitas NIST dapat membantu menyusun pertanyaan pengadaan, tetapi bukan bukti bahwa model atau firmware tertentu memenuhi semuanya ([NIST IoT capability catalog](https://pages.nist.gov/IoT-Device-Cybersecurity-Requirement-Catalogs/technical/)).

## Contoh keputusan praktis

Gunakan tabel berikut sebagai kerangka keputusan, bukan nilai desain final.

| Kondisi yang terverifikasi | Pilihan awal | Bukti yang harus diminta |
|---|---|---|
| Satu segmen kecil, satu pengelola jaringan, perangkat mendukung reservasi | Reservasi DHCP untuk kamera dan NVR; daftar MAC–IP terpusat | Ekspor lease, daftar reservasi, dan uji reboot |
| Perangkat lama perlu alamat statis | Rentang statis di luar pool DHCP | Diagram subnet, konfigurasi gateway/DNS, dan uji konflik |
| NVR dan kamera berada di VLAN berbeda | Aturan antar-VLAN paling sempit yang masih mendukung layanan | Matriks alur, log firewall, dan uji fungsi ONVIF |
| Internet tidak selalu tersedia | NTP internal; catat perilaku saat sumber luar gagal | Status sinkronisasi, waktu pemulihan, dan alarm pemantauan |
| Kamera memakai PoE | Hitung beban dan verifikasi switch, kabel, proteksi, serta jalur | Datasheet identitas tepat, pengukuran beban, dan hasil uji failover |

Untuk setiap baris, kolom “terverifikasi” harus berasal dari survei dan dokumen perangkat yang aktual. **[NEEDS DESIGN/ACCEPTANCE EVIDENCE: EG-02, EG-03, EG-09]** Tanpa itu, tabel hanya membantu menyusun pertanyaan, bukan menyetujui konfigurasi.

## Kesalahan umum dan cara memeriksanya

Kesalahan pertama adalah memasang semua kamera pada alamat otomatis lalu menganggap masalah selesai. Periksa apakah lease berubah setelah reboot, apakah ada perangkat dengan alamat sama, dan apakah daftar NVR memakai alamat yang benar. Kesalahan kedua adalah mencampur DNS publik, DNS router, dan DNS internal tanpa keputusan; uji resolusi nama dari segmen tempat aplikasi berjalan.

Kesalahan ketiga adalah mengatur waktu manual pada setiap kamera. Bandingkan jam kamera, NVR, dan komputer pemantau terhadap satu sumber acuan, lalu simpan hasil dan tanggal pengujian. Kesalahan keempat adalah membuka akses luas agar ONVIF “pasti terdeteksi”. Batasi jalur sesuai matriks layanan dan cocokkan fitur wajib dengan profil serta firmware yang benar; kemampuan opsional tidak otomatis tersedia.

Kesalahan kelima adalah menganggap PoE identik dengan ketahanan. Cabut atau pulihkan sumber daya hanya dalam prosedur yang disetujui, lalu uji dampaknya pada kamera, switch, NVR, dan waktu. Jangan mengubah proteksi, grounding, atau pengawatan langsung dari artikel ini. Pekerjaan yang menyentuh energi listrik memerlukan orang berwenang, metode lokasi, isolasi, verifikasi, dan pemeriksaan sesuai kondisi proyek.

## Pilihan yang tampak mudah

Shortcut yang sering dipilih adalah memakai alamat IP kamera yang sama di setiap lokasi agar teknisi mudah menghafalnya. Itu hanya tampak mudah sampai dua segmen terhubung: konflik alamat membuat perangkat saling menimpa dan diagnosis menjadi kabur. Alternatif yang lebih dapat ditelusuri adalah skema alamat per lokasi atau VLAN, reservasi yang konsisten, nama host yang bermakna, serta catatan perubahan. Skema tersebut tetap harus disetujui berdasarkan survei, kapasitas, jalur, dan kebutuhan akses yang nyata.

## Kesimpulan dan langkah berikutnya

Alamat IP memberi identitas, DHCP membagikan parameter, DNS menerjemahkan nama, dan NTP menyamakan waktu. Rancang keempatnya bersama topologi, beban lalu lintas, segmentasi, dan PoE; jangan mengira satu fitur menutup kegagalan fitur lain.

Teman Tukang.co.id, sebelum konfigurasi dianggap selesai, minta paket serah-terima yang berisi inventaris, diagram subnet/VLAN, tabel IP–MAC, sumber DNS/NTP, daftar firmware dan profil yang diuji, matriks alur, catatan PoE, serta hasil reboot dan uji waktu. Untuk mengatur survei atau pemasangan di lokasi, gunakan rute layanan yang memang tersedia seperti [konsultasi pasang CCTV di Wungu](/kota/jual-pasang-cctv-wungu/) atau [layanan pasang CCTV di Wuluhan](/kota/jual-pasang-cctv-wuluhan/). Tandai hal yang belum terbukti dan minta **[NEEDS COORDINATOR TECHNICAL REVIEW: EG-01, EG-02, EG-03, EG-09, EG-10]** sebelum perubahan di lokasi. Aturan operasionalnya sederhana: setiap alamat dan jam harus punya sumber, pemilik, dan bukti uji yang dapat diulang.
