# ASESMEN – PERTEMUAN 14
## Python: List & Fungsi

Informatika – Fase E / Kelas X – SMA Negeri 6 Cimahi

---

## Rubrik Penilaian

### A. List Dasar (Bobot 25%)

| Kriteria | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| Membuat & akses list | Tidak bisa | Sebagian | Benar | Benar + slicing |
| Method (append, sort, len) | Tidak bisa | Sebagian | Benar | Benar + eksplorasi |
| Loop & rata-rata | Tidak | Logika salah | Benar | Benar + rapi |
| List of lists | Tidak | Sebagian | Benar | Benar + akses |

### B. Fungsi (Bobot 30%)

| Kriteria | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| def + parameter | Tidak bisa | Struktur salah | Benar | Benar + default param |
| return | Tidak bisa | Salah tipe | Benar | Benar + multiple return |
| Fungsi faktorial/prima/search | 0/3 selesai | 1/3 | 2/3 | 3/3 + rapi |

### C. Studi Kasus Data Nilai (Bobot 45%)

| Kriteria | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| Input data (list of lists) | Tidak selesai | Error | Benar | Benar + rapi |
| Fungsi rata-rata | Tidak | Logika salah | Benar | Benar + format |
| Fungsi nilai tertinggi | Tidak | Logika salah | Benar | Benar + handle |
| Fungsi kelulusan | Tidak | Logika salah | Benar | Benar + rapi |
| Program jalan & test case | 0/3 | 1/3 | 2/3 | 3/3 |

---

## Kunci Jawaban LKPD

### A. List

**Soal 2:**
- `nilai[2]` = 78
- `nilai[-1]` = 88
- `nilai[1:4]` = [90, 78, 92]

**Soal 3:**
- `nilai.append(95)` → [85, 90, 78, 92, 88, 95]
- `nilai.sort()` → [78, 85, 88, 90, 92, 95]
- `len(nilai)` = 6

**Soal 4:**
```python
total += n
```
Rata-rata = (85+90+78+92+88)/5 = 86.6

**Soal 5:**
```
Andi: 85
Budi: 92
Cici: 78
```

### B. Fungsi

**Soal 6:** `Halo, Andi!`, `Halo, Budi!`

**Soal 7:** `return alas * tinggi / 2`
- luas(10,5) = 25
- luas(7,3) = 10.5

**Soal 8:** `hasil *= i`
- faktorial(5) = 120
- faktorial(7) = 5040

**Soal 9:**
```python
def cek_prima(n):
    if n < 2:
        return False
    for i in range(2, n):
        if n % i == 0:
            return False
    return True
```
- cek_prima(7) = True
- cek_prima(10) = False

**Soal 10:**
```python
def cari(data, target):
    for i in range(len(data)):
        if data[i] == target:
            return i
    return -1
```
- cari(8) = 2
- cari(99) = -1

### C. Studi Kasus

Test: 3 siswa (Andi 85, Budi 72, Cici 90)

| Fitur | Output |
|---|---|
| Rata-rata | 82.33 |
| Tertinggi | Cici (90) |
| Lulus | Andi (85), Cici (90) |
| Remidi | Budi (72) |

### Tugas Rumah — Urutkan Nilai
```python
def urutkan_nilai(data):
    # Bubble sort descending
    for i in range(len(data) - 1):
        for j in range(len(data) - 1 - i):
            if data[j][1] < data[j + 1][1]:
                data[j], data[j + 1] = data[j + 1], data[j]
    return data
```

Atau lebih sederhana:
```python
def urutkan_nilai(data):
    data.sort(key=lambda x: x[1], reverse=True)
    return data
```

---

**MGMP Informatika SMAN 6 Cimahi**
