---
marp: true
theme: uncover
class: invert
---

# PERTEMUAN 9 — SEMESTER 2
## Input/Output & Percabangan dalam Pseudocode
### Informatika – Fase E / Kelas X
#### SMA Negeri 6 Cimahi

---

## Review

Pertemuan 8: Pseudocode & Flowchart.

Hari ini kita perdalam:
> **INPUT, OUTPUT, dan IF-THEN-ELSE**

---

## Apersepsi

"Siapa yang pernah lihat nilai rapor dikonversi ke **huruf A, B, C, D**?"

Itu adalah percabangan!

> Hari ini kita belajar menulis aturan seperti itu dalam pseudocode!

---

# TUJUAN PEMBELAJARAN

1. ✅ INPUT, OUTPUT, Assignment
2. ✅ Tipe data (numerik, string, boolean)
3. ✅ IF-THEN-ELSE sederhana
4. ✅ Nested IF
5. ✅ Studi kasus: nilai → huruf mutu

---

## INPUT

Membaca data dari pengguna.

```
INPUT nama     → pengguna mengetik "Andi"
INPUT x        → pengguna mengetik 5
INPUT nilai    → pengguna mengetik 85
```

> Program **berhenti** menunggu input dari keyboard.

---

## OUTPUT

Menampilkan data ke layar.

```
OUTPUT "Halo"        → menampilkan: Halo
OUTPUT nama          → menampilkan: Andi
OUTPUT "Nilai: ", x  → menampilkan: Nilai: 5
```

> Teks pakai `" "`, variabel tanpa petik.

---

## Contoh Program: Sapa

```
PROGRAM sapa
    INPUT nama
    OUTPUT "Halo, ", nama
END
```

### Jika input: Budi
> Output: **Halo, Budi**

---

## Assignment

Menyimpan nilai ke variabel. Simbol `←`.

```
x ← 5               → x berisi 5
nama ← "Andi"       → nama berisi "Andi"
total ← a + b       → total berisi hasil jumlah
usia ← usia + 1     → usia bertambah 1
```

---

## Tipe Data Dasar

| Tipe | Contoh | Keterangan |
|---|---|---|
| **Numerik** | `5`, `3.14`, `-10` | Angka |
| **String** | `"Halo"`, `"Andi"` | Teks (pakai `" "`) |
| **Boolean** | `TRUE`, `FALSE` | Logika |

---

## IF Sederhana

```
IF kondisi THEN
    {aksi jika TRUE}
ENDIF
```

### Contoh:
```
IF nilai >= 75 THEN
    OUTPUT "Lulus"
ENDIF
```

---

## IF-ELSE

```
IF kondisi THEN
    {aksi jika TRUE}
ELSE
    {aksi jika FALSE}
ENDIF
```

### Contoh: Genap/Ganjil
```
IF x MOD 2 = 0 THEN
    OUTPUT "Genap"
ELSE
    OUTPUT "Ganjil"
ENDIF
```

---

## Nested IF

IF di dalam IF — untuk banyak kondisi berurutan.

```
IF kondisi1 THEN
    {aksi 1}
ELSE
    IF kondisi2 THEN
        {aksi 2}
    ELSE
        IF kondisi3 THEN
            {aksi 3}
        ENDIF
    ENDIF
ENDIF
```

---

## Operator Perbandingan

| Operator | Makna |
|---|---|
| `=` | Sama dengan |
| `≠` / `!=` | Tidak sama |
| `>` | Lebih besar |
| `<` | Lebih kecil |
| `>=` | ≥ |
| `<=` | ≤ |

---

## Operator Logika

| Operator | Makna | Contoh |
|---|---|---|
| `AND` | Keduanya TRUE | `x>0 AND x<10` |
| `OR` | Salah satu TRUE | `x<0 OR x>100` |
| `NOT` | Membalikkan | `NOT(x>0)` |

---

## Studi Kasus: Nilai → Huruf Mutu

| Rentang | Huruf |
|---|---|
| ≥ 92 | A |
| ≥ 83 | B |
| ≥ 75 | C |
| < 75 | D |

---

## Pseudocode: Nilai → Huruf

```
INPUT nilai_tugas, nilai_uts, nilai_pas
nilai_akhir ← (tugas×0.3)+(uts×0.3)+(pas×0.4)

IF nilai_akhir >= 92 THEN   → A
ELSE IF nilai_akhir >= 83 THEN → B
ELSE IF nilai_akhir >= 75 THEN → C
ELSE → D
ENDIF

OUTPUT nilai_akhir, huruf
```

---

## Aktivitas 1: Pseudocode Sederhana

### Individu — 10 menit

1. Diskon belanja: >100.000 → diskon 10%
2. Genap/ganjil

---

## Aktivitas 2: Nested IF

### Berpasangan — 10 menit

3. Maks dari 3 angka
4. Suhu udara: >30 "Panas", <20 "Dingin", 20–30 "Sejuk"

---

## Aktivitas 3: Studi Kasus

### Kelompok — 15 menit

Buat pseudocode lengkap:
- Input: nilai tugas (30%), UTS (30%), PAS (40%)
- Hitung nilai akhir
- Konversi ke huruf mutu
- Output: nilai akhir dan huruf

---

## Rangkuman

| Konsep | Notasi |
|---|---|
| Input | `INPUT var` |
| Output | `OUTPUT var/"teks"` |
| Assignment | `var ← nilai` |
| IF sederhana | `IF ... THEN ... ENDIF` |
| IF-ELSE | `IF ... THEN ... ELSE ... ENDIF` |
| Nested IF | IF di dalam IF |

---

## Pertemuan Depan

### Perulangan dalam Pseudocode (FOR, WHILE)
> Mengulang langkah-langkah tanpa menulis kode berulang kali

---

# Terima Kasih

### MGMP Informatika SMAN 6 Cimahi

> "Percabangan mengajarkan: dalam hidup, setiap kondisi punya konsekuensi."
