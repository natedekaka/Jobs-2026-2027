# BAHAN AJAR – PERTEMUAN 8
## Pseudocode & Flowchart

| TP | BK 1.4 — Notasi Algoritma |
|---|---|

---

### A. PENGANTAR

**Algoritma** adalah langkah-langkah logis untuk menyelesaikan masalah. Tapi bagaimana cara menuliskannya?

Ada **dua cara** utama:
1. **Pseudocode** — ditulis dalam bentuk teks, mirip kode pemrograman
2. **Flowchart** — digambar dalam bentuk diagram, visual

> Keduanya bisa dikonversi satu sama lain!

---

### B. PSEUDOCODE

**Pseudocode** = "pseudo" (mirip) + "code" (kode program)

Ciri-ciri:
- Tidak terikat bahasa pemrograman tertentu
- Menggunakan bahasa Indonesia/Inggris
- Fokus pada **logika**, bukan sintaksis detail

#### Notasi Dasar Pseudocode

| Notasi | Makna | Contoh |
|---|---|---|
| `INPUT` | Membaca input dari pengguna | `INPUT nama` |
| `OUTPUT` | Menampilkan output ke layar | `OUTPUT "Halo"` |
| `←` | Assignment (menyimpan nilai) | `x ← 10` |
| `IF` `THEN` `ELSE` `ENDIF` | Percabangan | `IF x>0 THEN OUTPUT "+"` |
| `FOR` `TO` `ENDFOR` | Perulangan dengan counter | `FOR i←1 TO 5` |
| `WHILE` `ENDWHILE` | Perulangan dengan kondisi | `WHILE x<10` |
| `REPEAT` `UNTIL` | Perulangan minimal sekali | `REPEAT ... UNTIL x=5` |

#### Contoh Pseudocode

**Contoh 1: Menjumlahkan dua bilangan**
```
PROGRAM jumlah_dua_bilangan
    INPUT a
    INPUT b
    hasil ← a + b
    OUTPUT hasil
END
```

**Contoh 2: Menentukan bilangan genap/ganjil**
```
PROGRAM genap_ganjil
    INPUT x
    IF x MOD 2 = 0 THEN
        OUTPUT "Genap"
    ELSE
        OUTPUT "Ganjil"
    ENDIF
END
```

**Contoh 3: Mencetak angka 1 sampai 5**
```
PROGRAM cetak_1_ke_5
    FOR i ← 1 TO 5
        OUTPUT i
    ENDFOR
END
```

**Contoh 4: Menghitung faktorial**
```
PROGRAM faktorial
    INPUT n
    hasil ← 1
    FOR i ← 1 TO n
        hasil ← hasil × i
    ENDFOR
    OUTPUT hasil
END
```

---

### C. FLOWCHART

**Flowchart** = diagram alir, representasi visual dari algoritma.

#### Simbol-Simbol Flowchart

| Simbol | Nama | Fungsi |
|---|---|---|
| 🟩 **Oval** | Terminator | Mulai (Start) / Selesai (End) |
| ⬜ **Persegi Panjang** | Proses | Assignment, operasi aritmatika |
| ◆ **Belah Ketupat** | Decision | Percabangan (Ya/Tidak) |
| ▱ **Jajar Genjang** | Input/Output | Membaca INPUT / menulis OUTPUT |
| ➡ **Garis Panah** | Arrow | Menunjukkan arah aliran |
| ⭕ **Lingkaran** | Connector | Menghubungkan bagian flowchart |

#### Aturan Membuat Flowchart

1. Satu **Start** dan satu **End**
2. Arrow mengalir dari atas ke bawah (atau kiri ke kanan)
3. Decision memiliki **dua cabang** (Ya dan Tidak)
4. Tidak ada jalur yang terputus (semua terhubung)
5. Simbol digunakan sesuai fungsinya

#### Contoh Flowchart

**Flowchart:  Menentukan bilangan genap/ganjil**

```
   ┌─────────────┐
   │    Start    │
   └──────┬──────┘
          ▼
   ┌─────────────┐
   │  INPUT x    │
   └──────┬──────┘
          ▼
      ┌──────┐
      │ x%2  │
      │ = 0? │──── Tidak ──→ ┌──────────┐
      └──┬───┘               │ OUTPUT   │
         │ Ya                │ "Ganjil" │
         ▼                   └────┬─────┘
   ┌──────────┐                  │
   │ OUTPUT   │                  │
   │ "Genap"  │                  │
   └────┬─────┘                  │
        │◄───────────────────────┘
        ▼
   ┌─────────────┐
   │    End      │
   └─────────────┘
```

**Flowchart: Mencetak 1 sampai 5**

```
   ┌─────────────┐
   │    Start    │
   └──────┬──────┘
          ▼
   ┌─────────────┐
   │   i ← 1     │
   └──────┬──────┘
          ▼
      ┌──────┐
      │ i≤5? │── Tidak ──→ ┌─────────────┐
      └──┬───┘             │    End      │
         │ Ya              └─────────────┘
         ▼
   ┌─────────────┐
   │  OUTPUT i   │
   └──────┬──────┘
          ▼
   ┌─────────────┐
   │  i ← i + 1  │
   └──────┬──────┘
          │
          └─────────→ (kembali ke decision)
```

---

### D. TRANSLASI PSEUDOCODE ↔ FLOWCHART

Aturan translasi:

| Pseudocode | Flowchart |
|---|---|
| `INPUT/OUTPUT` | ▱ Jajar Genjang |
| Assignment `←` | ▭ Persegi Panjang |
| `IF...THEN...ELSE` | ◆ Decision |
| `FOR/WHILE` | ◆ Decision + ▭ Proses (counter) |
| `PROGRAM...END` | ⬭ Terminator |

#### Contoh Translasi

**Pseudocode → Flowchart**

Pseudocode:
```
PROGRAM hitung_luas
    INPUT panjang
    INPUT lebar
    luas ← panjang × lebar
    OUTPUT luas
END
```

Flowchart:
```
   ┌─────────────┐
   │    Start    │
   └──────┬──────┘
          ▼
   ┌─────────────┐
   │INPUT panjang│
   └──────┬──────┘
          ▼
   ┌─────────────┐
   │ INPUT lebar │
   └──────┬──────┘
          ▼
   ┌─────────────┐
   │luas←panjang │
   │    × lebar  │
   └──────┬──────┘
          ▼
   ┌─────────────┐
   │OUTPUT luas  │
   └──────┬──────┘
          ▼
   ┌─────────────┐
   │    End      │
   └─────────────┘
```

**Flowchart → Pseudocode** (proses sebaliknya):
1. Baca simbol terminator → `PROGRAM ... END`
2. Baca jajar genjang → `INPUT` / `OUTPUT`
3. Baca persegi panjang → assignment
4. Baca decision → `IF...THEN...ELSE`

---

### E. RANGKUMAN

| Aspek | Pseudocode | Flowchart |
|---|---|---|
| **Bentuk** | Teks | Diagram visual |
| **Kelebihan** | Cepat ditulis, dekat dengan kode | Mudah dipahami secara visual |
| **Kekurangan** | Kurang visual | Butuh alat gambar |
| **Kapan dipakai** | Saat menulis algoritma cepat | Saat menjelaskan ke orang lain |
| **Translasi** | ↔ (dua arah) | ↔ (dua arah) |

**Tips:**
- Mulai dengan pseudocode → lalu gambar flowchart untuk visualisasi
- Atau gambar flowchart dulu → lalu tulis pseudocode untuk implementasi
- Keduanya adalah **alat bantu**, bukan tujuan akhir

---

**MGMP Informatika SMAN 6 Cimahi**
