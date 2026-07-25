# MODUL AJAR INFORMATIKA – FASE E (KELAS X)

| Komponen | Deskripsi |
|---|---|
| **Mata Pelajaran** | Informatika |
| **Fase / Kelas** | E / X |
| **Semester** | 2 (Genap) |
| **Pertemuan ke-** | 9 |
| **Alokasi Waktu** | 2 JP × 45 menit (90 menit) |
| **Tahun Pelajaran** | 2026/2027 |
| **Satuan Pendidikan** | SMA Negeri 6 Cimahi |

---

## Tujuan Pembelajaran

| TP | IKTP |
|---|---|
| **BK 1.4:** Menulis dan menerjemahkan notasi algoritma | 1.4.6 Menggunakan INPUT/OUTPUT dalam pseudocode |
| | 1.4.7 Menggunakan assignment dan tipe data dasar |
| | 1.4.8 Menulis percabangan IF-THEN-ELSE, nested IF |
| | 1.4.9 Menyelesaikan studi kasus (nilai → huruf mutu) |

---

## Langkah Pembelajaran

### Pembukaan (10 menit)

| Kegiatan | Waktu |
|---|---|
| 1. Salam, doa, cek kehadiran | 2 menit |
| 2. **Review**: "Pertemuan lalu kita belajar pseudocode & flowchart. Sekarang kita perdalam pseudocode — khususnya input/output dan percabangan." | 3 menit |
| 3. **Apersepsi**: "Siapa yang pernah lihat nilai rapor dikonversi ke huruf A, B, C, D? Itu contoh percabangan! Hari ini kita belajar menulis aturan seperti itu dalam pseudocode." | 5 menit |

### Inti (65 menit)

#### Memahami (20 menit)

**1. INPUT, OUTPUT, dan Assignment (8 menit)**
- **INPUT**: membaca data dari pengguna
- **OUTPUT**: menampilkan data ke layar
- **Assignment (←)**: menyimpan nilai ke variabel
- **Tipe data**: numerik (angka), string (teks), boolean (true/false)

| Konsep | Pseudocode | Makna |
|---|---|---|
| INPUT | `INPUT nama` | Baca teks → simpan ke `nama` |
| INPUT angka | `INPUT x` | Baca angka → simpan ke `x` |
| OUTPUT teks | `OUTPUT "Halo"` | Tampilkan teks |
| OUTPUT variabel | `OUTPUT x` | Tampilkan isi `x` |
| Assignment | `x ← 5` | Simpan 5 ke `x` |
| Assignment hitung | `total ← a + b` | Jumlahkan, simpan hasil |

**2. Percabangan IF-THEN-ELSE (7 menit)**
- **IF sederhana**: `IF kondisi THEN ... ENDIF`
- **IF-ELSE**: `IF kondisi THEN ... ELSE ... ENDIF`
- **Nested IF**: IF di dalam IF
- **Operator perbandingan**: `=`, `≠` atau `!=`, `>`, `<`, `>=`, `<=`
- **Operator logika**: `AND`, `OR`, `NOT`

**3. Contoh: Nilai ke Huruf Mutu (5 menit)**
```
INPUT nilai
IF nilai >= 92 THEN
    OUTPUT "A"
ELSE
    IF nilai >= 83 THEN
        OUTPUT "B"
    ELSE
        IF nilai >= 75 THEN
            OUTPUT "C"
        ELSE
            OUTPUT "D"
        ENDIF
    ENDIF
ENDIF
```

#### Mengaplikasi (35 menit)

**4. Aktivitas 1 — Menulis Pseudocode Sederhana (10 menit) — Individu**
   - "Tulis pseudocode untuk menghitung diskon 10% jika belanja > 100.000"
   - "Tulis pseudocode untuk menentukan bilangan genap/ganjil dengan OUTPUT sesuai"

**5. Aktivitas 2 — Nested IF (10 menit) — Berpasangan**
   - "Tulis pseudocode: input 3 angka → output terbesar"
   - "Tulis pseudocode: input suhu → output 'Panas' (>30), 'Dingin' (<20), 'Sejuk' (20-30)"

**6. Aktivitas 3 — Studi Kasus Nilai Akhir (15 menit) — Kelompok**
   - Input: nilai tugas (30%), UTS (30%), PAS (40%)
   - Hitung nilai akhir
   - Konversi ke huruf mutu (A: ≥92, B: ≥83, C: ≥75, D: <75)
   - Output: nilai akhir dan huruf mutu

#### Merefleksi (5 menit)

**7. Refleksi (5 menit)**
   - "Apa perbedaan IF sederhana dan nested IF?"
   - "Kapan kita perlu nested IF?"

### Penutup (15 menit)

| Kegiatan | Waktu |
|---|---|
| 1. Rangkuman | 3 menit |
| 2. Preview: "Pertemuan 10 — Perulangan dalam Pseudocode (FOR, WHILE)" | 3 menit |
| 3. Tugas rumah: Selesaikan studi kasus nilai akhir + gambar flowchart-nya | 5 menit |
| 4. Doa & salam | 4 menit |

---

## Asesmen

| Kriteria | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| INPUT/OUTPUT | Tidak bisa | Sebagian | Benar | Benar + rapi |
| IF sederhana | Tidak bisa | Struktur salah | Struktur benar | Benar + logika tepat |
| Nested IF | Tidak bisa | Sebagian | Benar | Benar + efisien |
| Studi kasus | Tidak selesai | Sebagian | Hampir sempurna | Sempurna + rapi |

---

**MGMP Informatika SMAN 6 Cimahi**
