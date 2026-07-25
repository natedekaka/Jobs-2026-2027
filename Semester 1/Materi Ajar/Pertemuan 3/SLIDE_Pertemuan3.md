---
marp: true
theme: uncover
class: invert
---

# PERTEMUAN 3
## Simulasi Dinamika Input-Proses-Output (IPO)
### Informatika – Fase E / Kelas X
#### SMA Negeri 6 Cimahi

---

## Review — Diagram Von Neumann

Tunjukkan diagram tugas rumah kalian!

**3 siswa maju** mempresentasikan diagramnya.

> Komponen apa yang paling sulit digambar? Mengapa?

---

## Apersepsi

**Coba lihat ini:**

Gelas kosong + kertas angka

> Kalau gelas = **Memori (RAM)** dan kertas = **Data**
> Bagaimana CPU menaruh data dan mengambilnya kembali?

---

# TUJUAN PEMBELAJARAN

1. ✅ Memahami konsep **alamat memori**
2. ✅ Membedakan operasi **READ** dan **WRITE**
3. ✅ Menjalankan simulasi eksekusi program sederhana
4. ✅ Menganalisis alur IPO pada studi kasus nyata

---

# KONSEP ALAMAT MEMORI

---

## Memori = Deretan Loker

```
Alamat:  0    1    2    3    4    5    6    7
        ┌────┬────┬────┬────┬────┬────┬────┬────┐
Data:   │ 7  │ 3  │ 0  │ 5  │ 2  │ 9  │ 4  │ 6  │
        └────┴────┴────┴────┴────┴────┴────┴────┘
```

| Analogi | Komputer |
|---|---|
| Kompleks perumahan | Memori (RAM) |
| Nomor rumah | Alamat (0, 1, 2, ...) |
| Orang di rumah | Data |
| Kurir | CPU (via Bus) |

---

## Dua Operasi Dasar CPU ↔ Memori

### READ (Load)
```
CPU → "Ambil data dari alamat 3"
    ← Data 5 diterima CPU
Data di alamat 3 TETAP ada (disalin)
```

### WRITE (Store)
```
CPU → "Simpan angka 100 ke alamat 5"
Data LAMA di alamat 5 HILANG, diganti 100
```

---

# CLOCK SPEED

---

## Detak Clock CPU

### CPU bekerja seperti irama drum:

```
┌───┬───┬───┬───┬───┬───┬───┬───┐
│ ♩ │ ♩ │ ♩ │ ♩ │ ♩ │ ♩ │ ♩ │ ♩ │
└───┴───┴───┴───┴───┴───┴───┴───┘
  1 siklus clock
```

| Istilah | Arti |
|---|---|
| **1 Clock Cycle** | Satu detak — satu langkah kerja CPU |
| **Clock Speed** | 3 GHz = 3 miliar detak/detik |
| **1 Instruksi** | Butuh 1–4 clock cycle |

---

# SIMULASI 1 — "POS INDONESIA"

---

## Persiapan

- **10 kartu/kotak** bernomor 0–9 di lantai = Memori
- Setiap kotak berisi angka = Data
- **Pemain:** CPU, CU, ALU, Bus

### Instruksi 1: READ
> "Baca data dari alamat 3"

### Instruksi 2: WRITE
> "Tulis angka 15 ke alamat 7"

---

## DEMO READ

```
CU → "Baca alamat 3!"
Bus → ambil data dari alamat 3
   → bawa ke CPU
CPU → "Data dari alamat 3 adalah 5"

Data di alamat 3 TIDAK HILANG
```

---

## DEMO WRITE

```
CPU → "Simpan 15 ke alamat 7!"
Bus → bawa 15 ke alamat 7
   → data LAMA di alamat 7 DIHAPUS
   → data BARU = 15

Data di alamat 7 sekarang 15
```

---

# SIMULASI 2 — "EKSEKUSI PROGRAM"

---

## Program: (5 + 3) × 2

**Kondisi Awal Memori:**

| Alamat | 0 | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9 | 10 |
|---|---|---|---|---|---|---|---|---|---|---|---|
| Isi | LOAD5 | LOAD6 | ADD | LOAD8 | MUL | STORE7 | HALT | - | 5 | 3 | 2 |

**Pemain:**
- 🅰 PC (Program Counter) — menunjuk alamat
- 🅱 Control Unit — membaca instruksi
- 🅲 ALU — menghitung
- 🅳 Register A — data pertama
- 🅴 Register B — data kedua
- 🅵 Memori — menulis hasil

---

## Langkah 1–2: LOAD

### PC=0 → LOAD 5
```
CU: "Ambil data dari alamat 5"
Register A ← memori[5] = 5
```

### PC=1 → LOAD 6
```
CU: "Ambil data dari alamat 6"
Register B ← memori[6] = 3
```

| Register A | Register B |
|---|---|
| **5** | **3** |

---

## Langkah 3: ADD

### PC=2 → ADD
```
CU: "Jumlahkan Register A dan Register B!"
ALU: 5 + 3 = 8
Register A ← 8
```

| Register A | Register B |
|---|---|
| **8** | **3** |

---

## Langkah 4–5: LOAD & MUL

### PC=3 → LOAD 8
```
Register B ← memori[8] = 2
```

### PC=4 → MUL
```
ALU: 8 × 2 = 16
Register A ← 16
```

| Register A | Register B |
|---|---|
| **16** | **2** |

---

## Langkah 6–7: STORE & HALT

### PC=5 → STORE 7
```
memori[7] ← Register A = 16
```

### PC=6 → HALT
```
Program selesai!
```

**Hasil:** Alamat 7 berisi **16** ✅

---

## Studi Kasus — Diskusi Kelompok

**Pilih 1 kasus, tulis alur IPO-nya di LKPD!**

| Kasus | Deskripsi |
|---|---|
| A | Membuka kamera HP & mengambil foto |
| B | Mencetak dari Word ke printer |
| C | Menonton video YouTube |

**Waktu:** 10 menit, presentasi 2 kelompok

---

## Refleksi

### Diskusi:
1. Apa yang terjadi jika alamat 5 berisi 100 (bukan 5)?
2. Kenapa CPU perlu **Register**? Kenapa tidak langsung akses memori?
3. Proses mana yang paling lambat dalam simulasi tadi?

### Tulis di LKPD:
- Skala pemahamanmu hari ini: ___ / 10
- Satu hal yang ingin kamu tanyakan

---

## Rangkuman

| No | Poin Penting |
|---|---|
| 1 | **Alamat memori** = nomor unik lokasi penyimpanan di RAM |
| 2 | **READ** = salin data (sumber tetap), **WRITE** = timpa data (lama hilang) |
| 3 | **Siklus Mesin**: Fetch → Decode → Execute → Store |
| 4 | **Program Counter** menunjuk instruksi yang akan dijalankan |
| 5 | **Clock speed** = kecepatan detak CPU (miliaran siklus/detik) |

---

## Tugas Rumah

### Tulis alur IPO untuk:
**"Menghitung rata-rata 3 nilai ulangan"**

Gunakan format tabel seperti simulasi tadi!

| Langkah | PC | Instruksi | A | B | Hasil |
|---|---|---|---|---|---|

> Kumpulkan pertemuan depan!

---

## Pertemuan Berikutnya

### Sistem Operasi & Perannya

> Bagaimana OS mengatur memori, proses, dan file?

---

# Terima Kasih

### MGMP Informatika SMAN 6 Cimahi

> "Di dalam CPU, miliaran transistor bekerja dalam irama clock — mengubah data menjadi informasi."
