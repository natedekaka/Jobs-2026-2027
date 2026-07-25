# BAHAN AJAR – PERTEMUAN 14
## Konsep Kualitas Data & GIGO

| TP | BK 1.2 |
|---|---|

---

### A. DATA BERKUALITAS — APA DAN MENGAPA?

#### 5 Dimensi Kualitas Data

| Dimensi | Definisi | Contoh Baik | Contoh Buruk |
|---|---|---|---|
| **Accuracy** | Data sesuai realitas | Nama: "Andi Pratama" | Nama: "Andi Pratama" (ejaan salah) |
| **Completeness** | Semua data terisi | Semua kolom terisi | Kolom alamat kosong |
| **Consistency** | Format seragam | Tanggal: DD-MM-YYYY | Campur: DD-MM-YYYY, YYYY-MM-DD |
| **Timeliness** | Data terkini | Tahun ini | Tahun 2019 |
| **Relevance** | Sesuai kebutuhan | Data nilai siswa | Data hobi (tidak perlu) |

#### Kenapa Data Berkualitas Penting?

| Sektor | Contoh | Dampak Data Jelek |
|---|---|---|
| **Kesehatan** | Diagnosis pasien | Salah diagnosis → fatal |
| **Keuangan** | Transfer bank | Salah transfer ke rekening lain |
| **Pendidikan** | Nilai rapor | Nilai salah → keputusan salah |
| **Pemerintahan** | Data penduduk | Bantuan sosial salah sasaran |
| **Transportasi** | GPS / maps | Salah arah, telat |

---

### B. PRINSIP GIGO — GARBAGE IN, GARBAGE OUT

GIGO menyatakan: **jika data input jelek, output pasti jelek — sekualitas apa pun prosesnya.**

```
📥 Input (Garbage) → ⚙️ Proses (Valid) → 📤 Output (Garbage)
```

#### Kasus Nyata GIGO

| Tahun | Kasus | Input Salah | Kerugian |
|---|---|---|---|
| 1999 | Mars Climate Orbiter NASA | Satuan imperial vs metrik | $327 juta — pesawat meledak |
| 2012 | Knight Capital Group | Software bug + data testing | $440 juta dalam 45 menit |
| 2015 | Volkswagen Dieselgate | Software manipulasi emisi | $30 miliar denda |
| 2020 | NHS Test & Trace (UK) | Data kontak tidak lengkap | Ribuan kasus tidak terdeteksi |
| 2023 | AI Chatbot (berbagai) | Data training bias | Output diskriminatif |

#### Analogi GIGO

| Analogi | Penjelasan |
|---|---|
| **Masak** | Bahan busuk → masakan tidak enak |
| **Bangun rumah** | Pondasi jelek → rumah ambruk |
| **Mobil** | Bensin kotor → mesin rusak |
| **Komputer** | Data jelek → analisis salah |

---

### C. JENIS DATA BERMASALAH

#### 1. Masalah Format

| Masalah | Contoh | Seharusnya |
|---|---|---|
| Tanggal campur | `15-03-2009` vs `2009-05-20` vs `20/05/2009` | Satu format konsisten |
| Angka sebagai teks | `"08567ABCD"` atau `"Tujuhpuluh"` | `85671234567`, `70` |
| Spasi berlebih | `"Cimahi "` | `"Cimahi"` |

#### 2. Missing Values

| Tipe | Contoh | Penanganan |
|---|---|---|
| **MCAR** (acak) | Kolom alamat kosong, tidak ada pola | Isi dengan rata-rata/mod, atau hapus |
| **MAR** (tidak acak) | Nilai kosong hanya di kelas tertentu | Investigasi penyebab |
| **MNAR** (sistematis) | Semua siswa X-3 tidak punya data | Cek ulang pengumpulan data |

#### 3. Duplicate Data

| Jenis | Contoh | Dampak |
|---|---|---|
| **Exact duplicate** | Baris Andi Pratama muncul 2× | Perhitungan rangkap |
| **Partial duplicate** | "Andi P" dan "Andi Pratama" — orang sama | Data tidak konsisten |

#### 4. Outlier (Data Pencilan)

| Outlier | Contoh | Penyebab |
|---|---|---|
| **Natural** | Tinggi badan 210 cm (atlet basket) | Valid, tapi ekstrem |
| **Error** | Usia 200 tahun, nilai 200 dari 100 | Salah input |

#### 5. Inkonsistensi Data

| Masalah | Contoh | Seharusnya |
|---|---|---|
| Kategorisasi beda | "L", "LK", "Laki", "Laki-laki" | "L" (standarisasi) |
| Satuan beda | Meter vs sentimeter, kg vs gram | Satu satuan |

#### 6. Data Tidak Valid

| Aturan Dilanggar | Contoh | Seharusnya |
|---|---|---|
| Range nilai | Nilai 200 (maks 100) | 0–100 |
| Tanggal mustahil | `30-02-2009` | Februari max 28/29 |

---

### D. DAMPAK DATA TIDAK BERKUALITAS

| Area | Dampak | Biaya (Estimasi) |
|---|---|---|
| **Bisnis** | Keputusan salah | 15–25% revenue |
| **Kesehatan** | Malapraktik | Tak ternilai |
| **Pemerintahan** | Kebijakan salah sasaran | Miliaran rupiah |
| **Akademik** | Penelitian salah | Publikasi retracted |
| **Pribadi** | Penipuan, kesalahan administrasi | Kerugian pribadi |

---

### E. RANGKUMAN

1. **Data berkualitas** = akurat + lengkap + konsisten + tepat waktu + relevan
2. **GIGO**: Input jelek → Output jelek — tidak peduli sebagus apa prosesnya
3. **Jenis masalah data**: format, missing, duplicate, outlier, inkonsistensi, invalid
4. Data tidak berkualitas bisa menyebabkan **kerugian besar** dan **keputusan salah**

---

**MGMP Informatika SMAN 6 Cimahi**
