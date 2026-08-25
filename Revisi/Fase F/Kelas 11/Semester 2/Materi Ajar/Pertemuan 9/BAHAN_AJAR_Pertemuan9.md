# BAHAN AJAR – PERTEMUAN 9 (S2)
## Program Sederhana 2 — To-Do List, Nilai Siswa, dan Kuis
*Mengacu pada Panduan Mapel 2025; INFORMATIKA Fase D-F — pendekatan Pembelajaran Mendalam (Memahami → Mengaplikasi → Merefleksi)*

| Informasi | Keterangan |
|---|---|
| **Fase / Kelas** | F / Kelas XI |
| **Alokasi Waktu** | 5 JP × 45 menit (225 menit) |
| **Elemen CP** | Analisis Data & Algoritma Pemrograman (AP) |
| **Tujuan Pembelajaran** | Membuat program To-Do List, pengelolaan nilai siswa, dan kuis interaktif; menggabungkan fungsi, list, dan perulangan dalam satu program |
| **Materi Prasyarat** | Semua materi Python (Pertemuan 1-8) |

---

## A. Kisah Pemantik 🎬

> **"Aplikasi Catatan untuk Sekretaris Kelas"**
>
> Sekretaris kelas kewalahan mencatat daftar tugas, rekap nilai teman-teman, dan menyiapkan kuis. Semua itu bisa diotomatisasi dengan program! Bayangkan: menambah tugas baru, melihat semua tugas, menghapus tugas yang selesai — semua hanya dengan beberapa klik.
>
> Program semacam itu menggabungkan **list** (tempat menyimpan data), **perulangan** (menampilkan semua isi), **percabangan** (memilih menu), dan **fungsi** (memecah tiap fitur).
>
> **Pertanyaan pemantik:** Program apa lagi di sekolah atau rumah yang bisa kamu buat dari kombinasi list, loop, dan percabangan?

---

## B. Konsep Inti: Menu, List, dan Loop 🔄

| Konsep | Peran dalam Program |
|---|---|
| **Menu** | Memberi pilihan aksi (tambah, lihat, hapus, keluar) |
| **List** | Menyimpan banyak data (tugas, nilai, soal) |
| **Loop `while True`** | Menjalankan menu berulang sampai user memilih keluar |
| **`break`** | Keluar dari loop saat menu "keluar" dipilih |
| **Dictionary** | Menyimpan data berpasangan (nama & nilai) |

**Pola menu umum:**
```python
while True:
    pilihan = input("Menu (1/2/3/4): ")
    if pilihan == "1":
        # aksi 1
    elif pilihan == "4":
        break
```

> 💡 **`while True`** membuat program terus berjalan sampai user memilih keluar. Ini pola standar untuk aplikasi menu.

---

## C. Program 1: To-Do List ✅

```python
tugas = []

while True:
    print("\n1. Lihat  2. Tambah  3. Hapus  4. Keluar")
    p = input("Pilih: ")

    if p == "1":
        if not tugas:
            print("[Kosong]")
        for i, t in enumerate(tugas, 1):
            print(f"{i}. {t}")

    elif p == "2":
        tugas.append(input("Tugas baru: "))

    elif p == "3":
        try:
            no = int(input("No: ")) - 1
            if 0 <= no < len(tugas):
                print(f"'{tugas.pop(no)}' dihapus")
            else:
                print("Nomor tidak valid")
        except ValueError:
            print("Masukkan angka!")

    elif p == "4":
        break
```

**Output (contoh alur):**
```
1. Lihat  2. Tambah  3. Hapus  4. Keluar
Pilih: 2
Tugas baru: Belajar Python
1. Lihat  2. Tambah  3. Hapus  4. Keluar
Pilih: 1
1. Belajar Python
```

---

## D. Program 2: Pengelolaan Nilai Siswa 📊

```python
siswa = []
n = int(input("Jumlah siswa: "))

for i in range(n):
    nama = input(f"Nama {i+1}: ")
    nilai = float(input(f"Nilai {nama}: "))
    siswa.append({"nama": nama, "nilai": nilai})

print("\n=== LAPORAN NILAI ===")
total = 0
for s in siswa:
    status = "Lulus" if s["nilai"] >= 70 else "Tidak Lulus"
    print(f"{s['nama']:15} {s['nilai']:<8.1f} {status}")
    total += s["nilai"]

rata = total / n
nilai_max = max(s["nilai"] for s in siswa)
nilai_min = min(s["nilai"] for s in siswa)
print(f"\nRata-rata: {rata:.1f}")
print(f"Tertinggi: {nilai_max}")
print(f"Terendah: {nilai_min}")
```

**Output (jika input 2 siswa: Ani 85, Budi 65):**
```
=== LAPORAN NILAI ===
Ani             85.0     Lulus
Budi            65.0     Tidak Lulus

Rata-rata: 75.0
Tertinggi: 85.0
Terendah: 65.0
```

---

## E. Program 3: Kuis Interaktif ❓

```python
soal = [
    {"q": "Ibu kota Indonesia?", "a": ["a. Bandung", "b. Surabaya", "c. Jakarta", "d. Jogja"], "k": "c"},
    {"q": "Penemu hukum gravitasi?", "a": ["a. Einstein", "b. Newton", "c. Galileo", "d. Archimedes"], "k": "b"},
]

skor = 0
for i, s in enumerate(soal, 1):
    print(f"\n{i}. {s['q']}")
    for o in s['a']:
        print(o)
    jawab = input("Jawab: ").lower()
    if jawab == s['k']:
        print("Benar!")
        skor += 1
    else:
        print(f"Salah! Jawaban: {s['k']}")

print(f"\nSkor: {skor}/{len(soal)}")
```

**Output (jika jawaban benar semua):**
```
1. Ibu kota Indonesia?
a. Bandung
b. Surabaya
c. Jakarta
d. Jogja
Jawab: c
Benar!

2. Penemu hukum gravitasi?
a. Einstein
b. Newton
c. Galileo
d. Archimedes
Jawab: b
Benar!

Skor: 2/2
```

---

## F. Teknik Pendukung 🛠️

**`enumerate(list, mulai)`** — mendapatkan indeks dan nilai sekaligus.

```python
buah = ["apel", "mangga", "jeruk"]
for i, b in enumerate(buah, 1):
    print(f"{i}. {b}")
```
**Output:**
```
1. apel
2. mangga
3. jeruk
```

**`try/except`** — menangani input yang salah agar program tidak crash.

```python
try:
    angka = int(input("Angka: "))
    print(angka * 2)
except ValueError:
    print("Harus berupa angka!")
```

**`max()` / `min()` / `sum()`** — fungsi bawaan untuk analisis cepat.

```python
nilai = [80, 90, 70]
print(sum(nilai))    # 240
print(max(nilai))    # 90
print(min(nilai))    # 70
```

---

## G. Contoh Soal & Penyelesaian 📝

**Contoh 1:** Jelaskan bagaimana `while True` dan `break` bekerja dalam To-Do List.
**Jawaban:** `while True` membuat menu tampil berulang. Setiap iterasi, user memilih aksi. Ketika user memilih opsi "Keluar", perintah `break` menghentikan perulangan sehingga program berakhir. Tanpa `break`, program tidak akan pernah berhenti.

**Contoh 2:** Tulis program yang menerima nilai 3 siswa lalu menampilkan status lulus/tidak lulus.
**Jawaban:**
```python
siswa = []
for i in range(3):
    nama = input(f"Nama {i+1}: ")
    nilai = float(input(f"Nilai {nama}: "))
    siswa.append({"nama": nama, "nilai": nilai})

for s in siswa:
    status = "Lulus" if s["nilai"] >= 70 else "Tidak Lulus"
    print(f"{s['nama']}: {s['nilai']} -> {status}")
```
**Output (jika Ani 85, Budi 60, Citra 75):**
```
Ani: 85.0 -> Lulus
Budi: 60.0 -> Tidak Lulus
Citra: 75.0 -> Lulus
```

**Contoh 3:** Mengapa `try/except` penting dalam program dengan `int(input())`?
**Jawaban:** Jika user mengetik huruf saat program meminta angka, `int()` memunculkan `ValueError` dan program berhenti. Dengan `try/except`, error ditangkap dan program menampilkan pesan ramah lalu melanjutkan, sehingga aplikasi tidak crash.

**Contoh 4:** Buat kuis satu soal dengan pilihan jawaban dan penilaian skor.
**Jawaban:** Gunakan struktur seperti pada bagian E dengan satu dictionary soal, lalu cetak "Benar"/"Salah" dan skor akhir `skor/1`.

**Contoh 5:** Apa fungsi `enumerate(tugas, 1)` pada program To-Do List?
**Jawaban:** `enumerate` menghasilkan pasangan (indeks, nilai). Parameter `1` membuat penomoran dimulai dari 1, sehingga user melihat daftar bernomor `1, 2, 3` — lebih mudah dipahami daripada indeks mulai 0.

---

## H. Miskonsepsi & Kesalahan Umum 🚫

| Miskonsepsi / Kesalahan | Fakta yang Benar |
|---|---|
| "Program menu tidak perlu `break`" | Tanpa `break`, menu `while True` tidak akan pernah berhenti |
| "`input()` angka langsung bisa dihitung" | Harus dikonversi dulu dengan `int()`/`float()` |
| "Data hilang saat program ditutup" | Benar, data hanya di memori; menyimpan ke file butuh teknik tambahan |
| "`try/except` hanya untuk pembagian nol" | `try/except` menangani berbagai error, misal `ValueError` pada `int()` |
| "Satu program hanya boleh satu list" | Program bisa memakai banyak list/dictionary sekaligus |
| "Menampilkan list tanpa nomor urut tidak masalah" | Nomor urut (`enumerate`) memudahkan pengguna memilih item |

---

## I. Tantangan Praktik (Mengaplikasi) 🎯

**Tantangan 1 — To-Do List Dasar (Mudah):** Buat program daftar tugas dengan fitur tambah dan lihat, memakai `while True` dan `break`.

**Tantangan 2 — Nilai dengan Predikat (Sedang):** Kembangkan program nilai dengan predikat A (≥85), B (≥70), C (≥55), D (<55), serta rata-rata, tertinggi, dan terendah.

**Tantangan 3 — Kuis 5 Soal (Sedang):** Buat kuis 5 soal pilihan ganda dari berbagai mata pelajaran, tampilkan skor akhir, dan beri tanggapan "Hebat!" jika skor ≥ 4.

**Tantangan 4 — Catatan Keuangan (Sulit):** Buat program mencatat pemasukan dan pengeluaran, tampilkan saldo, dan peringatkan jika saldo negatif.

**Tantangan 5 — Tebak Angka BerSkor (Sulit):** Komputer memilih angka 1-20; user menebak dengan jumlah kesempatan terbatas; tampilkan skor berdasarkan sisa kesempatan.

---

## J. Rangkuman Kunci 🔑

- Program menu memakai **`while True`** + **`break`**.
- **List** dan **dictionary** menyimpan data; loop menampilkannya.
- **`enumerate(list, 1)`** memberi nomor urut mulai dari 1.
- **`try/except`** menangani input salah agar program tidak crash.
- `max()`, `min()`, `sum()` untuk analisis data cepat.
- To-Do List, pengelolaan nilai, dan kuis adalah contoh aplikasi yang menggabungkan seluruh materi Python.
- Data di memori akan hilang saat program ditutup — pengamanan data butuh teknik penyimpanan ke file.

---

## K. Glosarium 📖

| Istilah | Arti |
|---|---|
| **Menu** | Pilihan aksi yang ditampilkan program |
| **while True** | Perulangan tanpa batas sampai `break` |
| **Dictionary** | Tipe data berpasangan kunci-nilai |
| **enumerate** | Fungsi memberi indeks saat iterasi |
| **try/except** | Mekanisme penanganan error |
| **ValueError** | Error karena konversi tipe gagal |
| **Break** | Menghentikan perulangan |

---

## L. Refleksi (Merefleksi) 🔍

- Dari tiga program (To-Do List, Nilai, Kuis), mana yang paling berguna bagimu? Mengapa?
- Apa tantangan terbesar saat menggabungkan banyak konsep dalam satu program?
- Bagaimana perasaanmu ketika program menu berhasil berjalan tanpa error?
- **Skala pemahaman diri:** ____/10
- Program apa yang ingin kamu kembangkan lebih lanjut di Pertemuan 10 (Review)?

---

**MGMP Informatika SMAN 6 Cimahi — Fase F (Kelas XI) Semester 2**