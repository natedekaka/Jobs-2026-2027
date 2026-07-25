# ASESMEN – PERTEMUAN 9
## Input/Output & Percabangan dalam Pseudocode

Informatika – Fase E / Kelas X – SMA Negeri 6 Cimahi

---

## Rubrik Penilaian

### A. Membaca Pseudocode (Bobot 15%)

| Kriteria | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| Soal 1 (90 → Lulus) | Salah | — | — | Benar |
| Soal 2 (a=12,b=7 → 12) | Salah | Salah 1 | — | Benar semua |

### B. Menulis Pseudocode Sederhana (Bobot 30%)

| Kriteria | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| Struktur (INPUT, OUTPUT, IF/ENDIF) | Tidak sesuai | Sebagian | Hampir benar | Tepat semua |
| Logika (benar secara algoritma) | Tidak berfungsi | Sebagian benar | Hampir benar | Tepat semua |

### C. Nested IF (Bobot 25%)

| Kriteria | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| Maks 3 angka | Tidak bisa | Struktur salah | Benar logika | Benar + efisien |
| Suhu udara | Tidak bisa | Struktur salah | Benar logika | Benar + efisien |

### D. Studi Kasus Nilai Akhir (Bobot 30%)

| Kriteria | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| Rumus nilai akhir | Tidak ada | Salah | Benar | Benar |
| Konversi huruf mutu | Tidak ada | Sebagian | Benar | Benar + rapi |
| Output | Tidak ada | Sebagian | Lengkap | Lengkap + rapi |
| Test case (3 data) | 0 benar | 1 benar | 2 benar | 3 benar |

---

## Kunci Jawaban LKPD

### Soal 1
Input 90 → 90 >= 75 → "Lulus"

### Soal 2
`a=12, b=7` → 12 > 7 → OUTPUT 12
`a=5, b=9` → 5 > 9? FALSE → ELSE → OUTPUT 9

### Soal 3 — Diskon Belanja
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

### Soal 4 — Genap/Ganjil
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

### Soal 5 — Maks 3 Angka
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

### Soal 7 — Nilai Akhir

Test case:
| Tugas | UTS | PAS | Nilai Akhir | Huruf |
|---|---|---|---|---|
| 90 | 85 | 95 | 90×0.3=27 + 85×0.3=25,5 + 95×0.4=38 = **90,5** | A (≥92? Tidak → ≥83? Ya → **B**) |
| 70 | 65 | 80 | 21 + 19,5 + 32 = **72,5** | D (<75) |
| 50 | 55 | 60 | 15 + 16,5 + 24 = **55,5** | D (<75) |

*Koreksi: 90,5 < 92 → bukan A. ≥83 → B*

```
PROGRAM nilai_akhir
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

---

**MGMP Informatika SMAN 6 Cimahi**
