# MODUL AJAR INFORMATIKA – FASE E (KELAS X)

| Komponen | Deskripsi |
|---|---|
| **Mata Pelajaran** | Informatika |
| **Fase / Kelas** | E / X |
| **Semester** | 2 (Genap) |
| **Pertemuan ke-** | 12 |
| **Alokasi Waktu** | 2 JP × 45 menit (90 menit) |
| **Tahun Pelajaran** | 2026/2027 |
| **Satuan Pendidikan** | SMA Negeri 6 Cimahi |

---

## Tujuan Pembelajaran

| TP | IKTP |
|---|---|
| **BK 1.4** Menulis notasi algoritma | 1.4.15 Mentranslasi pseudocode ke Python |
| **BK 2.1** Mengenal lingkungan pemrograman Python | 2.1.1 Menjalankan Python (IDLE/terminal/online) |
| | 2.1.2 Menggunakan variabel dan assignment |
| | 2.1.3 Menggunakan tipe data int, float, str, bool |
| | 2.1.4 Menggunakan input() dan print() |
| | 2.1.5 Menggunakan if-elif-else |

---

## Langkah Pembelajaran

### Pembukaan (10 menit)

| Kegiatan | Waktu |
|---|---|
| 1. Salam, doa, cek kehadiran | 2 menit |
| 2. **Review**: "11 pertemuan kita belajar algoritma — pseudocode, flowchart, struktur data. Mulai hari ini, algoritma itu akan **hidup**!" | 3 menit |
| 3. **Apersepsi**: Tampilkan pseudocode di papan tulis vs Python — "Hanya beda sedikit: `INPUT` → `input()`, `OUTPUT` → `print()`, `←` → `=`" | 5 menit |

### Inti (65 menit)

#### Memahami (25 menit)

**1. Cara Menjalankan Python (5 menit)**
- **Online**: Google Colab (colab.research.google.com) — tidak perlu instalasi
- **IDLE**: Start Menu → Python → IDLE
- **Terminal**: `python` atau `python3`
- **Pertama kali**: `print("Hello, World!")` — tradisi programmer!

**2. Variabel dan Tipe Data (5 menit)**

| Konsep | Pseudocode | Python |
|---|---|---|
| Assignment | `x ← 5` | `x = 5` |
| Tipe otomatis | — | `type(x)` |
| Integer | 5, -10 | `5`, `-10` |
| Float | 3.14 | `3.14` |
| String | "Halo" | `"Halo"` |
| Boolean | TRUE/FALSE | `True`/`False` |

**3. Input dan Output (5 menit)**

| Pseudocode | Python |
|---|---|
| `INPUT x` | `x = input()` — string |
| `INPUT x` (angka) | `x = int(input())` |
| `OUTPUT x` | `print(x)` |
| `OUTPUT "Halo", nama` | `print("Halo", nama)` |
| Gabung teks | `print(f"Halo {nama}")` — f-string |

**4. If-Elif-Else (5 menit)**

| Pseudocode | Python |
|---|---|
| `IF x>0 THEN` | `if x > 0:` |
| `ELSE` | `else:` |
| `ENDIF` | *(indentasi 4 spasi)* |
| `AND` | `and` |
| `OR` | `or` |
| `NOT` | `not` |

**5. Translasi Pseudocode → Python (5 menit)**
Tunjukkan tabel translasi lengkap (ada di Bahan Ajar).

#### Mengaplikasi (30 menit)

**6. Aktivitas 1 — "Hello, World!" & Variabel (10 menit) — Individu**
   - Buka Google Colab / IDLE
   - Jalankan `print("Hello, World!")`
   - Buat variabel nama, umur, kelas → print
   - Cek tipe data dengan `type()`

**7. Aktivitas 2 — Input & Output (10 menit) — Berpasangan**
   - Input nama → sapa
   - Input dua angka → jumlahkan
   - Input Celcius → output Fahrenheit
   - **Translasi**: Pseudocode → Python

**8. Aktivitas 3 — If-Elif-Else (10 menit) — Berpasangan**
   - Genap/ganjil
   - Nilai → huruf mutu (A/B/C/D)
   - **Translasi**: Ambil pseudocode dari pert 9 → tulis ulang di Python

#### Merefleksi (5 menit)

**9. Refleksi (5 menit)**

### Penutup (15 menit)

| Kegiatan | Waktu |
|---|---|
| 1. Rangkuman: "Pseudocode → Python sangat mirip. Yang perlu diingat: `input()`, `print()`, `=`, `:`, indentasi" | 3 menit |
| 2. Preview: "Pertemuan 13: Python — Perulangan FOR, WHILE, studi kasus" | 3 menit |
| 3. Tugas rumah: Translasi 3 pseudocode dari pert 9–10 ke Python, jalankan, catat hasil | 5 menit |
| 4. Doa & salam | 4 menit |

---

## Asesmen

| Kriteria | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| Menjalankan Python | Tidak bisa | Bantuan | Mandiri | Mandiri + eksplorasi |
| Variabel & tipe data | Tidak bisa | Sebagian | Benar | Benar + kreatif |
| Input/output | Tidak bisa | Bantuan | Mandiri variabel | Mandiri + f-string |
| If-elif-else | Tidak bisa | Struktur salah | Benar | Benar + nested if |

---

**MGMP Informatika SMAN 6 Cimahi**
