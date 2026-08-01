---
article_id: CCT-04-05
writing_contract_version: "native-id-v2"
title: "Motion blur, frame rate, dan shutter pada CCTV"
slug: "motion-blur-frame-rate-dan-shutter-cctv"
description: "Judge whether a proposed camera and configuration can produce useful images in the target scene."
status: draft
publication_date: "2025-08-14"
publication_date_basis: editorial_backfill
date_modified: null
parent_topic: CCT-04
primary_intent: "Tune motion capture tradeoffs for a defined scene."
reader_community: "Tukang.co.id"
reader_address: "Kawan Tukang.co.id"
final_route: "/artikel/motion-blur-frame-rate-dan-shutter-cctv.html"
technical_review: required
sources:
  - "https://webstore.iec.ch/en/publication/7353"
  - "https://webstore.iec.ch/en/publication/59704"
---

# Motion blur, frame rate, dan shutter pada CCTV

Halo, Kawan Tukang.co.id! Kamera dengan megapiksel tinggi belum tentu menghasilkan bukti gerakan yang berguna. Jika objek bergerak cepat sementara shutter terlalu lambat, satu frame dapat tampak berbayang. Jika shutter dipaksa terlalu cepat tanpa cahaya yang cukup, gambar menjadi gelap atau berisik. Frame rate lalu menentukan seberapa sering kamera mengambil sampel gerakan, bukan seberapa tajam setiap sampel.

Jawaban singkatnya: pilih kombinasi shutter, frame rate, cahaya, dan posisi kamera berdasarkan tugas di scene. Untuk membaca wajah orang yang berjalan, konfigurasi berbeda dari memantau kendaraan melintas atau menghitung orang. Spesifikasi kamera dan video contoh hanya titik awal; keputusan akhir perlu observasi pada sudut, jarak, kecepatan, dan kondisi cahaya sasaran. Pedoman aplikasi CCTV menempatkan tujuan scene, pemilihan, pemasangan, commissioning, pengujian, serta evaluasi objektif sebagai rangkaian yang saling terkait, bukan sekadar memilih resolusi ([IEC 62676-4](https://webstore.iec.ch/en/publication/7353)).

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

Motion blur adalah jejak atau pelebaran detail karena objek berpindah selama sensor mengumpulkan cahaya. Shutter (atau exposure time) adalah lamanya tiap frame menerima cahaya; dalam menu kamera sering ditulis sebagai pecahan waktu. Angka shutter yang lebih cepat mempersingkat waktu gerak terekam, tetapi cahaya yang masuk juga berkurang. Shutter yang lebih lambat memberi lebih banyak cahaya, dengan risiko blur lebih besar.

Frame rate, sering ditulis fps (frames per second), adalah jumlah frame per detik. Frame rate lebih tinggi dapat membuat urutan gerakan lebih rapat dan membantu pemutaran, tetapi tidak otomatis menghapus blur pada satu frame. Kamera tetap membutuhkan shutter dan cahaya yang sesuai. Karena itu, pertanyaan “berapa fps terbaik?” tidak dapat dijawab sebelum tugasnya jelas.

Artikel ini membahas keterbacaan gerakan pada kamera dan konfigurasi di scene. Ukuran hard disk, bitrate, dan lama penyimpanan adalah keputusan lain; jangan menyimpulkan kapasitas penyimpanan dari pembahasan ini. Demikian pula, artikel ini tidak menetapkan kepatuhan hukum, desain kelistrikan, atau hasil identifikasi yang dijamin untuk proyek tertentu.

## Cara kerjanya

Bayangkan sensor membuat rangkaian potret singkat. Selama satu potret, tangan, wajah, atau pelat nomor berpindah. Jarak perpindahan selama exposure menentukan seberapa lebar detail menyebar pada frame. Ketika exposure dipersingkat, perpindahan yang terekam per frame mengecil. Namun sensor menerima lebih sedikit cahaya sehingga sistem perlu membuka aperture, menaikkan gain, atau menambah pencahayaan—masing-masing dapat membawa konsekuensi lain seperti depth of field yang berubah, noise, atau sorotan berlebih.

Frame rate bekerja pada jarak waktu antar-potret. Pada fps rendah, kamera melewatkan lebih banyak momen di antara frame sehingga gerakan cepat dapat tampak meloncat. Pada fps tinggi, urutan lebih halus, tetapi setiap frame belum tentu lebih terang atau lebih tajam. Kompresi, fokus, rolling shutter, dan sudut pandang juga dapat memengaruhi hasil yang dilihat operator.

Urutan tuning yang masuk akal adalah: tetapkan tindakan yang harus dibaca; ukur jarak dan arah gerak terhadap kamera; periksa cahaya pada jam operasi; pilih shutter yang menahan blur; lalu tentukan fps yang cukup untuk kontinuitas dan sistem perekaman. Pedoman IEC menekankan persyaratan operasional, scene, pemasangan, commissioning, dan acceptance test yang terdokumentasi sebelum kinerja dinilai ([IEC 62676-4](https://webstore.iec.ch/en/publication/7353)).

Kawan Tukang.co.id, jangan mengubah satu parameter sambil menganggap semua lainnya tetap. Shutter cepat yang diuji siang hari dapat gagal ketika lampu toko diredupkan. Sebaliknya, menaikkan gain agar malam terlihat terang dapat menutupi detail halus dengan noise. Catat setiap perubahan dan bandingkan frame dari kondisi yang sama.

## Faktor yang mengubah hasil

Beberapa faktor berikut harus dibaca sebagai satu paket:

- **Kecepatan dan arah objek.** Gerak melintang bidang gambar biasanya memperlihatkan perpindahan lebih besar daripada gerak mendekati kamera. Kendaraan yang melintas dekat kamera menuntut pengujian lebih ketat daripada orang yang berjalan jauh.
- **Jarak, lensa, dan sudut.** Pembesaran optik dan sudut sempit membuat perpindahan tampak lebih besar pada frame. Posisi kamera yang terlalu tinggi atau miring dapat mengurangi detail wajah, walaupun tidak menimbulkan blur.
- **Cahaya aktual.** Uji pada jam terburuk, termasuk perubahan dari siang ke malam, lampu belakang, pantulan, dan area teduh. Jangan menjadikan video demo vendor sebagai pengganti scene sasaran.
- **Fokus dan stabilitas.** Fokus yang meleset, getaran dudukan, atau kaca pelindung kotor dapat terlihat seperti blur gerakan. Bedakan sumber masalah sebelum mengubah shutter.
- **Tugas dan konsekuensi salah baca.** Melihat arah kerumunan berbeda dari membaca karakter pelat nomor. Jika keluaran dipakai untuk alarm atau keputusan keamanan, definisikan dampak false positive dan false negative serta peran review manusia. Pedoman IEC untuk aplikasi dan klasifikasi objek mengingatkan bahwa label, klip contoh, atau persentase deteksi tidak membuktikan performa pada scene, cuaca, pencahayaan, dan alur respons Anda ([IEC 62676-6](https://webstore.iec.ch/en/publication/59704)).

Jika sebuah kamera memiliki mode auto shutter, minta dokumentasi rentang dan perilakunya, bukan hanya nama fiturnya. Mode otomatis dapat mengorbankan shutter ketika cahaya turun; hasilnya perlu dilihat pada rekaman nyata. Jika kamera menawarkan anti-flicker, pastikan pengaturan itu tidak disalahpahami sebagai penghilang motion blur.

## Contoh keputusan praktis

Gunakan tabel ini sebagai kerangka diskusi, bukan jaminan hasil. Asumsinya adalah kamera telah terpasang pada sudut yang direncanakan dan ada akses untuk mengambil klip uji.

| Tugas scene | Risiko utama | Arah pengujian | Bukti yang dicatat |
|---|---|---|---|
| Orang berjalan menuju pintu | Wajah kabur saat melangkah atau berbalik | Bandingkan shutter lebih cepat pada cahaya operasi; pastikan wajah tetap berada di area piksel yang dibutuhkan | Frame saat masuk, menoleh, dan berhenti |
| Kendaraan melintas melintang | Detail pelat atau bentuk kendaraan melebar | Uji pada kecepatan dan jarak sasaran; periksa sudut kamera dan pantulan lampu | Beberapa lintasan siang dan malam |
| Aktivitas cepat di area kerja | Frame terputus atau detail tertutup noise | Tentukan apakah perlu kontinuitas fps atau ketajaman satu frame; koordinasikan dengan operator | Klip asli, frame pilihan, kondisi cahaya |

Pada setiap skenario, minta pihak yang akan memakai rekaman menyatakan “berguna” itu berarti apa: membaca wajah, membedakan arah, atau sekadar melihat kejadian. Tanpa kriteria tersebut, debat shutter dan fps mudah berubah menjadi perlombaan angka. Sobat Tukang.co.id, simpan juga konfigurasi kamera, waktu uji, posisi, pencahayaan, dan versi firmware agar perubahan berikutnya dapat dibandingkan.

## Kesalahan umum dan cara memeriksanya

**Mengejar fps tertinggi.** Periksa satu frame dari objek bergerak, bukan hanya kelancaran playback. Jika blur tetap ada, fps tambahan belum menyelesaikan akar masalah.

**Mengunci shutter sangat cepat di semua kondisi.** Tanyakan dari mana cahaya tambahan berasal. Jika tidak ada pencahayaan yang memadai, periksa noise, area gelap, dan detail yang hilang pada jam operasi terburuk.

**Menganggap megapiksel mengalahkan gerak.** Resolusi membantu ketika detail memang tertangkap. Ia tidak mengembalikan detail yang sudah menyebar selama exposure atau tidak pernah masuk frame.

**Menguji hanya dengan orang yang berjalan pelan.** Buat variasi kecepatan, arah, pakaian, dan latar yang realistis, tanpa mengklaim hasil mewakili semua kondisi. Untuk fungsi analitik, definisikan corpus atau scene uji, ambang, konsekuensi salah deteksi, dan metode acceptance; spesifikasi vendor saja tidak cukup ([IEC 62676-6](https://webstore.iec.ch/en/publication/59704)).

**Menghapus rekaman uji setelah memilih setelan.** Simpan potongan asli dan catatan perubahan sesuai kebijakan akses dan retensi organisasi. Rekaman CCTV dapat memuat data pribadi; akses, distribusi, dan masa simpan perlu ditinjau oleh pemilik proses dan penasihat privasi yang berwenang. Jangan menaruh salinan uji di perangkat pribadi tanpa dasar dan pengamanan yang jelas.

## Jangan mengandalkan setelan otomatis

Shortcut yang sering terdengar adalah, “Setel 30 fps dan auto shutter; kalau ada masalah nanti dipotong dari video.” Ini gagal ketika frame yang dibutuhkan sudah blur atau terlalu gelap. Pemotongan hanya memilih frame yang ada, bukan menciptakan detail baru. Auto shutter juga dapat berubah mengikuti cahaya dan membuat hasil tidak konsisten antarjam.

Alternatif yang lebih dapat dipertanggungjawabkan adalah menetapkan satu atau dua tugas scene, mengambil klip pada kondisi terburuk yang wajar, lalu membandingkan kombinasi shutter, fps, dan pencahayaan dengan kriteria tertulis. Bila keputusan menyangkut identifikasi, alarm, atau area berisiko, minta technical review dan acceptance test berbasis scene sebelum konfigurasi dianggap selesai. [NEEDS SCENE TEST DATA: jarak, arah/kecepatan objek, cahaya minimum, kriteria “berguna”, dan klip pembanding belum disediakan dalam paket ini.]

## Kesimpulan

Motion blur terutama dikendalikan oleh lamanya exposure relatif terhadap gerak; frame rate mengatur kerapatan urutan, bukan ketajaman otomatis. Kamera dan konfigurasi dapat dianggap memadai hanya setelah tugas, sudut, cahaya, dan gerak sasaran diuji bersama. Kawan Tukang.co.id, langkah berikutnya adalah membuat lembar uji singkat berisi scene, shutter, fps, pencahayaan, frame contoh, dan keputusan lulus atau perlu penyesuaian.

Jangan mengubah hasil uji menjadi janji performa untuk semua lokasi. Untuk langkah lapangan berikutnya, Anda dapat meminta survei melalui [layanan jual dan pasang CCTV di Dau](/kota/jual-pasang-cctv-dau/) atau [layanan jual dan pasang CCTV di Bae](/kota/jual-pasang-cctv-bae/), dengan membawa lembar uji dan kriteria “berguna” yang sudah ditulis. Simpan batas kondisi yang diuji, minta peninjauan teknis untuk fungsi kritis, dan ulangi pengujian bila posisi, cahaya, firmware, atau tujuan penggunaan berubah.
