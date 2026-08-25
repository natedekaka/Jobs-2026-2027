# BAHAN AJAR – PERTEMUAN 1 (S1)
## Apa Itu Algoritma?
*Mengacu pada Panduan Mapel 2025; INFORMATIKA Fase D-F — pendekatan Pembelajaran Mendalam (Memahami → Mengaplikasi → Merefleksi)*

| Informasi | Keterangan |
|---|---|
| **Fase / Kelas** | F / Kelas XI |
| **Alokasi Waktu** | 5 JP × 45 menit (225 menit) |
| **Elemen CP** | Berpikir Komputasional (BK) |
| **Tujuan Pembelajaran** | Mendefinisikan algoritma, menjelaskan 5 ciri algoritma baik, mengenali algoritma dalam kehidupan sehari-hari, menulis serta mengevaluasi algoritma sederhana |
| **Materi Prasyarat** | Tidak ada (materi pembuka semester) |

---

## A. Kisah Pemantik 🎬

> **"Algoritma Mie Instan"**
>
> Saat istirahat, Raka ingin membuat mie instan. Ia menuangkan air panas lebih dulu, lalu memasukkan bumbu, baru terakhir memasukkan mie. Hasilnya? Mie menggumpal dan bumbu tidak tercampur! Sementara itu, temannya mengikuti urutan: masukkan mie, masukkan bumbu, tuang air panas, diamkan 3 menit, lalu aduk. Mienya sempurna!
>
> **Pertanyaan pemantik:** Mengapa hasil dua orang yang membuat makanan yang sama bisa berbeda hanya karena urutan langkahnya berbeda? Apa hubungannya dengan cara komputer menjalankan perintah?

---

## B. Definisi Algoritma

**Algoritma** adalah urutan langkah-langkah logis, sistematis, dan terbatas untuk menyelesaikan suatu masalah. Kata "algoritma" berasal dari nama ilmuwan Muslim Persia, **Al-Khawarizmi** (780–850 M), penulis buku tentang perhitungan matematika (`Al-Jabr wa al-Muqabala`).

| Istilah | Arti | Contoh |
|---|---|---|
| **Algoritma** | Urutan langkah logis untuk menyelesaikan masalah | Resep, petunjuk arah |
| **Instruksi** | Satu perintah tunggal | "Tambahkan gula" |
| **Program** | Algoritma yang ditulis dalam bahasa pemrograman | Kode Python/Java |

> 💡 **Ingat:** Semua orang sudah menjalankan algoritma setiap hari tanpa sadar — dari bangun tidur, menyikat gigi, hingga membeli jajan. Komputer hanyalah mesin yang menjalankan algoritma jauh lebih cepat.

---

## C. Ciri-Ciri Algoritma yang Baik

| No | Ciri | Arti | Contoh (Mie Instan) |
|---|---|---|---|
| 1 | **Input** | Memiliki data masukan (boleh nol) | Air, mie, bumbu, panci, kompor |
| 2 | **Output** | Menghasilkan keluaran yang jelas | Mie matang siap saji |
| 3 | **Definite** | Setiap langkah jelas, tidak ambigu | "Rebus air hingga mendidih", bukan "Panaskan air" |
| 4 | **Finite** | Berhenti setelah sejumlah langkah | Ada akhir: "Sajikan", bukan "Ulangi terus" |
| 5 | **Effective** | Langkah dapat dikerjakan | Bisa dilakukan dengan alat yang tersedia |

Jika salah satu ciri tidak terpenuhi, urutan tersebut **bukan algoritma yang baik**.

---

## D. Algoritma Baik vs Algoritma Buruk

**Algoritma Baik — Membuat Teh Manis ✅**
1. Siapkan gelas, teh celup, gula, dan air panas
2. Masukkan teh celup ke dalam gelas
3. Tuang air panas ke gelas
4. Diamkan selama 3 menit
5. Angkat teh celup dari gelas
6. Masukkan gula sesuai selera (1–2 sendok)
7. Aduk hingga gula larut
8. Teh siap diminum

**Algoritma Buruk — Membuat Teh Manis ❌**
1. Siapkan bahan
2. Masak air
3. Campurkan
4. Sajikan

**Analisis:** Algoritma buruk tidak *definite* (berapa banyak air? gula berapa sendok? "masak air" sampai apa?), tidak jelas output-nya, sehingga dua orang akan menghasilkan teh yang berbeda.

---

## E. Algoritma di Berbagai Bidang & Cara Mengevaluasi

| Bidang | Contoh Algoritma |
|---|---|
| Memasak | Resep masakan — urutan langkah memasak |
| Transportasi | Petunjuk arah — jalan lurus, belok kiri, sampai tujuan |
| Teknologi | Login aplikasi — buka browser, isi username/password, klik login |
| Kesehatan | Cuci tangan 6 langkah — urutan spesifik untuk hasil maksimal |
| Ekonomi | Kasir — hitung subtotal, hitung pajak, hitung kembalian |

**Langkah mengevaluasi algoritma (milik sendiri atau teman):**
1. **Langkah lengkap?** Apakah ada langkah yang terlewat?
2. **Urutan logis?** Jika ditukar, apakah hasilnya tetap sama?
3. **Bahasa jelas?** Apakah orang lain bisa mengikuti dengan mudah?
4. **Efisien?** Adakah langkah yang bisa dihilangkan tanpa mengurangi hasil?
5. **Hasil sesuai?** Jika dijalankan, apakah menghasilkan output yang diharapkan?

---

## F. Contoh Soal & Penyelesaian 📝

**Contoh 1:** Apakah perbedaan algoritma dengan instruksi biasa?
**Jawaban:** Algoritma adalah kumpulan instruksi yang tersusun logis, sistematis, terbatas, dan menghasilkan output untuk menyelesaikan satu masalah. Instruksi biasa hanya satu perintah terpisah; algoritma menyatukannya menjadi satu kesatuan yang utuh dengan awal dan akhir.

**Contoh 2:** Sebutkan 5 ciri algoritma yang baik beserta contoh singkat masing-masing!
**Jawaban:** 1) **Input** — mie, air, bumbu; 2) **Output** — mie matang; 3) **Definite** — "tuang 250 ml air", bukan "tuang air secukupnya"; 4) **Finite** — berakhir di langkah "sajikan"; 5) **Effective** — dapat dikerjakan dengan kompor dan panci.

**Contoh 3:** Berikut algoritma "Menggosok Gigi": ambil sikat, oleskan pasta, sikat gigi, bilas mulut, simpan sikat. Apakah sudah memenuhi 5 ciri?
**Jawaban:** Belum sempurna — langkah belum *definite* (berapa lama menyikat? pasta sebanyak apa?), dan tidak ada langkah "buka tutup pasta". Perlu diperbaiki dengan menambah detail: "sikat gigi selama 2 menit" dan "keluarkan pasta secukupnya (sebesar biji jagung)".

**Contoh 4:** Buat algoritma "Membeli Buku di Toko" minimal 6 langkah!
**Jawaban:** 1) Siapkan uang; 2) Berangkat ke toko buku; 3) Pilih buku yang diinginkan; 4) Bawa buku ke kasir; 5) Serahkan uang dan terima kembalian; 6) Ucapkan terima kasih lalu pulang.

---

## G. Miskonsepsi / Kesalahan Umum 🚫

| Miskonsepsi | Fakta yang Benar |
|---|---|
| "Semua urutan langkah adalah algoritma" | Urutan tanpa tujuan/logika atau tanpa akhir **bukan** algoritma |
| "Algoritma harus pakai komputer" | Algoritma bisa ditulis dan dijalankan tanpa komputer (resep, petunjuk) |
| "Urutan tidak penting" | Mengubah urutan bisa mengubah hasil secara drastis |
| "Algoritma harus rumit" | Algoritma terbaik justru paling sederhana dan efisien |
| "Algoritma = program" | Algoritma adalah logika; program adalah algoritma dalam bahasa kode |

---

## H. Tantangan Praktik (Mengaplikasi) 🎯

**Tantangan 1 — Tulis Algoritma (mudah):** Tulis algoritma salah satu kegiatan berikut minimal 5 langkah: membuat kopi, mengecas HP, atau membeli pulsa.

**Tantangan 2 — Tebak Algoritma (sedang):** Tulis algoritma "cuci tangan 6 langkah" tanpa judul, lalu berikan kepada teman. Teman harus menebak kegiatan apa yang kamu tulis.

**Tantangan 3 — Evaluasi (sulit):** Evaluasi algoritma temanmu berdasarkan 5 ciri. Tandai ciri yang kurang dan sarankan perbaikan spesifik.

**Tantangan 4 — Fingerprint Algoritma (paling sulit):** Tulis algoritma "menggambar rumah" di selembar kertas. Berikan ke pasanganmu yang harus menggambar hanya dari teks algoritmamu — tanpa melihat gambar asli. Bandingkan hasilnya: apakah persis sama?

---

## I. Rangkuman Kunci 🔑

- **Algoritma** = urutan langkah logis, sistematis, dan terbatas untuk menyelesaikan masalah.
- Nama "algoritma" berasal dari **Al-Khawarizmi**.
- 5 ciri algoritma baik: **Input, Output, Definite, Finite, Effective**.
- Algoritma ada di mana-mana: resep, petunjuk arah, login aplikasi, cuci tangan.
- Evaluasi algoritma: lengkap → logis → jelas → efisien → hasil sesuai.
- Algoritma ≠ program; program adalah algoritma yang sudah dikodekan.

---

## J. Glosarium 📖

| Istilah | Arti |
|---|---|
| **Algoritma** | Urutan langkah logis untuk menyelesaikan masalah |
| **Definite** | Setiap langkah jelas dan tidak bermakna ganda |
| **Finite** | Berhenti setelah sejumlah langkah tertentu |
| **Effective** | Langkah-langkahnya dapat benar-benar dikerjakan |
| **Input** | Data masukan yang diproses algoritma |
| **Output** | Hasil keluaran yang dihasilkan algoritma |

---

## K. Refleksi (Merefleksi) 🔍

- Konsep apa yang paling penting kamu pelajari hari ini?
- Bagaimana konsep algoritma terhubung dengan kehidupan sehari-harimu?
- Bagian mana yang masih sulit dipahami?
- **Skala pemahaman diri:** ____/10
- Apa yang ingin kamu pelajari lebih lanjut tentang algoritma?

---

**MGMP Informatika SMAN 6 Cimahi — Fase F (Kelas XI) Semester 1**