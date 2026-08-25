# BAHAN AJAR – PERTEMUAN 5 (S1)
## Studi Kasus Analisis Data
*Mengacu pada Panduan Mapel 2025; INFORMATIKA Fase D-F — pendekatan Pembelajaran Mendalam (Memahami → Mengaplikasi → Merefleksi)*

| Informasi | Keterangan |
|---|---|
| **Fase / Kelas** | F / Kelas XII |
| **Alokasi Waktu** | 5 JP × 45 menit (225 menit) |
| **Elemen CP** | Analisis Data (AD) |
| **Tujuan Pembelajaran** | Menganalisis data penjualan UMKM dengan Excel, menginterpretasi hasil, dan menyusun laporan analisis yang komunikatif beserta rekomendasi |
| **Materi Prasyarat** | Pivot Table, fungsi statistik bersyarat, dan pembuatan dashboard Excel |

---

## A. Kisah Pemantik 🎬

> **"Data UMKM yang Belum Berbicara"**
>
> Pak Santo memiliki kedai kopi bernama **"Kopi Nusantara"**. Ia mencatat semua transaksi di buku: siapa membeli, produk apa, dari kota mana, dan berapa harganya. Setahun berlalu, tumpukan catatan menumpuk — tetapi Pak Santo tidak tahu: produk apa yang paling laris? Bulan apa penjualan terbaik? Kota mana yang paling potensial? Padahal jawabannya **sudah ada di tumpukan buku itu**. Ia lalu meminta siswa magang untuk "membuat data itu berbicara".
>
> **Pertanyaan pemantik:** Data yang tersimpan tetapi tidak dianalisis ibarat apa? Apa keputusan bisnis yang bisa diambil pemilik kedai jika ia membaca polanya dengan benar?

---

## B. Kerangka Analisis Data

Analisis data adalah proses mengubah **data mentah → informasi → rekomendasi**. Alurnya:

```
Mengumpulkan → Membersihkan → Menganalisis → Menginterpretasi → Merekomendasikan
```

| Istilah | Arti |
|---|---|
| **Data mentah** | Catatan transaksi apa adanya (belum diolah) |
| **Insight** | Wawasan/penemuan penting dari data |
| **Interpretasi** | Menjelaskan makna di balik angka |
| **Rekomendasi** | Saran tindakan berdasarkan data |
| **Trend** | Pola naik/turun dari waktu ke waktu |

---

## C. Studi Kasus — UMKM "Kopi Nusantara"

UMKM menjual 3 kategori (Kopi, Minuman, Snack) selama 3 bulan (Jan–Mar 2025) dengan **90 baris transaksi**.

**Struktur data:**

| Tanggal | Produk | Kategori | Qty | Harga Satuan | Total | Pelanggan | Wilayah |
|---|---|---|---|---|---|---|---|
| 02/01/2025 | Kopi Arabika | Kopi | 5 | 25000 | 125000 | Andi | Bandung |
| 02/01/2025 | Pisang Goreng | Snack | 3 | 15000 | 45000 | Budi | Jakarta |
| ... | ... | ... | ... | ... | ... | ... | ... (90 baris) |

**Analisis yang dilakukan:**

**1. Produk Terlaris (berdasarkan Qty):** Pivot Rows = Produk, Values = Sum Qty, urutkan menurun. *Interpretasi:* "Kopi Arabika terjual 200 unit — tertinggi."

**2. Kategori Paling Menguntungkan:** Pivot Rows = Kategori, Values = Sum Total + Bar chart. *Interpretasi:* "Kopi menyumbang 60% dari total pendapatan."

**3. Tren Penjualan Bulanan:** Pivot Rows = Tanggal → Group Months, Values = Sum Total + Line chart. *Interpretasi:* "Penjualan naik 15% dari Januari ke Februari."

**4. Top Pelanggan:** Pivot Rows = Pelanggan, Values = Sum Total, urutkan menurun. *Interpretasi:* "5 pelanggan teratas menyumbang 40% pendapatan."

**5. Wilayah Pemasaran:** Pivot Rows = Wilayah, Values = Sum Total + Pie chart. *Interpretasi:* "Bandung menyumbang 50% penjualan."

---

## D. Membuat Dashboard UMKM

1. Sheet **"Data"**: 90 baris data mentah.
2. Sheet **"Analisis"**: Pivot Table + Chart untuk setiap poin analisis di atas.
3. Sheet **"Dashboard"**: satu tampilan berisi KPI + chart + slicer.

**KPI Cards:** Total Revenue 3 bulan, Rata-rata Transaksi, Produk Terlaris, Jumlah Pelanggan, Pertumbuhan Bulanan (%).

**Slicer:** Kategori, Wilayah, Bulan.

---

## E. Interpretasi Data dan Laporan

**Interpretasi yang baik** menghubungkan angka dengan kemungkinan penyebab dan langkah lanjut. Contoh:

> "Penjualan tertinggi terjadi di bulan Maret (Rp 25 juta), kemungkinan karena mendekati libur Ramadan. Kopi Arabika menjadi produk paling laris karena kualitasnya. Disarankan menambah stok Kopi Arabika 30% menjelang Ramadan."

**Sheet "Laporan"** berisi:
1. **Ringkasan:** total revenue, rata-rata transaksi, produk terlaris, kategori dominan.
2. **Kesimpulan:** 3–5 kalimat — apa yang terjadi dengan bisnis ini?
3. **Saran:** 2–3 rekomendasi konkret untuk pemilik UMKM.
4. **Data pendukung:** screenshot chart/pivot table.

---

## F. Contoh Soal & Penyelesaian 📝

**Contoh 1:** Sebutkan 5 langkah alur analisis data!
**Jawaban:** Mengumpulkan → Membersihkan → Menganalisis → Menginterpretasi → Merekomendasikan.

**Contoh 2:** Dari pivot "produk terlaris", ditemukan Kopi Arabika terjual 200 unit, tertinggi. Tuliskan satu kalimat interpretasi yang baik!
**Jawaban:** "Kopi Arabika merupakan produk paling laris dengan penjualan 200 unit, sehingga stok produk ini perlu diprioritaskan."

**Contoh 3:** Mengapa interpretasi harus disertai kemungkinan penyebab, bukan hanya menyebut angka?
**Jawaban:** Karena angka saja tidak menjelaskan **mengapa** suatu pola terjadi; penyebab membantu pemilik bisnis mengambil keputusan yang tepat, seperti menambah stok menjelang Ramadan.

**Contoh 4:** Tuliskan 3 isi utama sheet "Laporan"!
**Jawaban:** (1) Ringkasan data kunci, (2) kesimpulan kondisi bisnis, (3) saran/rekomendasi untuk pemilik UMKM.

**Contoh 5:** Dashboard UMKM disarankan memakai slicer apa saja?
**Jawaban:** Slicer Kategori, Wilayah, dan Bulan agar pemilik bisa memfilter data sesuai kebutuhan.

---

## G. Miskonsepsi yang Sering Terjadi 🚫

| Miskonsepsi | Fakta yang Benar |
|---|---|
| "Analisis data cukup menghitung total" | Analisis butuh **interpretasi** dan **rekomendasi** agar berguna |
| "Chart sudah otomatis menjelaskan data" | Chart harus **dibaca dan dijelaskan** — itulah interpretasi |
| "Rekomendasi boleh tanpa dasar data" | Rekomendasi harus **berakar pada data** yang dianalisis |
| "Semakin banyak angka, laporan semakin baik" | Laporan yang baik **ringkas dan komunikatif**, fokus pada insight penting |
| "Data mentah langsung dapat disimpulkan" | Data harus **dibersihkan** dulu sebelum dianalisis |

---

## H. Tantangan Praktik (Mengaplikasi) 🎯

**Tantangan 1 — Bangun Data (30 menit):** Buat 90 baris data penjualan 3 bulan dengan 8 kolom sesuai struktur di atas.

**Tantangan 2 — Analisis (75 menit):** Lakukan 5 analisis (produk terlaris, kategori, tren bulanan, top pelanggan, wilayah) menggunakan Pivot + Chart di sheet "Analisis".

**Tantangan 3 — Dashboard (60 menit):** Buat sheet "Dashboard" berisi 5 KPI cards, 2 chart utama, dan slicer Kategori + Wilayah.

**Tantangan 4 — Laporan (60 menit):** Tulis sheet "Laporan" berisi ringkasan, kesimpulan, 3 rekomendasi, dan screenshot data pendukung. Simpan sebagai `KopiNusantara_NamaKamu.xlsx`.

---

## I. Rangkuman Kunci 🔑

1. Alur analisis data: **mengumpulkan → membersihkan → menganalisis → menginterpretasi → merekomendasikan**.
2. **Pivot Table + chart** adalah alat utama untuk membaca pola data besar.
3. Interpretasi yang baik menyebut **angka + penyebab + saran**.
4. Dashboard dan laporan membuat insight mudah dipahami pemangku kepentingan.
5. Keputusan bisnis sebaiknya **berbasis data**, bukan perasaan.

---

## J. Glosarium 📖

| Istilah | Arti |
|---|---|
| **Data mentah** | Data apa adanya sebelum diolah |
| **Insight** | Penemuan/wawasan penting dari analisis data |
| **Interpretasi** | Penjelasan makna di balik angka |
| **Rekomendasi** | Saran tindakan berdasarkan temuan data |
| **Trend** | Pola kenaikan/penurunan dari waktu ke waktu |
| **UMKM** | Usaha Mikro, Kecil, dan Menengah |

---

## K. Refleksi (Merefleksi) 🔍

- Bagaimana analisis data mengubah cara pemilik bisnis mengambil keputusan?
- Bagian mana yang paling menantang: membuat pivot, membaca chart, atau menulis interpretasi?
- Data pribadi apa yang bisa kamu analisis untuk memperbaiki kebiasaan belajarmu?
- **Skala pemahaman diri:** ____/10
- Apa yang ingin kamu pelajari lebih lanjut tentang analisis data?

---

**MGMP Informatika SMAN 6 Cimahi — Fase F (Kelas XII) Semester 1**