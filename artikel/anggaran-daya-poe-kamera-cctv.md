---
article_id: CCT-06-03
title: "Menghitung anggaran daya PoE untuk kamera CCTV"
slug: "anggaran-daya-poe-kamera-cctv"
description: "Plan CCTV connectivity, addressing, bandwidth, time, segmentation, and network-delivered power."
status: draft
writing_contract_version: "native-id-v2"
publication_date: "2025-09-23"
publication_date_basis: editorial_backfill
date_modified: null
parent_topic: CCT-06
primary_intent: "Verify switch and injector capacity across operating conditions."
reader_community: "Tukang.co.id"
reader_address: "Teman Tukang.co.id"
final_route: "/artikel/anggaran-daya-poe-kamera-cctv.html"
technical_review: required
sources:
  - "https://webstore.iec.ch/en/publication/63699"
---

# Menghitung anggaran daya PoE untuk kamera CCTV

Halo, Teman Tukang.co.id! Jangan memilih switch PoE hanya karena jumlah portnya cukup. Keputusan yang benar membandingkan kebutuhan daya setiap kamera pada kondisi terberat dengan anggaran daya switch atau injector, lalu menyisakan cadangan yang disepakati. Jika salah satu angka itu belum ada di lembar data atau survei, hasilnya belum layak disebut perhitungan final.

Rumus kerjanya sederhana: jumlahkan kebutuhan maksimum kamera dan perangkat PoE lain yang benar-benar akan diberi daya, kemudian bandingkan dengan anggaran daya (power budget) perangkat sumber. Periksa juga batas per-port, kelas PoE yang dinegosiasikan, rugi kabel pada rute nyata, suhu, dan perubahan seperti pemanas atau lampu inframerah yang aktif. [NEEDS PROJECT EVIDENCE: kelas PoE, daya maksimum tiap perangkat, rute/kabel, anggaran switch atau injector, dan cadangan yang disetujui.] Batas keselamatan dan verifikasi instalasi listrik tetap memerlukan rancangan kompeten; IEC 60364-1 menempatkan perlindungan, pemisahan, verifikasi, dan perubahan sistem sebagai bagian yang harus ditinjau, bukan disimpulkan dari angka budget saja ([IEC 60364-1](https://webstore.iec.ch/en/publication/63699)).

![Ilustrasi CCTV Merk ZKTECO](/wp-content/uploads/2023/08/CCTV-Merk-ZKTECO.jpg)


*Aset lokal situs; gambar ini bukan dokumentasi proyek tertentu.*

## Definisi dan batas objek

Power over Ethernet (PoE) mengirim data dan daya melalui kabel jaringan ke kamera atau perangkat yang kompatibel. Dalam artikel ini, “anggaran daya” berarti kemampuan sumber PoE menyediakan daya pada seluruh port yang direncanakan, bukan konsumsi listrik gedung dari panel utama. Mains, UPS, ukuran pengaman, dan waktu cadangan baterai berada di pembahasan kelistrikan terpisah.

Objek yang dihitung adalah kamera, pemanas, iluminator inframerah, mikrofon, motor pan-tilt-zoom, atau aksesori lain yang mengambil daya dari port. Jangan memasukkan perangkat yang mendapat catu daya lokal ke total PoE, tetapi tetap catat agar tidak keliru saat uji penerimaan. Kawan Tukang.co.id, bedakan tiga angka: batas per-port, total anggaran perangkat sumber, dan kebutuhan aktual perangkat. Ketiganya bisa berbeda.

## Cara kerjanya

Mulailah dari daftar perangkat, bukan dari merek switch. Untuk setiap kamera, salin identitas model, kelas PoE, daya tipikal, dan daya maksimum dari datasheet atau manual yang berlaku. Jika kamera punya beberapa mode, gunakan angka pada mode yang memang akan dipakai—misalnya malam dengan inframerah—bukan angka demo siang hari. Simpan versi dokumen dan tanggal pemeriksaannya.

Gunakan lembar hitung berikut:

`Total maksimum = Σ (daya maksimum kamera + aksesori yang ditenagai PoE)`

`Kapasitas tersisa = anggaran daya sumber − total maksimum`

Perbandingan dilakukan dua kali. Pertama, setiap beban harus berada di bawah batas per-port dan kelas PoE yang didukung port tersebut. Kedua, jumlah seluruh beban harus berada di bawah anggaran total switch atau injector. “Port masih kosong” hanya menjawab kapasitas jumlah koneksi, bukan kapasitas watt.

Setelah itu, cocokkan media fisik: kategori kabel, panjang aktual, sambungan, patch panel, lingkungan, dan cara pemasangan. Jangan mengubah rugi kabel menjadi angka buatan tanpa data pabrikan atau pengukuran. Minta teknisi jaringan dan kelistrikan menyepakati asumsi, titik uji, label, serta gambar as-built sebelum sistem dinyatakan siap.

## Faktor yang mengubah hasil

Beberapa hal sering membuat total berubah setelah pemasangan:

- **Mode kamera.** Inframerah, pemanas, audio, analitik, atau motor dapat menaikkan kebutuhan dibanding mode dasar. Periksa maksimum, bukan hanya tipikal.
- **Kelas dan negosiasi.** Port sumber dan kamera harus memiliki kelas yang kompatibel. Logo atau tulisan “PoE” tanpa identitas kelas tidak cukup untuk menyimpulkan interoperabilitas.
- **Kabel dan rute.** Panjang, temperatur, bundel, konektor, dan kualitas terminasi memengaruhi tegangan yang sampai ke perangkat. Catat rute aktual dan uji sesuai prosedur yang disetujui.
- **Cadangan.** Cadangan bukan angka universal. Tetapkan berdasarkan perubahan yang mungkin, ekspansi, toleransi data pabrikan, dan kebijakan pemilik, lalu tulis siapa yang menyetujuinya.
- **Perubahan sistem.** Penambahan kamera, penggantian firmware, atau aksesori baru memicu hitung ulang. Anggaran lama tidak otomatis berlaku untuk konfigurasi baru.

Sobat Tukang.co.id, jangan memakai hasil hitung sebagai bukti keselamatan listrik, ketahanan jaringan, retensi rekaman, atau failover. IEC 60364-1 membedakan kebutuhan desain dan verifikasi sistem dari satu label kapasitas; pemeriksaan lapangan dan dokumen produk tetap diperlukan.

## Contoh keputusan praktis

Bayangkan daftar awal berisi enam kamera. Empat memakai daya maksimum `P1`, dua lainnya `P2` karena memiliki aksesori tambahan. Total desain adalah `4 × P1 + 2 × P2`. Jika satu port dicadangkan untuk aksesori jaringan, masukkan aksesori itu hanya bila benar-benar mendapat daya dari switch. Lalu bandingkan total dengan anggaran sumber dan setiap `P1`/`P2` dengan batas port.

Ada tiga hasil yang mungkin:

| Hasil pemeriksaan | Keputusan |
| --- | --- |
| Total dan semua port berada di bawah batas, dengan cadangan terdokumentasi | Lanjutkan ke verifikasi kabel, konfigurasi, dan uji beban sesuai metode proyek. |
| Total aman, tetapi satu port atau kelas tidak cocok | Ganti port/perangkat atau gunakan sumber PoE yang kompatibel; jangan mengandalkan port kosong. |
| Angka maksimum, rute kabel, atau cadangan belum terbukti | Tahan keputusan pembelian dan tandai `[NEEDS TECHNICAL REVIEW: identitas model, datasheet, rute, dan metode uji]`. |

Contoh ini hanya menunjukkan cara menyusun keputusan. Ia bukan bukti bahwa kamera, switch, atau kabel tertentu akan lolos di lokasi Anda.

## Kesalahan umum dan cara memeriksanya

Kesalahan paling mahal adalah mengalikan jumlah kamera dengan satu angka “watt per kamera” dari perkiraan. Periksa lembar data setiap model, termasuk keadaan maksimum dan aksesori. Kesalahan lain adalah memakai angka budget pada kotak tanpa memastikan apakah itu anggaran keluaran PoE atau konsumsi internal perangkat. Minta definisi istilah tersebut dari produsen.

Jangan menjumlahkan angka tipikal lalu menyebutnya cadangan. Tandai sumber setiap angka: datasheet, label perangkat, survei, atau hasil uji. Cocokkan nomor model dan revisi firmware; bukti untuk perangkat yang mirip bukan bukti untuk perangkat yang dikirim. Simpan tabel per-port, foto label, hasil uji, dan gambar as-built agar perubahan dapat ditelusuri.

Shortcut “switch 16 port pasti kuat untuk 16 kamera” gagal karena port dan anggaran total adalah batas yang berbeda. Shortcut “tes kamera menyala berarti selesai” juga gagal: kamera dapat menyala saat beban ringan tetapi tidak membuktikan mode maksimum, kabel, atau perubahan konfigurasi. Alternatif yang lebih aman adalah uji terencana pada kondisi operasi yang disepakati dan minta tinjauan teknis ketika data inti belum lengkap.

## Kesimpulan

Anggaran daya PoE dihitung dengan menjumlahkan kebutuhan maksimum semua beban PoE, memeriksa batas setiap port dan kelasnya, lalu membandingkan total itu dengan anggaran switch atau injector serta cadangan yang terdokumentasi. Sebelum membeli atau mengaktifkan sistem, lengkapi daftar model, datasheet terkini, rute dan jenis kabel, asumsi mode operasi, serta metode uji. [NEEDS COORDINATOR REVIEW: validasi angka proyek dan persetujuan desain jaringan/kelistrikan.] Aturan praktisnya: tanpa identitas perangkat dan bukti kondisi terberat, hasil perhitungan adalah perkiraan—bukan persetujuan instalasi.

Jika tinjauan lapangan diperlukan, siapkan tabel tersebut untuk teknisi setempat, misalnya melalui layanan [jual-pasang CCTV Sumba Barat Daya](/kota/jual-pasang-cctv-sumba-barat-daya/) atau [jual-pasang CCTV Maluku Barat Daya](/kota/jual-pasang-cctv-maluku-barat-daya/). Rute itu hanya langkah mencari bantuan; keputusan teknis tetap bergantung pada survei dan bukti proyek.

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
