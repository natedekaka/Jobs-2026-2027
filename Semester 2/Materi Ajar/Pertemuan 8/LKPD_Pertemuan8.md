# LEMBAR KERJA PESERTA DIDIK (LKPD)
## Pertemuan 8 – Pseudocode & Flowchart

| TP | BK 1.4 — Notasi Algoritma |
|---|---|
| Nama | ____________________ |
| Kelas | ____________________ |

---

### A. MEMBACA PSEUDOCODE (15 menit)

**Soal 1:** Baca pseudocode berikut — apa outputnya jika input = 7?

```
PROGRAM soal1
    INPUT x
    IF x > 0 THEN
        OUTPUT "Positif"
    ELSE
        IF x < 0 THEN
            OUTPUT "Negatif"
        ELSE
            OUTPUT "Nol"
        ENDIF
    ENDIF
END
```

Jawab: _________________________________

**Soal 2:** Baca pseudocode berikut — apa outputnya?

```
PROGRAM soal2
    FOR i ← 1 TO 4
        OUTPUT i × 2
    ENDFOR
END
```

Jawab: _________________________________

---

### B. MENULIS PSEUDOCODE

**Soal 3:** Tulis pseudocode untuk algoritma menentukan **bilangan genap atau ganjil**!

```
PROGRAM genap_ganjil

    _________________________________

    _________________________________

    _________________________________

    _________________________________

    _________________________________
END
```

**Soal 4:** Tulis pseudocode untuk algoritma **menghitung luas segitiga** (alas × tinggi / 2)!

```
PROGRAM luas_segitiga

    _________________________________

    _________________________________

    _________________________________

    _________________________________

END
```

---

### C. MEMBACA & MENGGAMBAR FLOWCHART (10 menit)

**Soal 5:** Gambar flowchart dari pseudocode berikut:

```
PROGRAM cek_kelulusan
    INPUT nilai
    IF nilai >= 75 THEN
        OUTPUT "Lulus"
    ELSE
        OUTPUT "Remidi"
    ENDIF
END
```

Gambar flowchart (gunakan penggaris!):

```

(Buat di buku tugas atau halaman kosong — tempel di sini)

```

**Soal 6:** Baca flowchart berikut — algoritma apa yang dijalankan?

```
   ┌─────────────┐
   │    Start    │
   └──────┬──────┘
          ▼
   ┌─────────────┐
   │ INPUT angka │
   └──────┬──────┘
          ▼
      ┌──────┐
      │angka │
      │ > 0? │── Ya ──→ ┌──────────────┐
      └──┬───┘          │OUTPUT "Positif│
         │ Tidak        └──────┬───────┘
         ▼                     │
      ┌──────┐                 │
      │angka │                 │
      │ < 0? │── Ya ──→ ┌──────────────┐
      └──┬───┘          │OUTPUT "Negatif│
         │ Tidak        └──────┬───────┘
         ▼                     │
   ┌──────────────┐            │
   │OUTPUT "Nol"  │            │
   └──────┬───────┘            │
          │◄───────────────────┘
          ▼
   ┌─────────────┐
   │    End      │
   └─────────────┘
```

Jawab: _________________________________

---

### D. TRANSLASI (10 menit)

**Soal 7:** Ubah flowchart berikut ke pseudocode!

Flowchart:
```
   ┌─────────────┐
   │    Start    │
   └──────┬──────┘
          ▼
   ┌─────────────┐
   │ INPUT a,b   │
   └──────┬──────┘
          ▼
   ┌─────────────┐
   │hasil ← a + b│
   └──────┬──────┘
          ▼
   ┌─────────────┐
   │OUTPUT hasil │
   └──────┬──────┘
          ▼
   ┌─────────────┐
   │    End      │
   └─────────────┘
```

Pseudocode:
```
PROGRAM ________________

    ____________________

    ____________________

    ____________________

    ____________________
END
```

**Soal 8:** Ubah pseudocode berikut ke flowchart!

```
PROGRAM hitung_diskon
    INPUT harga
    IF harga > 100000 THEN
        diskon ← harga × 0.1
    ELSE
        diskon ← 0
    ENDIF
    total ← harga - diskon
    OUTPUT total
END
```

Gambar flowchart di buku tugas!

---

### E. REFLEKSI (5 menit)

| Pertanyaan | Jawaban |
|---|---|
| Perbedaan pseudocode dan flowchart? | |
| Kapan pakai pseudocode? | |
| Kapan pakai flowchart? | |
| Skala pemahaman (1–10) | / 10 |

---

### F. TUGAS RUMAH

Cari **1 contoh flowchart sederhana** dari internet. Tempel/ gambar di buku catatan dan tuliskan penjelasan fungsinya dalam 2–3 kalimat!

---

**MGMP Informatika SMAN 6 Cimahi**
