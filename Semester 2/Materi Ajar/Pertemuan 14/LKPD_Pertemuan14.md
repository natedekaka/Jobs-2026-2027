# LEMBAR KERJA PESERTA DIDIK (LKPD)
## Pertemuan 14 – Python: List & Fungsi

| TP | BK 1.4, BK 2.1, BK 2.2 |
|---|---|
| Nama | ____________________ |
| Kelas | ____________________ |

---

### A. LIST DASAR (10 menit)

**Soal 1:** Buat list dan cetak isinya.

```python
nilai = [85, 90, 78, 92, 88]
print(nilai)
```

**Soal 2:** Akses beberapa elemen.

```python
print(nilai[2])       # indeks ke-2: ______
print(nilai[-1])      # elemen terakhir: ______
print(nilai[1:4])     # slicing 1-4: ______
```

**Soal 3:** Method list.

```python
nilai.append(95)      # tambah 95
print(nilai)          # ______

nilai.sort()
print(nilai)          # setelah diurutkan: ______

print(len(nilai))     # panjang list: ______
```

**Soal 4:** Cari rata-rata dengan loop FOR.

```python
nilai = [85, 90, 78, 92, 88]
total = 0
for n in nilai:
    total ____ n
rata = total / len(nilai)
print(f"Rata-rata: {rata}")
```
Output: _________

**Soal 5:** List of lists — data 3 siswa.

```python
data = [
    ["Andi", 85],
    ["Budi", 92],
    ["Cici", 78]
]

# Cetak nama dan nilai semua siswa
for siswa in data:
    print(f"{siswa[0]}: {siswa[1]}")
```

---

### B. FUNGSI (10 menit)

**Soal 6:** Fungsi sapa.

```python
def sapa(nama):
    print(f"Halo, {nama}!")

sapa("Andi")      # Output: ______
sapa("Budi")      # Output: ______
```

**Soal 7:** Fungsi luas segitiga.

```python
def luas_segitiga(alas, tinggi):
    return ______ * ______ / 2

print(luas_segitiga(10, 5))   # Output: ______
print(luas_segitiga(7, 3))    # Output: ______
```

**Soal 8:** Fungsi faktorial (dengan return).

```python
def faktorial(n):
    hasil = 1
    for i in range(1, n + 1):
        hasil ____ i
    return hasil

print(faktorial(5))   # Output: ______
print(faktorial(7))   # Output: ______
```

**Soal 9:** Fungsi cek prima (return True/False).

```python
def cek_prima(n):
    if n < 2:
        return ______
    for i in range(2, n):
        if n % i ____ 0:
            return False
    return ______

print(cek_prima(7))   # Output: ______
print(cek_prima(10))  # Output: ______
```

**Soal 10:** Fungsi sequential search.

```python
def cari(data, target):
    for i in range(len(____)):
        if data[i] == ____:
            return i
    return -1

angka = [5, 3, 8, 1, 6]
print(cari(angka, 8))    # Output: ______
print(cari(angka, 99))   # Output: ______
```

---

### C. STUDI KASUS — DATA NILAI SISWA (KELOMPOK — 15 menit)

Buat program lengkap menggunakan list + fungsi!

**Soal 11:** Program Data Nilai Siswa

Fitur yang harus ada:
1. Input jumlah siswa
2. Input nama dan nilai per siswa (simpan di list of lists)
3. Hitung rata-rata kelas (fungsi)
4. Cari nilai tertinggi (fungsi)
5. Tampilkan siswa lulus (≥75) dan remidi (<75) (fungsi)

```python
def input_data(jumlah):
    data = []
    for i in range(jumlah):
        nama = input(f"Nama siswa ke-{i+1}: ")
        nilai = float(input(f"Nilai {nama}: "))
        data.______([nama, nilai])
    return data

def rata_rata(data):
    total = 0
    for siswa in data:
        total += ______[1]
    return total / len(data)

def nilai_tertinggi(data):
    terbaik = data[0]
    for siswa in data:
        if ______[1] > terbaik[1]:
            terbaik = siswa
    return terbaik

def kelulusan(data):
    lulus = []
    remidi = []
    for siswa in data:
        if siswa[1] >= 75:
            lulus.______(siswa)
        else:
            remidi.______(siswa)
    return lulus, remidi

# ===== MAIN =====
n = int(input("Jumlah siswa: "))
data = input_data(n)

print(f"Rata-rata kelas: {rata_rata(data):.2f}")

terbaik = nilai_tertinggi(data)
print(f"Nilai tertinggi: {terbaik[0]} ({terbaik[1]})")

lulus, remidi = kelulusan(data)
print(f"Lulus: {len(lulus)} orang")
for s in lulus:
    print(f"  {s[0]}: {s[1]}")
print(f"Remidi: {len(remidi)} orang")
for s in remidi:
    print(f"  {s[0]}: {s[1]}")
```

**Test:**
Jumlah siswa: 3
- Andi, 85
- Budi, 72
- Cici, 90

| Fitur | Output |
|---|---|
| Rata-rata | |
| Tertinggi | |
| Lulus | |
| Remidi | |

---

### D. REFLEKSI

| Pertanyaan | Jawaban |
|---|---|
| Apa hubungan array (Pert 1) dengan list Python? | |
| Kenapa fungsi penting dalam programming? | |
| Bedanya parameter dan return? | |
| Kesulitan hari ini? | |
| Skala pemahaman (1–10) | / 10 |

---

### E. TUGAS RUMAH

Selesaikan program data nilai siswa + tambah fitur urutkan nilai descending (tertinggi ke terendah)!

```python
# Fitur tambahan
def urutkan_nilai(data):
    # Gunakan sorting — urut descending
    # ...
```

---

**MGMP Informatika SMAN 6 Cimahi**
