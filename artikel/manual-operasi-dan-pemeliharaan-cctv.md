---
article_id: CCT-17-06
title: "Isi manual operasi dan pemeliharaan CCTV"
slug: "manual-operasi-dan-pemeliharaan-cctv"
description: "Verify which standards, certificates, installer capabilities, and project records actually apply."
status: draft
writing_contract_version: "native-id-v2"
publication_date: "2026-06-28"
publication_date_basis: editorial_backfill
date_modified: null
parent_topic: CCT-17
primary_intent: "Specify the O&M information the owner needs after acceptance."
reader_community: "Tukang.co.id"
reader_address: "Kawan Tukang.co.id"
final_route: "/artikel/manual-operasi-dan-pemeliharaan-cctv.html"
technical_review: required
sources:
  - "https://www.ilo.org/topics-and-sectors/occupational-safety-and-health-guide-labour-inspectors-and-other/how-can-occupational-safety-and-health-be-managed/controlling-risks"
  - "https://bnsp.go.id/"
  - "https://www.iso.org/files/live/sites/isoorg/files/archive/pdf/en/iso_45001_-briefing_note.pdf"
  - "https://www.iso.org/standard/70017.html"
  - "https://peraturan.bpk.go.id/Details/5263/pp-no-50-tahun-2012"
  - "https://peraturan.bpk.go.id/Details/229798/uu-no-27-tahun-2022"
  - "https://www.iso.org/standard/62542.html"
  - "https://webstore.iec.ch/en/publication/7353"
  - "https://www.onvif.org/profiles/profile-t/"
  - "https://www.onvif.org/"
  - "https://webstore.iec.ch/en/publication/63699"
---

# Isi manual operasi dan pemeliharaan CCTV

Halo, Kawan Tukang.co.id! Manual operasi dan pemeliharaan (O&M) CCTV bukan sekadar buku petunjuk atau kumpulan brosur. Isinya harus membuat pemilik mampu mengenali sistem yang benar-benar terpasang, mengoperasikannya dengan aman, menjadwalkan perawatan, mencatat perubahan, dan menentukan kapan teknisi perlu dipanggil.

Isi minimumnya adalah identitas sistem dan gambar akhir pemasangan, tujuan tiap kamera, prosedur operasi normal dan gangguan, daftar perangkat serta firmware, konfigurasi jaringan dan penyimpanan, jadwal inspeksi, formulir catatan, daftar suku cadang, kontak eskalasi, dan batas kewenangan pengguna. Rincian akhirnya berubah sesuai model, lokasi, konfigurasi, hasil uji penerimaan, dan aturan organisasi. Tanpa rekaman proyek tersebut, manual hanya dapat menjadi templat—bukan bukti bahwa sistem tertentu sudah sesuai.

![Ilustrasi CCTV Merk ZKTECO](/wp-content/uploads/2023/08/CCTV-Merk-ZKTECO.jpg)

*Ilustrasi umum dari aset lokal cctv.tukang.co.id; bukan dokumentasi proyek tertentu.*

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

Manual O&M adalah dokumen terkendali yang menjelaskan cara menjalankan dan merawat sistem setelah pekerjaan diterima. Dokumen ini berbeda dari gambar desain, laporan commissioning, kontrak, dan sesi serah-terima. Gambar menjawab “apa dan di mana”; laporan uji menjawab “apa yang diverifikasi”; manual menjawab “bagaimana mengoperasikan dan menjaga kondisi itu”. Semuanya perlu dirujuk silang, dengan nomor revisi dan tanggal yang jelas.

Hal yang termasuk antara lain:

- daftar kamera, recorder, switch, UPS, monitor, dan aksesori beserta merek, model, nomor seri, lokasi, serta versi perangkat lunak;
- denah/as-built, diagram jaringan dan daya, jalur kabel, port, alamat logis, serta hubungan kamera–recorder–klien;
- tujuan pengamatan setiap kamera, batas area yang diharapkan, retensi rekaman yang disetujui, dan cara mencari atau mengekspor rekaman;
- langkah operasi harian, indikator normal, alarm, kehilangan koneksi, media penyimpanan penuh, dan pemulihan yang diizinkan;
- jadwal inspeksi, pembersihan, pencadangan konfigurasi, pembaruan, pengujian, serta formulir hasil dan tindak lanjut;
- matriks peran: siapa boleh melihat, mengekspor, mengubah konfigurasi, menyetujui perubahan, dan menghubungi eskalasi.

Serah-terima akun, penggantian kata sandi secara langsung, dan pelatihan tatap muka bukan pengganti isi manual dan berada di luar batas artikel ini. Kawan Tukang.co.id, minta keduanya dicatat sebagai aktivitas terpisah agar bukti akses tidak tercampur dengan dokumen teknis.

Untuk rekaman yang memuat orang, manual perlu menjelaskan pemilik data, tujuan penggunaan, hak akses, pencatatan ekspor, periode simpan, dan pemusnahan sesuai kebijakan yang berlaku. [NEEDS PROJECT RECORD REVIEW: pemilik data, dasar pemrosesan, retensi, dan matriks akses belum tersedia.] Prinsip pengelolaan rekaman dan bukti harus dibedakan dari dokumen kerja biasa; rujukan umum dapat dilihat pada [UU No. 27 Tahun 2022](https://peraturan.bpk.go.id/Details/229798/uu-no-27-tahun-2022) dan catatan [ISO 15489-1](https://www.iso.org/standard/62542.html).

## Cara kerjanya

Susun manual dari alur yang dapat ditelusuri, bukan dari urutan menu aplikasi. Mulai dengan lembar identitas sistem. Salin data dari daftar aset yang disetujui, gambar as-built, hasil commissioning, dan berita acara penerimaan. Setiap perbedaan antara desain dan kondisi akhir diberi catatan perubahan, alasan, tanggal, serta pihak yang menyetujui.

Berikut urutan yang mudah dipakai operator:

1. **Kenali kondisi normal.** Tunjukkan status daya, jaringan, waktu sistem, kapasitas penyimpanan, dan indikator kesehatan yang memang tersedia pada model tersebut. Jangan menyatakan indikator tertentu ada sebelum diverifikasi.
2. **Lakukan operasi rutin.** Jelaskan login sesuai peran, tampilan langsung, pencarian berdasarkan waktu/kejadian, ekspor dengan format yang disepakati, dan pencatatan setiap permintaan rekaman. Sertakan peringatan bahwa ekspor tidak boleh mengubah bukti asli.
3. **Tanggapi gangguan berjenjang.** Operator hanya melakukan pemeriksaan non-invasif yang diizinkan: mencatat waktu, gejala, kamera/kanal terdampak, pesan sistem, dan perubahan terakhir. Isolasi, pembukaan panel, pekerjaan listrik, atau penggantian perangkat harus dialihkan kepada personel berwenang.
4. **Rawat dan verifikasi.** Formulir mencatat tanggal, aset, kondisi sebelum dan sesudah, alat ukur bila digunakan, hasil, temuan, tindakan, dan persetujuan penutupan. Panduan [IEC 62676-4](https://webstore.iec.ch/en/publication/7353) menempatkan kebutuhan, pemilihan, pemasangan, commissioning, pemeliharaan, pengujian, dan evaluasi objektif sebagai rangkaian yang saling terkait; manual sebaiknya mencerminkan rangkaian itu.
5. **Kendalikan perubahan.** Firmware, lensa, alamat jaringan, aturan deteksi, kapasitas disk, dan integrasi klien tidak diubah hanya karena “lebih baru”. Catat permintaan, dampak, rencana kembali, hasil uji, dan revisi manual setelah perubahan.

Jika sistem memakai perangkat lintas merek, tulis peran perangkat dan fitur yang benar-benar diuji. [ONVIF Profile T](https://www.onvif.org/profiles/profile-t/) membantu mengidentifikasi lingkup streaming, imaging, event, metadata, PTZ, atau HTTPS yang relevan; logo atau centang protokol saja tidak membuktikan seluruh fitur opsional dan kompatibilitas recorder–klien. Verifikasi produk dan profil pada [direktori ONVIF](https://www.onvif.org/) tetap diperlukan.

## Faktor yang mengubah hasil

Manual yang baik menyebut kondisi yang dapat mengubah langkah, bukan memberi satu jadwal untuk semua lokasi. Faktor utamanya meliputi:

- **Tujuan dan adegan:** kamera untuk deteksi, pengamatan, atau identifikasi memerlukan kriteria uji dan penempatan yang berbeda. Jumlah megapiksel atau demo produk tidak membuktikan cakupan berguna.
- **Lingkungan:** debu, hujan, panas, pencahayaan malam, getaran, dan akses fisik memengaruhi inspeksi serta interval pembersihan. Interval harus berasal dari kondisi dan rekaman pemeliharaan setempat.
- **Jaringan dan daya:** perubahan beban PoE, UPS, jalur kabel, pemisahan jaringan, atau proteksi listrik dapat mengubah ketersediaan. [IEC 60364-1](https://webstore.iec.ch/en/publication/63699) tidak boleh dipakai untuk menebak desain instalasi tertentu; identitas beban, jalur, proteksi, dan verifikasi kompeten harus ada.
- **Peran dan kompetensi:** manual membedakan operator, administrator, teknisi jaringan, teknisi listrik, dan pihak penyetuju. Bukti kompetensi harus memuat lingkup, penerbit, identitas, masa berlaku, dan konteks praktik; cek sumber [BNSP](https://bnsp.go.id/) dan prinsip kompetensi dalam [briefing ISO 45001](https://www.iso.org/files/live/sites/isoorg/files/archive/pdf/en/iso_45001_-briefing_note.pdf). Sertifikat tidak otomatis memberi kewenangan bekerja pada sistem tertentu.
- **Risiko dan perubahan:** metode penilaian risiko perlu mengacu pada kondisi aktual, paparan, konsekuensi, dan efektivitas pengendalian—bukan menyalin matriks generik. Lihat pendekatan [ILO untuk pengendalian risiko](https://www.ilo.org/topics-and-sectors/occupational-safety-and-health-guide-labour-inspectors-and-other/how-can-occupational-safety-and-health-be-managed/controlling-risks). [NEEDS SITE REVIEW: kondisi lokasi, akses, interaksi pekerjaan, dan perubahan terakhir belum tersedia.]

## Contoh keputusan praktis

Gunakan tabel berikut sebagai pemeriksaan isi, bukan sebagai persetujuan otomatis.

| Situasi yang ditemukan | Isi manual yang harus ada | Keputusan aman |
|---|---|---|
| Operator hanya menerima brosur | Identitas aset, as-built, prosedur normal, dan catatan uji | Tahan penerimaan dokumen sampai data terpasang dicocokkan |
| Satu kamera sering offline | Peta port/jalur, indikator normal, log gangguan, batas pemeriksaan operator | Catat gejala dan eskalasi; jangan mengubah konfigurasi tanpa otorisasi |
| Firmware atau storage diubah | Versi sebelum–sesudah, alasan, rencana kembali, hasil uji, revisi manual | Perlakukan sebagai perubahan terkendali |
| Rekaman diminta untuk insiden | Prosedur pencarian/ekspor, format, hash atau penanda integritas jika dipakai organisasi, pemilik akses, log serah-terima | Simpan salinan kerja tanpa menimpa bukti asli dan ikuti kebijakan data |
| Fitur ONVIF disebut di penawaran | Profil, peran, firmware, fitur wajib/kondisional, skenario uji | Cocokkan dengan hasil uji produk dan konfigurasi aktual; bukan logo |

Contoh tersebut bersifat kondisional. Ia tidak menyatakan sistem tertentu telah gagal atau lulus. Untuk audit internal, ruang lingkup, kompetensi, sampel, temuan, tindakan, dan efektivitas harus ditetapkan lebih dulu; catatan [ISO 19011](https://www.iso.org/standard/70017.html) dan [PP No. 50 Tahun 2012](https://peraturan.bpk.go.id/Details/5263/pp-no-50-tahun-2012) membantu membedakan catatan aktivitas dari bukti pengendalian.

## Kesalahan umum dan cara memeriksanya

**Menyalin manual pabrik tanpa konfigurasi akhir.** Brosur menjelaskan kemampuan umum, bukan port, alamat, aturan rekaman, atau batas yang disetujui. Cocokkan setiap perangkat dengan nomor aset dan foto/rekaman uji yang diizinkan.

**Menulis “cek berkala” tanpa kriteria.** Ganti frasa itu dengan objek, kondisi normal, cara cek, pencatat, frekuensi yang disetujui, dan tindakan ketika hasil menyimpang. Jangan menciptakan angka interval tanpa catatan proyek atau rekomendasi produsen yang cocok.

**Menganggap sertifikat installer sebagai bukti hasil instalasi.** Sertifikat hanya satu bukti kompetensi dalam lingkup tertentu. Minta identitas penerbit, masa berlaku, peran orang tersebut, serta laporan pekerjaan dan pengujian sistem aktual.

**Menyimpan kata sandi di halaman yang beredar luas.** Manual sebaiknya menunjuk prosedur pengelolaan kredensial dan pemilik akses, bukan menyalin rahasia. Account transfer dilakukan dalam proses terpisah sesuai batas artikel ini.

**Mengukur keberhasilan dari jumlah kamera atau uptime yang diklaim.** Angka tanpa definisi, periode, denominasi, kondisi, dan sumber tidak menunjukkan cakupan atau pengendalian efektif. Catat kebutuhan adegan, hasil uji, gangguan, dan tindakan yang bisa ditelusuri.

**Menghapus peringatan saat data belum ada.** Sobat Tukang.co.id, penanda seperti `[NEEDS SITE REVIEW]` lebih jujur daripada mengisi lokasi, model, retensi, atau kewenangan dengan tebakan. Penanda harus ditutup oleh pemilik proyek dengan dokumen asli sebelum manual dianggap final.

## Kesimpulan

Isi manual operasi dan pemeliharaan CCTV adalah paket dokumen terkendali: identitas dan as-built, tujuan serta batas kamera, prosedur operasi dan gangguan, konfigurasi yang disetujui, jadwal dan formulir perawatan, aturan akses/rekaman, kompetensi dan eskalasi, daftar perubahan, serta rujukan hasil uji. Standar, logo, atau sertifikat hanya dipakai sesuai lingkupnya dan tidak menggantikan bukti sistem terpasang.

Langkah berikutnya adalah meminta pemilik proyek mengisi daftar aset, gambar akhir, berita acara uji, matriks peran, kebijakan rekaman, dan log perubahan; lalu minta pemeriksaan teknis atas bagian listrik, jaringan, keamanan, dan kewajiban hukum yang relevan. Untuk titik awal kontak lokal, lihat [beranda Tukang.co.id](/) atau [halaman jual-pasang CCTV di Dau](/kota/jual-pasang-cctv-dau/); keduanya bukan bukti konfigurasi proyek tertentu. [NEEDS COORDINATOR REVIEW: data proyek dan persetujuan profesional belum disediakan.] Aturan operasinya sederhana: jangan menutup manual sebagai final sebelum setiap langkah dapat ditelusuri ke sistem aktual, pemiliknya jelas, dan perubahan berikutnya memiliki catatan.
