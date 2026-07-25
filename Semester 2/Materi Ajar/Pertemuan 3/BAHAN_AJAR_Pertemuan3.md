# BAHAN AJAR – PERTEMUAN 3
## Queue (Antrian) — FIFO

| TP | BK 1.1 |
|---|---|

---

### A. KONSEP QUEUE

Queue (antrian) adalah struktur data yang mengikuti prinsip **FIFO**: **F**irst **I**n **F**irst **O**ut — data yang pertama masuk adalah yang pertama keluar.

#### Anatomi Queue
```
    ← dequeue()                    ← enqueue(data)
         │                              │
         ▼                              ▼
    ┌──────────────────────────────────────┐
    │ Depan  │       ANTRIAN        │ Belakang │
    │ (Front)│  A  B  C  D  E  F    │  (Rear)  │
    └──────────────────────────────────────┘
       Keluar duluan                Masuk baru
```

#### Operasi Dasar Queue

| Operasi | Fungsi |
|---|---|
| `enqueue(x)` | Menambahkan data x ke belakang antrian |
| `dequeue()` | Mengambil data dari depan antrian |
| `front()` / `peek()` | Melihat data paling depan tanpa mengambil |
| `isEmpty()` | Mengecek apakah antrian kosong |
| `size()` | Mengetahui panjang antrian |

---

### B. CONTOH QUEUE DALAM KEHIDUPAN

#### 1. Antrian Kasir / Kantin
```
Enqueue: pelangdat datang (di belakang)
Dequeue: pelanggan dilayani (dari depan)
Dequeue → Enqueue → Enqueue → Dequeue → ...
Yang datang duluan → dilayani duluan.
```

#### 2. Antrian Printer
```
Dokumen 1 dikirim → Enqueue
Dokumen 2 dikirim → Enqueue
Printer cetak → Dequeue (Dokumen 1 dulu)
Printer cetak → Dequeue (Dokumen 2)
```

#### 3. Antrian Bank / Loket
```
Ambil nomor antre → Enqueue
Teller panggil → Dequeue
Nomor 1 dipanggil dulu → baru 2, 3, ...
```

#### 4. Sistem Pesan (Chat)
```
Pesan A masuk → Enqueue
Pesan B masuk → Enqueue
Pesan A ditampilkan dulu → Dequeue
Pesan B ditampilkan → Dequeue
```

#### 5. Antrian Server (Request Handling)
```
User 1 request → Enqueue
User 2 request → Enqueue  
Server proses → Dequeue (User 1 dulu)
Server proses → Dequeue (User 2)
```

---

### C. PERBANDINGAN STACK VS QUEUE

| Aspek | Stack (LIFO) | Queue (FIFO) |
|---|---|---|
| **Prinsip** | Last In First Out | First In First Out |
| **Sisi masuk** | Satu (atas) | Belakang (rear) |
| **Sisi keluar** | Sama (atas) | Depan (front) |
| **Operasi** | push / pop | enqueue / dequeue |
| **Analogi** | Tumpukan piring | Antrian kasir |
| **Ukuran** | Dinamis (bisa tambah) | Dinamis (bisa tambah) |
| **Contoh** | Undo, Back button, Call stack | Print queue, antrian bank, chat |
| **Visual** | Vertikal (ke atas) | Horizontal (ke samping) |

---

### D. QUEUE DALAM PYTHON (Preview)

Di Python, queue bisa diimplementasikan dengan `collections.deque`:

```python
from collections import deque

antrian = deque()          # Buat antrian kosong

antrian.append(5)          # Enqueue 5
antrian.append(3)          # Enqueue 3
antrian.append(8)          # Enqueue 8 → [5, 3, 8]

x = antrian.popleft()      # Dequeue → 5 (yang pertama)
y = antrian.popleft()      # Dequeue → 3

print(x, y)                # Output: 5 3
print(antrian)             # Output: deque([8])
```

Atau dengan list biasa:
```python
antrian = []
antrian.append(5)          # Enqueue
antrian.append(3)
x = antrian.pop(0)         # Dequeue (ambil index 0)
```

---

### E. TEKA-TEKI QUEUE

**Soal 1:**
Enqueue: 5, 3, 8, 1, 6. Dequeue 3×. Urutan keluar?

**Jawab:**
```
Antrian: [5, 3, 8, 1, 6]  (5 di depan)
Dequeue 1: 5  → [3, 8, 1, 6]
Dequeue 2: 3  → [8, 1, 6]
Dequeue 3: 8  → [1, 6]
Urutan dequeue: 5, 3, 8
```

**Soal 2 (Stack vs Queue):**
Jika Stack: push 1→2→3, pop 1× → output ___
Jika Queue: enqueue 1→2→3, dequeue 1× → output ___

**Jawab:**
- Stack (LIFO): pop → 3 (yang terakhir masuk)
- Queue (FIFO): dequeue → 1 (yang pertama masuk)

---

### F. RANGKUMAN

1. **Queue** = antrian — FIFO (First In First Out)
2. **Enqueue** = tambah data di belakang, **Dequeue** = ambil data dari depan
3. **Stack** LIFO vs **Queue** FIFO: beda arah masuk/keluar
4. Contoh queue: antrian kasir, printer, bank, chat
5. Python: `append()` = enqueue, `popleft()` = dequeue

---

**MGMP Informatika SMAN 6 Cimahi**
