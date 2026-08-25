# BAHAN AJAR – PERTEMUAN 2 (S1)
## Pivot Table
*Mengacu pada Panduan Mapel 2025; INFORMATIKA Fase D-F — pendekatan Pembelajaran Mendalam (Memahami → Mengaplikasi → Merefleksi)*

| Informasi | Keterangan |
|---|---|
| **Fase / Kelas** | F / Kelas XII |
| **Alokasi Waktu** | 5 JP × 45 menit (225 menit) |
| **Elemen CP** | Analisis Data (AD) |
| **Tujuan Pembelajaran** | Membuat dan menganalisis Pivot Table dari data mentah berukuran besar, serta memanfaatkan slicer, timeline, dan pengelompokan data |
| **Materi Prasyarat** | Fungsi dasar Excel (SUM, AVERAGE, COUNTIF) dan pembuatan tabel rapi |

---

## A. Kisah Pemantik 🎬

> **"Rekap Bazar yang Menyiksa"**
>
> Panitia bazar sekolah mencatat **300 transaksi** di sebuah lembar kerja: siapa membeli, produk apa, berapa banyak, dan kapan. Menjelang laporan, Ketua Panitia bertanya: *"Berapa total penjualan makanan? Produk apa yang paling laris bulan ini?"* Tiga anggota panitia menghitung satu per satu dengan kalkulator dan **memakan waktu hampir 2 jam**. Kakak kelasnya tersenyum, *"Coba pakai Pivot Table — sekali klik, semua jawaban muncul."*
>
> **Pertanyaan pemantik:** Mengapa meringkas ratusan baris data secara manual itu melelahkan dan rawan salah? Perintah ringkas apa yang akan kamu berikan pada komputer agar jawabannya keluar seketika?

---

## B. Apa Itu Pivot Table?

**Pivot Table** adalah fitur Excel untuk **meringkas, mengelompokkan, dan menganalisis** data dalam jumlah besar — **tanpa mengubah data asli**. Ia seperti "kamera" yang memotret data mentah dari berbagai sudut pandang.

| Istilah | Arti | Contoh Pengisian |
|---|---|---|
| **Field** | Nama kolom pada data sumber | Produk, Kategori, Bulan |
| **Rows (Baris)** | Kategori yang dijadikan baris | Produk |
| **Columns (Kolom)** | Kategori kedua (opsional) | Kategori |
| **Values (Nilai)** | Data yang dihitung | Sum of Total |
| **Filters (Saring)** | Filter global seluruh pivot | Tahun |
| **Slicer** | Tombol visual untuk memfilter cepat | Klik "Minuman" |
| **Timeline** | Slider waktu untuk memfilter tanggal | Rentang Jan–Mar |

> 💡 **Ingat:** Pivot Table **hanya merangkum**, bukan mengubah data sumber. Data asli tetap aman di lembar asalnya.

---

## C. Syarat Data dan Langkah Membuat Pivot Table

### C.1 Syarat Data yang Baik
1. Data berbentuk **tabel rapi** — setiap kolom memiliki **header unik**.
2. **Tidak ada** sel gabungan (merged cells) di area data.
3. **Tidak ada** baris/kolom kosong di tengah data.
4. Tipe data **konsisten** — kolom angka berisi angka, kolom teks berisi teks.

### C.2 Langkah Membuat Pivot Table
1. Blok seluruh data (termasuk header) → **Insert → PivotTable** → pilih **New Worksheet** → **OK**.
2. Muncul panel **PivotTable Fields** di sisi kanan.
3. **Seret (drag and drop)** field ke salah satu dari 4 area:
   - **Rows:** kategori yang dianalisis (contoh: Produk)
   - **Columns:** kategori kedua (contoh: Bulan)
   - **Values:** data yang dihitung (contoh: Sum of Total)
   - **Filters:** filter global (contoh: Tahun)

---

## D. Contoh Praktik — Data Penjualan

Buat data minimal **30 baris** dengan kolom:

| Tanggal | Produk | Kategori | Qty | Harga | Total |
|---|---|---|---|---|---|

`Total = Qty × Harga` (gunakan rumus `=Qty*Harga`).

**Analisis 1 — Total per Produk:** Rows = Produk, Values = Sum of Total. → Produk mana paling laris?

**Analisis 2 — Transaksi per Kategori:** Rows = Kategori, Values = Count of Qty. → Kategori mana paling sering dibeli?

**Analisis 3 — Matriks Produk × Kategori:** Rows = Produk, Columns = Kategori, Values = Sum of Total. → Bandingkan penjualan tiap produk pada tiap kategori.

**Analisis 4 — Tren Bulanan:**
1. Klik kanan pada kolom tanggal di pivot → **Group** → pilih **Months** (bisa juga Quarters/Years) → OK.
2. Rows = Bulan (hasil pengelompokan), Values = Sum of Total.
3. **Insert → PivotChart → Line Chart** untuk melihat tren.

---

## E. Fitur Lanjutan Pivot Table

**Sort:** klik dropdown pada Row Labels → A-Z / Z-A, atau *More Sort Options* untuk mengurutkan berdasarkan nilai total.

**Filter:** klik dropdown → centang/hapus kategori yang ingin ditampilkan (misal hanya satu kategori, atau sembunyikan nilai 0).

**Group (Pengelompokan):**
- **Angka:** kelompokkan umur (0–10, 11–20, dst).
- **Tanggal:** kelompokkan per bulan, kuartal, atau tahun.
- **Manual:** pilih beberapa baris → klik kanan → Group.

**Slicer (Filter Visual):**
1. Klik Pivot Table → **PivotTable Analyze → Insert Slicer**.
2. Pilih field (Produk, Kategori, Bulan) → OK.
3. Klik tombol slicer untuk memfilter. Kelebihan: **satu slicer dapat terhubung ke beberapa pivot table** sekaligus (klik kanan slicer → Report Connections).

**Timeline (Filter Waktu):** **PivotTable Analyze → Insert Timeline** → pilih field tanggal → geser slider untuk memilih rentang waktu.

**Calculated Field (Kolom Hitung Kustom):**
1. Klik pivot → **PivotTable Analyze → Fields, Items & Sets → Calculated Field**.
2. Nama: "Profit"; Formula: `=Total - (Total*0.7)` (asumsi margin 30%).
3. Kolom baru langsung muncul di pivot table.

**Refresh:** jika data sumber berubah, klik kanan pivot → **Refresh**, atau **Data → Refresh All** saat membuka file.

**Format:** Design → Report Layout → *Show in Tabular Form*; Design → Grand Totals → *On for Rows and Columns*; klik kanan → Number Format untuk format Rp/desimal.

---

## F. Contoh Soal & Penyelesaian 📝

**Contoh 1:** Sebutkan 4 area (kuadran) dalam panel PivotTable Fields!
**Jawaban:** Rows, Columns, Values, dan Filters.

**Contoh 2:** Kamu ingin mengetahui total penjualan per kategori produk. Kemana saja field diletakkan?
**Jawaban:** Kategori ke **Rows**, dan Total ke **Values** (dengan perhitungan Sum).

**Contoh 3:** Bagaimana cara melihat tren penjualan per bulan menggunakan Pivot Table?
**Jawaban:** Kelompokkan field tanggal dengan **Group → Months**, letakkan Bulan di Rows dan Total di Values, lalu buat **PivotChart Line**.

**Contoh 4:** Apa fungsi slicer dan mengapa ia lebih nyaman daripada filter biasa?
**Jawaban:** Slicer adalah tombol visual untuk memfilter data dengan sekali klik, dan dapat dihubungkan ke beberapa pivot table sekaligus sehingga dashboard menjadi interaktif.

**Contoh 5:** Data sumber sudah diperbarui tetapi pivot table tidak berubah. Apa yang harus dilakukan?
**Jawaban:** Lakukan **Refresh** (klik kanan → Refresh, atau Data → Refresh All).

---

## G. Miskonsepsi yang Sering Terjadi 🚫

| Miskonsepsi | Fakta yang Benar |
|---|---|
| "Pivot Table mengubah data asli" | Pivot Table **tidak mengubah** data sumber; ia hanya merangkum |
| "Data boleh ada sel kosong atau merged cell" | Data harus rapi: header unik, tanpa merged cell dan baris kosong |
| "Filter dan Slicer fungsinya sama persis" | Sama-sama memfilter, tetapi **slicer lebih visual** dan bisa dipakai untuk banyak pivot sekaligus |
| "Rumus SUM harus ditulis manual di pivot" | Cukup seret field ke **Values** dan pilih **Sum** |
| "Pivot Table otomatis ter-update" | Perlu **Refresh** secara manual setelah data sumber berubah |

---

## H. Tantangan Praktik (Mengaplikasi) 🎯

**Tantangan 1 — Data Siap (20 menit):** Buat 30–40 baris data penjualan (Tanggal, Produk, Kategori, Qty, Harga, Total). Pastikan memenuhi semua syarat data pivot.

**Tantangan 2 — Pivot Dasar (50 menit):** Buat 3 pivot: total per produk, jumlah transaksi per kategori, dan matriks Produk × Kategori. Beri format angka Rupiah.

**Tantangan 3 — Tren & Interaktivitas (60 menit):** Kelompokkan data per bulan, tampilkan dalam PivotChart Line, lalu tambahkan **slicer** dan **timeline** yang terhubung ke seluruh pivot.

**Tantangan 4 — Kustom & Rapi (60 menit):** Tambahkan **Calculated Field "Profit"** (margin 30%), rapikan tampilan tabular, dan simpan sebagai `Latihan2_NamaKamu.xlsx`.

---

## I. Rangkuman Kunci 🔑

1. **Pivot Table** meringkas data besar tanpa mengubah data asli.
2. Empat area utama: **Rows, Columns, Values, Filters**.
3. Syarat data: header unik, tanpa merged cell, tanpa baris/kolom kosong, tipe data konsisten.
4. **Slicer** dan **Timeline** membuat filter cepat dan interaktif.
5. **Group** mengelompokkan angka/tanggal; **Calculated Field** menambah kolom hitung sendiri.
6. Selalu **Refresh** setelah data sumber diubah.

---

## J. Glosarium 📖

| Istilah | Arti |
|---|---|
| **Pivot Table** | Fitur meringkas dan menganalisis data tanpa mengubah data asli |
| **Field** | Nama kolom pada data sumber |
| **Slicer** | Tombol visual untuk memfilter data pivot |
| **Timeline** | Slider untuk memfilter berdasarkan rentang waktu |
| **Calculated Field** | Kolom perhitungan kustom di dalam pivot table |
| **Refresh** | Proses memperbarui pivot agar mengikuti perubahan data sumber |

---

## K. Refleksi (Merefleksi) 🔍

- Kapan sebaiknya kita menggunakan Pivot Table, bukan rumus biasa?
- Bagaimana slicer dan timeline mengubah cara orang membaca data?
- Tantangan apa yang kamu alami saat menyiapkan data yang rapi?
- **Skala pemahaman diri:** ____/10
- Analisis data apa di kehidupan nyata yang ingin kamu coba dengan Pivot Table?

---

**MGMP Informatika SMAN 6 Cimahi — Fase F (Kelas XII) Semester 1**