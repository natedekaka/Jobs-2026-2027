# KUNCI JAWABAN & RUBRIK PENILAIAN
## PENILAIAN AKHIR SEMESTER (PAS) GANJIL — INFORMATIKA FASE F / KELAS XI
### SMA Negeri 6 Cimahi — TP 2026/2027

---

## BAGIAN A — PILIHAN GANDA (25 Soal × 2 Poin = 50 Poin)

| No | Jawaban | No | Jawaban | No | Jawaban |
|---|---|---|---|---|---|
| 1 | **B** | 11 | **D** | 21 | **C** |
| 2 | **C** | 12 | **C** | 22 | **B** |
| 3 | **C** | 13 | **C** | 23 | **C** |
| 4 | **C** | 14 | **C** | 24 | **B** |
| 5 | **B** | 15 | **A** | 25 | **D** |
| 6 | **A** | 16 | **B** | | |
| 7 | **B** | 17 | **A** | | |
| 8 | **C** | 18 | **A** | | |
| 9 | **D** | 19 | **B** | | |
| 10 | **B** | 20 | **A** | | |

---

## BAGIAN B — ESAI (5 Soal × 10 Poin = 50 Poin)

### Soal 26 — Presensi Digital (10 poin)

| Bagian | Jawaban Contoh | Skor |
|---|---|---|
| **a. User Story** | **Siswa**: "Sebagai siswa, saya ingin mengisi presensi dengan mudah, sehingga saya tidak perlu antre tanda tangan." | 4 |
| (2 user story) | **Guru**: "Sebagai guru wali kelas, saya ingin melihat rekap presensi harian, sehingga saya bisa memantau kehadiran siswa." | |
| **b. Wireframe** | Kotak judul "Presensi Siswa" → Nama: [input] → Kelas: [dropdown] → Tombol "Presensi Sekarang" → Pesan sukses | 3 |
| **c. 3 Layer** | 1. **Frontend** (HTML/CSS/JS) — tampilan halaman presensi | 3 |
| | 2. **Backend** (PHP/Python/Node.js) — logika simpan data presensi | |
| | 3. **Database** (MySQL/PostgreSQL) — simpan data presensi siswa | |

### Soal 27 — Koin Greedy (10 poin)

| Bagian | Jawaban | Skor |
|---|---|---|
| **a. Langkah solusi** | 1. Rp 3.800: pakai Rp 1.000 (3×) → sisa Rp 800 | 4 |
| | 2. Rp 800: pakai Rp 500 (1×) → sisa Rp 300 | |
| | 3. Rp 300: pakai Rp 200 (1×) → sisa Rp 100 | |
| | 4. Rp 100: pakai Rp 100 (1×) → sisa Rp 0 | |
| | **Total**: 3 + 1 + 1 + 1 = **6 koin** | |
| **b. Pseudocode** | ``` | 4 |
| | procedure greedyKoin(pecahan, jumlah) | |
| | for each koin in pecahan do | |
| | while jumlah ≥ koin do | |
| | jumlah ← jumlah - koin | |
| | hitung ← hitung + 1 | |
| | end while | |
| | end for | |
| | return hitung | |
| | ``` | |
| **c. Optimal?** | Ya, untuk pecahan Rp 1000, 500, 200, 100 (kelipatan) greedy selalu optimal. Tapi jika pecahan tidak beraturan (misal 1000, 700, 300), greedy belum tentu optimal. | 2 |

### Soal 28 — Graph (10 poin)

| Bagian | Jawaban | Skor |
|---|---|---|
| **a. Graph** | A — B, A — C, B — D, C — D, C — E, D — E (gambar) | 3 |
| **b. Adjacency Matrix** | ``` | 3 |
| | A B C D E | |
| | A 0 1 1 0 0 | |
| | B 1 0 0 1 0 | |
| | C 1 0 0 1 1 | |
| | D 0 1 1 0 1 | |
| | E 0 0 1 1 0 | |
| | ``` | |
| **c. BFS (dari A)** | A → B → C → D → E (atau A → C → B → D → E, tergantung urutan tetangga) | 2 |
| **d. DFS (dari A)** | A → B → D → C → E (atau variasi lain, asalkan depth-first) | 2 |

### Soal 29 — Visualisasi Data (10 poin)

| Bagian | Jawaban Contoh | Skor |
|---|---|---|
| **a. 3 grafik + tujuan** | 1. **Column chart**: rata-rata nilai per kelas — membandingkan performa antar kelas | 6 |
| | 2. **Pie chart**: proporsi siswa remedial vs lulus — melihat persentase siswa yang perlu perhatian | |
| | 3. **Scatter plot**: korelasi UTS vs UAS — melihat hubungan kedua nilai (apakah siswa yang UTS bagus juga bagus di UAS) | |
| | Alternatif: Line chart tidak tepat (bukan data waktu); Histogram untuk distribusi nilai | |
| **b. 2 prinsip** | 1. **Sumbu Y dari 0**: agar perbandingan antar kelas tidak menyesatkan | 4 |
| | 2. **Minimalis / Data-ink ratio**: tidak perlu efek 3D, warna minimal, grid tipis — fokus pada data | |
| | Alternatif: warna konsisten, label jelas, chartjunk dihindari | |

### Soal 30 — Keamanan Data (10 poin)

| Bagian | Jawaban Contoh | Skor |
|---|---|---|
| **a. 3 kesalahan** | 1. Menggunakan HTTP (tidak terenkripsi) — data dikirim dalam bentuk teks | 3 |
| | 2. Database tidak dienkripsi — password tersimpan dalam plaintext | |
| | 3. Tidak ada firewall / penetration testing — celah keamanan tidak terdeteksi | |
| **b. 3 rekomendasi** | 1. Gunakan **HTTPS** dengan SSL/TLS — enkripsi data saat dikirim | 3 |
| | 2. **Enkripsi database** — hash password dengan bcrypt, enkripsi data sensitif | |
| | 3. **Penetration testing** rutin dan **firewall** — deteksi celah sebelum hacker | |
| **c. Pasal UU ITE** | **Pasal 30**: Intersepsi ilegal — 10 tahun / Rp 800 juta | 4 |
| | atau **Pasal 32**: Perusakan data elektronik — 8 tahun / Rp 2 miliar | |
| | atau **Pasal 35**: Phishing/penipuan — 12 tahun / Rp 12 miliar | |
| | (tergantung apakah data bocor karena intersepsi, perusakan, atau penipuan) | |

---

## Rubrik Penilaian Esai

| Skor | Kriteria |
|---|---|
| 10 | Jawaban lengkap, tepat, detail, contoh konkret, struktur jelas |
| 8–9 | Jawaban tepat, hampir lengkap, sedikit kurang detail |
| 6–7 | Jawaban benar tapi kurang detail atau kurang tepat sebagian |
| 4–5 | Jawaban setengah benar, banyak kurang |
| 2–3 | Jawaban kurang tepat, minimal |
| 1 | Ada usaha menjawab tapi salah |
| 0 | Tidak menjawab |

---

## Kriteria Penilaian Akhir

| Nilai Akhir | Predikat |
|---|---|
| 92–100 | A (Sangat Baik) |
| 83–91 | B+ (Baik Sekali) |
| 75–82 | B (Baik) |
| 67–74 | C+ (Cukup Baik) |
| 60–66 | C (Cukup) |
| < 60 | D (Kurang — Remedial) |

**Nilai Akhir = (Nilai PAS × 70%) + (Nilai Portofolio × 30%)**

Contoh:
- PAS: 80
- Portofolio: 85
- NA = (80 × 0,7) + (85 × 0,3) = 56 + 25,5 = **81,5 (B)** ✅

---

**MGMP Informatika SMAN 6 Cimahi**
