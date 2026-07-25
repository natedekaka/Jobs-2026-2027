---
marp: true
theme: uncover
class: invert
---

# PERTEMUAN 3 — SEMESTER 2
## Queue (Antrian) — FIFO
### Informatika – Fase E / Kelas X
#### SMA Negeri 6 Cimahi

---

## Review — Stack

- **LIFO**: Last In First Out
- Push & Pop
- Contoh: Undo, Back button

> Hari ini kita belajar kebalikannya!

---

## Apersepsi

**Siapa yang antre di kantin tadi pagi?**

- Siapa dapat duluan?
- Yang **datang pertama**!
- Siapa dapat belakangan?
- Yang **datang belakangan**!

> Itulah **Queue** = **FIFO**!

---

# TUJUAN PEMBELAJARAN

1. ✅ Memahami FIFO
2. ✅ Operasi enqueue & dequeue
3. ✅ Membedakan Stack vs Queue
4. ✅ Contoh queue di kehidupan

---

## Apa Itu Queue?

**Queue = Antrian**

Prinsip: **FIFO** — First In, First Out
- Yang pertama masuk → pertama keluar

| Operasi | Fungsi |
|---|---|
| **Enqueue** | Tambah data di belakang |
| **Dequeue** | Ambil data dari depan |

---

## Anatomi Queue

```
← dequeue()      ← enqueue(data)
     │                 │
     ▼                 ▼
┌──────────────────────────────┐
│ Depan │ ANTRIAN │ Belakang   │
│   A   │  B  C  D │    E      │
└──────────────────────────────┘
  Keluar 1             Masuk baru
```

---

## Contoh Queue 1: Antrian Kasir 🏪

| Situasi | Operasi |
|---|---|
| Pelangdat datang | **Enqueue** |
| Kasir panggil | **Dequeue** |
| Yang **pertama** datang | Dilayani **pertama** |

---

## Contoh Queue 2: Antrian Printer 🖨️

| Langkah | Operasi |
|---|---|
| Dok 1 dikirim | Enqueue |
| Dok 2 dikirim | Enqueue |
| Printer cetak | **Dequeue → Dok 1** |
| Printer cetak | **Dequeue → Dok 2** |

---

## Contoh Queue 3: Chat 💬

| Aksi | Operasi |
|---|---|
| Andi kirim "Halo" | Enqueue |
| Budi kirim "Apa kabar?" | Enqueue |
| Chat ditampilkan | **Dequeue → "Halo" dulu** |
| Chat ditampilkan | **Dequeue → "Apa kabar?"** |

---

## Stack vs Queue

| Aspek | Stack (LIFO) | Queue (FIFO) |
|---|---|---|
| **Prinsip** | Last In First Out | First In First Out |
| **Masuk** | Atas | Belakang |
| **Keluar** | Atas | Depan |
| **Operasi** | push / pop | enqueue / dequeue |
| **Analogi** | Tumpukan piring 🥞 | Antrian kasir 🏪 |

---

## Aktivitas 1: Antrian Kelas

### 10 menit — 6 siswa maju

1. Guru sebut → **Enqueue** (masuk antrian)
2. Guru sebut → **Dequeue** (keluar dari depan)
3. Catat urutan!

> Apakah FIFO terbukti?

---

## Aktivitas 2: Kartu Queue

### Berpasangan — 15 menit

**Percobaan 1:**
Enqueue 5→3→8, Dequeue 2×
Enqueue 1→6, Dequeue 1×

Prediksi urutan keluar?

**Percobaan 2:**
Enqueue A→B→C, Dequeue 1×
Enqueue D→E, Dequeue 3×

---

## Aktivitas 3: Poster

### Kelompok — 15 menit

Buat poster perbandingan Stack vs Queue:
| Aspek | Stack | Queue |
|---|---|---|
| Prinsip | LIFO | FIFO |
| Operasi | push/pop | enq/deq |
| 3 contoh | | |

> Siap presentasi!

---

## Kuis Cepat!

1. Enqueue A→B→C, Dequeue? → ___
2. Push A→B→C, Pop? → ___
3. Queue digunakan di...?
4. Stack digunakan di...?

---

## Queue dalam Python 🐍

```python
from collections import deque
q = deque()
q.append(5)        # Enqueue 5
q.append(3)        # Enqueue 3
x = q.popleft()    # Dequeue → 5
```

---

## Rangkuman

| Konsep | Inti |
|---|---|
| **Queue** | Antrian — FIFO |
| **Enqueue** | Tambah di belakang |
| **Dequeue** | Ambil dari depan |
| **Contoh** | Printer, kasir, chat |
| **Vs Stack** | FIFO vs LIFO |

---

## Tugas Ramadan 📚

Selama libur Ramadan (15 Feb–5 Mar):
1. Baca modul Searching & Sorting
2. Kerjakan 5 soal latihan
3. Eksplorasi **visualgo.net**
4. Kumpulkan setelah Idul Fitri

> Selamat menjalankan ibadah Ramadan! 🕌

---

## Pertemuan 4 (setelah libur)

### Sequential Search (Pencarian Berurutan)
> Cari data dalam array — satu per satu!

---

# Terima Kasih

### MGMP Informatika SMAN 6 Cimahi

> "Queue mengajarkan: kesabaran itu FIFO — yang pertama sabar, pertama dapat hasil."
