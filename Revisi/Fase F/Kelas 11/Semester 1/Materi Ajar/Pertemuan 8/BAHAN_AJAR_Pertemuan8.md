# BAHAN AJAR – PERTEMUAN 8 (S1)
## Flowchart — Perulangan
*Mengacu pada Panduan Mapel 2025; INFORMATIKA Fase D-F — pendekatan Pembelajaran Mendalam (Memahami → Mengaplikasi → Merefleksi)*

| Informasi | Keterangan |
|---|---|
| **Fase / Kelas** | F / Kelas XI |
| **Alokasi Waktu** | 5 JP × 45 menit (225 menit) |
| **Elemen CP** | Algoritma dan Pemrograman (AP) |
| **Tujuan Pembelajaran** | Menjelaskan konsep perulangan, menggambar flowchart FOR dan WHILE, membuat loop bersarang, dan menerapkan akumulasi (running total) |
| **Materi Prasyarat** | Pertemuan 5–7 — Simbol flowchart, urutan, dan percabangan |

---

## A. Kisah Pemantik 🎬

> **"Penjaga Keamanan yang Berkeliling"**
>
> Pak Dedi berkeliling area sekolah dari jam 07.00 sampai 15.00: ia berjalan mengelilingi halaman, kembali ke pos, lalu mengelilingi lagi. Ia tidak menulis 8 kali perintah "kelilingi halaman" — cukup satu perintah yang **diulang** sampai jam menunjukkan waktu pulang. Ini persis cara komputer menangani pekerjaan berulang.
>
> **Pertanyaan pemantik:** Pekerjaan berulang apa yang kamu lakukan setiap hari? Apakah lebih efisien menulisnya sekali lalu mengulang, atau menuliskannya berkali-kali?

---

## B. Konsep Perulangan (Loop)

**Perulangan** memungkinkan algoritma menjalankan blok instruksi **berulang kali**. Dalam flowchart, perulangan digambarkan dengan **panah kembali** ke langkah sebelumnya (back loop) atau memeriksa kembali kondisi pada belah ketupat.

**Jenis Perulangan:**
| Jenis | Ciri | Kapan Digunakan |
|---|---|---|
| **FOR** | Jumlah perulangan sudah diketahui | Cetak 1–10 → 10 kali |
| **WHILE** | Berhenti berdasarkan kondisi | Ulangi sampai tebakan benar |
| **Repeat-Until** | Dijalankan minimal sekali | do...while (jarang di flowchart dasar) |

> 💡 **Bahaya:** jika kondisi tidak pernah menjadi salah, perulangan tidak pernah berhenti — disebut **infinite loop**. Selalu pastikan ada langkah yang mengubah kondisi!

---

## C. Flowchart FOR Loop

**Contoh 1 — Cetak 1–5:**
```
┌─────────┐
│  START  │
└────┬────┘
     ▼
┌──────────┐
│  i = 1   │
└────┬─────┘
     ▼
   ┌────────────┐
   │  i <= 5?   │◀──────────┐
   └──┬─────┬───┘           │
    Ya│     │Tidak          │
      ▼     ▼               │
┌────────┐ ┌────────┐       │
│OUTPUT i│ │  END   │       │
└───┬────┘ └────────┘       │
    ▼                       │
┌───────────┐               │
│ i = i + 1 │───────────────┘
└───────────┘
```

**Contoh 2 — Cetak Bilangan Genap 2–10:** i mulai dari 2, tambah 2 setiap loop: 2, 4, 6, 8, 10.

---

## D. Flowchart WHILE Loop

**Contoh 3 — Hitung Mundur:**
Start → input n → `n > 0?` → Ya → output n → n = n − 1 → kembali ke kondisi `n > 0?`; Tidak → output "Go!" → End.

**Contoh 4 — Tebak Angka:**
Start → komputer = random 1–10 → input tebakan → `tebakan != komputer?` → Ya → input tebakan lagi → kembali; Tidak → output "Benar!" → End. (Ini WHILE: berhenti saat tebakan benar.)

---

## E. Akumulasi (Running Total)

**Contoh 5 — Jumlah 1–100:**
Start → total = 0 → i = 1 → `i <= 100?` → Ya → total = total + i → i = i + 1 → kembali; Tidak → output total → End. Hasil: **5050**.

**Contoh 6 — Rata-rata N Nilai:**
Start → input n → total = 0 → i = 1 → `i <= n?` → Ya → input nilai → total = total + nilai → i = i + 1 → kembali; Tidak → rata = total / n → output rata → End.

**Contoh 7 — Faktorial n!:** Start → input n → faktorial = 1 → i = 1 → `i <= n?` → Ya → faktorial = faktorial × i → i = i + 1 → kembali; Tidak → output faktorial → End. Tracing: n=5 → 1×2×3×4×5 = **120**.

---

## F. Loop Bersarang (Nested Loop)

**Contoh 8 — Tabel Perkalian 3×3:**
Start → baris = 1 → `baris <= 3?` → Ya → kolom = 1 → `kolom <= 3?` → Ya → hitung = baris × kolom → output hitung → kolom = kolom + 1 → kembali ke kondisi kolom; Tidak → baris = baris + 1 → kembali ke kondisi baris; Tidak → End.

**Cara membacanya:** untuk setiap baris, jalankan seluruh kolom. Total iterasi = 3 × 3 = **9 kali**.

---

## G. Contoh Soal & Penyelesaian 📝

**Contoh 1:** Buat flowchart mencetak bilangan ganjil 1–19!
**Jawaban:** Start → i = 1 → `i <= 19?` → Ya → output i → i = i + 2 → kembali; Tidak → End. Output: 1, 3, 5, ..., 19.

**Contoh 2:** Buat flowchart menghitung jumlah bilangan genap 1–50!
**Jawaban:** Start → total = 0 → i = 2 → `i <= 50?` → Ya → total = total + i → i = i + 2 → kembali; Tidak → output total → End. Hasil = 2+4+...+50 = **650**.

**Contoh 3:** Buat flowchart menghitung faktorial n! (n × (n−1) × ... × 1)!
**Jawaban:** Start → input n → faktorial = 1 → i = 1 → `i <= n?` → Ya → faktorial = faktorial × i → i = i + 1 → kembali; Tidak → output faktorial → End. Tracing: 6! = **720**.

**Contoh 4:** Buat flowchart mencetak pola bintang segitiga siku-siku (3 baris)!
**Jawaban:** Start → baris = 1 → `baris <= 3?` → Ya → kolom = 1 → `kolom <= baris?` → Ya → output "*" → kolom = kolom + 1 → kembali; Tidak → baris = baris + 1 → kembali; Tidak → End. Output: `*`, `**`, `***`.

**Contoh 5:** Buat flowchart menu: pilih 1–4, ulang sampai pilih 4 (keluar)!
**Jawaban:** Start → output menu → input pilihan → `pilihan == 4?` → Tidak → jalankan proses sesuai pilihan → kembali ke output menu; Ya → output "Terima kasih" → End. (Pola WHILE berbasis menu.)

---

## H. Miskonsepsi / Kesalahan Umum 🚫

| Miskonsepsi / Kesalahan | Fakta yang Benar |
|---|---|
| Lupa update counter (i = i + 1) | Tanpa update, loop tidak pernah berhenti (infinite) |
| FOR dan WHILE tidak dibedakan | FOR: jumlah pasti; WHILE: berdasarkan kondisi |
| Kondisi salah arah (menggunakan < bukan <=) | Periksa batas: untuk 1–5 gunakan `i <= 5` |
| Reset akumulator di dalam loop | `total = 0` diletakkan **sebelum** loop, bukan di dalam |
| Loop bersarang tidak memahami urutan | Loop dalam diselesaikan penuh untuk tiap iterasi loop luar |

---

## I. Tantangan Praktik (Mengaplikasi) 🎯

**Tantangan 1 — Cetak Angka (mudah):** Buat flowchart mencetak bilangan 1 sampai 10.

**Tantangan 2 — Hitung Mundur (sedang):** Buat flowchart hitung mundur dari n ke 1 lalu output "Go!".

**Tantangan 3 — Rata-rata N Nilai (sulit):** Buat flowchart menerima n, lalu n nilai, dan menampilkan rata-ratanya.

**Tantangan 4 — Tabel Perkalian (paling sulit):** Buat flowchart nested loop mencetak tabel perkalian 1–5, lalu hitung total iterasi yang terjadi.

---

## J. Rangkuman Kunci 🔑

- **Perulangan** menjalankan blok instruksi berulang kali.
- **FOR** = jumlah perulangan diketahui; **WHILE** = berhenti berdasarkan kondisi.
- Panah kembali (back loop) adalah penanda perulangan di flowchart.
- **Akumulator** (`total = total + i`) menghitung jumlah kumulatif; inisialisasi di luar loop.
- **Nested loop**: loop dalam selesai penuh untuk setiap iterasi loop luar.
- Selalu update counter agar terhindar dari **infinite loop**.

---

## K. Glosarium 📖

| Istilah | Arti |
|---|---|
| **Loop** | Perulangan eksekusi blok instruksi |
| **FOR loop** | Perulangan dengan jumlah iterasi pasti |
| **WHILE loop** | Perulangan berdasarkan kondisi yang diperiksa |
| **Counter** | Variabel penghitung (misal: i = i + 1) |
| **Akumulator** | Variabel penampung jumlah kumulatif |
| **Nested loop** | Perulangan di dalam perulangan |
| **Infinite loop** | Perulangan yang tidak pernah berhenti |

---

## L. Refleksi (Merefleksi) 🔍

- Konsep apa yang paling penting kamu pelajari hari ini?
- Kapan kita memilih FOR dan kapan memilih WHILE?
- Bagian mana yang masih sulit dipahami?
- **Skala pemahaman diri:** ____/10
- Apa yang ingin kamu pelajari lebih lanjut?

---

**MGMP Informatika SMAN 6 Cimahi — Fase F (Kelas XI) Semester 1**