# BAHAN AJAR – PERTEMUAN 4 (S2)
## IF — Percabangan
*Mengacu pada Panduan Mapel 2025; INFORMATIKA Fase D-F — pendekatan Pembelajaran Mendalam (Memahami → Mengaplikasi → Merefleksi)*

| Informasi | Keterangan |
|---|---|
| **Fase / Kelas** | F / Kelas XI |
| **Alokasi Waktu** | 5 JP × 45 menit (225 menit) |
| **Elemen CP** | Analisis Data & Algoritma Pemrograman (AP) |
| **Tujuan Pembelajaran** | Menggunakan `if`, `elif`, `else` untuk percabangan; membuat program berlogika percabangan; menggabungkan operator logika; memahami perbedaan `if` dan `elif` |
| **Materi Prasyarat** | Variabel, Tipe Data, dan Operator (Pertemuan 2-3) |

---

## A. Kisah Pemantik 🎬

> **"Petugas Loket Bioskop"**
>
> Di sebuah bioskop, petugas loket menilai penonton berdasarkan umur dan tiketnya: anak-anak di bawah 7 tahun masuk gratis, pelajar mendapat diskon, dan dewasa membayar penuh. Setiap penonton diarahkan ke jalur yang berbeda **berdasarkan kondisi**.
>
> Komputer melakukan hal yang sama dengan **percabangan**: memeriksa sebuah kondisi, lalu menjalankan perintah tertentu jika kondisinya benar, dan perintah lain jika salah. Inilah cara program membuat keputusan seperti manusia.
>
> **Pertanyaan pemantik:** Jika bioskop menambah aturan "lansia di atas 65 tahun gratis", bagaimana urutan pemeriksaan yang harus dilakukan agar aturan lama dan baru tidak bertabrakan?

---

## B. IF Sederhana — Satu Keputusan 🚦

Struktur `if` menjalankan blok kode **hanya jika** kondisi bernilai `True`.

```python
usia = 17
if usia >= 17:
    print("Kamu sudah cukup umur.")
```

**Output:**
```
Kamu sudah cukup umur.
```

| Komponen | Arti |
|---|---|
| `if` | Kata kunci awal percabangan |
| `usia >= 17` | Kondisi yang diperiksa |
| `:` | Titik dua menandai awal blok |
| Indentasi (4 spasi) | Menandai kode yang termasuk dalam blok `if` |

> 💡 **Indentasi itu wajib!** Kode di dalam blok `if` harus diberi indentasi. Tanpa indentasi, Python akan memunculkan `IndentationError`.

---

## C. IF-ELSE — Dua Arah 🔀

`if...else` memberi dua jalur: jika kondisi benar jalankan blok `if`, jika salah jalankan blok `else`.

```python
usia = 15
if usia >= 17:
    print("Kamu sudah cukup umur.")
else:
    print("Kamu masih di bawah umur.")
```

**Output:**
```
Kamu masih di bawah umur.
```

**Contoh genap/ganjil:**

```python
angka = int(input("Masukkan angka: "))
if angka % 2 == 0:
    print(angka, "adalah bilangan genap")
else:
    print(angka, "adalah bilangan ganjil")
```

**Output (jika input 8):**
```
8 adalah bilangan genap
```

---

## D. IF-ELIF-ELSE — Banyak Pilihan 🪜

`elif` (else if) memungkinkan memeriksa beberapa kondisi berurutan. Kondisi pertama yang benar akan dijalankan, sisanya dilewati.

```python
nilai = int(input("Masukkan nilai: "))
if nilai >= 85:
    predikat = "A (Sangat Baik)"
elif nilai >= 70:
    predikat = "B (Baik)"
elif nilai >= 55:
    predikat = "C (Cukup)"
else:
    predikat = "D (Kurang)"
print("Predikat:", predikat)
```

**Output (jika input 78):**
```
Predikat: B (Baik)
```

**Perbedaan `if` beruntun vs `elif`:** dengan `elif`, hanya satu blok yang dieksekusi; dengan `if` beruntun, semua kondisi dievaluasi satu per satu meskipun kondisi pertama sudah benar.

---

## E. IF Bersarang (Nested IF) 🪆

`if` di dalam `if` dipakai ketika keputusan berjenjang.

```python
usia = int(input("Usia: "))
nilai = int(input("Nilai: "))

if usia >= 17:
    if nilai >= 70:
        print("Lulus dan cukup umur")
    else:
        print("Cukup umur tapi tidak lulus")
else:
    if nilai >= 70:
        print("Lulus tapi belum cukup umur")
    else:
        print("Tidak lulus dan belum cukup umur")
```

**Output (jika input 18 dan 75):**
```
Lulus dan cukup umur
```

---

## F. IF dengan Logika AND/OR 🔗

Kombinasikan beberapa kondisi dalam satu `if` memakai operator logika.

```python
usia = int(input("Usia: "))
sehat = input("Sehat? (ya/tidak): ")
if usia >= 17 and sehat == "ya":
    print("Boleh ikut lomba")
else:
    print("Tidak boleh ikut lomba")
```

**Output (jika input 18 dan "ya"):**
```
Boleh ikut lomba
```

**Program lengkap — Cek Kesehatan:**

```python
print("=== CEK KESEHATAN ===")
suhu = float(input("Suhu tubuh: "))
batuk = input("Batuk? (ya/tidak): ")
if suhu > 37.5 and batuk == "ya":
    print("Periksa ke dokter!")
elif suhu > 37.5 or batuk == "ya":
    print("Istirahat di rumah")
else:
    print("Sehat walafiat")
```

---

## G. Operator Ternary 🍬

Cara singkat menulis `if...else` sederhana dalam satu baris.

```python
nilai = 75
status = "Lulus" if nilai >= 70 else "Tidak Lulus"
print(status)
```

**Output:**
```
Lulus
```

---

## H. Contoh Soal & Penyelesaian 📝

**Contoh 1:** Tulis program yang menentukan apakah sebuah angka positif, negatif, atau nol.
**Jawaban:**
```python
angka = int(input("Masukkan angka: "))
if angka > 0:
    print("Positif")
elif angka < 0:
    print("Negatif")
else:
    print("Nol")
```
**Output (jika input -5):**
```
Negatif
```

**Contoh 2:** Tulis program pengecek tahun kabisat (habis dibagi 4, kecuali abad yang tidak habis dibagi 400).
**Jawaban:**
```python
tahun = int(input("Masukkan tahun: "))
if (tahun % 4 == 0 and tahun % 100 != 0) or tahun % 400 == 0:
    print(tahun, "adalah tahun kabisat")
else:
    print(tahun, "bukan tahun kabisat")
```
**Output (jika input 2024):**
```
2024 adalah tahun kabisat
```

**Contoh 3:** Klasifikasikan usia ke kategori: Balita (0-5), Anak (6-12), Remaja (13-17), Dewasa (18+).
**Jawaban:**
```python
usia = int(input("Usia: "))
if usia <= 5:
    kategori = "Balita"
elif usia <= 12:
    kategori = "Anak"
elif usia <= 17:
    kategori = "Remaja"
else:
    kategori = "Dewasa"
print("Kategori:", kategori)
```
**Output (jika input 14):**
```
Kategori: Remaja
```

**Contoh 4:** Jelaskan mengapa urutan kondisi pada `elif` sangat penting.
**Jawaban:** Python memeriksa kondisi dari atas ke bawah dan berhenti pada kondisi pertama yang benar. Jika urutan dibalik (misal "nilai ≥ 55" ditulis sebelum "nilai ≥ 85"), maka nilai 90 akan masuk ke "C" karena `90 ≥ 55` benar lebih dulu. Urutan yang benar: dari kondisi paling ketat ke paling longgar.

---

## I. Miskonsepsi & Kesalahan Umum 🚫

| Miskonsepsi / Kesalahan | Fakta yang Benar |
|---|---|
| "Lupa titik dua `:` setelah kondisi" | Setiap `if`/`elif`/`else` harus diakhiri `:` |
| "Indentasi tidak penting" | Indentasi menentukan blok kode; tanpa indentasi muncul IndentationError |
| "Memakai `=` di dalam kondisi" | Kondisi harus memakai `==`, bukan `=` |
| "Semua `if` beruntun seperti `elif`" | `elif` hanya menjalankan satu blok; `if` beruntun mengevaluasi semua |
| "`else if` ditulis sebagai satu kata `elseif`" | Di Python ditulis `elif` |
| "Kondisi dibalik urutannya tidak masalah" | Urutan `elif` sangat menentukan hasil akhir |

---

## J. Tantangan Praktik (Mengaplikasi) 🎯

**Tantangan 1 — Kelulusan (Mudah):** Input nilai, cetak "Lulus" jika ≥ 70, selain itu "Tidak Lulus".

**Tantangan 2 — Positif/Negatif/Nol (Sedang):** Input angka dan tentukan apakah positif, negatif, atau nol memakai `if/elif/else`.

**Tantangan 3 — Tahun Kabisat (Sedang):** Buat pengecek tahun kabisat dengan logika yang benar (habis dibagi 4 dan tidak habis dibagi 100, atau habis dibagi 400).

**Tantangan 4 — Kategori Usia (Sulit):** Klasifikasikan usia menjadi Balita, Anak, Remaja, dan Dewasa; tambahkan pesan keterangan yang sesuai tiap kategori.

**Tantangan 5 — Ternary (Sulit):** Tulis ulang program genap/ganjil memakai operator ternary dalam satu baris.

---

## K. Rangkuman Kunci 🔑

- `if` menjalankan blok kode saat kondisi `True`.
- `if...else` menyediakan dua jalur keputusan.
- `if...elif...else` untuk banyak pilihan; hanya satu blok yang dijalankan.
- **Nested IF** untuk keputusan berjenjang.
- Kombinasikan kondisi dengan `and`, `or`, `not`.
- Operator ternary: `nilai_benar if kondisi else nilai_salah`.
- Jangan lupa `:` dan indentasi!

---

## L. Glosarium 📖

| Istilah | Arti |
|---|---|
| **Percabangan** | Struktur program yang memilih jalur berdasarkan kondisi |
| **IF** | Menjalankan kode jika kondisi benar |
| **ELIF** | Periksa kondisi berikutnya jika sebelumnya salah |
| **ELSE** | Jalankan kode jika semua kondisi salah |
| **Nested IF** | `if` yang berada di dalam `if` lain |
| **Ternary** | Bentuk singkat `if...else` dalam satu baris |
| **Kondisi** | Ekspresi yang bernilai `True`/`False` |
| **Indentasi** | Spasi di awal baris untuk menandai blok kode |

---

## M. Refleksi (Merefleksi) 🔍

- Mengapa urutan kondisi pada `elif` sangat menentukan hasil program?
- Di mana kamu bisa menerapkan logika percabangan dalam kehidupan sehari-hari?
- Kesalahan apa yang paling sering kamu buat saat menulis percabangan?
- **Skala pemahaman diri:** ____/10
- Apa program percabangan yang ingin kamu buat selanjutnya?

---

**MGMP Informatika SMAN 6 Cimahi — Fase F (Kelas XI) Semester 2**