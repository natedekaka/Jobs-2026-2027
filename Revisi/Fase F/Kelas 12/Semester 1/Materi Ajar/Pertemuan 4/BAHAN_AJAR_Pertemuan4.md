# BAHAN AJAR – PERTEMUAN 4 (S1)
## Dashboard Excel
*Mengacu pada Panduan Mapel 2025; INFORMATIKA Fase D-F — pendekatan Pembelajaran Mendalam (Memahami → Mengaplikasi → Merefleksi)*

| Informasi | Keterangan |
|---|---|
| **Fase / Kelas** | F / Kelas XII |
| **Alokasi Waktu** | 5 JP × 45 menit (225 menit) |
| **Elemen CP** | Analisis Data (AD) |
| **Tujuan Pembelajaran** | Merancang dan membangun dashboard Excel yang memadukan Pivot Table, chart, slicer, KPI cards, dan timeline untuk pengambilan keputusan |
| **Materi Prasyarat** | Pivot Table, fungsi statistik bersyarat, dan dasar visualisasi data |

---

## A. Kisah Pemantik 🎬

> **"Satu Pandangan untuk Mengambil Keputusan"**
>
> Saat mengendarai mobil, pengemudi tidak perlu membuka puluhan buku catatan untuk mengetahui kecepatan, bahan bakar, atau suhu mesin. Semua informasi penting tampil **sekilas** di dashboard. Begitu juga pemilik kafe online yang memiliki ribuan transaksi. Ia harus membuka banyak file untuk tahu: berapa pendapatan bulan ini? Produk apa yang laris? Jawabannya tersebar — dan keputusan jadi lambat. Ia pun ingin **satu lembar kerja** yang merangkum semuanya: *dashboard Excel*.
>
> **Pertanyaan pemantik:** Informasi apa saja yang menurutmu paling penting untuk "dashboard" sebuah sekolah? Bagaimana menyajikannya agar orang memahami dalam 10 detik?

---

## B. Apa Itu Dashboard dan KPI?

**Dashboard** adalah tampilan visual yang merangkum data-data penting dalam satu halaman/layar, sehingga pengguna bisa melihat kondisi bisnis atau proyek **sekilas** dan mengambil keputusan dengan cepat.

**KPI (Key Performance Indicator)** adalah **angka kunci** yang menandakan kinerja — seperti pendapatan total, rata-rata transaksi, atau produk terlaris.

| Istilah | Arti |
|---|---|
| **Dashboard** | Tampilan satu halaman yang merangkum data penting |
| **KPI** | Indikator kinerja utama (angka penting) |
| **Chart** | Grafik visualisasi data |
| **Slicer** | Tombol filter visual yang interaktif |
| **Timeline** | Slider filter berdasarkan waktu |
| **PivotTable** | Sumber ringkasan data dashboard |

---

## C. 5 Komponen Utama Dashboard Excel

**1. Pivot Table — Sumber Ringkasan:** Tempatkan pivot table sebagai sumber data utama. Dashboard biasanya memakai **beberapa pivot** untuk analisis berbeda, dan setiap pivot dihubungkan ke chart-nya.

**2. Chart — Visualisasi Grafik:** Pilih jenis grafik sesuai data:
| Jenis Grafik | Cocok Untuk |
|---|---|
| Bar / Column | Membandingkan kategori (penjualan per produk) |
| Line | Menunjukkan tren waktu (penjualan per bulan) |
| Pie | Menunjukkan proporsi (market share) |
| Combo | Dua data berbeda skala (bar + line) |
| Stacked Bar | Total sekaligus komposisi |

**3. Slicer — Filter Interaktif:** Tombol visual untuk menyaring data. Satu slicer bisa dihubungkan ke beberapa pivot: klik kanan slicer → **Report Connections** → centang pivot tujuan.

**4. KPI Cards — Angka Penting:** Kotak dengan angka besar di bagian atas dashboard:
- Total Revenue: `=SUM(penjualan[Total])`
- Rata-rata Transaksi: `=AVERAGE(penjualan[Total])`
- Produk Terlaris / Persentase Target: `=Total/Target`

**5. Timeline — Filter Waktu:** **PivotTable Analyze → Insert Timeline** untuk memilih rentang tanggal dengan slider.

---

## D. Langkah Membuat Dashboard

1. **Siapkan data:** tabel rapi 30–100 baris dengan header jelas (Tanggal, Produk, Kategori, Qty, Harga, Total).
2. **Pivot Table 1:** Rows = Produk, Values = Sum of Total.
3. **Pivot Table 2:** Rows = Tanggal → **Group → Months**, Values = Sum of Total.
4. **Chart 1:** Column Chart dari Pivot 1 (penjualan per produk).
5. **Chart 2:** Line Chart dari Pivot 2 (tren bulanan).
6. **Slicer:** pilih field Kategori, hubungkan ke **kedua** pivot.
7. **KPI Cards:** buat 3–4 kotak angka penting di bagian atas.
8. **Layout & Format:**
   - Buat sheet baru bernama **DASHBOARD**.
   - Susun: KPI di atas, chart di tengah, slicer di samping.
   - Gunakan warna konsisten (maksimal 3 warna).
   - Sembunyikan gridlines (View → Gridlines) dan header baris/kolom.

---

## E. Tips Desain Dashboard Profesional

1. **Hierarki:** informasi terpenting di bagian atas (KPI cards), detail di bawahnya.
2. **Konsistensi warna:** pilih 2–3 warna dan gunakan di seluruh dashboard.
3. **White space:** beri jarak antar komponen agar tidak sesak — ruang kosong memberi "napas visual".
4. **Ukuran font:** judul 18pt, KPI 24pt, label chart 10pt.
5. **Bersihkan elemen pengganggu:** gridlines, header baris/kolom, scrollbar.
6. **Beri judul jelas:** misal "Dashboard Penjualan Q1 2025".

**Contoh Layout:**
```
+-----------------------------------------------------------+
|  [LOGO]      DASHBOARD PENJUALAN 2025          [Tanggal]   |
+-----------------------------------------------------------+
| [Total Rp50jt] [Rata-rata Rp1,5jt] [Produk: Kopi] [Target] |
+----------------------------+-----------------------------+
| Penjualan per Produk (Bar) | Tren Bulanan (Line)         |
| [CHART]                    | [CHART]                     |
+----------------------------+-----------------------------+
| [Slicer: Kategori]         | [Timeline: 2024-2025]       |
+----------------------------+-----------------------------+
```

---

## F. Contoh Soal & Penyelesaian 📝

**Contoh 1:** Sebutkan 5 komponen utama dashboard Excel!
**Jawaban:** Pivot Table, Chart, Slicer, KPI Cards, dan Timeline.

**Contoh 2:** Data penjualan per bulan selama 12 bulan. Jenis chart apa yang paling tepat dan mengapa?
**Jawaban:** **Line Chart**, karena paling baik menampilkan tren/perubahan nilai dari waktu ke waktu.

**Contoh 3:** Bagaimana cara menghubungkan satu slicer ke beberapa pivot table?
**Jawaban:** Klik kanan pada slicer → **Report Connections** → centang pivot table tujuan → OK.

**Contoh 4:** Tuliskan rumus untuk KPI "Rata-rata Transaksi" jika kolom Total bernama `total` pada tabel bernama `penjualan`!
**Jawaban:** `=AVERAGE(penjualan[total])`

**Contoh 5:** Sebutkan 3 tips desain dashboard yang baik!
**Jawaban:** (1) Utamakan hierarki — KPI di atas; (2) konsistensi warna maksimal 3 warna; (3) cukupi white space agar tidak sesak.

---

## G. Miskonsepsi yang Sering Terjadi 🚫

| Miskonsepsi | Fakta yang Benar |
|---|---|
| "Semakin banyak warna, dashboard makin menarik" | Maksimal **3 warna** konsisten agar fokus dan profesional |
| "Dashboard harus penuh sesak dengan data" | **White space** penting agar informasi mudah dibaca |
| "Pie chart cocok untuk semua data" | Pie chart hanya untuk **proporsi**, bukan perbandingan banyak kategori |
| "Dashboard langsung ter-update otomatis" | Perlu **Refresh** pivot setelah data sumber berubah |
| "Slicer hanya bisa untuk satu pivot" | Slicer dapat terhubung ke **banyak pivot** melalui Report Connections |

---

## H. Tantangan Praktik (Mengaplikasi) 🎯

**Tantangan 1 — Sumber Data (30 menit):** Buat 30–40 baris data penjualan (Tanggal, Produk, Kategori, Qty, Harga, Total) dengan 3 kategori dan 3 bulan.

**Tantangan 2 — Fondasi Dashboard (60 menit):** Buat 2 pivot (total per produk, tren bulanan) dan 2 chart (Column dan Line) di sheet terpisah.

**Tantangan 3 — Interaktivitas (60 menit):** Tambahkan slicer Kategori yang terhubung ke kedua pivot, tambahkan timeline, dan buat 3 KPI cards (Total Revenue, Rata-rata Transaksi, Produk Terlaris).

**Tantangan 4 — Finishing (60 menit):** Susun semuanya dalam satu sheet **DASHBOARD** yang bersih: tanpa gridlines, warna konsisten, judul jelas. Simpan sebagai `Dashboard_NamaKamu.xlsx`.

---

## I. Rangkuman Kunci 🔑

1. **Dashboard** merangkum data penting dalam satu layar untuk keputusan cepat.
2. 5 komponen: **Pivot Table, Chart, Slicer, KPI Cards, Timeline**.
3. Pilih chart sesuai tujuan: **Bar** membandingkan, **Line** menunjukkan tren, **Pie** proporsi.
4. **Slicer** membuat dashboard interaktif dan bisa dipakai banyak pivot.
5. Desain baik: hierarki, warna konsisten (≤3), white space, font proporsional.
6. Selalu **Refresh** pivot saat data sumber berubah.

---

## J. Glosarium 📖

| Istilah | Arti |
|---|---|
| **Dashboard** | Tampilan satu halaman yang merangkum data penting |
| **KPI** | Key Performance Indicator — angka kunci kinerja |
| **Chart** | Grafik visualisasi data (bar, line, pie) |
| **Slicer** | Tombol filter visual interaktif |
| **Timeline** | Slider filter berdasarkan waktu |
| **White space** | Ruang kosong yang membuat desain mudah dibaca |

---

## K. Refleksi (Merefleksi) 🔍

- Mengapa dashboard lebih efektif daripada tabel data mentah untuk pengambilan keputusan?
- Komponen dashboard mana yang paling sulit kamu buat, dan mengapa?
- Bagaimana prinsip desain dashboard berlaku juga pada poster atau presentasi?
- **Skala pemahaman diri:** ____/10
- Dashboard untuk "kehidupan" apa yang ingin kamu buat selanjutnya?

---

**MGMP Informatika SMAN 6 Cimahi — Fase F (Kelas XII) Semester 1**