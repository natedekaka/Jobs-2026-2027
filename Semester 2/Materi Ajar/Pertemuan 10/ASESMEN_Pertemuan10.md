# ASESMEN – PERTEMUAN 10
## Perulangan dalam Pseudocode

Informatika – Fase E / Kelas X – SMA Negeri 6 Cimahi

---

## Rubrik Penilaian

### A. Membaca Pseudocode FOR (Bobot 15%)

| No | Jawaban | Skor |
|---|---|---|
| 1 | 2, 4, 6, 8 | 1 per angka |
| 2 | Input 6 → 1+2+3+4+5+6 = 21 | 2 |

### B. Menulis Pseudocode FOR (Bobot 25%)

| Kriteria | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| Soal 3 (genap 2–20) | Tidak bisa | Struktur salah | STEP 2 benar | Benar semua |
| Soal 4 (tabel 7) | Tidak bisa | Sebagian | Hampir benar | Tepat |
| Soal 5 (jumlah 1..n) | Tidak bisa | Sebagian | Hampir benar | Tepat |

### C. Membaca Pseudocode WHILE (Bobot 15%)

| No | Jawaban | Skor |
|---|---|---|
| 6 | 1, 4, 9, 16, 25 (kuadrat 1–5) | 2 |
| 7 | Total: 10 (3+5+2) | 2 |

### D. Menulis Pseudocode WHILE (Bobot 20%)

| Kriteria | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| Soal 8 (jumlah + rata-rata) | Tidak bisa | Sebagian | Hampir benar | Tepat |
| Soal 9 (tebak angka) | Tidak bisa | Sebagian | Hampir benar | Tepat + petunjuk |

### E. Studi Kasus Faktorial (Bobot 25%)

| Kriteria | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| Versi FOR | Tidak selesai | Logika salah | Benar | Benar + rapi |
| Versi WHILE | Tidak selesai | Logika salah | Benar | Benar + rapi |
| Test case (3/3 benar) | 0 benar | 1 benar | 2 benar | 3 benar |

---

## Kunci Jawaban

### Soal 1
`FOR i ← 1 TO 4` → i=1: 2, i=2: 4, i=3: 6, i=4: 8
Output: `2 4 6 8`

### Soal 2
n=6 → total = 0+1+2+3+4+5+6 = 21
Output: `21`

### Soal 3
```
PROGRAM genap_2_20
    FOR i ← 2 TO 20 STEP 2
        OUTPUT i
    ENDFOR
END
```

### Soal 4
```
PROGRAM tabel_perkalian_7
    FOR i ← 1 TO 10
        hasil ← 7 × i
        OUTPUT "7 × ", i, " = ", hasil
    ENDFOR
END
```

### Soal 5
```
PROGRAM jumlah_1_ke_n
    INPUT n
    total ← 0
    FOR i ← 1 TO n
        total ← total + i
    ENDFOR
    OUTPUT total
END
```

### Soal 6
Fungsi kuadrat: WHILE x <= 5
x=1 → 1, x=2 → 4, x=3 → 9, x=4 → 16, x=5 → 25
Output: `1 4 9 16 25`

### Soal 7
Input: 3, 5, 2, 0
total = 0+3+5+2 = 10 (0 stop)
Output: `Total: 10`

### Soal 8
```
PROGRAM jumlah_rata2
    total ← 0
    count ← 0
    INPUT x
    WHILE x ≠ 0
        total ← total + x
        count ← count + 1
        INPUT x
    ENDWHILE
    OUTPUT "Jumlah: ", total
    IF count > 0 THEN
        rata ← total / count
        OUTPUT "Rata-rata: ", rata
    ENDIF
END
```

### Soal 9
```
PROGRAM tebak_angka
    angka_rahasia ← 8
    tebakan ← 0
    WHILE tebakan ≠ angka_rahasia
        INPUT tebakan
        IF tebakan < angka_rahasia THEN
            OUTPUT "Terlalu kecil!"
        ELSE
            IF tebakan > angka_rahasia THEN
                OUTPUT "Terlalu besar!"
            ENDIF
        ENDIF
    ENDWHILE
    OUTPUT "Selamat! Tebakan benar!"
END
```

### Soal 10 — Faktorial

**FOR:**
```
PROGRAM faktorial_for
    INPUT n
    hasil ← 1
    FOR i ← 1 TO n
        hasil ← hasil × i
    ENDFOR
    OUTPUT n, "! = ", hasil
END
```

**WHILE:**
```
PROGRAM faktorial_while
    INPUT n
    hasil ← 1
    i ← 1
    WHILE i <= n
        hasil ← hasil × i
        i ← i + 1
    ENDWHILE
    OUTPUT n, "! = ", hasil
END
```

Test case:
| n | n! | Hasil |
|---|---|---|
| 3 | 6 | 6 |
| 5 | 120 | 120 |
| 7 | 5040 | 5040 |

---

**MGMP Informatika SMAN 6 Cimahi**
