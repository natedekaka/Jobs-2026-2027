---
marp: true
theme: uncover
class: invert
---

# PERTEMUAN 10 — SEMESTER 2
## Perulangan dalam Pseudocode
### Informatika – Fase E / Kelas X
#### SMA Negeri 6 Cimahi

---

## Review — Dua Pertemuan Terakhir

| Pert | Materi |
|---|---|
| 8 | Pseudocode & Flowchart |
| 9 | INPUT/OUTPUT & IF-THEN-ELSE |
| **10** | **Perulangan (FOR, WHILE)** |

---

## Apersepsi

"Coba sebutkan bilangan genap dari **2 sampai 20**!"

> Tanpa perulangan: 10 baris
> Dengan perulangan: **3 baris**

---

# TUJUAN PEMBELAJARAN

1. ✅ Konsep perulangan
2. ✅ FOR — counter otomatis
3. ✅ WHILE — selama kondisi TRUE
4. ✅ REPEAT-UNTIL — minimal sekali
5. ✅ Studi kasus: faktorial

---

## Tanpa Perulangan

```
OUTPUT 1
OUTPUT 2
OUTPUT 3
OUTPUT 4
OUTPUT 5
... (100 baris!)
```

---

## Dengan Perulangan

```
FOR i ← 1 TO 100
    OUTPUT i
ENDFOR
```

> **Hanya 3 baris!** 100 kali lebih efisien.

---

## FOR — Sintaks

```
FOR variabel ← awal TO akhir
    {kode yang diulang}
ENDFOR
```

### Contoh:
```
FOR i ← 1 TO 5
    OUTPUT i
ENDFOR
```
> Output: **1 2 3 4 5**

---

## FOR — STEP

```
FOR i ← 2 TO 10 STEP 2
    OUTPUT i
ENDFOR
```
> Output: **2 4 6 8 10**

---

## FOR — Akumulasi

```
total ← 0
FOR i ← 1 TO 10
    total ← total + i
ENDFOR
OUTPUT total
```

> Total 1+2+...+10 = **55**

---

## WHILE — Sintaks

```
WHILE kondisi TRUE
    {kode yang diulang}
ENDWHILE
```

### Contoh:
```
i ← 1
WHILE i <= 5
    OUTPUT i
    i ← i + 1    ← INGAT update!
ENDWHILE
```

---

## WHILE — Input Sampai 0

```
total ← 0
INPUT x
WHILE x ≠ 0
    total ← total + x
    INPUT x
ENDWHILE
OUTPUT "Total: ", total
```

### Input: 5, 3, 2, 0
> Total: **10**

---

## ⚠️ Hati-hati Infinite Loop!

```
i ← 1
WHILE i <= 5
    OUTPUT i
    ← lupa i ← i + 1 !!
ENDWHILE
```

> Program akan jalan **terus** sampai komputer hang!

**Solusi:** pastikan ada update variabel kondisi!

---

## REPEAT-UNTIL

```
REPEAT
    {kode yang diulang}
UNTIL kondisi TRUE
```

Cek kondisi di **akhir** — minimal sekali jalan.

### Contoh:
```
i ← 1
REPEAT
    OUTPUT i
    i ← i + 1
UNTIL i > 5
```

---

## FOR vs WHILE vs REPEAT-UNTIL

| Aspek | FOR | WHILE | REPEAT-UNTIL |
|---|---|---|---|
| Counter | ✅ Otomatis | Manual | Manual |
| Cek kondisi | Awal | Awal | **Akhir** |
| Minimal | 0 | 0 | **1** |
| Risiko loop | Rendah | Tinggi | Tinggi |

---

## Kapan Pakai?

| Situasi | Pakai |
|---|---|
| Cetak 1–100 | **FOR** |
| Input sampai 0 | **WHILE** |
| Menu program | **REPEAT-UNTIL** |
| Jumlah tidak pasti | WHILE/REPEAT |

---

## Aktivitas 1: FOR

### Individu — 10 menit

1. Cetak genap 2–20
2. Tabel perkalian 5
3. Jumlah 1+2+...+10

---

## Aktivitas 2: WHILE

### Berpasangan — 10 menit

4. Input sampai 0 → tampilkan jumlah & rata-rata
5. Tebak angka (rahasia: 8)

---

## Aktivitas 3: Faktorial

### Kelompok — 15 menit

n! = n × (n-1) × ... × 1

Buat 2 versi:
- ✅ **FOR**
- ✅ **WHILE**

### Uji: n=5 → 120

---

## Faktorial — FOR

```
INPUT n
hasil ← 1
FOR i ← 1 TO n
    hasil ← hasil × i
ENDFOR
OUTPUT n, "! = ", hasil
```

### 5! = 1×2×3×4×5 = 120

---

## Faktorial — WHILE

```
INPUT n
hasil ← 1
i ← 1
WHILE i <= n
    hasil ← hasil × i
    i ← i + 1
ENDWHILE
OUTPUT n, "! = ", hasil
```

> Dua versi, hasil sama!

---

## Rangkuman

| Notasi | Fungsi | Contoh |
|---|---|---|
| `FOR` | Counter pasti | Cetak 1..10 |
| `WHILE` | Kondisi di awal | Input sampai 0 |
| `REPEAT` | Kondisi di akhir | Menu program |

---

## Tugas Rumah

### Deret Fibonacci
Buat pseudocode cetak Fibonacci sampai suku ke-n

Deret: 0, 1, 1, 2, 3, 5, 8, 13, ...

> Gunakan FOR!

---

## Pertemuan Depan

### Latihan Soal Algoritma
> Review semua materi pseudocode sebelum masuk Python!

---

# Terima Kasih

### MGMP Informatika SMAN 6 Cimahi

> "Perulangan mengajarkan: konsistensi kecil yang dilakukan berulang akan menghasilkan perubahan besar."
