# TAHAP 4 — ANALISIS DATA
## Rencana Harian (14 Hari) — Excel Lanjut & Dashboard

**Tujuan tahap:** Menguasai analisis data yang diajarkan di Kelas XII (dan Excel lanjut Kelas XI) untuk mengajar sekaligus menyajikan data sekolah secara profesional.

**Syarat kelulusan (produk bukti):**
- ✅ Dashboard 1 halaman dari data sekolah (nilai/absensi)
- ✅ Laporan otomatis (VLOOKUP/XLOOKUP + IFERROR + conditional formatting)
- ✅ Analisis Python utk data yang sama, bandingkan dengan Excel

---

## MINGGU 1 — FUNGSI & OTOMATISASI

### Hari 1 — Review Cepat & Table
- **Tugas:** Salin `DATA_DUMMY_NILAI_PTS.csv` ke Excel → ubah jadi Table (`Ctrl+T`). Gunakan SUM, AVERAGE, MAX, MIN, COUNT, COUNTA.
- **Jalan pintas:** `Ctrl+T` sebelum semua formula (range otomatis ikut).

### Hari 2 — Fungsi Logika: IF & COUNTIF
- **Tugas:** Buat kolom Status (IF ≥ KKM). Hitung jumlah LULUS/TIDAK LULUS dengan COUNTIF, dan rata-rata per kelas dengan AVERAGEIF.
- **Simulasi:** Terapkan langsung ke data rapor siswa nyata.

### Hari 3 — Fungsi Pencarian: VLOOKUP & XLOOKUP
- **Tugas:** Buat tabel acuan (mis. nama → nilai, atau nilai → predikat) → VLOOKUP. Latih XLOOKUP utk ke-2 arah.
- **Jalan pintas:** Selalu pakai `FALSE`/exact match; bungkus `IFERROR`.

### Hari 4 — Conditional Formatting
- **Tugas:** Tandai nilai < 70 merah, ≥ 85 hijau. Highlight baris status "TIDAK LULUS" (formula rule).
- **Simulasi:** Format laporan nilai utk rapat wali kelas.

### Hari 5 — Proyek Mini: Laporan Otomatis
- **Tugas:** Gabungkan Hari 1-4: 1 file "Laporan Nilai" yang hanya perlu update data → semua formula & warna ter-update.
- **Bukti:** Laporan 1 halaman yang rapi & otomatis.

### Hari 6 — Data Validasi & Error Handling
- **Tugas:** Buat dropdown (Data Validation) utk kolom kelas. Gunakan IFERROR agar tidak tampil #N/A.
- **Bukti:** File yang "anti-bodoh" — error muncul karena data salah, bukan karena formula.

### Hari 7 — Review & Uji Coba
- **Tugas:** Buka file laporan tanpa melihat catatan, update data 10 baris, pastikan semuanya berubah benar.

---

## MINGGU 2 — DASHBOARD & PYTHON

### Hari 8 — Pivot Table (Dasar)
- **Tugas:** Buat pivot dari data nilai: rata-rata per kelas, jumlah LULUS/TIDAK LULUS per kelas.
- **Jalan pintas:** Tarik field → pilih "Value Field Settings" (Average, Count).

### Hari 9 — Pivot Lanjut & Slicer
- **Tugas:** Tambah Slicer utk filter kelas. Tambah Timeline (jika ada tanggal).
- **Simulasi nyata:** Buat pivot "distribusi predikat per kelas" utk laporan sekolah.

### Hari 10 — Chart & Visualisasi
- **Tugas:** Buat bar chart rata-rata per kelas, pie chart status, line chart tren (jika data ada). Rapikan axis, label, judul, warna.
- **Aturan visual:** maksimal 1 pesan per chart, label jelas, tidak penuh dekorasi.

### Hari 11 — Dashboard 1 Halaman
- **Tugas:** Gabungkan semua elemen di 1 sheet "DASHBOARD": title, 4-6 chart, 3-5 KPI (angka besar), slicer, 0 tabel mentah.
- **Simulasi akhir:** Siapkan utk presentasi 10 menit di rapat MGMP.

### Hari 12 — Analisis Python (Pandas) — Bagian 1
- **Tugas:** Di Colab, `import pandas as pd`, baca CSV, hitung statistik: `mean()`, `count()`, `groupby()`.

### Hari 13 — Analisis Python — Bagian 2 (Visualisasi)
- **Tugas:** `import matplotlib` → bar & pie chart utk data yang sama. Bandingkan workflow Excel vs Python.

### Hari 14 — Presentasi Data & Simulasi Penuh
- **Tugas:** Presentasikan dashboard ke dewan rekan guru dlm 10 menit. Terima pertanyaan keras (siapkan utk Rapat MGMP).
- **Syarat akhir:** Bisa menjawab "mengapa pakai Excel/Python" utk kebutuhan berbeda.

---

## Checklist Penyelesaian Tahap 4
- [ ] Table + formula dasar (Hari 1-2)
- [ ] VLOOKUP/XLOOKUP + IFERROR (Hari 3)
- [ ] Conditional formatting (Hari 4)
- [ ] Dashboard 1 halaman (Hari 11)
- [ ] Analisis Python + presentasi 10 menit (Hari 13-14)

---

**MGMP Informatika SMAN 6 Cimahi — Program Magang Guru Informatika TP 2026/2027**