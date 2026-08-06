# TAHAP 3 — SOAL LATIHAN & KUNCI (Flowchart, Pseudocode, Python)
## Materi: Berpikir Komputasional → Pseudocode → Python

---

## SOAL 1 — Cek Kelulusan (Percabangan)
**Kasus:** Program membaca nilai, menampilkan "LULUS" jika ≥ 70, selain itu "TIDAK LULUS".

**Pseudocode (kunci):**
```
MULAI
    TAMPILKAN "Masukkan nilai: "
    BACA nilai
    JIKA nilai >= 70 MAKA
        TAMPILKAN "LULUS"
    SEBALIKNYA
        TAMPILKAN "TIDAK LULUS"
    AKHIR JIKA
SELESAI
```

**Python (kunci):**
```python
nilai = int(input("Masukkan nilai: "))
if nilai >= 70:
    print("LULUS")
else:
    print("TIDAK LULUS")
```

---

## SOAL 2 — Hitung 1 sampai 10 (Perulangan FOR)
**Kasus:** Menampilkan angka 1 sampai 10.

**Pseudocode (kunci):**
```
MULAI
    UNTUK i DARI 1 SAMPAI 10
        TAMPILKAN i
    AKHIR UNTUK
SELESAI
```

**Python (kunci):**
```python
for i in range(1, 11):
    print(i)
```

---

## SOAL 3 — Password Sampai Benar (Perulangan WHILE)
**Kasus:** Minta password berulang sampai password "rahasia123" dimasukkan.

**Pseudocode (kunci):**
```
MULAI
    BACA password
    SELAMA password != "rahasia123"
        TAMPILKAN "Salah, coba lagi"
        BACA password
    AKHIR SELAMA
    TAMPILKAN "Berhasil"
SELESAI
```

**Python (kunci):**
```python
password = input("Masukkan password: ")
while password != "rahasia123":
    print("Salah, coba lagi")
    password = input("Masukkan password: ")
print("Berhasil")
```

---

## SOAL 4 — Luas Persegi Panjang (Urutan)
**Kasus:** Baca panjang & lebar, hitung & tampilkan luas.

**Pseudocode (kunci):**
```
MULAI
    BACA panjang
    BACA lebar
    luas = panjang * lebar
    TAMPILKAN luas
SELESAI
```

**Python (kunci):**
```python
panjang = int(input("Panjang: "))
lebar = int(input("Lebar: "))
luas = panjang * lebar
print("Luas =", luas)
```

---

## SOAL 5 — Sistem Antrean Sederhana (List) — TANTANGAN
**Kasus:** Simulasikan antrean: tambah nama, layani yang paling depan, tampilkan antrean. Menu 1=Tambah, 2=Layani, 3=Tampilkan, 0=Keluar.

**Python (kunci):**
```python
antrean = []
while True:
    print("\n1. Tambah  2. Layani  3. Tampilkan  0. Keluar")
    pilihan = input("Pilih: ")
    if pilihan == "1":
        nama = input("Nama: ")
        antrean.append(nama)
    elif pilihan == "2":
        if antrean:
            print("Melayani", antrean.pop(0))
        else:
            print("Antrean kosong")
    elif pilihan == "3":
        print("Antrean:", antrean)
    elif pilihan == "0":
        print("Selesai")
        break
    else:
        print("Pilihan tidak valid")
```

---

## Catatan Penilaian (untuk guru)
- **Simbol flowchart benar** (oval/persegi/parallelogram/belah ketupat) = indicator pemahaman struktur.
- **Alur satu arah** — bedakan sequence vs decision vs loop.
- **Python:** mudah dibaca & idempotent (input sama → output sama).
- Di era AI, kunci jawaban inti = **cara berpikir (dekomposisi), bukan hafalan sintaks.**

---

**MGMP Informatika SMAN 6 Cimahi — Program Magang Guru Informatika TP 2026/2027**