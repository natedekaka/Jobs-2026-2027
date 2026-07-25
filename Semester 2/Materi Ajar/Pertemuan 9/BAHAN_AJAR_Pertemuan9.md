# BAHAN AJAR – PERTEMUAN 9
## Input/Output & Percabangan dalam Pseudocode

| TP | BK 1.4 — Notasi Algoritma |
|---|---|

---

### A. INPUT DAN OUTPUT

#### INPUT

INPUT digunakan untuk **membaca data** dari pengguna.

```
INPUT namaVariabel
```

Saat pseudocode dijalankan, program akan berhenti dan menunggu pengguna mengetik data. Data tersebut akan disimpan ke dalam `namaVariabel`.

**Contoh:**
```
INPUT nama       → pengguna mengetik "Andi" → nama berisi "Andi"
INPUT x          → pengguna mengetik 5 → x berisi 5
INPUT nilai      → pengguna mengetik 85 → nilai berisi 85
```

#### OUTPUT

OUTPUT digunakan untuk **menampilkan data** ke layar.

```
OUTPUT ekspresi
```

Ekspresi bisa berupa teks (diapit `" "`) atau variabel.

**Contoh:**
```
OUTPUT "Halo Dunia"    → menampilkan teks: Halo Dunia
OUTPUT nama            → menampilkan isi variabel nama (misal: Andi)
OUTPUT "Nilai: ", x    → menampilkan: Nilai: 5
```

**Program lengkap:**
```
PROGRAM sapa
    INPUT nama
    OUTPUT "Halo, ", nama
END
```

Jika pengguna mengetik "Budi", output: `Halo, Budi`

---

### B. ASSIGNMENT DAN TIPE DATA

#### Assignment

Assignment = **menyimpan nilai** ke dalam variabel. Simbol `←`.

```
namaVariabel ← nilai/ekspresi
```

**Contoh:**
```
x ← 5               → x berisi 5
nama ← "Andi"       → nama berisi teks "Andi"
total ← a + b       → total berisi hasil penjumlahan a dan b
usia ← usia + 1     → usia bertambah 1 (increment)
```

#### Tipe Data Dasar dalam Pseudocode

| Tipe | Contoh | Keterangan |
|---|---|---|
| **Numerik** (angka) | `5`, `3.14`, `-10` | Bilangan bulat/pecahan |
| **String** (teks) | `"Halo"`, `"Andi"` | Diapit tanda petik |
| **Boolean** (logika) | `TRUE`, `FALSE` | Hanya dua nilai |

**Catatan:** Dalam pseudocode, tipe data tidak perlu dideklarasikan secara eksplisit (tidak seperti Pascal/C). Cukup gunakan saja.

---

### C. PERCABANGAN IF-THEN-ELSE

#### 1. IF Sederhana

```
IF kondisi THEN
    {aksi jika kondisi TRUE}
ENDIF
```

**Contoh:**
```
IF nilai >= 75 THEN
    OUTPUT "Lulus"
ENDIF
```

#### 2. IF-ELSE

```
IF kondisi THEN
    {aksi jika TRUE}
ELSE
    {aksi jika FALSE}
ENDIF
```

**Contoh:**
```
IF x MOD 2 = 0 THEN
    OUTPUT "Genap"
ELSE
    OUTPUT "Ganjil"
ENDIF
```

#### 3. Nested IF (IF Bersarang)

IF di dalam IF — untuk **banyak kondisi** yang berurutan.

```
IF kondisi1 THEN
    {aksi 1}
ELSE
    IF kondisi2 THEN
        {aksi 2}
    ELSE
        IF kondisi3 THEN
            {aksi 3}
        ELSE
            {aksi 4}
        ENDIF
    ENDIF
ENDIF
```

---

### D. OPERATOR

#### Operator Perbandingan (menghasilkan TRUE/FALSE)

| Operator | Makna |
|---|---|
| `=` | Sama dengan |
| `≠` atau `!=` | Tidak sama dengan |
| `>` | Lebih besar |
| `<` | Lebih kecil |
| `>=` | Lebih besar atau sama |
| `<=` | Lebih kecil atau sama |

#### Operator Logika

| Operator | Makna | Contoh |
|---|---|---|
| `AND` | Keduanya TRUE | `IF x>0 AND x<10` |
| `OR` | Salah satu TRUE | `IF x<0 OR x>100` |
| `NOT` | Membalikkan logika | `IF NOT(x>0)` |

---

### E. STUDI KASUS

#### Kasus 1: Diskon Belanja

Buat pseudocode: jika belanja > 100.000, diskon 10%. Tampilkan total bayar.

```
PROGRAM diskon_belanja
    INPUT total_belanja
    IF total_belanja > 100000 THEN
        diskon ← total_belanja × 0.1
        total_bayar ← total_belanja - diskon
    ELSE
        total_bayar ← total_belanja
    ENDIF
    OUTPUT "Total bayar: ", total_bayar
END
```

#### Kasus 2: Bilangan Terbesar dari 3 Angka

```
PROGRAM maks_3_angka
    INPUT a, b, c
    IF a >= b AND a >= c THEN
        maks ← a
    ELSE
        IF b >= a AND b >= c THEN
            maks ← b
        ELSE
            maks ← c
        ENDIF
    ENDIF
    OUTPUT "Terbesar: ", maks
END
```

#### Kasus 3: Nilai Akhir → Huruf Mutu

| Rentang | Huruf |
|---|---|
| ≥ 92 | A |
| ≥ 83 | B |
| ≥ 75 | C |
| < 75 | D |

```
PROGRAM nilai_huruf
    INPUT nilai_tugas, nilai_uts, nilai_pas
    nilai_akhir ← (nilai_tugas × 0.3) + (nilai_uts × 0.3) + (nilai_pas × 0.4)
    
    IF nilai_akhir >= 92 THEN
        huruf ← "A"
    ELSE
        IF nilai_akhir >= 83 THEN
            huruf ← "B"
        ELSE
            IF nilai_akhir >= 75 THEN
                huruf ← "C"
            ELSE
                huruf ← "D"
            ENDIF
        ENDIF
    ENDIF
    
    OUTPUT "Nilai akhir: ", nilai_akhir
    OUTPUT "Huruf mutu: ", huruf
END
```

#### Kasus 4: Suhu Udara

```
PROGRAM suhu_udara
    INPUT suhu
    IF suhu > 30 THEN
        OUTPUT "Panas"
    ELSE
        IF suhu < 20 THEN
            OUTPUT "Dingin"
        ELSE
            OUTPUT "Sejuk"
        ENDIF
    ENDIF
END
```

---

### F. KESALAHAN UMUM

| Kesalahan | Salah | Benar |
|---|---|---|
| Lupa ENDIF | `IF x>0 THEN OUTPUT "Positif"` | `IF x>0 THEN OUTPUT "Positif" ENDIF` |
| Kurung bersarang | `IF IF x>0 THEN` | Gunakan nested IF |
| Operator logika | `IF x>0 & x<10` | `IF x>0 AND x<10` |
| Assignment terbalik | `5 ← x` | `x ← 5` |
| String tanpa petik | `OUTPUT Halo` | `OUTPUT "Halo"` |

---

### G. RANGKUMAN

| Konsep | Notasi | Contoh |
|---|---|---|
| Input | `INPUT var` | `INPUT nama` |
| Output | `OUTPUT var/teks` | `OUTPUT "Halo"` |
| Assignment | `var ← nilai` | `x ← 5` |
| IF sederhana | `IF ... THEN ... ENDIF` | `IF x>0 THEN OUTPUT "+" ENDIF` |
| IF-ELSE | `IF ... THEN ... ELSE ... ENDIF` | Genap/ganjil |
| Nested IF | IF di dalam IF | Nilai → huruf mutu |
| Operator | `= ≠ > < >= <= AND OR NOT` | `IF x>=75 AND x<83` |

---

**MGMP Informatika SMAN 6 Cimahi**
