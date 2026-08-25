# BAHAN AJAR – PERTEMUAN 10 (S1)
## PTS — Excel Dashboard & Konten Digital
*Mengacu pada Panduan Mapel 2025; INFORMATIKA Fase D-F — pendekatan Pembelajaran Mendalam (Memahami → Mengaplikasi → Merefleksi)*

| Informasi | Keterangan |
|---|---|
| **Fase / Kelas** | F / Kelas XII |
| **Alokasi Waktu** | 5 JP × 45 menit (225 menit) |
| **Elemen CP** | Dampak Sosial Informatika (DSI) |
| **Tujuan Pembelajaran** | Menilai penguasaan analisis data Excel (Pivot, fungsi statistik, dashboard) dan produksi konten digital dari pertemuan 1–9 |
| **Materi Prasyarat** | Seluruh materi Pertemuan 1–9 |

---

## A. Skenario & Instruksi Ujian 📋

> **"Analis Data Muda untuk Bazar Sekolah"**
>
> Kamu adalah **analis data muda** yang diminta mengelola data penjualan bazar sekolah. Pihak sekolah membutuhkan: (1) ringkasan penjualan per produk dan kategori, (2) dashboard yang mudah dibaca, serta (3) poster kampanye **"Anti Hoaks"** untuk mengedukasi siswa. Hari ini kamu akan membuktikan kemampuanmu dalam dua sesi ujian. **Bekerjalah mandiri, fokus, dan kelola waktu dengan baik.**
>
> **Instruksi:** Kerjakan Sesi 1 dan Sesi 2 sesuai panduan. Perhatikan bobot penilaian dan rubrik. Gunakan seluruh keterampilan dari pertemuan sebelumnya.

---

## B. Panduan Pelaksanaan PTS

| Sesi | Durasi | Materi | Output |
|---|---|---|---|
| Sesi 1 | ±100 menit | Excel Dashboard | File `.xlsx` (sheet Data, Analisis, Dashboard) |
| Sesi 2 | ±100 menit | Konten Digital | Poster `.png` + caption + refleksi |
| Total | 200 menit + jeda | — | Kumpulkan sesuai instruksi |

**Aturan:**
1. Kerjakan secara **mandiri**.
2. Data yang dibuat harus **konsisten** antara sheet Data, Analisis, dan Dashboard.
3. Periksa kembali rumus dan desain sebelum dikumpulkan.
4. Nama file mengikuti format yang ditentukan (misal `PTS10_NamaKamu.xlsx`).

---

## C. Sesi 1: Excel Dashboard

**Langkah 1 — Sheet "Data" (30 baris):** Buat data penjualan dengan 5 produk, 3 kategori, dan 3 bulan.

| Tanggal | Produk | Kategori | Qty | Harga | Total |
|---|---|---|---|---|---|

**Langkah 2 — Sheet "Analisis":** Buat 5 analisis berikut:
| No | Analisis | Tipe | Keterangan |
|---|---|---|---|
| 1 | Total penjualan per produk | Pivot | Rows=Produk, Values=Sum Total |
| 2 | Jumlah transaksi per kategori | Pivot | Rows=Kategori, Values=Count Qty |
| 3 | Produk dengan rata-rata > Rp100.000 | AVERAGEIF | Lakukan juga pengecekan manual |
| 4 | Tren penjualan per bulan | Pivot + Line | Group by Months |
| 5 | Produk terlaris | Sort Pivot | Urutkan menurun, ambil top 1 |

**Langkah 3 — Sheet "Dashboard":**
- 3 KPI cards: Total Revenue, Rata-rata Transaksi, Produk Terlaris.
- 1 Bar Chart: Penjualan per Produk.
- 1 Slicer: Kategori.

**Bobot: Pivot & Analisis 30%, Dashboard 20%.**

---

## D. Sesi 2: Konten Digital

**Tugas 1 — Poster "Anti Hoaks" (1080×1080):**
- Judul yang jelas.
- 3–4 tips verifikasi hoaks.
- Terapkan prinsip hierarki, kontras, dan white space.

**Tugas 2 — Caption IG:**
- 1 paragraf (50–80 kata), gaya edukatif santai.
- 3–5 hashtag relevan.

**Tugas 3 — Refleksi (dikirim via Google Form/teks):**
- Apa yang paling berguna dari materi Excel?
- Bagaimana AI bisa membantu pembuatan konten?
- Apa tantangan terbesar dalam desain?

**Bobot: Poster 20%, Caption 10%, Refleksi 10%.**

---

## E. Rubrik Penilaian dan Nilai Akhir

| Aspek | Bobot | 4 (Sangat Baik) | 3 (Baik) | 2 (Cukup) | 1 (Kurang) |
|---|---|---|---|---|---|
| Excel Pivot | 10% | Pivot rapi, 3+ analisis | 2 analisis | 1 analisis | Tidak selesai |
| Dashboard | 10% | KPI + chart + slicer | Kurang 1 elemen | Kurang 2 elemen | Tidak ada |
| Fungsi | 10% | AVERAGEIF + COUNTIFS benar | 1 fungsi benar | Rumus salah | Tidak memakai |
| Poster | 10% | Desain profesional, isi tepat | Rapi, isi kurang | Isi tepat, desain kurang | Tidak selesai |
| Caption | 5% | Menarik, tepat, hashtag baik | Kurang menarik | Terlalu pendek | Tidak ada |
| Refleksi | 5% | Mendalam, spesifik, jujur | Cukup | Dangkal | Tidak diisi |

**Nilai PTS = (Nilai Excel × 60%) + (Nilai Konten × 40%)**
Konversi: 85–100 = A, 70–84 = B, 55–69 = C, 0–54 = D.

---

## F. Contoh Soal & Penyelesaian 📝

**Contoh 1:** Untuk analisis "total penjualan per produk", ke area mana saja field diletakkan?
**Jawaban:** Produk ke **Rows**, dan Total ke **Values** dengan perhitungan **Sum**.

**Contoh 2:** Tuliskan rumus menghitung jumlah transaksi kategori "Minuman" (kategori di kolom C, 30 baris)!
**Jawaban:** `=COUNTIF(C2:C31,"Minuman")`

**Contoh 3:** Bagaimana cara menampilkan tren penjualan per bulan pada pivot?
**Jawaban:** Klik kanan pada field tanggal → **Group → Months**, letakkan Bulan di Rows dan Total di Values, lalu buat **PivotChart Line**.

**Contoh 4:** Sebutkan 3 KPI cards yang harus ada di dashboard!
**Jawaban:** Total Revenue, Rata-rata Transaksi, dan Produk Terlaris.

**Contoh 5:** Poster "Anti Hoaks" harus memuat apa saja agar memenuhi rubrik?
**Jawaban:** Judul jelas, 3–4 tips verifikasi hoaks, dan desain yang menerapkan hierarki, kontras, serta white space.

---

## G. Kesalahan Umum yang Harus Dihindari 🚫

| Kesalahan | Akibat | Cara Menghindari |
|---|---|---|
| Data antar sheet tidak konsisten | Nilai dashboard salah | Gunakan satu sumber data yang sama |
| Lupa memformat angka Rupiah | Tampilan kurang profesional | Terapkan Number Format |
| Pivot tidak di-refresh | Data lama tetap muncul | Klik kanan → Refresh |
| Poster penuh teks | Sulit dibaca | Gunakan hierarki dan white space |
| Tidak mengecek rumus | Hasil salah tanpa disadari | Verifikasi dengan hitung manual |

---

## H. Tantangan Praktik (Mengaplikasi) 🎯

**Tantangan 1 — Pemanasan Excel (30 menit):** Siapkan kerangka 30 baris data penjualan dengan 5 produk, 3 kategori, 3 bulan sebelum ujian.

**Tantangan 2 — Uji Coba Analisis (60 menit):** Latihan membuat 5 analisis sesuai panduan Sesi 1 pada data latihanmu sendiri.

**Tantangan 3 — Uji Coba Konten (60 menit):** Buat draf poster "Anti Hoaks" dan caption IG, lalu periksa dengan rubrik penilaian.

**Tantangan 4 — Simulasi Waktu (75 menit):** Kerjakan simulasi PTS dalam batas waktu, kumpulkan sesuai format penamaan, dan evaluasi sendiri dengan rubrik.

---

## I. Rangkuman Kunci 🔑

1. PTS menguji **dua sesi**: Excel Dashboard (60%) dan Konten Digital (40%).
2. Excel: **Data → Analisis (5 pivot/fungsi) → Dashboard (3 KPI + bar chart + slicer)**.
3. Konten: **poster Anti Hoaks + caption IG + refleksi**.
4. Perhatikan **rubrik** dan **bobot** saat mengerjakan.
5. Kelola waktu dan **verifikasi rumus** sebelum mengumpulkan.

---

## J. Glosarium 📖

| Istilah | Arti |
|---|---|
| **PTS** | Penilaian Tengah Semester |
| **KPI** | Indikator kinerja utama (angka penting) |
| **AVERAGEIF** | Fungsi rata-rata dengan satu kriteria |
| **Rubrik** | Pedoman penilaian dengan skala mutu |
| **CTA** | Ajakan bertindak pada konten |

---

## K. Refleksi (Merefleksi) 🔍

- Bagian mana yang paling kamu kuasai: Excel atau konten digital?
- Strategi apa yang membantumu menyelesaikan ujian dalam waktu terbatas?
- Apa yang akan kamu perbaiki jika mengerjakan ulang?
- **Skala pemahaman diri:** ____/10
- Materi apa yang ingin kamu perdalam sebelum PAS?

---

**MGMP Informatika SMAN 6 Cimahi — Fase F (Kelas XII) Semester 1**