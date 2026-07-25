# MODUL AJAR INFORMATIKA – FASE F (KELAS XI)

| Komponen | Deskripsi |
|---|---|
| **Mata Pelajaran** | Informatika |
| **Fase / Kelas** | F / XI |
| **Semester** | 2 (Genap) |
| **Pertemuan ke-** | 5 |
| **Alokasi Waktu** | 5 JP × 45 menit (225 menit) |
| **Tahun Pelajaran** | 2026/2027 |
| **Satuan Pendidikan** | SMA Negeri 6 Cimahi |
| **Materi Esensial** | Pengolahan Data Bervolume Besar |

---

## Tujuan Pembelajaran

| TP | IKTP |
|---|---|
| **BK, AD, AP:** Menerapkan seluruh pipeline pengolahan data pada dataset nyata | 5.1 Memilih dataset nyata dari sumber terbuka |
| | 5.2 Membersihkan dataset |
| | 5.3 Mengolah data dengan Python (CSV/JSON) |
| | 5.4 Membuat visualisasi/dashboard |
| | 5.5 Menyusun laporan analisis + insight |

---

## Langkah Pembelajaran

### Pembukaan (20 menit)

| Kegiatan | Waktu |
|---|---|
| 1. Salam, doa, cek kehadiran | 3 menit |
| 2. **Review**: "Pert 1–4: sumber data → cleaning → dashboard → Python. Sekarang: **gabung semua!** Kalian dapat dataset, bersihkan, olah Python, visualisasi, presentasi." | 7 menit |
| 3. **Apersepsi**: "Bayangkan kalian analis data di perusahaan. Bos minta laporan dari data mentah — apa yang kalian lakukan?" | 10 menit |

### Inti (175 menit)

#### Memahami (15 menit)

**1. Pipeline Pengolahan Data (15 menit)**

```
┌─────────┐   ┌─────────┐   ┌──────────┐   ┌──────────┐   ┌─────────┐
│ 1. CARI  │──▶│ 2. CUCI  │──▶│ 3. OLAH  │──▶│ 4. VISUAL │──▶│ 5. LAPOR│
│ Dataset  │   │        │   │ Python   │   │ Dashboard│   │ Insight │
│ data.go.id│   │ missing │   │ CSV/JSON │   │ Sheets   │   │ Temuan  │
│ Kaggle   │   │ duplikat│   │ Statistik│   │ Looker   │   │ Saran   │
└─────────┘   └─────────┘   └──────────┘   └──────────┘   └─────────┘
```

#### Mengaplikasi — Proyek (135 menit)

**2. Aktivitas 1 — Pilih & Download Dataset (15 menit) — Individu**

Pilih 1 dataset dari:
- `data.go.id` (rekomendasi: Data Sekolah, Jumlah Penduduk, APBD)
- `kaggle.com/datasets` (tema pendidikan / sosial)
- Dataset sendiri (min 50 baris, 5 kolom)

Setelah pilih, isi:
| Aspek | Isian |
|---|---|
| Nama dataset | |
| Sumber | |
| Format | CSV / JSON / XLSX |
| Jumlah baris | |
| Jumlah kolom | |
| Topik | |

**3. Aktivitas 2 — Data Cleaning (25 menit) — Individu**

| Langkah | Tools | Hasil |
|---|---|---|
| Cek missing | Sheets / Python | ... |
| Hapus duplikat | Sheets / Python | ... |
| Standarisasi format | Sheets / Python | ... |
| Deteksi outlier | Sheets / Python | ... |
| Simpan data bersih | CSV | `data_bersih.csv` |

**4. Aktivitas 3 — Analisis Python (35 menit) — Berpasangan**

Buat notebook Google Colab dengan:

```python
import csv, json

# 1. Baca data bersih
# 2. Hitung statistik (rata-rata, max, min, median)
# 3. Filter data berdasarkan kriteria
# 4. Simpan hasil sebagai JSON
# 5. Cetak 5 insight
```

**Insight wajib:**
- 1 insight dari statistik deskriptif
- 1 insight dari perbandingan kategori
- 1 insight dari nilai ekstrem (tertinggi/terendah)

**5. Aktivitas 4 — Dashboard (30 menit) — Berpasangan**

Buat dashboard di Looker Studio atau Google Sheets:

| Komponen | Ada? |
|---|---|
| 4 KPI | ✅ |
| 2 grafik | ✅ |
| Filter | ✅ |
| Judul + sumber data | ✅ |

**6. Aktivitas 5 — Presentasi (30 menit) — Kelompok**

Presentasi 3 menit per kelompok:
| Slide | Waktu |
|---|---|
| Dataset: sumber, isi | 30 detik |
| Cleaning: masalah & solusi | 30 detik |
| Python: analisis & insight | 60 detik |
| Dashboard | 30 detik |
| Kesimpulan & saran | 30 detik |

#### Merefleksi (15 menit)

**7. Refleksi Jurnal (15 menit)**
- Bagian paling sulit dari pipeline?
- Skill baru yang paling berguna?
- Jika bisa ulang, apa yang akan dilakukan berbeda?
- Skala pemahaman 1–10

### Penutup (30 menit)

| Kegiatan | Waktu |
|---|---|
| 1. Rangkuman pipeline: Cari → Cuci → Olah → Visual → Lapor | 10 menit |
| 2. Kuis: "Pipeline pengolahan data 5 langkah?" | 5 menit |
| 3. Preview: "Pert 6: PTS — ujian materi Pengolahan Data (Pert 1–5)" | 5 menit |
| 4. Tugas rumah: Sempurnakan laporan + siapkan presentasi final | 10 menit |

---

## Asesmen

| Kriteria | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| Dataset (relevan, cukup, legal) | Tidak sesuai | Kurang sesuai | Sesuai | Sesuai + menarik |
| Cleaning (masalah diatasi) | < 50% | 50–70% | 70–90% | 90–100% + dokumentasi |
| Python (baca, olah, simpan) | Tidak jalan | 1–2 fungsi | 3–4 fungsi | 5 fungsi + insight |
| Dashboard (KPI, grafik, filter) | Tidak buat | 1 komponen | 2 komponen | 3+ komponen + rapi |
| Presentasi (jelas, insight, saran) | Tidak siap | Kurang jelas | Jelas | Jelas + insight + saran |

---

**MGMP Informatika SMAN 6 Cimahi**
