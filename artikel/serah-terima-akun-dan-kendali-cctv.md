---
article_id: CCT-18-01
title: "Checklist serah terima akun dan kendali CCTV"
slug: "serah-terima-akun-dan-kendali-cctv"
description: "Ambil kendali sistem, pahami syarat garansi, jaga bahan insiden, dan tutup siklus hidup data."
status: draft
publication_date: "2026-07-03"
publication_date_basis: editorial_backfill
date_modified: null
parent_topic: CCT-18
primary_intent: "Transfer credentials, ownership, licenses, apps, cloud services, and recovery access."
reader_community: "Tukang.co.id"
reader_address: "Kawan Tukang.co.id"
final_route: "/artikel/serah-terima-akun-dan-kendali-cctv.html"
technical_review: required
writing_contract_version: "native-id-v2"
sources:
  - "https://csrc.nist.gov/pubs/ir/8259/r1/final"
  - "https://pages.nist.gov/IoT-Device-Cybersecurity-Requirement-Catalogs/technical/"
  - "https://www.onvif.org/profiles/profile-t/"
  - "https://www.onvif.org/"
  - "https://peraturan.bpk.go.id/Details/229798/uu-no-27-tahun-2022"
  - "https://www.iso.org/standard/62542.html"
  - "https://www.ilo.org/topics-and-sectors/occupational-safety-and-health-guide-labour-inspectors-and-other/how-can-occupational-safety-and-health-be-managed/controlling-risks"
---

# Checklist serah terima akun dan kendali CCTV

Halo, Kawan Tukang.co.id! Serah terima CCTV belum selesai ketika kamera menampilkan gambar. Kendali yang benar berpindah jika pemilik baru dapat masuk ke seluruh akun, mengetahui siapa yang berwenang, menerima bukti lisensi dan garansi, mengambil rekaman yang diperlukan, serta memiliki prosedur menutup akses lama. Jika salah satu bagian itu hilang, sistem bisa tetap menyala tetapi tidak sepenuhnya berada di tangan pemilik.

Gunakan checklist ini dalam rapat serah terima. Cocokkan setiap item dengan catatan proyek yang sebenarnya—nama model, nomor seri, aplikasi, penyedia cloud, periode garansi, dan kebijakan penyimpanan. Detail seperti masa garansi, retensi rekaman, atau status akun tidak boleh ditebak; minta dokumen asli atau beri tanda **[NEEDS PROJECT RECORD: identitas sistem, pemilik akun, dan syarat garansi]**.

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

## Hasil akhir dan prasyarat

Tujuan serah terima adalah membuat pemilik baru mampu mengelola sistem tanpa bergantung pada akun pribadi pemasang. Hadirkan pemilik atau wakil yang berwenang, pengelola jaringan, dan pihak penyerah. Siapkan berita acara, daftar perangkat dan nomor seri, diagram jaringan atau as-built yang tersedia, daftar aplikasi, kontrak cloud, bukti pembelian, lisensi, syarat garansi, serta catatan insiden yang masih terbuka.

Sebelum sesi dimulai, sepakati apa yang termasuk: kamera, recorder, penyimpanan, monitor, aplikasi seluler, portal cloud, notifikasi, integrasi, dan akses pemulihan. Pisahkan pula apa yang bukan bagian serah terima, misalnya perubahan desain, penggantian perangkat, atau penguatan keamanan awal. Penguatan akun setelah akses berpindah adalah pekerjaan tersendiri; halaman ini tidak menggantikan penilaian keamanan sistem.

## Langkah 1 — tetapkan cakupan

Buat daftar aset dengan tiga kolom: komponen, akun atau pemilik layanan, dan bukti penguasaan. Untuk setiap kamera dan recorder, catat identitas yang dapat diverifikasi dari label atau dokumen, bukan hanya nama dagang. Untuk layanan cloud, catat organisasi pemilik, alamat pemulihan, metode pembayaran, dan administrator. Jangan menyalin kata sandi ke badan berita acara; gunakan kanal serah terima yang disepakati lalu catat bahwa akses telah diterima.

Tentukan peran setelah handover: administrator, operator harian, auditor, dan kontak pemulihan. Satu orang boleh memegang lebih dari satu peran hanya jika organisasi menerima risikonya. Kawan Tukang.co.id, jangan menganggap akun teknisi sebagai akun pemilik. Bila akun tidak dapat dipindahkan atau lisensinya melekat pada pihak lama, tahan tanda terima untuk item tersebut dan minta keputusan tertulis tentang penggantian atau pengalihan.

Scope juga harus menjawab batas data: area yang direkam, siapa yang boleh melihat, kanal ekspor, dan kapan rekaman dihapus. UU Pelindungan Data Pribadi menuntut pengelolaan data pribadi secara bertanggung jawab; penerapan pada lokasi dan peran tertentu perlu ditinjau berdasarkan kondisi nyata. Simpan penanda **[NEEDS LEGAL/PRIVACY REVIEW: tujuan, akses, retensi, dan penghapusan rekaman]** jika register itu belum tersedia. (Sumber: [UU No. 27 Tahun 2022](https://peraturan.bpk.go.id/Details/229798/uu-no-27-tahun-2022).)

## Langkah 2 — kumpulkan dan cocokkan bukti

Gunakan urutan cocokkan, uji terbatas, lalu catat hasil. Cocokkan nomor seri dengan daftar aset, model perangkat dengan lisensi, dan aplikasi dengan recorder atau cloud yang dilayaninya. Logo atau tulisan “kompatibel” tidak cukup untuk membuktikan semua fitur berjalan. ONVIF menjelaskan profil dan peran perangkat, tetapi kesesuaian profil tidak otomatis membuktikan setiap fitur opsional, kompatibilitas firmware, atau dukungan sepanjang siklus hidup. Verifikasi produk dan alur yang benar-benar dipakai melalui dokumentasi serta uji penerimaan yang disetujui. (Sumber: [ONVIF Profile T](https://www.onvif.org/profiles/profile-t/) dan [panduan produk conformant ONVIF](https://www.onvif.org/).)

Minta empat kelompok bukti:

- **Kendali akses:** akun pemilik, daftar admin/operator, alamat pemulihan, lisensi, dan bukti bahwa akses penyerah dapat dicabut.
- **Operasi:** peta perangkat, versi perangkat lunak atau firmware yang terdokumentasi, alur notifikasi, serta prosedur ekspor rekaman.
- **Kontrak dan dukungan:** invoice atau kontrak, nomor tiket yang terbuka, kontak vendor, cakupan dan pengecualian garansi, serta tanggal mulai atau berakhir yang tertulis.
- **Data dan insiden:** indeks rekaman yang sedang ditahan, hash atau nama berkas bila sudah diekspor, alasan penahanan, pihak yang menerima, dan batas akses.

NIST menempatkan identitas perangkat, konfigurasi aman, perlindungan data, pembaruan, pencatatan keadaan, dan kemampuan operasi aman sebagai kemampuan yang perlu diprofilkan sesuai penggunaan. Karena itu, checklist ini tidak menyatakan bahwa sistem sudah aman hanya karena satu kata sandi telah berpindah. (Sumber: [NISTIR 8259 Rev. 1](https://csrc.nist.gov/pubs/ir/8259/r1/final) dan [katalog kapabilitas IoT NIST](https://pages.nist.gov/IoT-Device-Cybersecurity-Requirement-Catalogs/technical/).)

## Langkah 3 — jalankan urutan kerja

Mulai dengan pembacaan daftar aset bersama. Pihak penyerah menunjukkan lokasi akun, aplikasi, portal, dan dokumen; penerima mencatat akun mana yang berhasil diakses tanpa menyalin rahasia ke dokumen terbuka. Setelah itu, lakukan demonstrasi minimum yang disepakati: masuk sebagai pemilik, melihat status perangkat, mencari rekaman pada waktu yang disepakati, mengekspor satu berkas uji, dan memastikan penerima tahu lokasi panduan pemulihan.

Lakukan ekspor insiden secara terpisah dari uji biasa. Tulis waktu yang dipakai, zona waktu, nama berkas, sumber kamera, siapa yang mengekspor, media penyimpanan, dan checksum bila organisasi menggunakannya. Jangan mengirim rekaman melalui grup umum. Jika ada permintaan aparat, sengketa, atau kebutuhan investigasi, minta arahan pemilik data dan penasihat yang berwenang sebelum menyalin atau menghapus.

Terakhir, sepakati pencabutan akses pihak lama. Catat akun teknisi, akun vendor, token integrasi, tautan berbagi, dan akses pembayaran yang harus ditutup atau dialihkan. Jangan melakukan perubahan yang dapat memutus layanan di tengah serah terima tanpa rencana pemulihan dan persetujuan pemilik. Pengelolaan rekaman mengikuti kebutuhan, kewenangan, dan jadwal retensi organisasi; standar manajemen rekaman membantu membedakan dokumen terkendali dari catatan kejadian, tetapi tidak menetapkan jadwal retensi untuk lokasi Anda. (Sumber: [ISO 15489-1:2016](https://www.iso.org/standard/62542.html).)

## Titik tahan dan kondisi berhenti

Hentikan tanda tangan final jika identitas aset tidak cocok, akun pemilik tidak dapat dipulihkan, lisensi atau garansi hanya berupa janji lisan, rekaman uji tidak dapat diekspor, atau ada akun lama yang masih memiliki hak administrator. Beri status “terbuka”, pemilik tindakan, bukti yang diminta, dan tanggal peninjauan. Jangan menutup celah dengan membuat akun baru yang tidak tercantum dalam kontrak atau dengan menghapus rekaman untuk merapikan penyimpanan.

Berhenti juga ketika permintaan menyentuh perubahan jaringan, firmware, pengaturan proteksi listrik, atau penghapusan data yang mungkin menjadi bukti. Pekerjaan itu memerlukan prosedur dan persetujuan yang sesuai. [NEEDS TECHNICAL REVIEW: dampak perubahan konfigurasi dan rencana pemulihan sistem.] Siklus pengendalian risiko yang baik dimulai dari kondisi nyata dan tindakan pengendalian, bukan dari banyaknya formulir; panduan ILO menekankan penilaian dan pengendalian yang berulang sesuai risiko. (Sumber: [ILO—controlling risks](https://www.ilo.org/topics-and-sectors/occupational-safety-and-health-guide-labour-inspectors-and-other/how-can-occupational-safety-and-health-be-managed/controlling-risks).)

## Verifikasi hasil dan serah terima

Berita acara sebaiknya memuat tanggal, pihak dan kewenangan, daftar item diterima, item tertunda, hasil demonstrasi, lokasi dokumen, status akses lama, dan tindakan lanjutan. Gunakan tabel ringkas berikut sebagai lembar paraf:

| Item penerimaan | Bukti yang dilihat | Status |
| --- | --- | --- |
| Akun pemilik dan pemulihan | Portal/aplikasi, alamat pemulihan, berita acara akses | diterima / terbuka |
| Perangkat dan lisensi | Daftar nomor seri, invoice, lisensi, kontrak | cocok / selisih |
| Rekaman dan ekspor | Berkas uji, indeks insiden, media penyimpanan | berhasil / ulangi |
| Garansi dan dukungan | Syarat tertulis, kontak, tiket terbuka | jelas / minta klarifikasi |
| Akses pihak lama | Daftar admin, vendor, token, tautan | dicabut / dijadwalkan |
| Data lifecycle | Tujuan, akses, retensi, penghapusan, penahanan | disetujui / review |

Penerima menandatangani hanya item yang buktinya tersedia. “Diterima dengan catatan” harus menyebut catatan itu secara spesifik, bukan sekadar “akan dicek”. Tetapkan pemeriksa untuk item terbuka dan jangan menganggap sistem telah disetujui secara teknis hanya karena berita acara sudah ditandatangani.

## Jalan pintas yang sering gagal

Jalan pintas yang paling menggoda adalah menerima satu akun admin dan menganggap sisanya dapat diurus nanti. Cara ini menyembunyikan kepemilikan cloud, akses pemulihan, lisensi, dan rekaman yang mungkin berada di layanan berbeda. Ketika nomor telepon pemulihan milik teknisi tidak aktif atau kontrak cloud berakhir, pemilik baru bisa kehilangan kendali dan bukti kejadian sekaligus.

Alternatif yang lebih aman adalah membuat inventaris, menguji fungsi minimum, mencatat pengecualian, lalu mencabut akses lama secara terencana. Untuk menyiapkan kebutuhan instalasi atau dukungan lanjutan, gunakan [halaman layanan CCTV](/services/) dan pastikan ruang lingkupnya tertulis. Sobat Tukang.co.id, bila bukti belum ada, status yang jujur adalah “belum terbukti”, bukan “diasumsikan beres”.

## Kesimpulan

Checklist serah terima akun dan kendali CCTV harus menutup enam hal: siapa pemiliknya, perangkat dan lisensinya apa, akses pemulihannya di mana, rekaman diperlakukan bagaimana, syarat dukungan tertulis apa, dan akses lama kapan dicabut. Mulailah dengan berita acara serta inventaris; minta [NEEDS PROJECT RECORD] untuk setiap identitas, garansi, retensi, atau hak akses yang belum dapat dibuktikan.

Teman Tukang.co.id, langkah berikutnya adalah menjadwalkan sesi demonstrasi bersama pemilik yang berwenang dan meminta technical/privacy review untuk item terbuka. Bila perlu membandingkan konteks pekerjaan, mulai dari [beranda Tukang.co.id](/) lalu kembali ke checklist ini. Aturan operasionalnya sederhana: tidak ada tanda tangan “selesai” tanpa bukti yang dapat ditelusuri, dan tidak ada penghapusan atau perubahan berisiko sebelum pemilik serta pihak kompeten menyetujuinya.
