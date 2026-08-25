# BAHAN AJAR – PERTEMUAN 10 (S2)
## Review Python
*Mengacu pada Panduan Mapel 2025; INFORMATIKA Fase D-F — pendekatan Pembelajaran Mendalam (Memahami → Mengaplikasi → Merefleksi)*

| Informasi | Keterangan |
|---|---|
| **Fase / Kelas** | F / Kelas XI |
| **Alokasi Waktu** | 5 JP × 45 menit (225 menit) |
| **Elemen CP** | Analisis Data & Algoritma Pemrograman (AP) |
| **Tujuan Pembelajaran** | Mereview seluruh materi Python (Pertemuan 1-9) dan membuat program mandiri berjenjang |
| **Materi Prasyarat** | Seluruh materi Python Semester 2 (Pertemuan 1-9) |

---

## A. Kisah Pemantik 🎬

> **"Gladi Bersih Sebelum Pertunjukan"**
>
> Sebelum pentas besar, para pemain mengadakan gladi bersih: mengulang semua adegan, mengecek adegan mana yang masih lemah, dan memperbaikinya sebelum tampil. Begitu pula seorang programmer sebelum ujian: ia **mereview** semua materi, menemukan kelemahan, lalu berlatih dengan soal-soal yang menantang.
>
> Hari ini adalah "gladi bersih" kamu! Semua materi dari print() sampai program menu akan diuji lewat tantangan berjenjang. Semakin cepat kamu menemukan kelemahanmu, semakin siap kamu menghadapi PTS.
>
> **Pertanyaan pemantik:** Dari seluruh materi Python yang sudah dipelajari, bagian mana yang masih terasa sulit? Apa rencanamu untuk memperbaikinya hari ini?

---

## B. Peta Materi Python Semester 2 🗺️

| Pert | Materi | Skill Kunci |
|---|---|---|
| 1 | Python & Colab | `print()`, membaca error |
| 2 | Variabel & Tipe Data | int, float, str, bool, casting |
| 3 | Operator | aritmatika, perbandingan, logika |
| 4 | IF Percabangan | if, elif, else, nested |
| 5 | FOR & WHILE | range, break, continue |
| 6 | List & Tuple | indexing, slicing, method |
| 7 | Fungsi | def, parameter, return |
| 8 | Program Sederhana 1 | kalkulator, konversi, BMI |
| 9 | Program Sederhana 2 | To-Do List, nilai, kuis |

**Kisi-kisi inti yang harus dikuasai:**

| Topik | Yang harus bisa kamu lakukan |
|---|---|
| Input/Output | `print()`, `input()`, f-string |
| Variabel & tipe | Menyimpan data, konversi tipe, `type()` |
| Percabangan | Menentukan alur program dengan kondisi |
| Perulangan | Mengulang aksi dengan `for`/`while` |
| List | Menyimpan dan mengolah banyak data |
| Fungsi | Membungkus kode agar bisa dipakai ulang |

---

## C. Tantangan Hari Ini — 4 Level 🏆

**Level 1 (Mudah) — Sapaan Tahun Depan:**
Input nama dan umur, cetak `"Halo [nama], tahun depan kamu [umur+1] tahun"`.

```python
nama = input("Nama: ")
umur = int(input("Umur: "))
print(f"Halo {nama}, tahun depan kamu {umur + 1} tahun")
```

**Output (jika input Andi dan 17):**
```
Halo Andi, tahun depan kamu 18 tahun
```

**Level 2 (Sedang) — Faktor Bilangan:**
Input sebuah angka, cetak semua faktornya. Contoh: 6 → 1, 2, 3, 6.

```python
def faktor(n):
    return [i for i in range(1, n + 1) if n % i == 0]

angka = int(input("Masukkan angka: "))
print(f"Faktor dari {angka}: {faktor(angka)}")
```

**Output (jika input 12):**
```
Faktor dari 12: [1, 2, 3, 4, 6, 12]
```

**Level 3 (Sulit) — Tebak Kata (Hangman):**
Program memilih satu kata; user menebak huruf per huruf dengan nyawa terbatas.

```python
import random

kata = random.choice(["python", "komputer", "program"])
tebak = ["_"] * len(kata)
nyawa = 6

while nyawa > 0 and "_" in tebak:
    print(" ".join(tebak), f"  Nyawa: {nyawa}")
    h = input("Huruf: ").lower()
    if len(h) != 1:
        continue
    if h in kata:
        for i, ch in enumerate(kata):
            if ch == h:
                tebak[i] = h
    else:
        nyawa -= 1

print("Menang!" if "_" not in tebak else f"Kalah! Kata: {kata}")
```

**Contoh output (potongan):**
```
_ _ _ _ _ _   Nyawa: 6
Huruf: p
p _ _ _ _ _   Nyawa: 6
...
```

**Level 4 (Expert) — Catatan Keuangan:**
Catat pemasukan dan pengeluaran, tampilkan saldo, dan peringatkan jika saldo negatif.

```python
saldo = 0
while True:
    print("\n1. Pemasukan  2. Pengeluaran  3. Saldo  4. Keluar")
    p = input("Pilih: ")
    if p == "1":
        saldo += float(input("Jumlah pemasukan: "))
    elif p == "2":
        saldo -= float(input("Jumlah pengeluaran: "))
    elif p == "3":
        print(f"Saldo: {saldo}")
        if saldo < 0:
            print("Peringatan: saldo negatif!")
    elif p == "4":
        break
```

---

## D. Contoh Soal Gabungan & Penyelesaian 📝

**Contoh 1:** Buat fungsi `rata_rata(list_angka)` yang menghitung rata-rata dari sebuah list.
**Jawaban:**
```python
def rata_rata(angka):
    return sum(angka) / len(angka)

print(rata_rata([80, 90, 70, 60]))
```
**Output:**
```
75.0
```

**Contoh 2:** Tulis program yang mencetak bilangan genap dan jumlahnya dari 1 sampai 50.
**Jawaban:**
```python
genap = [i for i in range(1, 51) if i % 2 == 0]
print("Genap:", genap)
print("Jumlah:", sum(genap))
```
**Output:**
```
Genap: [2, 4, 6, ..., 50]
Jumlah: 650
```

**Contoh 3:** Tulis program yang menerima 3 angka lalu mencetak yang terbesar (tanpa `max()`).
**Jawaban:**
```python
a = float(input("Angka 1: "))
b = float(input("Angka 2: "))
c = float(input("Angka 3: "))

terbesar = a
if b > terbesar:
    terbesar = b
if c > terbesar:
    terbesar = c
print("Terbesar:", terbesar)
```
**Output (jika input 12, 45, 7):**
```
Terbesar: 45.0
```

**Contoh 4:** Buat fungsi `cek_prima(n)` dan gunakan untuk mencetak semua bilangan prima 1-100.
**Jawaban:**
```python
def cek_prima(n):
    if n < 2:
        return False
    for i in range(2, int(n ** 0.5) + 1):
        if n % i == 0:
            return False
    return True

prima = [i for i in range(1, 101) if cek_prima(i)]
print(prima)
```
**Output (sebagian):**
```
[2, 3, 5, 7, 11, 13, ..., 97]
```

---

## E. Miskonsepsi & Kesalahan Umum 🚫

| Miskonsepsi / Kesalahan | Fakta yang Benar |
|---|---|
| "Menghafal kode lebih penting daripada memahami logika" | Pahami alur logika; kode hanya alat untuk menuangkannya |
| "Sudah bisa, tidak perlu latihan" | Latihan justru menguatkan ingatan dan kecepatan menulis |
| "Satu cara menyelesaikan soal" | Ada banyak cara; yang penting hasilnya benar dan kodenya rapi |
| "Error berarti materi belum dikuasai" | Error adalah bagian proses belajar; yang penting bisa membacanya |
| "List comprehension terlalu sulit, hindari" | List comprehension justru mempersingkat kode dan sering dipakai |

---

## F. Tantangan Praktik (Mengaplikasi) 🎯

**Tantangan 1 — Daftar Cek Penguasaan (Mudah):** Tandai topik yang sudah kamu kuasai dari tabel di Bagian B. Identifikasi 2 topik terlemahmu.

**Tantangan 2 — Faktor Bilangan (Sedang):** Kerjakan Level 2 dan uji dengan angka 6, 12, dan 28.

**Tantangan 3 — Tebak Kata (Sulit):** Kerjakan Level 3. Modifikasi: tampilkan huruf yang sudah ditebak dan yang salah.

**Tantangan 4 — Catatan Keuangan (Expert):** Kerjakan Level 4, lalu tambahkan riwayat transaksi yang menampilkan semua pemasukan dan pengeluaran.

**Tantangan 5 — Program Gabungan (Expert):** Buat satu program yang memuat minimal 3 topik (misal fungsi + list + percabangan + loop), lalu presentasikan hasilnya.

---

## G. Rangkuman Kunci 🔑

- Review mencakup: input/output, variabel & tipe data, operator, percabangan, perulangan, list, dan fungsi.
- Latihan berjenjang membantu menemukan dan memperbaiki kelemahan.
- Program gabungan menguatkan pemahaman keterkaitan antar materi.
- Siapkan dirimu untuk PTS dengan menguasai kisi-kisi inti di Bagian B.

---

## H. Glosarium 📖

| Istilah | Arti |
|---|---|
| **Review** | Mengulang dan menguatkan pemahaman materi |
| **Challenge** | Tantangan soal berjenjang untuk berlatih |
| **Hangman** | Permainan menebak kata huruf per huruf |
| **Faktor** | Bilangan yang habis membagi suatu bilangan |
| **Saldo** | Selisih pemasukan dan pengeluaran |

---

## I. Refleksi (Merefleksi) 🔍

- Level mana yang paling sulit kamu kerjakan hari ini? Apa yang kamu lakukan untuk menyelesaikannya?
- Topik Python mana yang paling perlu kamu perkuat sebelum PTS?
- Bagaimana strategi belajarmu setelah mengetahui kelemahanmu?
- **Skala pemahaman diri:** ____/10
- Apa yang ingin kamu tanyakan kepada guru sebelum menghadapi PTS?

---

**MGMP Informatika SMAN 6 Cimahi — Fase F (Kelas XI) Semester 2**