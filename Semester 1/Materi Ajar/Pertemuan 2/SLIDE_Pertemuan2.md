---
marp: true
theme: uncover
class: invert
---

# PERTEMUAN 2
## Model Arsitektur Von Neumann & Input-Proses-Output (IPO)
### Informatika – Fase E / Kelas X
#### SMA Negeri 6 Cimahi

---

## Review — Pertemuan 1

Sebutkan **1 komponen komputer** dan fungsinya!

| Komponen | Fungsi |
|---|---|
| CPU | ________________ |
| RAM | ________________ |
| Hard Disk | ________________ |
| Monitor | ________________ |
| Keyboard | ________________ |

---

## Apersepsi

**Coba tebak jalurnya!**

Kamu mengetik huruf **A** di keyboard, lalu huruf itu muncul di layar monitor.

> Menurutmu, bagaimana urutan perjalanan data dari keyboard sampai ke monitor?

---

# TUJUAN PEMBELAJARAN

1. ✅ Menjelaskan arsitektur Von Neumann dan komponennya
2. ✅ Menggambarkan diagram blok Von Neumann
3. ✅ Menjelaskan alur IPO dalam sistem komputer
4. ✅ Melakukan simulasi sederhana IPO

---

# ARSITEKTUR VON NEUMANN

---

## John von Neumann (1903–1957)

| | |
|---|---|
| Matematikawan Hungaria-Amerika | |
| Kontribusi: arsitektur komputer, game theory, quantum mechanics | |
| **1945** — First Draft of a Report on the EDVAC | |

> **Ide revolusioner:** Program dan data disimpan di memori yang sama
> → **Stored Program Concept**

---

## Komponen Utama Von Neumann

```
┌──────────┐     ┌─────────────────────┐     ┌──────────┐
│  INPUT   │────→│        CPU          │────→│  OUTPUT  │
│(Keyboard)│     │  ┌───────┬───────┐  │     │(Monitor) │
└──────────┘     │  │ ALU  │  CU   │  │     └──────────┘
                 │  └───┬───┴───┬───┘  │
                 └──────┼───────┼──────┘
                        │       │
                        ▼       ▼
                 ┌──────────────────┐
                 │     MEMORI      │
                 │  (RAM/ROM)      │
                 └──────────────────┘
      SEMUA TERHUBUNG VIA BUS
```

---

## Central Processing Unit (CPU)

### Tiga Bagian Utama:

| Bagian | Fungsi |
|---|---|
| **ALU** | Aritmatika (+, -, ×, ÷) & Logika (=, >, <, AND, OR) |
| **Control Unit** | Mengatur & mengkoordinasi semua aktivitas |
| **Register** | Memori kecepatan tinggi di dalam CPU |

### Siklus Kerja CPU:
```
FETCH → DECODE → EXECUTE → STORE
```

---

## Memori — Stored Program Concept

### Inilah kunci arsitektur Von Neumann:

| Konsep | Penjelasan |
|---|---|
| **Program & data** disimpan di **memori yang sama** | Instruksi program dan data berada di satu ruang alamat |
| **Alamat memori** | Setiap lokasi memori punya alamat unik (seperti nomor rumah) |
| CPU membaca instruksi dari memori → eksekusi → simpan hasil | |

> Tanpa konsep ini, kita harus ganti hardware untuk setiap program berbeda!

---

## Bus System

| Bus | Fungsi |
|---|---|
| **Data Bus** | Membawa data antar komponen |
| **Address Bus** | Membawa alamat memori |
| **Control Bus** | Membawa sinyal kontrol |

---

## Model IPO — Input-Proses-Output

### Aliran Data Dasar:

```
┌──────────┐    ┌──────────┐    ┌──────────┐
│  INPUT   │───→│  PROSES  │───→│  OUTPUT  │
│          │    │  (CPU)   │    │          │
└──────────┘    └────┬─────┘    └──────────┘
                     │
                     ▼
              ┌──────────────┐
              │   STORAGE    │
              │  (RAM/HDD)   │
              └──────────────┘
```

---

## Contoh IPO 1: Mengetik Huruf

| Tahap | Proses |
|---|---|
| **Input** | Tombol 'H' ditekan |
| **CPU** | → kode ASCII 72 diterjemahkan |
| **RAM** | → disimpan sementara |
| **Output** | → huruf 'H' tampil di layar |
| **Storage** | → saat Save, pindah ke Hard Disk |

---

## Contoh IPO 2: Membuka Aplikasi

| Tahap | Proses |
|---|---|
| **Input** | Klik ganda ikon Chrome |
| **CPU** | Membaca chrome.exe dari HDD → salin ke RAM |
| **RAM** | Menyimpan program yang sedang berjalan |
| **Output** | Jendela Chrome muncul di layar |

---

# SIMULASI "MANUSIA KOMPUTER"

---

## 5 Pemain — 5 Peran

| Pemain | Peran | Tugas |
|---|---|---|
| A | **Input** | Membaca kartu instruksi |
| B | **Control Unit** | Mengatur urutan |
| C | **ALU** | Menghitung / memproses |
| D | **Memori** | Mencatat data di papan |
| E | **Output** | Mengumumkan hasil |

**Instruksi 1:** Hitung 5 + 3
**Instruksi 2:** Cari nilai terbesar dari [7, 2, 9]

---

## Refleksi Simulasi

**Diskusikan:**

1. Apa yang terjadi jika **Memori** tidak bekerja?
2. Apa perbedaan **Control Unit** vs **ALU**?
3. Kenapa data harus lewat CPU dulu sebelum output?

---

## Rangkuman Hari Ini

| No | Poin Penting |
|---|---|
| 1 | **Von Neumann** = Input → CPU (ALU+CU) → Memori → Output |
| 2 | **Stored Program Concept**: program & data di memori sama |
| 3 | **Siklus CPU**: Fetch → Decode → Execute → Store |
| 4 | **IPO** adalah model dasar aliran data komputer |

---

## Tugas Rumah

### Buat Diagram Von Neumann versi kalian!

- Kertas A4
- Gambar diagram lengkap (Input, CPU, Memori, Output, Bus)
- Tambahkan penjelasan singkat tiap komponen
- **Dikumpulkan pertemuan depan!**

---

## Pertemuan Berikutnya

### Simulasi Dinamika IPO

> Akan ada praktik langsung simulasi IPO dengan alat peraga!

---

# Terima Kasih

### MGMP Informatika SMAN 6 Cimahi

> "Arsitektur Von Neumann adalah cetak biru dari setiap komputer yang kamu gunakan hari ini."
