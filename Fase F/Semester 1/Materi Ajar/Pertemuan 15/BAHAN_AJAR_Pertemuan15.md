# BAHAN AJAR – PERTEMUAN 15
## Praktik Pengolahan Data

| TP | BK, AP — Pengolahan Data Bervolume Besar |
|---|---|

---

### A. ALAT PENGOLAHAN DATA

Untuk praktik kali ini, kita gunakan **Google Sheets** (gratis, online, tidak perlu instalasi).

Alternatif: **Microsoft Excel** (jika sudah terinstal).

#### Mengakses Google Sheets
1. Buka `sheets.google.com`
2. Login dengan akun Google
3. Klik "+" (Blank) untuk spreadsheet baru

---

### B. TEKNIK DASAR PENGOLAHAN DATA

#### 1. Import Data

| Cara | Langkah |
|---|---|
| Manual | Ketik langsung |
| Copy-paste | Copy dari sumber → Paste di Sheets |
| Import CSV | File → Import → Upload |

#### 2. Sorting (Mengurutkan)

| Sorting | Cara | Contoh |
|---|---|---|
| A→Z | Klik header kolom → Data → Sort A→Z | Nama: A–Z |
| Z→A | Data → Sort Z→A | Nilai: tertinggi ke terendah |
| Multiple | Data → Sort range → Add column | Kelas dulu, baru Nilai |

#### 3. Filtering (Menyaring)

Gunakan **Filter** untuk menampilkan data tertentu.

**Langkah:**
1. Pilih semua data (termasuk header)
2. Data → Create a filter
3. Klik ikon filter di header kolom
4. Pilih kriteria (misal: Nilai ≥ 75)

#### 4. Missing Values (Data Kosong)

Data kosong bisa menyebabkan kesalahan perhitungan.

| Teknik | Rumus | Keterangan |
|---|---|---|
| Cek kosong | `=ISBLANK(A2)` | TRUE = kosong |
| Isi dengan rata-rata | `=IF(ISBLANK(A2), AVERAGE(B2:B100), A2)` | Jika kosong, isi rata-rata |
| Hapus baris kosong | Data → Data cleanup → Cleanup suggestions | Otomatis |

#### 5. Duplicates (Duplikat)

| Teknik | Cara |
|---|---|
| Cek duplikat | Format → Conditional formatting → Custom formula: `=COUNTIF(A:A,A1)>1` |
| Hapus duplikat | Data → Data cleanup → Remove duplicates |

#### 6. Statistik Dasar

| Rumus | Fungsi | Contoh |
|---|---|---|
| `=AVERAGE(range)` | Rata-rata | `=AVERAGE(C2:C41)` |
| `=MEDIAN(range)` | Median | `=MEDIAN(C2:C41)` |
| `=MAX(range)` | Nilai tertinggi | `=MAX(C2:C41)` |
| `=MIN(range)` | Nilai terendah | `=MIN(C2:C41)` |
| `=COUNT(range)` | Jumlah data | `=COUNT(C2:C41)` |
| `=COUNTIF(range, "≥75")` | Jumlah dengan syarat | `=COUNTIF(C2:C41,"≥75")` |

#### 7. Pivot Table

Membuat rangkuman data secara otomatis.

**Langkah:**
1. Pilih semua data → Data → Pivot table
2. **Rows**: pilih kolom kategori (misal: Kelas)
3. **Values**: pilih kolom yang dirangkum (misal: Rata-rata Nilai)
4. **Summarize by**: pilih fungsi (SUM, AVERAGE, COUNT, dll.)

#### 8. Grafik / Chart

**Langkah:**
1. Pilih data (termasuk header)
2. Insert → Chart
3. Pilih jenis grafik:
   - **Column chart**: perbandingan antar kelompok
   - **Pie chart**: proporsi
   - **Line chart**: tren dari waktu ke waktu
4. Edit judul, warna, label di Chart editor

---

### C. STUDI KASUS — DATA NILAI SISWA

#### Dataset

| Nama | Kelas | Nilai UTS | Nilai UAS | Rata-rata |
|---|---|---|---|---|
| Adi Pratama | X-A | 82 | 88 | =AVERAGE(C2:D2) |
| Budi Santoso | X-A | 75 | 70 | 72.5 |
| Citra Dewi | X-A | 90 | 92 | 91 |
| ... | ... | ... | ... | ... |
| (40 siswa) | | | | |

#### Langkah Praktik

**1. Data Cleaning**
```
Cari data kosong: =ISBLANK(C2:C41)
Cek duplikat: conditional formatting → COUNTIF
Pastikan nilai 0-100: filter nilai > 100
```

**2. Statistik**
```
Rata-rata UTS:   =AVERAGE(C2:C41)
Rata-rata UAS:   =AVERAGE(D2:D41)
Nilai tertinggi: =MAX(E2:E41)
Nilai terendah:  =MIN(E2:E41)
Jumlah remedial: =COUNTIF(E2:E41,"<75")
Persen remedial: =COUNTIF(E2:E41,"<75") / COUNT(E2:E41) * 100
```

**3. Pivot Table**
```
Rows: Kelas
Values: Rata-rata (AVERAGE)
→ Bandingkan rata-rata antar kelas
```

**4. Grafik**
```
Column chart: perbandingan rata-rata per kelas
Pie chart: proporsi siswa ≥ 75 vs < 75
```

---

### D. INTERPRETASI DATA

Setelah mengolah data, langkah terakhir adalah **interpretasi** — apa arti semua angka itu?

| Pertanyaan | Contoh Jawaban |
|---|---|
| Kelas mana rata-rata tertinggi? | "X-A" |
| Berapa persen remedial? | "15%" |
| Mata pelajaran mana yang perlu diperbaiki? | "Matematika" |
| Rekomendasi untuk guru? | "Tambah jam tutoring untuk X-C" |

---

### E. RANGKUMAN

| Langkah | Teknik | Fungsi/Rumus |
|---|---|---|
| 1. Cleaning | Cek missing, duplikat | `ISBLANK`, `COUNTIF` |
| 2. Sorting | Urutkan data | Data → Sort |
| 3. Filtering | Tampilkan data tertentu | Data → Filter |
| 4. Statistik | Mean, max, min | `AVERAGE`, `MAX`, `MIN` |
| 5. Pivot | Rangkum data | Data → Pivot table |
| 6. Grafik | Visualisasi | Insert → Chart |
| 7. Interpretasi | Ambil kesimpulan | Analisis |

---

**MGMP Informatika SMAN 6 Cimahi**
