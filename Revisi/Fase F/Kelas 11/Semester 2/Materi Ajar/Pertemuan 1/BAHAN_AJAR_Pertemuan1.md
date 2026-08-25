# BAHAN AJAR – PERTEMUAN 1 (S2)
## Pengenalan Python & Google Colab
*Mengacu pada Panduan Mapel 2025; INFORMATIKA Fase D-F — pendekatan Pembelajaran Mendalam (Memahami → Mengaplikasi → Merefleksi)*

| Informasi | Keterangan |
|---|---|
| **Fase / Kelas** | F / Kelas XI |
| **Alokasi Waktu** | 5 JP × 45 menit (225 menit) |
| **Elemen CP** | Analisis Data & Algoritma Pemrograman (AP) |
| **Tujuan Pembelajaran** | Mengenal Python, mengoperasikan Google Colab, menulis program pertama, dan membaca pesan error |
| **Materi Prasyarat** | Dasar penggunaan browser dan akun Google |

---

## A. Kisah Pemantik 🎬

> **"Buku Resep Ajaib"**
>
> Dina ingin mesin kopinya otomatis menyajikan minuman sesuai pesanan: memilih biji, menggiling, mengatur suhu air. Semua instruksi itu harus ditulis sebagai kumpulan perintah yang dipahami mesin — persis seperti **bahasa pemrograman**. Ia lalu menemukan **Python**, bahasa yang mudah dibaca seperti bahasa Inggris, yang kini dipakai untuk aplikasi, data, hingga kecerdasan buatan.
>
> **Pertanyaan pemantik:** Apa yang terjadi jika perintah mengandung satu kesalahan kecil (lupa tanda kutip)? Bagaimana sikap yang tepat saat program menghasilkan error?

---

## B. Apa Itu Python? 🐍

**Python** adalah bahasa pemrograman tingkat tinggi yang mudah dibaca dan ditulis. Dibuat oleh **Guido van Rossum** (1991), namanya terinspirasi acara *Monty Python's Flying Circus*.

| Istilah | Arti |
|---|---|
| **Bahasa tingkat tinggi** | Bahasa yang mirip bahasa manusia |
| **Interpreter** | Menjalankan kode baris per baris, tanpa kompilasi |
| **Sintaks** | Aturan penulisan yang harus diikuti |
| **Cell** | Kotak tempat menulis & menjalankan kode di Colab |
| **Output** | Hasil yang tampil setelah kode dijalankan |

**Karakteristik Python:** mudah dibaca, interpreted, dinamis (tanpa deklarasi tipe), multipurpose (web, data, AI, otomatisasi), dan open source. Bidang pemakaian: web (Django, Flask), data (Pandas, NumPy), AI (TensorFlow, PyTorch), dan otomatisasi tugas.

---

## C. Google Colab 🧪

**Google Colaboratory (Colab)** adalah platform menulis Python secara online dan gratis.

| Keunggulan | Penjelasan |
|---|---|
| Tanpa instalasi | Cukup pakai browser |
| Gratis | Termasuk akses GPU/TPU |
| Tersimpan di Drive | Notebook otomatis tersimpan |
| Kolaborasi | Bisa diedit bersama real-time |

**Langkah akses:** buka `colab.research.google.com` → login Gmail → **File → New Notebook** → ganti judul → tulis kode di cell.

| Shortcut | Fungsi |
|---|---|
| `Shift+Enter` | Jalankan cell, pindah ke cell berikutnya |
| `Ctrl+Enter` | Jalankan cell tanpa pindah |
| `Alt+Enter` | Jalankan cell dan buat cell baru |

---

## D. Program Pertama — Hello, World! 👋

```python
print("Hello, World!")
```
**Output:**
```
Hello, World!
```

**Variasi `print()`:**
```python
print(123)                 # mencetak angka
print("Halo", "dunia")     # beberapa nilai dipisah spasi
print("Hasil:", 5 + 3)     # teks + hasil operasi
print("Python" * 3)        # mengulang teks
print("Baris 1\nBaris 2")  # \n = baris baru
```
**Output:**
```
123
Halo dunia
Hasil: 8
PythonPythonPython
Baris 1
Baris 2
```

> 💡 Teks boleh memakai kutip satu (`'...'`) atau kutip dua (`"..."`); pastikan berpasangan.

---

## E. Komentar & Error 💬

**Komentar** tidak dieksekusi: pakai `#` untuk satu baris dan `'''...'''` untuk banyak baris.

```python
# ini komentar
print("Halo")   # komentar di samping kode
```

**Error itu wajar — bacalah pesannya:**

| Kode Salah | Error | Arti |
|---|---|---|
| `print("Halo` | SyntaxError | Kutip belum ditutup |
| `print(halo)` | NameError | `halo` belum didefinisikan |
| `prnt("Halo")` | NameError | Salah ketik nama fungsi |
| `print(10 + "a")` | TypeError | Tipe data tidak cocok |

---

## F. Contoh Soal & Penyelesaian 📝

**Contoh 1:** Tulis program yang mencetak nama, kelas, dan hobi dalam tiga baris.
**Jawaban:**
```python
print("Nama  : Anisa Rahma")
print("Kelas : XI-A")
print("Hobi  : Membaca")
```
**Output:**
```
Nama  : Anisa Rahma
Kelas : XI-A
Hobi  : Membaca
```

**Contoh 2:** Tentukan output `print("Hasil:", 20 / 4)`.
**Jawaban:** `Hasil: 5.0`. Angka `20/4` dihitung dulu menjadi `5.0` (float), lalu dicetak setelah teks.

**Contoh 3:** Mengapa `print("Halo)` error?
**Jawaban:** Kutip pembuka tidak ditutup (SyntaxError: EOL). Perbaiki menjadi `print("Halo")`.

**Contoh 4:** Jelaskan perbedaan output `print("123" + "45")` dan `print(123 + 45)`.
**Jawaban:** Yang pertama menggabungkan teks → `"12345"`; yang kedua menjumlahkan angka → `168`. Tipe data menentukan cara operator bekerja.

---

## G. Miskonsepsi & Kesalahan Umum 🚫

| Miskonsepsi / Kesalahan | Fakta yang Benar |
|---|---|
| "Python harus diinstall dulu" | Colab sudah menyediakan Python via browser |
| "Error berarti saya gagal" | Error adalah umpan balik yang bisa diperbaiki |
| "Kutip boleh tidak seimbang" | Kutip harus selalu berpasangan |
| "Nama fungsi boleh salah ketik" | Nama fungsi harus persis, misal `print` |
| "Komputer mengerti maksudku walau salah ketik" | Komputer menjalankan perintah yang benar-benar tertulis |

---

## H. Tantangan Praktik (Mengaplikasi) 🎯

**Tantangan 1 (Mudah):** Buka Colab, buat notebook `Pertemuan1_HelloPython`, tulis `print("Hello, World!")`, jalankan dengan `Shift+Enter`.

**Tantangan 2 (Sedang):** Buat program yang mencetak biodata 5 baris: nama lengkap, kelas/jurusan, tanggal lahir, hobi, cita-cita.

**Tantangan 3 (Sedang):** Tulis `print("Halo)`, `print(halo)`, `prnt("Halo")`. Catat pesan error masing-masing, lalu perbaiki agar berjalan.

**Tantangan 4 (Sulit):** Eksperimen dengan `print("Hasil:", 20/4)`, `print("Saya"+" "+"suka")`, `print("Baris 1\nBaris 2")`, `print("\tTab")`. Jelaskan hasilnya.

---

## I. Rangkuman Kunci 🔑

- **Python** = bahasa tingkat tinggi, interpreted, dan multipurpose.
- **Google Colab** menulis Python online, gratis, tersimpan di Drive.
- **`print()`** menampilkan teks, angka, dan hasil operasi.
- Kutip harus seimbang; **komentar** (`#`) tidak dieksekusi.
- **Error itu normal**; bacalah pesannya (SyntaxError, NameError, TypeError).

---

## J. Glosarium 📖

| Istilah | Arti |
|---|---|
| **Python** | Bahasa pemrograman tingkat tinggi |
| **Interpreter** | Menjalankan kode baris per baris |
| **Sintaks** | Aturan penulisan kode |
| **Colab** | Notebook Python online dari Google |
| **Cell** | Kotak menulis & menjalankan kode |
| **Output** | Hasil eksekusi kode |
| **Error** | Pesan kesalahan program |

---

## K. Refleksi (Merefleksi) 🔍

- Konsep apa yang paling penting kamu pelajari hari ini?
- Bagaimana perasaanmu saat pertama melihat error? Bagaimana seharusnya menyikapinya?
- Apa yang akan kamu lakukan agar terbiasa menulis kode yang rapi dan teliti?
- **Skala pemahaman diri:** ____/10
- Apa yang ingin kamu pelajari lebih lanjut tentang Python?

---

**MGMP Informatika SMAN 6 Cimahi — Fase F (Kelas XI) Semester 2**