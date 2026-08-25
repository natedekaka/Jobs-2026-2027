# BAHAN AJAR – PERTEMUAN 7 (S2)
## Fungsi
*Mengacu pada Panduan Mapel 2025; INFORMATIKA Fase D-F — pendekatan Pembelajaran Mendalam (Memahami → Mengaplikasi → Merefleksi)*

| Informasi | Keterangan |
|---|---|
| **Fase / Kelas** | F / Kelas XI |
| **Alokasi Waktu** | 5 JP × 45 menit (225 menit) |
| **Elemen CP** | Analisis Data & Algoritma Pemrograman (AP) |
| **Tujuan Pembelajaran** | Mendefinisikan dan memanggil fungsi dengan `def`, memakai parameter dan return, memahami scope, serta membuat parameter default |
| **Materi Prasyarat** | Variabel, Percabangan, Perulangan, dan List (Pertemuan 2-6) |

---

## A. Kisah Pemantik 🎬

> **"Resep Masakan di Dapur Restoran"**
>
> Koki restoran punya buku resep: setiap resep berisi langkah-langkah yang sama, bisa dipakai berulang kali setiap ada pesanan. Daripada menulis ulang cara memasak setiap kali, koki cukup membuka resepnya dan mengikuti langkah-langkahnya. Jika ingin variasinya, ia tinggal mengubah bahan yang dimasukkan.
>
> Dalam Python, **fungsi** adalah "resep" itu: blok kode bernama yang bisa dipanggil berkali-kali. Fungsi menerima **parameter** (bahan) dan mengembalikan **hasil** (masakan).
>
> **Pertanyaan pemantik:** Apa keuntungan menulis kode dalam fungsi dibanding menulis semua perintah berulang-ulang? Bagaimana kaitannya dengan prinsip DRY (*Don't Repeat Yourself*)?

---

## B. Apa Itu Fungsi? 🧩

**Fungsi** adalah blok kode yang diberi nama dan bisa dipanggil berkali-kali. Manfaat utamanya: menghindari pengulangan kode (prinsip **DRY** — Don't Repeat Yourself).

| Istilah | Arti |
|---|---|
| **def** | Kata kunci untuk mendefinisikan fungsi |
| **Parameter** | Variabel input yang diterima fungsi |
| **Argument** | Nilai yang dikirim saat fungsi dipanggil |
| **Return** | Nilai yang dikembalikan fungsi kepada pemanggil |
| **Scope** | Daerah jangkauan sebuah variabel (lokal/global) |
| **DRY** | Prinsip Don't Repeat Yourself |

---

## C. Fungsi Tanpa Parameter 📢

```python
def sapa():
    print("Halo! Selamat datang!")

sapa()
sapa()   # bisa dipanggil berkali-kali
```

**Output:**
```
Halo! Selamat datang!
Halo! Selamat datang!
```

---

## D. Fungsi dengan Parameter 🎁

Fungsi dapat menerima input berupa parameter.

```python
def sapa_user(nama):
    print(f"Halo, {nama}!")

sapa_user("Andi")
sapa_user("Budi")
```

**Output:**
```
Halo, Andi!
Halo, Budi!
```

> 💡 **Ingat:** urutan dan jumlah argument harus sesuai dengan parameter yang didefinisikan.

---

## E. Fungsi dengan Return ↩️

`return` mengirim nilai hasil fungsi kembali ke pemanggil untuk diolah lebih lanjut.

```python
def luas_persegi(sisi):
    return sisi * sisi

hasil = luas_persegi(5)
print(hasil)   # 25
```

**Output:**
```
25
```

**Contoh cek genap:**

```python
def cek_genap(angka):
    return angka % 2 == 0

print(cek_genap(4))   # True
if cek_genap(10):
    print("Genap!")
```

**Output:**
```
True
Genap!
```

---

## F. Fungsi dengan Banyak Return 🎯

Fungsi bisa mengembalikan lebih dari satu nilai sekaligus (dipisah koma → tuple).

```python
def hitung(a, b):
    return a + b, a - b, a * b, a / b

jumlah, selisih, kali, bagi = hitung(10, 3)
print(jumlah, selisih, kali, round(bagi, 2))
```

**Output:**
```
13 7 30 3.33
```

---

## G. Parameter Default ⚙️

Parameter dapat diberi nilai bawaan, sehingga boleh dilewati saat dipanggil.

```python
def sapa(nama="Teman"):
    print(f"Halo, {nama}!")

sapa("Andi")   # Halo, Andi!
sapa()         # Halo, Teman!
```

**Output:**
```
Halo, Andi!
Halo, Teman!
```

> 💡 Parameter default harus diletakkan setelah parameter tanpa default.

---

## H. Scope — Lokal vs Global 🌍

Variabel di dalam fungsi bersifat **lokal** (hanya berlaku di dalam fungsi). Variabel di luar fungsi bersifat **global**.

```python
nama = "Andi"      # global

def ubah():
    nama = "Budi"  # lokal (tidak mengubah variabel global)
    print("Di dalam fungsi:", nama)

ubah()             # Di dalam fungsi: Budi
print("Di luar fungsi:", nama)   # Andi
```

**Output:**
```
Di dalam fungsi: Budi
Di luar fungsi: Andi
```

---

## I. Program Kalkulator dalam Fungsi 🧮

```python
def kalkulator():
    a = float(input("Angka pertama: "))
    b = float(input("Angka kedua: "))
    op = input("Operator (+, -, *, /): ")
    if op == "+":
        print(f"Hasil: {a + b}")
    elif op == "-":
        print(f"Hasil: {a - b}")
    elif op == "*":
        print(f"Hasil: {a * b}")
    elif op == "/":
        if b == 0:
            print("Error: tidak bisa dibagi nol!")
        else:
            print(f"Hasil: {a / b}")

kalkulator()
```

**Output (jika input 10, 4, dan "+"):**
```
Hasil: 14.0
```

---

## J. Contoh Soal & Penyelesaian 📝

**Contoh 1:** Buat fungsi `sapa(nama)` yang mencetak `"Halo [nama]!"`.
**Jawaban:**
```python
def sapa(nama):
    print(f"Halo {nama}!")

sapa("Citra")
```
**Output:**
```
Halo Citra!
```

**Contoh 2:** Buat fungsi `luas_lingkaran(r)` yang mengembalikan luas lingkaran.
**Jawaban:**
```python
def luas_lingkaran(r):
    return 3.14 * r ** 2

print(luas_lingkaran(7))
```
**Output:**
```
153.86
```

**Contoh 3:** Buat fungsi `cek_kabisat(tahun)` yang mengembalikan `True`/`False`.
**Jawaban:**
```python
def cek_kabisat(tahun):
    return (tahun % 4 == 0 and tahun % 100 != 0) or tahun % 400 == 0

print(cek_kabisat(2024))   # True
print(cek_kabisat(2025))   # False
```
**Output:**
```
True
False
```

**Contoh 4:** Buat fungsi `faktorial(n)` yang menghitung `n!` menggunakan perulangan.
**Jawaban:**
```python
def faktorial(n):
    hasil = 1
    for i in range(1, n + 1):
        hasil *= i
    return hasil

print(faktorial(5))
```
**Output:**
```
120
```

**Contoh 5:** Jelaskan apa yang terjadi jika sebuah variabel lokal diberi nama sama dengan variabel global.
**Jawaban:** Variabel lokal akan "menutupi" variabel global di dalam fungsi. Perubahan pada variabel lokal tidak mengubah nilai variabel global di luar fungsi, seperti ditunjukkan pada contoh Scope (H).

---

## K. Miskonsepsi & Kesalahan Umum 🚫

| Miskonsepsi / Kesalahan | Fakta yang Benar |
|---|---|
| "Fungsi harus mencetak hasil dengan `print`" | Fungsi bisa `return` nilai untuk diolah pemanggil |
| "Tanpa `return`, fungsi tetap mengembalikan nilai" | Fungsi tanpa `return` mengembalikan `None` |
| "Parameter dan argument sama persis" | Parameter = variabel dalam definisi; argument = nilai saat dipanggil |
| "Variabel global bisa diubah dari dalam fungsi" | Tanpa kata kunci `global`, perubahan hanya lokal |
| "Nama fungsi bisa dipakai untuk variabel" | Nama fungsi tidak boleh bentrok dengan variabel |
| "Fungsi tidak bisa memanggil fungsi lain" | Fungsi bebas memanggil fungsi lain |

---

## L. Tantangan Praktik (Mengaplikasi) 🎯

**Tantangan 1 — Sapaan (Mudah):** Buat fungsi `sapa(nama)` yang mencetak `"Halo [nama]!"`, panggil dengan 3 nama berbeda.

**Tantangan 2 — Luas Lingkaran (Sedang):** Buat fungsi `luas_lingkaran(r)` yang mengembalikan `3.14 * r**2`, lalu cetak hasilnya untuk beberapa jari-jari.

**Tantangan 3 — Cek Kabisat (Sedang):** Buat fungsi `cek_kabisat(tahun)` yang mengembalikan `True`/`False`; uji dengan 2000, 2024, dan 1900.

**Tantangan 4 — Faktorial (Sulit):** Buat fungsi `faktorial(n)` dengan perulangan `for`; uji untuk `n = 5` dan `n = 10`.

**Tantangan 5 — BMI + Kategori (Sulit):** Buat dua fungsi: `hitung_bmi(berat, tinggi)` dan `kategori_bmi(bmi)` (Kurus/Ideal/Gemuk/Obesitas). Gabungkan dalam satu program yang menerima input user.

---

## M. Rangkuman Kunci 🔑

- Fungsi dibuat dengan **`def nama_fungsi(parameter):`** dan dipanggil dengan `nama_fungsi(argument)`.
- `return` mengembalikan nilai; fungsi tanpa `return` mengembalikan `None`.
- Fungsi dapat memiliki parameter default: `def sapa(nama="Teman")`.
- Fungsi dapat mengembalikan banyak nilai (tuple).
- Variabel **lokal** hanya berlaku di dalam fungsi; variabel **global** berlaku di seluruh program.
- Prinsip **DRY**: jangan ulang kode, bungkus dalam fungsi.

---

## N. Glosarium 📖

| Istilah | Arti |
|---|---|
| **Fungsi** | Blok kode bernama yang dapat dipanggil ulang |
| **def** | Kata kunci pendefinisian fungsi |
| **Parameter** | Variabel input dalam definisi fungsi |
| **Argument** | Nilai yang dikirim saat pemanggilan |
| **Return** | Mengirim nilai hasil fungsi |
| **Scope** | Jangkauan variabel (lokal/global) |
| **DRY** | Prinsip Don't Repeat Yourself |
| **None** | Nilai kembalian fungsi tanpa `return` |

---

## O. Refleksi (Merefleksi) 🔍

- Mengapa membagi program menjadi fungsi-fungsi kecil membuat kode lebih baik?
- Apa perbedaan penting antara `print` di dalam fungsi dan `return`?
- Bagian mana dari konsep scope yang masih membingungkanmu?
- **Skala pemahaman diri:** ____/10
- Program apa yang ingin kamu rakit dari beberapa fungsi?

---

**MGMP Informatika SMAN 6 Cimahi — Fase F (Kelas XI) Semester 2**