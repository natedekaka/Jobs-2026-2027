# MODUL AJAR INFORMATIKA – FASE F (KELAS XI)

| Komponen | Deskripsi |
|---|---|
| **Mata Pelajaran** | Informatika |
| **Fase / Kelas** | F / XI |
| **Semester** | 2 (Genap) |
| **Pertemuan ke-** | 2 |
| **Alokasi Waktu** | 5 JP × 45 menit (225 menit) |
| **Tahun Pelajaran** | 2026/2027 |
| **Satuan Pendidikan** | SMA Negeri 6 Cimahi |
| **Materi Esensial** | Pengolahan Data Bervolume Besar |

---

## Tujuan Pembelajaran

| TP | IKTP |
|---|---|
| **BK, AD:** Membersihkan dan memberi label pada dataset | 2.1 Mengidentifikasi masalah kualitas data (missing, duplikat, outlier) |
| | 2.2 Melakukan data cleaning dengan Google Sheets |
| | 2.3 Menjelaskan konsep data labeling untuk klasifikasi |
| | 2.4 Mempraktikkan labeling dataset sederhana |

---

## Langkah Pembelajaran

### Pembukaan (20 menit)

| Kegiatan | Waktu |
|---|---|
| 1. Salam, doa, cek kehadiran | 3 menit |
| 2. **Review**: "Pert 1: kita tahu sumber data legal — data.go.id. Tapi data dari sana belum tentu bersih. Ada yang kosong, duplikat, aneh." | 5 menit |
| 3. **Apersepsi**: Tampilkan dataset kotor (nilai: -5, 120, kosong, "Budi", "budi", "BUDI"). "Bisakah kita analisis data ini tanpa dibersihkan?" | 7 menit |
| 4. **Trigger**: "Garbage In, Garbage Out — data kotor → hasil analisis kotor" | 5 menit |

### Inti (170 menit)

#### Memahami (55 menit)

**1. Masalah Kualitas Data (20 menit)**

| Masalah | Definisi | Contoh | Dampak |
|---|---|---|---|
| **Missing Values** | Data kosong/tidak diisi | Nilai UTS kosong | Rata-rata jadi salah |
| **Duplicates** | Data yang sama muncul > 1× | "Budi" muncul 3× | Perhitungan ganda |
| **Outliers** | Nilai yang tidak wajar | Nilai 1000 dari skala 0–100 | Statistik melenceng |
| **Inconsistent** | Format tidak seragam | "Jl. Merdeka", "Jalan Merdeka", "Jl.Merdeka" | Sulit dikelompokkan |
| **Typo** | Salah ketik | "Cimahi" vs "Cimahy" | Tidak match saat filter |

**2. Teknik Data Cleaning (20 menit)**

| Teknik | Cara di Google Sheets | Cara di Python |
|---|---|---|
| Cek missing | `=ISBLANK()` | `df.isnull().sum()` |
| Isi missing | Isi rata-rata / hapus baris | `df.fillna()` / `df.dropna()` |
| Hapus duplikat | Data → Data cleanup → Remove duplicates | `df.drop_duplicates()` |
| Deteksi outlier | Filter → sort → cari nilai ekstrem | `df[df > threshold]` |
| Standarisasi | `=UPPER()`, `=LOWER()`, `=PROPER()` | `df['kolom'].str.lower()` |
| Trim spasi | `=TRIM()` | `df['kolom'].str.strip()` |

**3. Data Labeling (15 menit)**

> **Labeling** = memberi label/kategori pada data untuk pembelajaran mesin.

| Jenis Labeling | Contoh |
|---|---|
| **Klasifikasi biner** | Email: Spam / Bukan Spam |
| **Klasifikasi multi-kelas** | Sentimen: Positif / Netral / Negatif |
| **Regresi** | Harga rumah: Rp 500 juta |
| **Multi-label** | Gambar: [mobil, biru, jalan] |

**Cara Labeling:**
- **Manual**: manusia memberi label satu per satu
- **Semi-automatic**: aturan sederhana → label otomatis + cek manual
- **Crowdsourcing**: banyak orang label (Amazon Mechanical Turk)

#### Mengaplikasi — Praktik (85 menit)

**4. Demonstrasi Data Cleaning (15 menit)**
- Buka dataset kotor (guru sediakan)
- Tunjukkan: cek missing, hapus duplikat, deteksi outlier, standarisasi
- Tunjukkan perbedaan "sebelum" vs "sesudah"

**5. Aktivitas 1 — Bersihkan Dataset (35 menit) — Individu**

Gunakan dataset kotor berikut (link dari guru):

| Kolom | Masalah |
|---|---|
| Nama | Typo, inconsistent case |
| Kelas | "X-A", " X-A", "XA", "10A" |
| Nilai UTS | Ada kosong, ada nilai >100, ada -10 |
| Nilai UAS | Ada kosong |
| Email | Ada format salah |

Tugas:
1. Identifikasi semua masalah (tulis di tabel)
2. Bersihkan:
   - Missing: isi dengan rata-rata (nilai) atau "Tidak Diisi" (nama)
   - Duplikat: hapus
   - Outlier: koreksi atau hapus
   - Standarisasi: format konsisten
3. Buat sheet baru "Hasil Cleaning"
4. Hitung statistik sebelum vs sesudah (rata-rata, jumlah data)

**6. Aktivitas 2 — Labeling Data Sentimen (25 menit) — Berpasangan**

Dataset: 10 komentar tentang sekolah

| No | Komentar | Label (Positif/Netral/Negatif) |
|---|---|---|
| 1 | "Sekolahku keren banget!" | |
| 2 | "Gurunya ramah dan sabar" | |
| 3 | "Tugasnya banyak banget" | |
| 4 | "Kantinnya enak!" | |
| 5 | "Belajar di sini biasa aja" | |
| 6 | "Fasilitasnya lengkap" | |
| 7 | "Ujiannya susah :(" | |
| 8 | "Teman-teman asyik" | |
| 9 | "Parkirannya sempit" | |
| 10 | "Sekolahnya bersih dan nyaman" | |

Setelah labeling, bandingkan dengan kelompok lain — apakah sama? Diskusikan perbedaan!

**7. Aktivitas 3 — Studi Kasus: Data Cleaning Real (10 menit) — Kelompok**
- Bayangkan: Data.go.id dataset "Data Sekolah" — ada kolom kosong, alamat tidak standar
- Diskusikan: "Langkah cleaning apa yang diperlukan?"
- Presentasi 2 kelompok

#### Merefleksi (15 menit)

**8. Refleksi Jurnal (15 menit)**
- Masalah data paling sering ditemui?
- Teknik cleaning mana yang paling berguna?
- Skala pemahaman 1–10

### Penutup (35 menit)

| Kegiatan | Waktu |
|---|---|
| 1. Rangkuman: Data kotor → Identifikasi masalah → Cleaning → Labeling → Siap analisis | 10 menit |
| 2. Kuis lisan: "Apa itu outlier? Bagaimana deteksi missing values? Apa fungsi labeling?" | 10 menit |
| 3. Preview: "Pert 3: Visualisasi Data & Dashboard — buat dashboard keren dari data bersih!" | 5 menit |
| 4. Tugas rumah: Cari dataset kotor di internet (Kaggle "Dirty Data" / buat sendiri) + cleaning | 10 menit |

---

## Asesmen

| Kriteria | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| Identifikasi masalah data | 0–1 masalah | 2 masalah | 3–4 masalah | 5 masalah + analisis |
| Cleaning dataset | < 50% bersih | 50–70% | 70–90% | 90–100% + dokumentasi |
| Labeling sentimen | 0–3 benar | 4–6 benar | 7–9 benar | 10 benar + konsisten |
| Studi kasus | Tidak paham | Ikut diskusi | Analisis tepat | Analisis + solusi |

---

**MGMP Informatika SMAN 6 Cimahi**
