---
marp: true
theme: uncover
class: invert
---

# PERTEMUAN 8 — SEMESTER 2
## Pseudocode & Flowchart
### Informatika – Fase E / Kelas X
#### SMA Negeri 6 Cimahi

---

## Review PTS

Kemarin kalian mengerjakan:
- Stack, Queue, Searching, Sorting
- Semua ditulis dalam **bahasa Indonesia**

> Tapi komputer tidak ngerti bahasa Indonesia!
> Komputer butuh instruksi yang **standar & tidak ambigu**

---

## Apersepsi

"Coba jelaskan cara membuat kopi ke teman sebangku!"

Diskusi:
- Ada yang urutannya beda
- Ada yang kurang jelas
- Ada yang terlalu detail

> Nah, pseudocode & flowchart adalah bahasa **standar** untuk algoritma!

---

# TUJUAN PEMBELAJARAN

1. ✅ Notasi pseudocode (INPUT, OUTPUT, assignment, IF, FOR)
2. ✅ Simbol-simbol flowchart
3. ✅ Membaca & menulis pseudocode
4. ✅ Membaca & menggambar flowchart
5. ✅ Translasi pseudocode ↔ flowchart

---

## Apa Itu Pseudocode?

**Pseudo** = mirip/palsu
**Code** = kode program

> Pseudocode = kode mirip pemrograman, tapi lebih sederhana

Ciri:
- Tidak terikat bahasa pemrograman
- Fokus pada **logika**
- Bisa diterjemahkan ke Python, C++, Java, dll.

---

## Notasi Pseudocode

| Notasi | Makna | Contoh |
|---|---|---|
| `INPUT` | Baca input | `INPUT nama` |
| `OUTPUT` | Tampilkan | `OUTPUT "Halo"` |
| `←` | Simpan nilai | `x ← 5` |
| `IF...THEN...ELSE` | Percabangan | `IF x>0` |
| `FOR...ENDFOR` | Perulangan | `FOR i←1 TO 5` |
| `WHILE` | Ulang selama | `WHILE x<10` |

---

## Contoh Pseudocode

```
PROGRAM jumlah_dua_bilangan
    INPUT a
    INPUT b
    hasil ← a + b
    OUTPUT hasil
END
```

### Output jika a=5 dan b=3?
> **8**

---

## Contoh Pseudocode — Genap/Ganjil

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

### Output jika x=7?
> **Ganjil**

---

## Apa Itu Flowchart?

**Flowchart** = diagram alir — representasi **visual** dari algoritma

> "Satu gambar bernilai seribu kata"

---

## Simbol Flowchart

| Simbol | Nama | Fungsi |
|---|---|---|
| ⬭ Oval | Terminator | Start / End |
| ▭ Persegi | Proses | Assignment |
| ◇ Belah Ketupat | Decision | IF (Ya/Tidak) |
| ▱ Jajar Genjang | I/O | INPUT / OUTPUT |
| ➡ Panah | Arrow | Arah aliran |

---

## Contoh Flowchart

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
      │ x>0? │── Ya ──→ ┌──────────┐
      └──┬───┘          │ OUTPUT   │
         │ Tidak        │ "Positif"│
         ▼              └──────────┘
      ┌──────┐                 │
      │ x<0? │── Ya ──→ ┌──────────┐
      └──┬───┘          │ OUTPUT   │
         │ Tidak        │ "Negatif"│
         ▼              └──────────┘
   ┌──────────┐              │
   │ OUTPUT   │              │
   │  "Nol"   │              │
   └────┬─────┘              │
        │◄───────────────────┘
        ▼
   ┌─────────────┐
   │    End      │
   └─────────────┘
```

---

## Translasi Pseudocode ↔ Flowchart

| Pseudocode | Flowchart |
|---|---|
| `INPUT/OUTPUT` | ▱ Jajar Genjang |
| `←` Assignment | ▭ Persegi Panjang |
| `IF...THEN...ELSE` | ◆ Decision |
| `FOR/WHILE` | ◆ + ▭ |
| `PROGRAM...END` | ⬭ Oval |

> **Keduanya bisa dikonversi satu sama lain!**

---

## Aktivitas 1: Baca & Tulis Pseudocode

### Individu — 15 menit

1. Baca pseudocode — apa output jika input=7?
2. Baca pseudocode FOR — output apa?
3. Tulis pseudocode genap/ganjil
4. Tulis pseudocode luas segitiga

---

## Aktivitas 2: Baca & Gambar Flowchart

### Berpasangan — 10 menit

5. Gambar flowchart dari pseudocode cek kelulusan
6. Baca flowchart angka positif/negatif — algoritma apa?

---

## Aktivitas 3: Translasi

### Berpasangan — 10 menit

7. Ubah flowchart → pseudocode (penjumlahan)
8. Ubah pseudocode → flowchart (hitung diskon)

---

## Rangkuman

| Aspek | Pseudocode | Flowchart |
|---|---|---|
| **Bentuk** | Teks | Gambar |
| **Kelebihan** | Cepat ditulis | Mudah dipahami visual |
| **Kapan pakai** | Saat coding | Saat presentasi |

> Dua sisi mata uang yang sama!

---

## Pertemuan Depan

### Input/Output & Percabangan dalam Pseudocode
> Memperdalam pseudocode untuk algoritma yang lebih kompleks

---

# Terima Kasih

### MGMP Informatika SMAN 6 Cimahi

> "Algoritma yang baik dimulai dengan notasi yang jelas."
