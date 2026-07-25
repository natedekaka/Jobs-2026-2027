# PROYEK AKHIR – INFORMATIKA FASE E
## Semester 2 — SMA Negeri 6 Cimahi

| | |
|---|---|
| **Nama** | ____________________ |
| **Kelas** | ____________________ |
| **Opsi Proyek** | A / B / C (lingkari) |
| **Tanggal** | ____________________ |

---

### Ketentuan Umum

1. Kerjakan **individu**
2. Waktu: **45 menit** (hari ini) + dapat dilanjutkan di rumah
3. Kumpulkan: file `.py` + screenshot hasil run
4. Gunakan **Google Colab** atau **Python IDLE**
5. Semua proyek harus menggunakan:
   - ✅ `print()` dan `input()`
   - ✅ `if-elif-else`
   - ✅ Perulangan (FOR atau WHILE)
   - ✅ List (minimal 1 list)
   - ✅ Fungsi (minimal 1 fungsi `def`)

---

## OPSI A: KALKULATOR SEDERHANA

### Spesifikasi

Buat program kalkulator dengan menu:

```
=== KALKULATOR ===
1. Tambah
2. Kurang
3. Kali
4. Bagi
5. Keluar
Pilih (1-5):
```

### Fitur Wajib
1. Menu muncul berulang sampai user pilih 5
2. Input dua angka
3. Tampilkan hasil operasi
4. Validasi: jika bagi dengan 0 → tampilkan error

### Fitur Tambahan (bonus)
- Pangkat (6)
- Akar kuadrat (7)
- Riwayat perhitungan (simpan di list, tampilkan)

### Contoh Output
```
=== KALKULATOR ===
1. Tambah
2. Kurang
3. Kali
4. Bagi
5. Keluar
Pilih (1-5): 1
Angka 1: 10
Angka 2: 5
10 + 5 = 15

=== KALKULATOR ===
... (menu lagi)
```

### Kode Awal
```python
def tambah(a, b):
    return a + b

def kurang(a, b):
    return a - b

def kali(a, b):
    return a * b

def bagi(a, b):
    if b == 0:
        return "Error: pembagian dengan 0"
    return a / b

# ===== MAIN =====
while True:
    print("\n=== KALKULATOR ===")
    print("1. Tambah")
    print("2. Kurang")
    print("3. Kali")
    print("4. Bagi")
    print("5. Keluar")
    
    pilihan = int(input("Pilih (1-5): "))
    
    if pilihan == 5:
        print("Terima kasih!")
        break
    
    a = float(input("Angka 1: "))
    b = float(input("Angka 2: "))
    
    if pilihan == 1:
        print(f"{a} + {b} = {tambah(a, b)}")
    elif pilihan == 2:
        print(f"{a} - {b} = {kurang(a, b)}")
    elif pilihan == 3:
        print(f"{a} × {b} = {kali(a, b)}")
    elif pilihan == 4:
        print(f"{a} ÷ {b} = {bagi(a, b)}")
    else:
        print("Pilihan tidak valid!")
```

---

## OPSI B: PROGRAM CATATAN NILAI

### Spesifikasi

Buat program untuk mencatat dan menganalisis nilai siswa.

### Fitur Wajib
1. Input data siswa (nama + nilai) berulang sampai user ketik "selesai"
2. Simpan di **list of lists**: `[[nama, nilai], ...]`
3. Tampilkan:
   - Rata-rata kelas
   - Nilai tertinggi (nama + nilai)
   - Nilai terendah (nama + nilai)
   - Jumlah siswa lulus (≥75) dan remidi (<75)
   - Daftar siswa diurutkan dari nilai tertinggi

### Fitur Tambahan (bonus)
- Simpan data ke file (jika sudah belajar file I/O)
- Tampilkan grafik sederhana dengan `===`

### Contoh Output
```
=== CATATAN NILAI ===
Masukkan data (ketik "selesai" untuk stop)
Nama: Andi
Nilai: 85
Nama: Budi
Nilai: 72
Nama: Cici
Nilai: 90
Nama: selesai

=== HASIL ANALISIS ===
Jumlah siswa: 3
Rata-rata: 82.33
Tertinggi: Cici (90)
Terendah: Budi (72)
Lulus: 2 orang
Remidi: 1 orang

Peringkat:
1. Cici: 90
2. Andi: 85
3. Budi: 72
```

### Kode Awal
```python
def input_data():
    data = []
    print("Masukkan data (ketik \"selesai\" untuk stop)")
    while True:
        nama = input("Nama: ")
        if nama.lower() == "selesai":
            break
        nilai = float(input(f"Nilai {nama}: "))
        data.append([nama, nilai])
    return data

def rata_rata(data):
    total = sum(siswa[1] for siswa in data)
    return total / len(data)

def tertinggi(data):
    terbaik = data[0]
    for siswa in data:
        if siswa[1] > terbaik[1]:
            terbaik = siswa
    return terbaik

def terendah(data):
    terburuk = data[0]
    for siswa in data:
        if siswa[1] < terburuk[1]:
            terburuk = siswa
    return terburuk

# Lanjutkan: fungsi lulus/remidi, urutkan, main...
```

---

## OPSI C: GAME TEBAK ANGKA

### Spesifikasi

Buat game tebak angka dengan skor.

### Fitur Wajib
1. Angka rahasia: `random.randint(1, 100)`
2. Pemain menebak angka
3. Petunjuk: "Terlalu besar!" / "Terlalu kecil!"
4. Hitung jumlah tebakan
5. Simpan **riwayat tebakan** di list
6. Tampilkan riwayat tebakan setelah selesai
7. Skor: 100 - (jumlah_tebakan × 5) — minimal 0

### Fitur Tambahan (bonus)
- Main lagi (tanpa restart program)
- Batasi tebakan maksimal 10 kali
- Simpan high score

### Contoh Output
```
=== GAME TEBAK ANGKA ===
Tebak angka antara 1-100

Tebakan ke-1: 50
Terlalu besar!

Tebakan ke-2: 25
Terlalu kecil!

Tebakan ke-3: 37
Terlalu kecil!

Tebakan ke-4: 43
Terlalu besar!

Tebakan ke-5: 40
🎉 SELAMAT! Tebakan benar!

Riwayat tebakan: [50, 25, 37, 43, 40]
Jumlah tebakan: 5
Skor: 75
```

### Kode Awal
```python
import random

def main():
    print("=== GAME TEBAK ANGKA ===")
    print("Tebak angka antara 1-100\n")
    
    rahasia = random.randint(1, 100)
    tebakan = 0
    jumlah = 0
    riwayat = []
    
    while tebakan != rahasia:
        tebakan = int(input(f"Tebakan ke-{jumlah + 1}: "))
        riwayat.append(tebakan)
        jumlah += 1
        
        if tebakan < rahasia:
            print("Terlalu kecil!\n")
        elif tebakan > rahasia:
            print("Terlalu besar!\n")
    
    print(f"\n🎉 SELAMAT! Tebakan benar!")
    print(f"Riwayat tebakan: {riwayat}")
    print(f"Jumlah tebakan: {jumlah}")
    skor = max(0, 100 - (jumlah * 5))
    print(f"Skor: {skor}")

main()
```

---

## Rubrik Penilaian Proyek

| Aspek | Bobot | 1 | 2 | 3 | 4 |
|---|---|---|---|---|---|
| **Fungsionalitas** | 30% | Tidak jalan | Sebagian fitur | Semua fitur wajib | Semua fitur + validasi |
| **Struktur Kode** | 25% | Berantakan | Variabel jelas | Fungsi + loop + if rapi | Modular + efisien |
| **List & Fungsi** | 20% | Tidak ada | Ada 1 | Ada list + fungsi | Digunakan dengan baik |
| **Kreativitas** | 15% | Minimal | 1 fitur tambahan | 2+ fitur tambahan | Fitur unik + rapi |
| **Presentasi** | 10% | Tidak demo | Demo sebagian | Demo semua | Demo + jelas |

---

**MGMP Informatika SMAN 6 Cimahi**
