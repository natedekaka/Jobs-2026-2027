# MODUL AJAR INFORMATIKA – FASE E (KELAS X)

| Komponen | Deskripsi |
|---|---|
| **Mata Pelajaran** | Informatika |
| **Fase / Kelas** | E / X |
| **Semester** | 2 (Genap) |
| **Pertemuan ke-** | 10 |
| **Alokasi Waktu** | 2 JP × 45 menit (90 menit) |
| **Tahun Pelajaran** | 2026/2027 |
| **Satuan Pendidikan** | SMA Negeri 6 Cimahi |

---

## Tujuan Pembelajaran

| TP | IKTP |
|---|---|
| **BK 1.4:** Menulis dan menerjemahkan notasi algoritma | 1.4.10 Menjelaskan konsep perulangan (looping) |
| | 1.4.11 Menggunakan FOR untuk perulangan dengan counter |
| | 1.4.12 Menggunakan WHILE untuk perulangan bersyarat |
| | 1.4.13 Membedakan FOR, WHILE, REPEAT-UNTIL |
| | 1.4.14 Menyelesaikan studi kasus dengan perulangan |

---

## Langkah Pembelajaran

### Pembukaan (10 menit)

| Kegiatan | Waktu |
|---|---|
| 1. Salam, doa, cek kehadiran | 2 menit |
| 2. **Review**: "Pertemuan 8 kita belajar pseudocode & flowchart. Pertemuan 9 kita belajar INPUT/OUTPUT dan IF. Masih kurang satu hal: **perulangan**." | 3 menit |
| 3. **Apersepsi**: "Coba sebutkan bilangan genap dari 2 sampai 20. — Tanpa perulangan, kita harus menulis OUTPUT 10 kali. Dengan perulangan, cukup 3 baris!" | 5 menit |

### Inti (65 menit)

#### Memahami (20 menit)

**1. Konsep Perulangan (5 menit)**
- **Perulangan (looping)** = menjalankan blok kode berulang kali
- **Mengapa penting?** Menghindari kode berulang, efisien
- **Tiga jenis perulangan:**

| Jenis | Kapan digunakan | Contoh |
|---|---|---|
| **FOR** | Jumlah perulangan **pasti** | Cetak 1–10 |
| **WHILE** | Perulangan **selama** kondisi TRUE | Ulang sampai tebak benar |
| **REPEAT-UNTIL** | Minimal **sekali** jalan dulu | Menu program |

**2. FOR — Perulangan dengan Counter (5 menit)**
```
FOR variabel ← nilai_awal TO nilai_akhir
    {kode yang diulang}
ENDFOR
```

**Contoh:**
```
FOR i ← 1 TO 5
    OUTPUT i
ENDFOR
```
→ Output: 1 2 3 4 5

**3. WHILE — Perulangan Bersyarat (5 menit)**
```
WHILE kondisi TRUE
    {kode yang diulang}
ENDWHILE
```

**Contoh:**
```
x ← 1
WHILE x <= 5
    OUTPUT x
    x ← x + 1
ENDWHILE
```
→ Output: 1 2 3 4 5

**4. REPEAT-UNTIL — Minimal Sekali (5 menit)**
```
REPEAT
    {kode yang diulang}
UNTIL kondisi TRUE
```

**Contoh:**
```
x ← 1
REPEAT
    OUTPUT x
    x ← x + 1
UNTIL x > 5
```
→ Output: 1 2 3 4 5

#### Mengaplikasi (35 menit)

**5. Aktivitas 1 — FOR (10 menit) — Individu**
   - "Cetak bilangan genap 2–20 dengan FOR"
   - "Cetak tabel perkalian 5 (5×1=5 sampai 5×10=50)"
   - "Hitung jumlah 1+2+3+...+10"

**6. Aktivitas 2 — WHILE (10 menit) — Berpasangan**
   - "WHILE: input angka terus sampai pengguna mengetik 0, lalu tampilkan jumlah"
   - "WHILE: tebak angka (angka rahasia 7), terus minta tebak sampai benar"

**7. Aktivitas 3 — Studi Kasus Faktorial (15 menit) — Kelompok**
   - "Buat pseudocode untuk menghitung faktorial n (n! = n × (n-1) × ... × 1)"
   - "Selesaikan dengan FOR dan dengan WHILE — bandingkan"

#### Merefleksi (5 menit)

**8. Refleksi (5 menit)**

### Penutup (15 menit)

| Kegiatan | Waktu |
|---|---|
| 1. Rangkuman — kapan pakai FOR, WHILE, REPEAT-UNTIL | 3 menit |
| 2. Preview: "Pertemuan 11 — Latihan Soal Algoritma" | 3 menit |
| 3. Tugas rumah: cetak deret Fibonacci (0,1,1,2,3,5,8,...) sampai suku ke-10 | 5 menit |
| 4. Doa & salam | 4 menit |

---

## Asesmen

| Kriteria | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| FOR | Tidak bisa | Sebagian | Benar | Benar + kreatif |
| WHILE | Tidak bisa | Sebagian | Benar | Benar + logika tepat |
| Studi kasus | Tidak selesai | Sebagian | Lengkap | Lengkap + 2 versi |

---

## Bahan: Perbandingan FOR vs WHILE vs REPEAT-UNTIL

| Aspek | FOR | WHILE | REPEAT-UNTIL |
|---|---|---|---|
| Counter otomatis | ✅ Ya | ❌ Manual | ❌ Manual |
| Kondisi di awal | ✅ (implisit) | ✅ | ❌ (di akhir) |
| Minimal eksekusi | 0 (jika range kosong) | 0 (kondisi awal FALSE) | 1 (jalan dulu) |
| Cocok untuk | Jumlah pasti | Kondisi berubah | Minimal 1 kali |

---

**MGMP Informatika SMAN 6 Cimahi**
