# BAHAN AJAR – PERTEMUAN 2 (S2)
## Variabel & Tipe Data
*Mengacu pada Panduan Mapel 2025; INFORMATIKA Fase D-F — pendekatan Pembelajaran Mendalam (Memahami → Mengaplikasi → Merefleksi)*

| Informasi | Keterangan |
|---|---|
| **Fase / Kelas** | F / Kelas XI |
| **Alokasi Waktu** | 5 JP × 45 menit (225 menit) |
| **Elemen CP** | Analisis Data & Algoritma Pemrograman (AP) |
| **Tujuan Pembelajaran** | Menjelaskan variabel dan aturan penamaan, mengidentifikasi tipe data dasar, memakai `type()`, dan melakukan konversi tipe data |
| **Materi Prasyarat** | Pengenalan Python & Google Colab (Pertemuan 1) |

---

## A. Kisah Pemantik 🎬

> **"Kotak Kemasan di Gudang"**
>
> Pak Agus mengelola gudang yang harus menandai setiap kotak dengan label: kotak berisi beras diberi label *"beras"*, kotak berisi telur diberi label *"telur"*. Setiap hari jumlah isi bisa berubah — beras ditambah, telur dikurangi — tetapi **labelnya tetap**. Dengan label itu, Pak Agus tahu apa isi setiap kotak tanpa membukanya.
>
> Dalam Python, konsep ini disebut **variabel**: sebuah wadah bernama yang menyimpan data. Nama variabel adalah labelnya, dan isinya adalah data yang bisa berubah.
>
> **Pertanyaan pemantik:** Apa yang terjadi jika Pak Agus memberi label sama pada dua kotak yang berbeda? Bagaimana hal ini mirip dengan aturan penamaan variabel di Python?

---

## B. Apa Itu Variabel? 📦

**Variabel** adalah wadah untuk menyimpan data di memori komputer. Analoginya seperti **kotak berlabel** — label adalah nama variabel, isinya adalah data.

```python
nama = "Andi"      # variabel nama berisi teks "Andi"
usia = 17          # variabel usia berisi angka 17
tinggi = 165.5     # variabel tinggi berisi angka desimal
```

Cara membaca: **"nama diisi dengan Andi"**, bukan "nama sama dengan Andi". Tanda `=` di sini adalah operator penugasan (assignment), bukan perbandingan.

| Istilah | Arti |
|---|---|
| **Variabel** | Wadah bernama untuk menyimpan data |
| **Assignment (`=`)** | Memberi nilai ke sebuah variabel |
| **Tipe data** | Jenis nilai yang disimpan (angka, teks, logika) |
| **Cast / Konversi** | Mengubah suatu nilai dari satu tipe ke tipe lain |
| **Input** | Data yang dimasukkan pengguna saat program berjalan |

---

## C. Aturan Penamaan Variabel 📛

1. Boleh memakai **huruf, angka, dan underscore (`_`)** — contoh: `nama`, `usia_siswa`, `nilai1`.
2. **Tidak boleh diawali angka** — `1nilai` salah, `nilai1` benar.
3. **Case-sensitive** — `Nama` berbeda dengan `nama`.
4. **Tidak boleh memakai spasi** — gunakan `usia_siswa`, bukan `usia siswa`.
5. **Tidak boleh memakai kata kunci Python** — `if`, `for`, `while`, `True`, `False`, `def`.
6. **Konvensi `snake_case`** — pisahkan kata dengan underscore, misalnya `rata_rata`.

```python
nama_lengkap = "Anisa Rahma"
nilai_uts = 88
is_lulus = True
```

> 💡 **Ingat:** pilih nama yang **deskriptif** — `rata_rata` lebih jelas daripada `x`.

---

## D. Tipe Data Dasar 🏷️

| Tipe Data | Contoh | Penjelasan |
|---|---|---|
| `int` | `17`, `0`, `-5` | Bilangan bulat |
| `float` | `3.14`, `2.0`, `-0.5` | Bilangan desimal |
| `str` | `"Halo"`, `'Python'` | Teks (string) |
| `bool` | `True`, `False` | Nilai logika benar/salah |
| `NoneType` | `None` | Menandakan tidak ada nilai |

```python
nama = "Anisa"          # str
usia = 17               # int
tinggi = 158.5          # float
aktif = True            # bool
```
<br>

**Mengecek tipe data dengan `type()`:**

```python
nama = "Andi"
usia = 17
print(type(nama))    # <class 'str'>
print(type(usia))    # <class 'int'>
print(type(3.14))    # <class 'float'>
```

**Output:**
```
<class 'str'>
<class 'int'>
<class 'float'>
```

---

## E. Operasi String & Konversi Tipe (Casting) 🔄

**Operasi pada string:**

```python
# Penggabungan (+)
nama_depan = "Andi"
nama_belakang = "Prasetyo"
nama_lengkap = nama_depan + " " + nama_belakang
print(nama_lengkap)      # Andi Prasetyo

# Perkalian string (*)
print("Ha" * 3)          # HaHaHa

# Panjang string (len)
print(len("Python"))     # 6

# Ubah huruf besar/kecil
print("python".upper())  # PYTHON
print("PYTHON".lower())  # python
```

**Output:**
```
Andi Prasetyo
HaHaHa
6
PYTHON
python
```

**Konversi tipe data (casting):**

```python
# String ke Integer
umur_str = "17"
umur_int = int(umur_str)
print(umur_int + 3)              # 20

# Integer ke String
tahun = 2025
print("Tahun " + str(tahun))     # Tahun 2025

# Float ke Integer (membulatkan ke bawah)
pi = 3.99
print(int(pi))                   # 3
```

**Output:**
```
20
Tahun 2025
3
```

**Input dari pengguna:**

```python
nama = input("Siapa namamu? ")
print("Halo, " + nama + "!")
usia = input("Berapa usiamu? ")
print("Tahun depan kamu", int(usia) + 1, "tahun")
```

> 💡 **Penting:** `input()` selalu mengembalikan **string**. Jika ingin menghitung, ubah dulu dengan `int()` atau `float()`.

---

## F. Contoh Soal & Penyelesaian 📝

**Contoh 1:** Buat variabel `nama`, `kelas`, dan `usia`, lalu cetak semuanya dalam satu kalimat.
**Jawaban:**
```python
nama = "Budi"
kelas = "XI-A"
usia = 17
print("Halo", nama, "dari kelas", kelas, "usia", usia, "tahun")
```
**Output:**
```
Halo Budi dari kelas XI-A usia 17 tahun
```

**Contoh 2:** Tentukan output dari kode berikut: `print(len("Informatika"))`.
**Jawaban:** `len` menghitung panjang string, termasuk spasi. "Informatika" terdiri dari 11 huruf, sehingga outputnya adalah `11`.

**Contoh 3:** Tulis program yang menerima input dua angka dan mencetak hasil penjumlahannya.
**Jawaban:**
```python
a = int(input("Angka pertama: "))
b = int(input("Angka kedua: "))
print("Jumlah:", a + b)
```
**Output (jika input 10 dan 5):**
```
Jumlah: 15
```

**Contoh 4:** Mengapa kode `"Tahun " + 2025` menghasilkan error, sedangkan `"Tahun " + str(2025)` tidak?
**Jawaban:** Operator `+` untuk string hanya bisa menggabungkan string dengan string. Karena `2025` bertipe `int`, Python memunculkan TypeError. Dengan `str(2025)` angka diubah menjadi teks sehingga penggabungan berhasil.

---

## G. Miskonsepsi & Kesalahan Umum 🚫

| Miskonsepsi / Kesalahan | Fakta yang Benar |
|---|---|
| "`=` berarti sama dengan" | `=` adalah penugasan; perbandingan memakai `==` |
| "Variabel harus diawali huruf kapital" | Tidak; yang penting tidak diawali angka dan tidak pakai spasi |
| "`input()` langsung menghasilkan angka" | `input()` selalu string, harus dikonversi dengan `int()`/`float()` |
| "`Nama` dan `nama` itu sama" | Python membedakan huruf besar/kecil (case-sensitive) |
| "Tipe data tidak penting" | Tipe data menentukan operasi apa yang sah dilakukan |
| "Angka di dalam kutip itu angka" | `"17"` adalah teks; `17` adalah angka — keduanya berbeda |

---

## H. Tantangan Praktik (Mengaplikasi) 🎯

**Tantangan 1 — Profil Diri (Mudah):** Buat variabel `nama`, `kelas`, `usia`, `hobi`, lalu cetak semuanya. Cek tipe data tiap variabel dengan `type()`.

**Tantangan 2 — Sapaan Interaktif (Sedang):** Minta user input nama dan usia, lalu cetak `"Halo [nama], usia [usia]"`. Pastikan usia tetap bertipe string saat dicetak.

**Tantangan 3 — Konversi Suhu (Sedang):** Input suhu dalam Celsius (float), lalu cetak hasil konversi ke Fahrenheit dengan rumus `F = C * 9/5 + 32`. Bulatkan 1 angka desimal.

**Tantangan 4 — Penjumlahan Dua Angka (Sulit):** Minta input dua angka, jumlahkan, lalu tampilkan hasilnya dalam bentuk kalimat lengkap seperti `"10 + 5 = 15"` dengan memakai casting string.

---

## I. Rangkuman Kunci 🔑

- **Variabel** = wadah berlabel untuk menyimpan data; baca "diisi dengan", bukan "sama dengan".
- Nama variabel: huruf/angka/underscore, tidak diawali angka, tanpa spasi, dan **case-sensitive**.
- Tipe data dasar: `int`, `float`, `str`, `bool`, `NoneType`.
- `type()` digunakan untuk mengecek tipe data suatu nilai.
- String bisa digabung dengan `+` dan diulang dengan `*`.
- **Casting** mengubah tipe data: `int()`, `float()`, `str()`.
- `input()` selalu mengembalikan string; konversi dulu sebelum menghitung.

---

## J. Glosarium 📖

| Istilah | Arti |
|---|---|
| **Variabel** | Wadah bernama untuk menyimpan data |
| **Assignment** | Memberi nilai ke variabel memakai `=` |
| **Tipe data** | Jenis nilai yang disimpan sebuah variabel |
| **String (str)** | Tipe data teks |
| **Integer (int)** | Tipe data bilangan bulat |
| **Float** | Tipe data bilangan desimal |
| **Boolean (bool)** | Tipe data logika `True`/`False` |
| **Casting** | Konversi nilai dari satu tipe ke tipe lain |
| **Snake_case** | Konvensi penulisan nama variabel dengan underscore |

---

## K. Refleksi (Merefleksi) 🔍

- Apa perbedaan terpenting antara `=` dan `==` yang kamu pahami hari ini?
- Mengapa tipe data menentukan cara suatu operasi bekerja?
- Bagian mana dari aturan penamaan variabel yang masih membingungkan?
- **Skala pemahaman diri:** ____/10
- Apa yang ingin kamu coba selanjutnya dengan variabel dan tipe data?

---

**MGMP Informatika SMAN 6 Cimahi — Fase F (Kelas XI) Semester 2**