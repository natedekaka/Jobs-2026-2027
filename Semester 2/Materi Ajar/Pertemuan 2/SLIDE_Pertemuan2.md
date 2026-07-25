---
marp: true
theme: uncover
class: invert
---

# PERTEMUAN 2 — SEMESTER 2
## Stack (Tumpukan) — LIFO
### Informatika – Fase E / Kelas X
#### SMA Negeri 6 Cimahi

---

## Review — Tugas Pertemuan 1

Siapa yang nemu contoh array di rumah?

> Array = deretan indeks. Hari ini kita belajar struktur data kedua: **Stack**!

---

## Apersepsi

**Guru menumpuk buku di meja...**

- Buku mana yang bisa diambil pertama?
- Buku paling **atas**!
- Buku paling **bawah**?

> Yang terakhir ditumpuk = pertama diambil
> Itulah **LIFO**! 🥞

---

# TUJUAN PEMBELAJARAN

1. ✅ Memahami konsep LIFO
2. ✅ Operasi push & pop
3. ✅ Contoh stack di kehidupan & teknologi
4. ✅ Menyelesaikan teka-teki stack

---

## Apa Itu Stack?

**Stack = Tumpukan**

Prinsip: **LIFO** — Last In, First Out
- Yang terakhir masuk → pertama keluar

| Operasi | Fungsi |
|---|---|
| **Push** | Menambah data ke atas |
| **Pop** | Mengambil data dari atas |

---

## Ilustrasi Stack

```
   ← pop()            ← push(data)
     │                     │
     ▼                     ▼
┌──────────────────────┐
│    DATA BARU (atas)  │
├──────────────────────┤
│    DATA LAMA         │
├──────────────────────┤
│    DATA PALING LAMA  │
└──────────────────────┘
```

---

## Contoh Stack 1: Tumpukan Piring 🍽️

| Aksi | Operasi |
|---|---|
| Cuci piring → tumpuk | **Push** |
| Ambil piring buat makan | **Pop** |

> Piring yang terakhir dicuci = yang pertama dipakai.

---

## Contoh Stack 2: Undo (Ctrl+Z) ↩️

| Aksi | Operasi Stack |
|---|---|
| Ketik "Halo" | Push("Halo") |
| Ketik " Halo" | Push(" Halo") |
| Ketik "Dunia" | Push("Dunia") |
| **Ctrl+Z** | **Pop → "Dunia" dihapus** |
| **Ctrl+Z** | **Pop → " Halo" dihapus** |

> Setiap aksi di-push ke stack. Undo = pop!

---

## Contoh Stack 3: Back Button 🌐

| Aksi | Operasi |
|---|---|
| Buka Google | Push |
| Buka YouTube | Push |
| Buka Video | Push |
| **Klik Back** | **Pop → YouTube** |
| **Klik Back** | **Pop → Google** |

> Riwayat browser = stack halaman!

---

## Aktivitas 1: Simulasi Buku

### Klasikal — 15 menit

5 siswa maju bawa buku:

1. Guru sebut nama → **Push** (tumpuk)
2. Guru minta ambil → **Pop** (ambil atas)
3. Catat urutan!

> Apakah LIFO terbukti? ✅

---

## Aktivitas 2: Kartu Stack

### Berpasangan — 15 menit

**Percobaan 1:**
Push 5→3→8→1→6, Pop 3×

Prediksi: angka apa yang keluar?

**Percobaan 2:**
Push 2→4, Pop, Push 7→9, Pop 2×

---

## Teka-teki Stack

### Soal:
Push A→B→C→D, Pop 2×
Push E→F, Pop 3×

**Urutan pop?**
> D, C, __, __, __

**Stack akhir?**
> [__, __]

---

## Stack dalam Python 🐍

```python
stack = []
stack.append(5)   # Push 5
stack.append(3)   # Push 3
stack.append(8)   # Push 8
x = stack.pop()   # Pop → 8
y = stack.pop()   # Pop → 3
```

> `append()` = push, `pop()` = pop!
> Nanti kita coding sendiri di pertemuan Python.

---

## Diskusi

1. Bedanya stack dengan array biasa?
2. Kenapa browser pake stack buat tombol Back?
3. Kelemahan stack?

---

## Rangkuman

| Konsep | Inti |
|---|---|
| **Stack** | Tumpukan — LIFO |
| **Push** | Tambah ke atas |
| **Pop** | Ambil dari atas |
| **Contoh** | Undo, Back, tumpukan piring |

---

## Tugas Rumah

**Cari 2 contoh stack** di rumah/sekolah!
1. ________________ — Push? Pop?
2. ________________ — Push? Pop?

> Siapa yang bisa nemu contoh paling kreatif?

---

## Pertemuan Depan

### Queue (Antrian) — FIFO
> Yang pertama masuk = pertama keluar!

---

# Terima Kasih

### MGMP Informatika SMAN 6 Cimahi

> "Stack mengajarkan: apa yang terakhir masuk, akan pertama keluar. Seperti antrean prioritas — atau tumpukan PR?"
