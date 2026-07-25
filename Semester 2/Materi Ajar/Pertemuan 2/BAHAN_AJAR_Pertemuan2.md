# BAHAN AJAR – PERTEMUAN 2
## Stack (Tumpukan) — LIFO

| TP | BK 1.1 |
|---|---|

---

### A. KONSEP STACK

Stack (tumpukan) adalah struktur data yang mengikuti prinsip **LIFO**: **L**ast **I**n **F**irst **O**ut — data yang terakhir masuk adalah yang pertama keluar.

#### Anatomi Stack
```
       ← pop()          ← push(data)
         │                    │
         ▼                    ▼
    ┌──────────────────────┐
    │      DATA 3 (atas)   │ ← Top (puncak)
    ├──────────────────────┤
    │      DATA 2          │
    ├──────────────────────┤
    │      DATA 1 (bawah)  │ ← Bottom (dasar)
    └──────────────────────┘
```

#### Operasi Dasar Stack

| Operasi | Fungsi | Ilustrasi |
|---|---|---|
| `push(x)` | Menambahkan data x ke atas stack | Tumpukan bertambah |
| `pop()` | Mengambil data dari atas stack | Tumpukan berkurang |
| `top()` / `peek()` | Melihat data paling atas tanpa mengambil | Intip piring paling atas |
| `isEmpty()` | Mengecek apakah stack kosong | Apakah tumpukan habis? |
| `size()` | Mengetahui jumlah data di stack | Berapa tinggi tumpukan? |

---

### B. CONTOH STACK DALAM KEHIDUPAN

#### 1. Tumpukan Piring

```
Push: menaruh piring bersih di atas
Pop: mengambil piring untuk dipakai
```
Piring yang terakhir dicuci (paling atas) akan dipakai pertama.

#### 2. Fitur Undo (Ctrl+Z)

```
Aksi 1: Ketik "A" → Push
Aksi 2: Ketik "B" → Push  
Aksi 3: Hapus "B" → Push (delete)
Ctrl+Z: Pop → kembali ke "AB"
Ctrl+Z: Pop → kembali ke "A"
```

#### 3. Riwayat Browser (Tombol Back)

```
Halaman 1: Google → Push
Halaman 2: YouTube → Push
Halaman 3: Video → Push
Klik Back: Pop → kembali ke YouTube
Klik Back: Pop → kembali ke Google
```

#### 4. Tumpukan Buku

```
Buku Matematika → Push (bawah)
Buku Fisika     → Push
Buku Kimia      → Push (atas)
Ambil buku      → Pop (Kimia diambil duluan)
```

#### 5. Pemanggilan Fungsi (Call Stack)

```
Program:
  1. main() panggil fungsi A()  → Push A ke call stack
  2. A() panggil fungsi B()      → Push B ke call stack
  3. B() selesai                 → Pop B dari call stack
  4. A() selesai                 → Pop A dari call stack
```

---

### C. TEKA-TEKI STACK

**Soal 1:** Push urutan: 5→3→8→1→6. Pop 3×. Urutan angka yang keluar?

**Jawab:**
```
Stack: [5, 3, 8, 1, 6]  (6 di atas)
Pop 1: 6  → stack: [5, 3, 8, 1]
Pop 2: 1  → stack: [5, 3, 8]
Pop 3: 8  → stack: [5, 3]
Urutan pop: 6, 1, 8
```

**Soal 2:** Push A→B→C, Pop 1×, Push D→E, Pop 2×. Urutan pop?

**Jawab:**
```
Push A, B, C → stack: [A, B, C]
Pop 1: C     → stack: [A, B]
Push D, E    → stack: [A, B, D, E]
Pop 2: E     → stack: [A, B, D]
Pop 3: D     → stack: [A, B]
Urutan pop: C, E, D
```

---

### D. STACK DI PYTHON (Preview)

Di Python, list bisa digunakan sebagai stack dengan metode `append()` (push) dan `pop()`:

```python
stack = []          # Buat stack kosong

stack.append(5)     # Push 5   → [5]
stack.append(3)     # Push 3   → [5, 3]
stack.append(8)     # Push 8   → [5, 3, 8]

x = stack.pop()     # Pop → 8  → [5, 3]
y = stack.pop()     # Pop → 3  → [5]

print(x)            # Output: 8
print(y)            # Output: 3
print(stack)        # Output: [5]
```

---

### E. RANGKUMAN

1. **Stack** = tumpukan — LIFO (Last In First Out)
2. **Push** = menambah data ke atas, **Pop** = mengambil data dari atas
3. Contoh: Undo, Back button, tumpukan piring, call stack
4. Python: `append()` = push, `pop()` = pop

---

**MGMP Informatika SMAN 6 Cimahi**
