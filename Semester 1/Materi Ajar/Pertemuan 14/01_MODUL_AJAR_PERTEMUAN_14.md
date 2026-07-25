# MODUL AJAR INFORMATIKA – FASE E (KELAS X)

## Informasi Umum

| Komponen | Deskripsi |
|---|---|
| **Mata Pelajaran** | Informatika |
| **Fase / Kelas** | E / X |
| **Semester** | 1 (Ganjil) |
| **Pertemuan ke-** | 14 |
| **Alokasi Waktu** | 2 JP × 45 menit (90 menit) |
| **Tahun Pelajaran** | 2026/2027 |
| **Satuan Pendidikan** | **SMA Negeri 6 Cimahi** |

---

## Profil Pelajar Pancasila

| Dimensi | Indikator |
|---|---|
| Bernalar Kritis | Menganalisis kualitas data dan mengidentifikasi data bermasalah |
| Mandiri | Mengelola data dengan cermat dan bertanggung jawab |

---

## Sarana & Prasarana

| Sarana | Keterangan |
|---|---|
| Lab komputer / laptop | 1 unit per 2 siswa |
| Aplikasi | Excel / Google Sheets |
| Dataset contoh | Disiapkan guru (file CSV) |
| Proyektor / LCD | Untuk demo |

---

## Tujuan Pembelajaran (TP 1.2)

| TP | Indikator Ketercapaian Tujuan Pembelajaran (IKTP) |
|---|---|
| **BK 1.2:** Memahami kualitas data, prinsip GIGO, dan mampu mengidentifikasi data bermasalah | 1.2.1 Menjelaskan pengertian data berkualitas dan ciri-cirinya<br>1.2.2 Menjelaskan prinsip GIGO (Garbage In, Garbage Out)<br>1.2.3 Mengidentifikasi berbagai jenis data bermasalah (format, anomali, duplikat, outlier)<br>1.2.4 Menganalisis dampak data tidak berkualitas pada pengambilan keputusan |

---

## Peta Kompetensi

```
Pertemuan 14 — Konsep Kualitas Data & GIGO
│
├── Pendahuluan (10 menit)
│   ├── Review keamanan akun: siapa yang sudah audit?
│   └── Apersepsi: "Pernah salah transfer karena salah angka? Itulah GIGO."
│
├── Inti (65 menit)
│   ├── Memahami (15 menit)
│   │   ├── Data berkualitas vs tidak
│   │   ├── Prinsip GIGO — contoh nyata
│   │   └── Jenis data bermasalah
│   │
│   ├── Mengaplikasi (40 menit)
│   │   └── [40'] Praktik identifikasi data bermasalah (dataset)
│   │
│   └── Merefleksi (10 menit)
│       └── Dampak data tidak berkualitas
│
└── Penutup (15 menit)
```

---

## Langkah Pembelajaran

### Pembukaan (10 menit)

| Kegiatan | Waktu |
|---|---|
| 1. Salam, doa, cek kehadiran | 2 menit |
| 2. **Review**: Tanya 2–3 siswa hasil audit privasi — perubahan paling signifikan? | 4 menit |
| 3. **Apersepsi**: Cerita — "Tahun 1999, NASA kehilangan Mars Climate Orbiter senilai $327 juta karena satu tim pakai satuan imperial dan tim lain pakai metrik. Data tidak konsisten → roket meledak." | 2 menit |
| 4. Sampaikan tujuan: hari ini kita belajar **kualitas data** — karena data jelek = keputusan jelek | 2 menit |

### Inti (65 menit)

#### Memahami (berkesadaran, menggembirakan) — 15 menit

1. **Data Berkualitas vs Tidak (5 menit)**

   | Kriteria | Data Berkualitas | Data Tidak Berkualitas |
   |---|---|---|
   | **Akurat** | Sesuai kenyataan | Salah, typo |
   | **Lengkap** | Semua field terisi | Banyak null/missing |
   | **Konsisten** | Format seragam | Format campur aduk |
   | **Tepat waktu** | Data terbaru | Data usang |
   | **Relevan** | Sesuai kebutuhan | Tidak relevan |

2. **Prinsip GIGO — Garbage In, Garbage Out (5 menit)**

   ```
   Data MASUK (Input)  →  Proses  →  Data KELUAR (Output)
   ❌ Sampah            ❌ Apapun  ❌ Sampah juga
   ✅ Berkualitas       ✅ Benar   ✅ Berkualitas
   ```

   **Contoh nyata GIGO:**
   | Kasus | Input Salah | Akibat |
   |---|---|---|
   | Transfer bank | Salah satu digit no rekening | Uang ke rekening lain |
   | Nilai rapor | Nilai "80" tertulis "8" | Siswa dapat nilai jelek |
   | Data penduduk | Tanggal lahir 01-01-1900 (default) | Ribuan orang "berusia 120+" |
   | Mars Orbiter | Satuan pound-force vs newton | Pesawat meledak ($327M) |

3. **Jenis Data Bermasalah (5 menit)**

   | Jenis | Contoh | Dampak |
   |---|---|---|
   | **Format tidak konsisten** | Tanggal: 01/02/2025 vs 2 Jan 2025 vs 2025-01-02 | Sulit diolah |
   | **Missing value (kosong)** | Kolom alamat tidak diisi | Data tidak lengkap |
   | **Duplicate** | Data siswa muncul 2× | Perhitungan dobel |
   | **Outlier (pencilan)** | Usia 200 tahun | Analisis statistik bias |
   | **Typo / salah ketik** | "Jakartaa", "0813-..." bukan angka | Tidak bisa diproses |
   | **Inkon sistensi** | "L" / "LK" / "Laki" / "Laki-laki" | Sulit dikategorikan |

#### Mengaplikasi (bermakna, menggembirakan) — 40 menit

4. **Praktik Identifikasi Data Bermasalah (40 menit) — Berpasangan**

   **Skenario:** Guru menyediakan dataset "Data Siswa" yang mengandung berbagai masalah kualitas data.

   **Contoh dataset (guru siapkan di Excel/Sheets):**
   | Nama | Kelas | Tgl Lahir | No HP | Nilai | Alamat |
   |---|---|---|---|---|---|
   | Andi Pratama | X-1 | 15-03-2009 | 08123456789 | 85 | Cimahi |
   | Budi Santoso | X-1 | 2009-05-20 | 08234567890 | | Cimahi |
   | Cici | X-2 | 20/05/2009 | 08345678901 | 95 | |
   | Andi Pratama | X-1 | 15-03-2009 | 08123456789 | 85 | Cimahi |
   | Dedi | X-3 | 01-01-1900 | 08456789 | 200 | Bandung |
   | Euis | X-1 | 10-10-2009 | 08567ABCD | Tujuhpuluh | Cimahi |
   | Fitri | X-2 | 30-02-2009 | 08678901234 | 80 | Cimahi |

   **Tugas per pasangan:**
   | Langkah | Waktu | Aktivitas |
   |---|---|---|
   | 1. Buka dataset | 3 menit | Copy dataset ke spreadsheet |
   | 2. Identifikasi masalah | 15 menit | Cari dan catat semua data bermasalah |
   | 3. Klasifikasikan | 10 menit | Tentukan jenis masalah tiap baris |
   | 4. Analisis dampak | 7 menit | Apa dampak jika data ini diproses? |
   | 5. Siapkan laporan | 5 menit | Tulis temuan di LKPD |

   **Laporan temuan (format tabel di LKPD):**

   | Baris | Field | Masalah | Jenis | Dampak |
   |---|---|---|---|---|

   **Diferensiasi:**
   - **Pemula**: Identifikasi minimal 5 masalah
   - **Mahir**: Identifikasi semua masalah + usulan perbaikan
   - **Excel**: Dataset lebih besar (20+ baris) dengan masalah lebih kompleks

#### Merefleksi (berkesadaran, bermakna) — 10 menit

5. **Diskusi Kelas (5 menit)**
   - Masalah apa yang paling sering ditemukan?
   - Bagaimana perasaan kalian melihat data sekacau itu?
   - "Kalau data nilai kaya gitu di sekolah, apa jadinya?"

6. **Refleksi Individu (5 menit)**
   - Satu contoh GIGO dalam kehidupan sehari-hari
   - Skala pemahaman kualitas data: ___ / 10

### Penutup (15 menit)

| Kegiatan | Waktu |
|---|---|
| 1. Rangkuman: "Data berkualitas = akurat + lengkap + konsisten. GIGO: sampah masuk, sampah keluar." | 3 menit |
| 2. Tanya jawab | 5 menit |
| 3. **Tugas**: Cari 1 berita tentang dampak data tidak berkualitas (bencana karena GIGO) — tulis ringkasan | 3 menit |
| 4. Sampaikan pertemuan depan: Validasi, Verifikasi & Data Cleansing — kita bersihkan dataset ini! | 2 menit |
| 5. Doa & salam | 2 menit |

---

## Asesmen

### Rubrik Formatif — LKPD

| Kriteria | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| **Identifikasi masalah** | < 3 masalah | 3–4 masalah | 5–6 masalah | ≥ 7 masalah |
| **Klasifikasi jenis** | Tidak tepat | Sebagian tepat | Tepat | Tepat + analisis |
| **Analisis dampak** | Tidak ada | Minimal | Cukup | Mendalam |

---

## Lampiran: Dataset Praktik

(File terpisah: `DATASET_Pertemuan14.csv`)

---

**MGMP Informatika SMAN 6 Cimahi**
