# BAHAN AJAR – PERTEMUAN 6 (S1)
## Flowchart — Urutan & I/O
*Mengacu pada Panduan Mapel 2025; INFORMATIKA Fase D-F — pendekatan Pembelajaran Mendalam (Memahami → Mengaplikasi → Merefleksi)*

| Informasi | Keterangan |
|---|---|
| **Fase / Kelas** | F / Kelas XI |
| **Alokasi Waktu** | 5 JP × 45 menit (225 menit) |
| **Elemen CP** | Algoritma dan Pemrograman (AP) |
| **Tujuan Pembelajaran** | Menjelaskan struktur urutan (sequence), membuat flowchart dengan input-proses-output, dan melakukan konversi/perhitungan sederhana dalam flowchart |
| **Materi Prasyarat** | Pertemuan 5 — Notasi algoritma dan simbol flowchart dasar |

---

## A. Kisah Pemantik 🎬

> **"Kasir yang Efisien"**
>
> Di toko kelontong, Bu Rina menghitung total belanja pelanggan dengan urutan tetap: catat harga tiap barang, jumlahkan semua harga, kalikan dengan jumlah barang, lalu umumkan totalnya. Urutan ini selalu sama — tidak pernah terbalik, karena jika terbalik hasilnya kacau. Inilah yang disebut **alur urutan (sequence)**.
>
> **Pertanyaan pemantik:** Aktivitas sehari-hari apa yang selalu dijalankan dengan urutan tetap yang sama? Apa yang terjadi jika salah satu langkah dihilangkan?

---

## B. Struktur Urutan (Sequence)

**Urutan (sequence)** adalah struktur algoritma paling sederhana — langkah dieksekusi **berurutan dari atas ke bawah**, tanpa lompatan dan tanpa pengulangan. Ini fondasi semua flowchart.

```
┌─────────┐
│  START  │
└────┬────┘
     ▼
┌─────────────────────┐
│  INPUT (data)       │
└────┬────────────────┘
     ▼
┌─────────────────────┐
│  PROSES (hitungan)  │
└────┬────────────────┘
     ▼
┌─────────────────────┐
│  OUTPUT (hasil)     │
└────┬────────────────┘
     ▼
┌─────────┐
│   END   │
└─────────┘
```

**Aturan membuat flowchart sequence:**
1. Mulai dengan simbol START/END (terminal)
2. Tiap langkah ditulis dalam satu simbol
3. Gunakan panah untuk menunjukkan alur
4. Satu jalur masuk, satu jalur keluar (kecuali pada percabangan)
5. Sederhana dan jelas — hindari garis saling menimpa

---

## C. Input/Output (I/O) dalam Flowchart

**Input** dan **Output** digambarkan dengan simbol **jajar genjang**.

| Jenis | Simbol | Contoh Notasi |
|---|---|---|
| **Input** | Jajar genjang | input(nama), input(usia), input(r) |
| **Output** | Jajar genjang | output("Halo, " + nama), output(luas) |

> 💡 **Ingat:** tanpa input, program tidak punya data; tanpa output, hasil tidak pernah sampai ke pengguna.

---

## D. Contoh Flowchart Urutan + I/O

**Contoh 1 — Sapa Pengguna:**
```
┌─────────┐
│  START  │
└────┬────┘
     ▼
┌───────────────────┐
│ INPUT nama        │
└────┬──────────────┘
     ▼
┌───────────────────────┐
│ OUTPUT "Halo, "+ nama │
└────┬──────────────────┘
     ▼
┌─────────┐
│  END    │
└─────────┘
```

**Contoh 2 — Luas Persegi Panjang:**
Start → input panjang → input lebar → luas = p × l → output luas → End

**Contoh 3 — Konversi Suhu (Celcius → Fahrenheit):**
Start → input C → F = C × 9/5 + 32 → output F → End

**Contoh 4 — Hitung Rata-rata 3 Nilai:**
Start → input nilai1 → input nilai2 → input nilai3 → rata = (n1 + n2 + n3) / 3 → output rata → End

**Contoh 5 — Kalkulator Sederhana (a + b, a − b, a × b):**
Start → input a → input b → jumlah = a + b → selisih = a − b → kali = a × b → output jumlah, selisih, kali → End

---

## E. Studi Kasus — Konversi Rupiah ke Dolar

**Kasus:** Buat flowchart mengonversi uang dalam Rupiah ke Dolar dengan kurs 1 USD = 15.000 IDR.

**Algoritma (langkah):**
1. Start
2. Input uangRupiah
3. dollar = uangRupiah / 15000
4. Output dollar
5. End

**Tracing:** Input uangRupiah = 450.000 → dollar = 450000 / 15000 = **30 USD** → output "30 USD".

---

## F. Contoh Soal & Penyelesaian 📝

**Contoh 1:** Gambarkan flowchart: input nama, cetak "Halo [nama]!"
**Jawaban:** Start → input nama → output "Halo, " + nama → End. (Semua menggunakan simbol: oval Start, jajar genjang input/output, oval End.)

**Contoh 2:** Buat flowchart: input 2 angka, cetak hasil penjumlahan dan perkalian!
**Jawaban:** Start → input a → input b → jumlah = a + b → kali = a × b → output jumlah → output kali → End.

**Contoh 3:** Buat flowchart: input panjang & lebar, hitung dan cetak luas persegi panjang!
**Jawaban:** Start → input panjang → input lebar → luas = panjang × lebar → output luas → End. Tracing: p=8, l=5 → luas = **40**.

**Contoh 4:** Buat flowchart: input jam & menit, konversi ke total menit (jam × 60 + menit)!
**Jawaban:** Start → input jam → input menit → total = jam × 60 + menit → output total → End. Tracing: jam=2, menit=15 → total = 2×60 + 15 = **135 menit**.

**Contoh 5:** Buat flowchart konversi Rupiah ke Dolar (kurs 1 USD = 15.000 IDR)!
**Jawaban:** Start → input rupiah → dollar = rupiah / 15000 → output dollar → End. Tracing: rupiah = 300.000 → dollar = **20 USD**.

---

## G. Miskonsepsi / Kesalahan Umum 🚫

| Miskonsepsi / Kesalahan | Fakta yang Benar |
|---|---|
| Input dan output memakai simbol yang berbeda | Keduanya sama-sama **jajar genjang** |
| Menulis "input a, b, c" dalam satu simbol | Satu simbol = satu aktivitas; pisahkan tiap input |
| Lupa simbol Start/End | Flowchart wajib dimulai Start dan diakhiri End |
| Menggabungkan hitungan dan tampilan dalam satu simbol | Proses (persegi) terpisah dari output (jajar genjang) |
| Tidak memberi nilai saat tracing | Tracing harus mencatat nilai variabel tiap langkah |

---

## H. Tantangan Praktik (Mengaplikasi) 🎯

**Tantangan 1 — Sapa Pengguna (mudah):** Buat flowchart: input nama → output "Halo, [nama]! Selamat belajar."

**Tantangan 2 — Jumlah & Kali (sedang):** Buat flowchart: input 2 angka → output jumlah dan perkaliannya.

**Tantangan 3 — Konversi Waktu (sulit):** Buat flowchart: input jumlah detik → output jam, menit, dan sisa detik (gunakan pembagian dan modulo).

**Tantangan 4 — Keliling Bangun (paling sulit):** Buat flowchart menghitung keliling persegi panjang (2 × (p+l)), lalu lakukan tracing dengan p=12, l=7 dan tuliskan nilai tiap variabel di setiap langkah.

---

## I. Rangkuman Kunci 🔑

- **Urutan (sequence)** = langkah dieksekusi berurutan dari atas ke bawah.
- Input dan output menggunakan simbol **jajar genjang**; proses menggunakan **persegi panjang**.
- Flowchart dimulai dengan **Start** dan diakhiri **End**.
- Pola umum sequence: **Start → Input → Proses → Output → End**.
- **Tracing** penting untuk membuktikan flowchart benar sebelum dipakai.

---

## J. Glosarium 📖

| Istilah | Arti |
|---|---|
| **Sequence** | Struktur algoritma yang menjalankan langkah berurutan |
| **Input** | Data yang dimasukkan ke program |
| **Output** | Hasil yang ditampilkan program |
| **Jajar genjang** | Simbol flowchart untuk input/output |
| **Persegi panjang** | Simbol flowchart untuk proses/hitungan |
| **Tracing** | Menelusuri alur dengan nilai konkret untuk memeriksa kebenaran |

---

## K. Refleksi (Merefleksi) 🔍

- Konsep apa yang paling penting kamu pelajari hari ini?
- Apa perbedaan simbol proses dan simbol input/output?
- Bagian mana yang masih sulit dipahami?
- **Skala pemahaman diri:** ____/10
- Apa yang ingin kamu pelajari lebih lanjut?

---

**MGMP Informatika SMAN 6 Cimahi — Fase F (Kelas XI) Semester 1**