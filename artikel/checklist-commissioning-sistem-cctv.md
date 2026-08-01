---
article_id: CCT-12-01
title: "Checklist commissioning sistem CCTV"
slug: "checklist-commissioning-sistem-cctv"
description: "Test the installed system against documented requirements before sign-off."
status: draft
writing_contract_version: "native-id-v2"
publication_date: "2026-02-09"
publication_date_basis: editorial_backfill
date_modified: null
parent_topic: CCT-12
primary_intent: "Verify every installed subsystem before acceptance."
reader_community: "Tukang.co.id"
reader_address: "Sobat Tukang.co.id"
final_route: "/artikel/checklist-commissioning-sistem-cctv.html"
technical_review: required
sources:
  - "https://www.ilo.org/topics-and-sectors/occupational-safety-and-health-guide-labour-inspectors-and-other/how-can-occupational-safety-and-health-be-managed/controlling-risks"
  - "https://www.ilo.org/publications/5-step-guide-employers-workers-and-their-representatives-conducting"
  - "https://www.iso.org/standard/70017.html"
  - "https://peraturan.bpk.go.id/Details/5263/pp-no-50-tahun-2012"
  - "https://peraturan.bpk.go.id/Details/229798/uu-no-27-tahun-2022"
  - "https://www.iso.org/standard/62542.html"
  - "https://peraturan.bpk.go.id/Details/47614/uu-no-1-tahun-1970"
  - "https://peraturan.bpk.go.id/Details/145984/permenaker-no-12-tahun-2015"
  - "https://webstore.iec.ch/en/publication/7353"
  - "https://webstore.iec.ch/en/publication/59704"
  - "https://www.onvif.org/profiles/profile-t/"
  - "https://www.onvif.org/"
  - "https://webstore.iec.ch/en/publication/63699"
---

# Checklist commissioning sistem CCTV

Halo, Sobat Tukang.co.id! Jangan menandatangani serah terima hanya karena semua kamera menyala. Commissioning adalah pemeriksaan sistem terpasang terhadap kebutuhan yang sudah disepakati, lalu mencatat bukti, temuan, dan keputusan penerimaan. Hasil yang benar bukan sekadar “gambar muncul”, melainkan setiap subsistem, fungsi, antarmuka, dan dokumen dapat ditelusuri ke persyaratan.

Gunakan urutan sederhana: tetapkan scope, cocokkan bukti, jalankan uji konseptual yang aman, tahan pekerjaan bila ada ketidakcocokan, lalu serahkan paket rekaman. Nilai lulus atau gagal harus mengikuti kebutuhan operasional, desain yang disetujui, instruksi produsen, dan kondisi lokasi yang sebenarnya. Tanpa data itu, checklist ini hanya kerangka; [NEEDS PROJECT REVIEW: EG-01, EG-02, EG-03, EG-09, EG-10] sebelum dipakai sebagai dasar sign-off.

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

## Hasil akhir dan prasyarat

Target commissioning adalah satu keputusan yang bisa dipertanggungjawabkan: diterima, diterima dengan daftar pekerjaan tersisa, atau ditolak sampai koreksi selesai. Penanggung jawab penerimaan perlu ditetapkan sejak awal—misalnya pemilik sistem, pengawas, dan pelaksana—dengan batas kewenangan yang jelas. Artikel ini tidak mengesahkan kompetensi seseorang atau kepatuhan suatu lokasi.

Siapkan setidaknya dokumen kebutuhan (area yang harus dipantau, tujuan bukti, retensi, pengguna), gambar dan daftar perangkat terpasang, alamat atau identitas setiap perangkat, konfigurasi yang disetujui, manual, catatan perubahan, serta formulir uji. Sertakan daftar titik yang tidak dapat diuji saat itu dan alasannya. Untuk pekerjaan yang menyentuh energi listrik, pengujian harus dilakukan oleh orang berwenang dengan pengamanan dan verifikasi yang sesuai; [NEEDS SITE-SPECIFIC ELECTRICAL METHOD] jika prosedur dan otorisasinya belum tersedia. Dasar kewajiban keselamatan kerja tetap bergantung pada tempat, kegiatan, dan aturan pelaksana yang berlaku, bukan pada checklist generik ([UU No. 1 Tahun 1970](https://peraturan.bpk.go.id/Details/47614/uu-no-1-tahun-1970)).

## Langkah 1 — tetapkan ruang lingkup

Tuliskan batas sistem dalam satu halaman: kamera, lensa, dudukan, jaringan, PoE atau sumber daya lain, perekam, penyimpanan, monitor atau aplikasi klien, alarm, audio bila termasuk, sinkronisasi waktu, serta antarmuka ke sistem lain. Nyatakan juga apa yang tidak termasuk. Pengujian kualitas gambar rinci, misalnya penilaian siang-malam per adegan, tetap memerlukan metode dan kriteria tersendiri; jangan menggantinya dengan centang “kamera hidup”.

Petakan antarmuka dengan pihak lain: jaringan gedung, UPS, firewall, kontrol akses, pusat monitoring, atau ruang yang tetap dihuni. Catat kondisi lingkungan dan akses yang membatasi uji. Cara ini sejalan dengan prinsip pengendalian risiko yang dimulai dari identifikasi bahaya, penilaian kondisi, pengendalian, dan peninjauan ulang—bukan menumpuk formulir tanpa keputusan ([ILO, controlling risks](https://www.ilo.org/topics-and-sectors/occupational-safety-and-health-guide-labour-inspectors-and-other/how-can-occupational-safety-and-health-be-managed/controlling-risks); [ILO, five-step guide](https://www.ilo.org/publications/5-step-guide-employers-workers-and-their-representatives-conducting)).

Checklist scope praktis:

- setiap perangkat memiliki identitas dan lokasi yang cocok dengan daftar terpasang;
- jalur daya, jaringan, dan proteksi berada pada batas pekerjaan yang disetujui;
- fungsi yang dijanjikan dibedakan dari fitur opsional atau demo vendor;
- akses pengujian, keselamatan penghuni, dan jadwal penghentian layanan sudah disepakati.

## Langkah 2 — kumpulkan dan cocokkan bukti

Bandingkan tiga hal untuk setiap item: apa yang diminta, apa yang dirancang atau dibeli, dan apa yang benar-benar terpasang. Simpan nomor model, versi perangkat lunak, konfigurasi, hasil observasi, tanggal, penguji, dan referensi dokumen. Logo atau klaim kompatibilitas tidak cukup; untuk perangkat yang mengandalkan ONVIF, cocokkan produk, profil, peran, fitur wajib atau bersyarat, dan alur yang benar-benar diuji. ONVIF Profile T sendiri tidak membuktikan semua fitur opsional, keamanan, atau dukungan siklus hidup ([ONVIF Profile T](https://www.onvif.org/profiles/profile-t/); [ONVIF conformant-product guidance](https://www.onvif.org/)).

Kumpulkan bukti fungsi pada level sistem: kamera terdaftar, tampilan langsung, perekaman, pencarian dan ekspor, notifikasi atau event bila ada, hak akses pengguna, serta perilaku saat koneksi atau daya terganggu. Catat kriteria penerimaan sebelum melihat hasil agar keputusan tidak berubah mengikuti demo. IEC 62676-4 menekankan kebutuhan, tujuan adegan, instalasi, commissioning, pemeliharaan, pengujian, dan evaluasi objektif; jumlah megapiksel atau cuplikan contoh saja tidak membuktikan cakupan yang berguna ([IEC 62676-4](https://webstore.iec.ch/en/publication/7353)).

Kawan Tukang.co.id, bila hasil uji harus ditindaklanjuti di lapangan, bagikan hanya paket bukti yang relevan kepada pihak yang berwenang. Contoh rute koordinasi lokal seperti [layanan CCTV di Dau](/kota/jual-pasang-cctv-dau/) atau [layanan CCTV di Bae](/kota/jual-pasang-cctv-bae/) bukan pengganti persetujuan teknis; gunakan hanya bila wilayah dan ruang lingkupnya memang sesuai.

Perlakukan rekaman, konfigurasi, dan formulir sebagai rekod terkontrol: beri versi, pemilik, lokasi penyimpanan, dan aturan akses. Data video dapat memuat informasi pribadi, sehingga tujuan, akses, retensi, distribusi, dan penghapusan harus mengikuti peninjauan privasi dan hukum yang berlaku. UU Pelindungan Data Pribadi dan prinsip manajemen rekod menuntut pengendalian yang bergantung pada konteks; artikel ini tidak menetapkan masa simpan untuk proyek tertentu ([UU No. 27 Tahun 2022](https://peraturan.bpk.go.id/Details/229798/uu-no-27-tahun-2022); [ISO 15489-1](https://www.iso.org/standard/62542.html)).

## Langkah 3 — jalankan urutan kerja

Mulai dengan briefing singkat: tujuan uji, peran, komunikasi, area yang boleh dimasuki, dan kondisi penghentian. Gunakan urutan berikut tanpa mengubahnya menjadi instruksi live-work atau pembongkaran:

1. Verifikasi dokumen, identitas perangkat, label, dan perubahan terakhir.
2. Periksa kesiapan daya, jaringan, ruang, dan keselamatan secara visual sesuai prosedur proyek; jangan membuka atau mengubah panel tanpa kewenangan.
3. Uji registrasi dan komunikasi antar-sub sistem secara bertahap, sambil mencatat waktu, perangkat, kondisi, dan hasil.
4. Uji alur pengguna: live view, perekaman, pencarian, ekspor, alarm atau event, dan hak akses yang memang ada dalam scope.
5. Uji skenario gangguan yang telah disetujui—misalnya kehilangan koneksi atau sumber daya—hanya dengan metode, isolasi, dan otorisasi yang terdokumentasi.
6. Tinjau hasil bersama pemilik dan tandai pass, fail, blocked, atau not applicable beserta bukti pendukung.

Untuk tugas analitik, bedakan deteksi real-time dari pencarian forensik. Label AI, persentase dari dashboard, atau video contoh tidak membuktikan kinerja pada adegan, cuaca, keramaian, cahaya, dan alur respons target; kriteria, corpus atau adegan uji, konsekuensi salah positif/negatif, dan tinjauan manusia harus ditentukan proyek ([IEC 62676-6:2026](https://webstore.iec.ch/en/publication/59704)).

## Titik tahan dan kondisi berhenti

Hentikan dan eskalasi bila identitas atau versi perangkat tidak cocok, desain atau kriteria penerimaan belum disetujui, ada fungsi keselamatan yang tidak bekerja, bukti kritis hilang, akses data tidak jelas, atau perubahan memengaruhi antarmuka. Jangan “meluluskan sementara” dengan menghapus temuan dari formulir.

Teman Tukang.co.id, tahan uji juga ketika pekerjaan mengharuskan pekerjaan listrik, isolasi energi, atau kondisi tidak aman tanpa metode dan personel berwenang. Identifikasi sumber, isolasi, pembuktian tidak bertegangan, pembumian/proteksi, kondisi lingkungan, dan otorisasi adalah bukti yang berbeda; checklist ini tidak menggantikan prosedur disiplin tersebut ([Permenaker No. 12 Tahun 2015](https://peraturan.bpk.go.id/Details/145984/permenaker-no-12-tahun-2015)). Jika perubahan desain atau konfigurasi menimbulkan risiko baru, lakukan penilaian ulang sebelum melanjutkan, bukan mengandalkan matriks generik ([PP No. 50 Tahun 2012](https://peraturan.bpk.go.id/Details/5263/pp-no-50-tahun-2012)).

## Verifikasi hasil dan serah terima

Buat lembar penerimaan dengan kolom: ID item, persyaratan, metode atau referensi, kondisi uji, hasil, bukti (foto, log, ekspor, atau dokumen), temuan, pemilik tindakan, batas waktu, dan keputusan. Pisahkan pekerjaan tersisa dari cacat yang menghalangi fungsi utama. Setiap perubahan setelah uji harus memiliki versi baru dan jejak persetujuan.

Paket handover setidaknya memuat daftar perangkat final, gambar/as-built yang disetujui, konfigurasi dan akun yang diserahkan melalui kanal aman, hasil uji, daftar pengecualian, instruksi operasi dan pemeliharaan, serta pemicu review berikutnya. Gunakan pendekatan audit yang menetapkan scope, kompetensi, bukti lapangan, temuan, tindakan, efektivitas, dan tinjauan—bukan sekadar menghitung jumlah checklist ([ISO 19011:2018](https://www.iso.org/standard/70017.html)). Untuk daya, PoE, UPS, jalur kabel, dan perubahan, minta verifikasi desain listrik/jaringan yang kompeten; label anggaran PoE atau runtime UPS tidak dengan sendirinya membuktikan keselamatan, bandwidth, retensi, atau failover ([IEC 60364-1:2025](https://webstore.iec.ch/en/publication/63699)).

## Jalan pintas yang sering gagal

Jalan pintas yang paling menggoda adalah meminta vendor menunjukkan satu video, lalu menandai seluruh sistem lulus. Demo hanya menunjukkan kondisi dan adegan yang dipilih; ia tidak membuktikan identitas semua perangkat, konfigurasi final, retensi, hak akses, perilaku gangguan, atau kecocokan dengan kebutuhan lokasi. Alternatif yang lebih kuat adalah memilih sampel dan skenario berdasarkan kebutuhan tertulis, merekam hasil yang dapat ditelusuri, lalu meminta pemilik menandatangani pengecualian secara eksplisit. Bila bukti tidak tersedia, statusnya tetap *blocked* atau [NEEDS EVIDENCE], bukan lulus.

## Kesimpulan

Checklist commissioning sistem CCTV yang layak menguji keseluruhan rantai—scope, identitas dan desain, fungsi, antarmuka, gangguan, rekaman, keamanan akses, serta dokumen handover—terhadap kebutuhan tertulis. Langkah berikutnya adalah tetapkan pemilik penerimaan, bekukan kriteria uji, dan siapkan lembar bukti sebelum jadwal pengujian. [NEEDS COORDINATOR TECHNICAL REVIEW: EG-01, EG-02, EG-03, EG-09, EG-10] tetap berlaku karena artikel ini tidak memiliki data lokasi, desain, konfigurasi, atau hasil uji proyek tertentu. Aturan operasionalnya sederhana: tidak ada bukti yang cocok dengan persyaratan, tidak ada sign-off.
