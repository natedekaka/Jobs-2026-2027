# BAHAN AJAR – PERTEMUAN 8 (S2)
## Program Sederhana 1 — Kalkulator, Konversi Suhu, dan BMI
*Mengacu pada Panduan Mapel 2025; INFORMATIKA Fase D-F — pendekatan Pembelajaran Mendalam (Memahami → Mengaplikasi → Merefleksi)*

| Informasi | Keterangan |
|---|---|
| **Fase / Kelas** | F / Kelas XI |
| **Alokasi Waktu** | 5 JP × 45 menit (225 menit) |
| **Elemen CP** | Analisis Data & Algoritma Pemrograman (AP) |
| **Tujuan Pembelajaran** | Membuat program Python utuh (input-proses-output), membangun kalkulator, konversi suhu, dan pengecek BMI |
| **Materi Prasyarat** | Variabel, Operator, Percabangan, Perulangan, List, dan Fungsi (Pertemuan 2-7) |

---

## A. Kisah Pemantik 🎬

> **"Bengkel Koding Keliling"**
>
> Seorang teknisi membuka "bengkel" kecil untuk membuat program-program praktis: menghitung total belanja, mengonversi suhu, hingga mengecek berat badan ideal. Setiap program adalah gabungan dari bagian-bagian kecil: **menerima input**, **mengolah data**, dan **menampilkan hasil**.
>
> Kini giliranmu menjadi teknisi itu! Kamu sudah mempelajari variabel, operator, percabangan, perulangan, list, dan fungsi. Semua itu akan kamu rakit menjadi program-program yang benar-benar berguna.
>
> **Pertanyaan pemantik:** Sebuah program yang baik harus mengantisipasi kesalahan pengguna (misal membagi dengan nol). Apa saja kemungkinan kesalahan input yang harus kamu waspadai saat membuat program?

---

## B. Alur Program: Input → Proses → Output 🔄

Setiap program mengikuti alur dasar yang sama.

| Tahap | Fungsi | Contoh |
|---|---|---|
| **Input** | Menerima data dari pengguna | `input()`, `int()`, `float()` |
| **Proses** | Mengolah data | operasi matematika, percabangan, perulangan |
| **Output** | Menampilkan hasil | `print()`, `f-string` |

**Template program:**
```python
# 1. INPUT
nama = input("Nama: ")
# 2. PROSES (mengubah/menghitung)
pesan = "Halo, " + nama
# 3. OUTPUT
print(pesan)
```

> 💡 Gunakan **f-string** untuk output yang rapi: `print(f"Hasil: {hasil}")`.

---

## C. Program 1: Kalkulator Sederhana 🧮

```python
def kalkulator():
    print("=" * 30)
    print("KALKULATOR SEDERHANA")
    print("=" * 30)
    print("1. Penjumlahan (+)")
    print("2. Pengurangan (-)")
    print("3. Perkalian (*)")
    print("4. Pembagian (/)")
    print("5. Pangkat (**)")

    pilihan = input("Pilih operasi (1-5): ")
    a = float(input("Angka pertama: "))
    b = float(input("Angka kedua: "))

    if pilihan == "1":
        print(f"{a} + {b} = {a + b}")
    elif pilihan == "2":
        print(f"{a} - {b} = {a - b}")
    elif pilihan == "3":
        print(f"{a} * {b} = {a * b}")
    elif pilihan == "4":
        if b != 0:
            print(f"{a} / {b} = {a / b:.2f}")
        else:
            print("ERROR: Tidak bisa dibagi nol!")
    elif pilihan == "5":
        print(f"{a} ** {b} = {a ** b}")

kalkulator()
```

**Output (jika pilih 4, input 10 dan 4):**
```
================================
KALKULATOR SEDERHANA
================================
1. Penjumlahan (+)
2. Pengurangan (-)
3. Perkalian (*)
4. Pembagian (/)
5. Pangkat (**)
Pilih operasi (1-5): 4
Angka pertama: 10
Angka kedua: 4
10.0 / 4.0 = 2.50
```

---

## D. Program 2: Konversi Suhu 🌡️

```python
def konversi_suhu():
    print("KONVERSI SUHU")
    print("1. C -> F")
    print("2. F -> C")
    print("3. C -> K")
    pilihan = input("Pilih (1-3): ")
    suhu = float(input("Suhu: "))

    if pilihan == "1":
        print(f"{suhu}C = {suhu * 9 / 5 + 32:.1f}F")
    elif pilihan == "2":
        print(f"{suhu}F = {(suhu - 32) * 5 / 9:.1f}C")
    elif pilihan == "3":
        print(f"{suhu}C = {suhu + 273.15:.1f}K")

konversi_suhu()
```

**Output (jika pilih 1, input 100):**
```
KONVERSI SUHU
1. C -> F
2. F -> C
3. C -> K
Pilih (1-3): 1
Suhu: 100
100.0C = 212.0F
```

**Rumus konversi yang dipakai:**
- `F = C × 9/5 + 32`
- `C = (F − 32) × 5/9`
- `K = C + 273.15`

---

## E. Program 3: Cek BMI ⚖️

**BMI (Body Mass Index)** mengukur proporsi berat dan tinggi badan. `BMI = berat(kg) / tinggi(m)²`.

```python
def hitung_bmi(berat, tinggi):
    return berat / (tinggi ** 2)

def kategori_bmi(bmi):
    if bmi < 18.5:
        return "Kurus"
    elif bmi < 25:
        return "Ideal"
    elif bmi < 30:
        return "Gemuk"
    else:
        return "Obesitas"

nama = input("Nama: ")
berat = float(input("Berat (kg): "))
tinggi = float(input("Tinggi (cm): ")) / 100
bmi = hitung_bmi(berat, tinggi)
print(f"BMI {nama}: {bmi:.1f} ({kategori_bmi(bmi)})")
```

**Output (jika input Ani, 55, 160):**
```
Nama: Ani
Berat (kg): 55
Tinggi (cm): 160
BMI Ani: 21.5 (Ideal)
```

| Kategori | Rentang BMI |
|---|---|
| Kurus | < 18.5 |
| Ideal | 18.5 – 24.9 |
| Gemuk | 25.0 – 29.9 |
| Obesitas | ≥ 30.0 |

---

## F. Program Bonus: Bilangan Prima 🔢

Bilangan prima hanya habis dibagi 1 dan dirinya sendiri.

```python
def cek_prima(n):
    if n < 2:
        return False
    for i in range(2, int(n ** 0.5) + 1):
        if n % i == 0:
            return False
    return True

print("Bilangan prima 1-50:")
for i in range(1, 51):
    if cek_prima(i):
        print(i, end=" ")
```

**Output:**
```
Bilangan prima 1-50:
2 3 5 7 11 13 17 19 23 29 31 37 41 43 47
```

---

## G. Contoh Soal & Penyelesaian 📝

**Contoh 1:** Jelaskan alur input-proses-output pada program kalkulator.
**Jawaban:** Input = pilihan operasi, angka pertama, dan angka kedua (dari `input()`). Proses = memeriksa pilihan dengan `if/elif` lalu menghitung sesuai operator. Output = hasil perhitungan dicetak dengan `f-string`. Program juga mengantisipasi pembagian nol.

**Contoh 2:** Tulis program konversi dari Celsius ke Fahrenheit lengkap dengan input dan output.
**Jawaban:**
```python
c = float(input("Suhu dalam Celsius: "))
f = c * 9 / 5 + 32
print(f"{c} Celsius = {f:.1f} Fahrenheit")
```
**Output (jika input 30):**
```
30.0 Celsius = 86.0 Fahrenheit
```

**Contoh 3:** Hitung BMI untuk berat 70 kg dan tinggi 170 cm, lalu tentukan kategorinya.
**Jawaban:** Tinggi dalam meter = `170/100 = 1.7`. BMI = `70 / (1.7)² = 70 / 2.89 = 24.2`. Karena berada di rentang `18.5–24.9`, kategori = **Ideal**.

**Contoh 4:** Mengapa pembagian dengan nol perlu dicek sebelum dihitung?
**Jawaban:** Dalam matematika, pembagian dengan nol tidak terdefinisi. Jika dibiarkan, Python memunculkan `ZeroDivisionError` dan program berhenti. Dengan pengecekan `if b != 0`, program menampilkan pesan yang ramah dan tidak crash.

**Contoh 5:** Tulis program yang mencetak bilangan prima dari 1 sampai 100.
**Jawaban:** Gunakan fungsi `cek_prima` seperti pada bagian F, ubah rentang loop menjadi `range(1, 101)`.

---

## H. Miskonsepsi & Kesalahan Umum 🚫

| Miskonsepsi / Kesalahan | Fakta yang Benar |
|---|---|
| "Tinggi langsung dipakai dalam meter" | Input `input()` adalah string; harus diubah ke float dan cm diubah ke m (`/100`) |
| "Program pasti benar tanpa diuji" | Selalu uji dengan berbagai input, termasuk input ekstrem (0, negatif) |
| "Error membuat program jelek" | Program yang baik justru menangani error dengan pesan yang jelas |
| "Satu fungsi cukup untuk semua program" | Pecah program menjadi fungsi-fungsi kecil agar mudah diuji dan dipelihara |
| "`f-string` hanya untuk teks" | f-string juga bisa memformat angka, misal `:.2f` untuk 2 desimal |

---

## I. Tantangan Praktik (Mengaplikasi) 🎯

**Tantangan 1 — Kalkulator Sederhana (Mudah):** Bangun kalkulator dengan 5 operasi (+ , -, *, /, **), lengkap dengan penanganan pembagian nol.

**Tantangan 2 — Konversi Suhu Lengkap (Sedang):** Tambahkan konversi Reamur: `R = C × 4/5` ke program konversi suhu.

**Tantangan 3 — BMI + Saran (Sedang):** Kembangkan program BMI dengan menampilkan saran kesehatan sesuai kategori (misal "perbanyak makan" untuk Kurus).

**Tantangan 4 — Bilangan Prima dalam Range (Sulit):** Buat program yang menerima dua angka dari user (awal dan akhir), lalu mencetak semua bilangan prima di antara keduanya.

**Tantangan 5 — Program Nilai (Sulit):** Input nilai beberapa siswa, hitung total, rata-rata, tertinggi, terendah, dan predikat kelulusan masing-masing, lalu tampilkan dalam laporan rapi.

---

## J. Rangkuman Kunci 🔑

- Setiap program mengikuti alur **input → proses → output**.
- Gunakan **fungsi** untuk memecah program menjadi bagian-bagian yang jelas.
- **f-string** membuat output rapi, misal `f"{hasil:.2f}"` untuk 2 desimal.
- Program yang baik **mengantisipasi error** (misal pembagian nol).
- Konversi suhu: `F = C × 9/5 + 32`; `C = (F−32) × 5/9`; `K = C + 273.15`.
- BMI dihitung dari berat (kg) dibagi tinggi kuadrat (m); tinggi cm harus diubah ke meter.
- Selalu **uji program** dengan berbagai macam input.

---

## K. Glosarium 📖

| Istilah | Arti |
|---|---|
| **Input** | Data yang dimasukkan pengguna |
| **Proses** | Pengolahan data oleh program |
| **Output** | Hasil yang ditampilkan |
| **BMI** | Indeks massa tubuh: berat(kg)/tinggi(m)² |
| **f-string** | Format string untuk mencetak variabel |
| **Konversi** | Mengubah satuan/tipe nilai |
| **Error handling** | Penanganan kesalahan agar program tidak crash |

---

## L. Refleksi (Merefleksi) 🔍

- Manakah dari ketiga program (kalkulator, konversi, BMI) yang paling menantang? Mengapa?
- Mengapa penting menguji program dengan input yang tidak biasa?
- Bagaimana perasaanmu saat program pertamamu berhasil berjalan tanpa error?
- **Skala pemahaman diri:** ____/10
- Program sederhana apa yang ingin kamu buat sendiri selanjutnya?

---

**MGMP Informatika SMAN 6 Cimahi — Fase F (Kelas XI) Semester 2**