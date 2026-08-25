# BAHAN AJAR – PERTEMUAN 2 (S1)
## Dekomposisi
*Mengacu pada Panduan Mapel 2025; INFORMATIKA Fase D-F — pendekatan Pembelajaran Mendalam (Memahami → Mengaplikasi → Merefleksi)*

| Informasi | Keterangan |
|---|---|
| **Fase / Kelas** | F / Kelas XI |
| **Alokasi Waktu** | 5 JP × 45 menit (225 menit) |
| **Elemen CP** | Berpikir Komputasional (BK) |
| **Tujuan Pembelajaran** | Mendefinisikan dekomposisi, menjelaskan manfaatnya, menguraikan masalah kompleks menjadi sub-masalah, dan memilih strategi dekomposisi yang efektif |
| **Materi Prasyarat** | Pertemuan 1 — Algoritma dan ciri-cirinya |

---

## A. Kisah Pemantik 🎬

> **"Sepiring Nasi"**
>
> Coba bayangkan kamu harus menghabiskan sepiring nasi dalam **satu suapan**. Mustahil! Kamu akan tersedak. Cara cerdasnya? Makan satu sendok kecil, lalu satu sendok lagi, sampai piring habis.
>
> **Pertanyaan pemantik:** Masalah besar apa yang pernah kamu hadapi yang terasa mustahil sampai kamu memecahnya menjadi bagian-bagian kecil? Bagaimana cara komputer memecah masalah raksasa seperti "mengadakan olimpiade sekolah"?

---

## B. Definisi & Manfaat Dekomposisi

**Dekomposisi** adalah teknik memecah masalah kompleks menjadi bagian-bagian kecil yang lebih mudah dikelola dan diselesaikan. Dekomposisi merupakan **pilar pertama** dari 4 pilar berpikir komputasional (Computational Thinking).

| Manfaat | Penjelasan |
|---|---|
| **Lebih ringan** | Masalah besar terasa jauh lebih mudah jika sudah dipecah |
| **Bisa paralel** | Sub-masalah bisa dikerjakan orang berbeda secara bersamaan |
| **Mudah dilacak** | Jika gagal, kita langsung tahu bagian mana yang salah |
| **Fokus** | Setiap bagian dikerjakan dengan konsentrasi penuh |
| **Kolaborasi** | Cocok untuk kerja tim — setiap orang punya tanggung jawab jelas |

> 💡 **Rumus 3 detik:** BESAR → KECIL → SELESAIKAN SATU PER SATU.

---

## C. Contoh Dekomposisi

**1. Travel Planning (Liburan)**
| Sub-Masalah | Detail |
|---|---|
| Tentukan tujuan & tanggal | Riset destinasi, cek kalender libur |
| Cari transportasi | Bandingkan harga tiket pesawat/kereta |
| Pesan akomodasi | Cek hotel, booking via aplikasi |
| Siapkan dokumen | Paspor, visa, asuransi perjalanan |
| Packing barang | Daftar pakaian, obat-obatan, elektronik |
| Atur anggaran | Hitung total biaya, siapkan dana darurat |

**2. Membuat Aplikasi Ojek Online**
| Sub-Masalah | Tim yang Bertanggung Jawab |
|---|---|
| Fitur pemesanan | Developer backend |
| Pembayaran digital | Developer payment gateway |
| Tracking driver | Developer GPS & maps |
| Registrasi pengguna | Developer autentikasi |
| Desain UI/UX | Designer |
| Marketing | Tim marketing |

**3. Mengadakan Class Meeting**
| Sub-Masalah |
|---|
| Menentukan jenis lomba |
| Membagi panitia (per lomba) |
| Menyiapkan peralatan |
| Menentukan jadwal |
| Mengelola anggaran |
| Dokumentasi & publikasi |

---

## D. Dekomposisi vs Algoritma

| Aspek | Dekomposisi | Algoritma |
|---|---|---|
| Fungsi | Memecah masalah | Menyusun langkah |
| Output | Sub-masalah yang lebih kecil | Urutan langkah |
| Hubungan | Dilakukan pertama | Dilakukan setelah dekomposisi |

**Urutan yang benar:** Identifikasi masalah → **Dekomposisi** → Algoritma untuk setiap sub-masalah.

---

## E. Dekomposisi dalam Masalah Nyata — Strategi Efektif

Saat menyelesaikan masalah nyata, berpikir komputasional menuntut kita **memilih strategi yang efektif dan efisien**. Contoh: kamu punya **5 tugas** dengan durasi berbeda dan hanya punya waktu **6 jam** sebelum semuanya dikumpulkan.

| Tugas | A | B | C | D | E |
|---|---|---|---|---|---|
| Durasi (jam) | 3 | 1 | 2 | 1,5 | 2,5 |

**Strategi:** urutkan tugas dari durasi **terkecil** → B(1), D(1,5), C(2), E(2,5), A(3). Ambil berturut-turut selama total ≤ 6 jam: **B + D + C = 4,5 jam**, lalu E(2,5) tidak muat lagi. Jadi maksimal **3 tugas** selesai. Inilah kekuatan dekomposisi: memecah masalah "6 jam untuk semua tugas" menjadi "pilih tugas mana yang paling menguntungkan".

---

## F. Contoh Soal & Penyelesaian 📝

**Contoh 1:** Jelaskan apa yang dimaksud dekomposisi dan berikan 2 contoh!
**Jawaban:** Dekomposisi adalah memecah masalah besar menjadi bagian kecil yang lebih mudah diselesaikan. Contoh: (1) mengadakan class meeting dipecah menjadi menentukan lomba, panitia, peralatan, jadwal, anggaran, dokumentasi; (2) membuat aplikasi ojek online dipecah menjadi fitur pemesanan, pembayaran, tracking, dan desain.

**Contoh 2:** Sebutkan 3 manfaat dekomposisi!
**Jawaban:** (1) masalah lebih ringan dikerjakan; (2) sub-masalah bisa dikerjakan paralel oleh banyak orang; (3) mudah melacak kesalahan karena kita tahu bagian mana yang bermasalah.

**Contoh 3:** Dekomposisikan "Membangun startup edukasi online" menjadi 6 sub-masalah!
**Jawaban:** 1) riset pasar & kurikulum; 2) pengembangan platform (web/app); 3) pembuatan konten & materi; 4) sistem pembayaran; 5) tim pemasaran & promosi; 6) layanan pelanggan & evaluasi.

**Contoh 4:** Apa perbedaan dekomposisi dengan algoritma? Mana yang dilakukan lebih dulu?
**Jawaban:** Dekomposisi memecah masalah menjadi sub-masalah; algoritma menyusun langkah untuk tiap sub-masalah. **Dekomposisi dilakukan lebih dulu**, baru kemudian disusun algoritma untuk setiap bagian.

**Contoh 5:** Mengapa dekomposisi penting dalam kerja tim?
**Jawaban:** Karena dengan memecah masalah, setiap anggota tim mendapat tanggung jawab yang jelas dan dapat mengerjakan bagiannya secara paralel, sehingga seluruh pekerjaan selesai lebih cepat.

---

## G. Miskonsepsi / Kesalahan Umum 🚫

| Miskonsepsi | Fakta yang Benar |
|---|---|
| "Dekomposisi = membagi tugas ke orang lain" | Membagi tugas adalah salah satu hasilnya, tapi intinya adalah **memecah masalah**, bukan sekedar membagi kerja |
| "Dekomposisi sama dengan algoritma" | Dekomposisi memecah masalah, algoritma menyusun langkah; keduanya berbeda pilar CT |
| "Semakin banyak sub-masalah semakin baik" | Dekomposisi yang baik berhenti saat tiap bagian sudah mudah dikerjakan |
| "Dekomposisi harus dilakukan sendirian" | Dekomposisi justru mendorong kolaborasi dan eksekusi paralel |

---

## H. Tantangan Praktik (Mengaplikasi) 🎯

**Tantangan 1 — Class Meeting (mudah):** Dekomposisikan "mengadakan class meeting" menjadi 6 sub-masalah beserta penanggung jawabnya.

**Tantangan 2 — Urutkan Angka (sedang):** Urutkan `9 8 2 7 5 6` dari kecil ke besar dengan 2 cara: (A) Bubble Sort — bandingkan lalu tukar; (B) Selection Sort — cari terkecil lalu taruh di depan. Hitung berapa kali tukar masing-masing dan pilih yang paling efektif.

**Tantangan 3 — Startup Edukasi (sulit):** Dekomposisikan "membangun startup edukasi online" dalam tabel berisi 6 sub-masalah + tim yang bertanggung jawab. Jelaskan mengapa pembagian per tim lebih efektif.

**Tantangan 4 — Mengerjakan PR (paling sulit):** Kamu punya 5 tugas dengan durasi 3, 1, 2, 1,5, dan 2,5 jam serta waktu hanya 6 jam. Pilih kombinasi tugas yang menghasilkan jumlah tugas maksimal dan jelaskan strategi yang kamu gunakan.

---

## I. Rangkuman Kunci 🔑

- **Dekomposisi** = memecah masalah besar menjadi bagian-bagian kecil yang mudah diselesaikan.
- Dekomposisi adalah **pilar pertama** dari 4 pilar Computational Thinking.
- Manfaat: ringan, paralel, mudah dilacak, fokus, dan mendorong kolaborasi.
- Dekomposisi dilakukan **SEBELUM** menyusun algoritma.
- Berpikir komputasional menuntut pemilihan strategi yang **efektif dan efisien**.

---

## J. Glosarium 📖

| Istilah | Arti |
|---|---|
| **Dekomposisi** | Memecah masalah kompleks menjadi sub-masalah kecil |
| **Computational Thinking** | Cara berpikir untuk menyelesaikan masalah seperti cara komputer |
| **Sub-masalah** | Bagian kecil dari masalah yang sudah dipecah |
| **Paralel** | Mengerjakan banyak bagian secara bersamaan |
| **Bubble Sort** | Mengurutkan dengan membandingkan dan menukar dua angka |
| **Selection Sort** | Mengurutkan dengan memilih angka terkecil lalu menaruhnya di depan |

---

## K. Refleksi (Merefleksi) 🔍

- Konsep apa yang paling penting kamu pelajari hari ini?
- Bagaimana dekomposisi membantu tim menyelesaikan masalah?
- Bagian mana yang masih sulit dipahami?
- **Skala pemahaman diri:** ____/10
- Apa yang ingin kamu pelajari lebih lanjut tentang dekomposisi?

---

**MGMP Informatika SMAN 6 Cimahi — Fase F (Kelas XI) Semester 1**