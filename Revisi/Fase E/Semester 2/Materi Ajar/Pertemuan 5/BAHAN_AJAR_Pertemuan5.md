# BAHAN AJAR – PERTEMUAN 5 (S2)
## Studi Kasus — Pengolahan Data Nyata
*Mengacu pada Panduan Mapel 2025; INFORMATIKA Fase D-F — pendekatan Pembelajaran Mendalam (Memahami → Mengaplikasi → Merefleksi)*

| Informasi | Keterangan |
|---|---|
| **Fase / Kelas** | E / Kelas X |
| **Alokasi Waktu** | 2 JP × 45 menit (90 menit) |
| **Elemen CP** | Analisis Data (AD) / Teknik Informatika dan Komunikasi (TIK) |
| **Tujuan Pembelajaran** | Menerapkan seluruh keterampilan Excel (rumus, fungsi, filter, dan grafik) untuk menganalisis data penjualan nyata dan menarik kesimpulan |
| **Materi Prasyarat** | Rumus, referensi sel, IF/VLOOKUP, dan grafik dasar (Pertemuan 1–4) |

---

## A. Kisah Pemantik 🎬

> **"Warung Kopi yang Bangkrut karena Tidak Membaca Data"**
>
> Sebuah kafe menjual kopi, teh, dan jus. Pemiliknya selalu merasa "kopi yang paling laris". Ternyata saat data penjualan 1 bulan diolah di Excel, **jus** justru menyumbang 60% pendapatan! Kopi hanya sedikit. Karena telanjur fokus pada kopi, kafe itu akhirnya kesulitan. Andai pemiliknya menganalisis data lebih awal, ia bisa mengubah strateginya. 📉
>
> **Pertanyaan pemantik:** Bagaimana sebuah usaha kecil bisa mengambil keputusan berdasarkan data, bukan sekadar perasaan? Data apa yang mungkin bisa kamu kumpulkan dan analisis di sekitarmu?

---

## B. Mengapa Studi Kasus Penting? 🎯

Di pertemuan ini seluruh kemampuan Excel kamu dipakai secara terpadu untuk memecahkan masalah nyata: **mengumpulkan data → mengolah dengan rumus → menganalisis → menarik kesimpulan → menyajikan dengan grafik**. Inilah siklus kerja analisis data yang sesungguhnya.

```
Data mentah → Rumus & Fungsi → Analisis → Kesimpulan → Grafik & Laporan
```

---

## C. Studi Kasus: Analisis Penjualan Toko Kelontong 🏪

Sebuah toko mencatat 20 transaksi penjualan dalam satu minggu. Kamu bertugas menganalisisnya.

### Data yang Disediakan (contoh 5 baris dari 20)
| No | Tanggal | Produk | Qty | Harga Satuan | Total |
|---|---|---|---|---|---|
| 1 | 10/08/2026 | Kopi | 3 | 8.000 | `=D2*E2` |
| 2 | 10/08/2026 | Teh | 5 | 5.000 | `=D3*E3` |
| 3 | 11/08/2026 | Kopi | 2 | 8.000 | `=D4*E4` |
| 4 | 11/08/2026 | Jus | 4 | 10.000 | `=D5*E5` |
| 5 | 12/08/2026 | Roti | 2 | 12.000 | `=D6*E6` |

**Kolom Total** dihitung dengan rumus `=D2*E2` (Qty × Harga), lalu disalin ke bawah.

---

## D. Langkah Analisis 📋

### D.1 Menghitung Ringkasan dengan Fungsi
| Metrik | Rumus | Contoh Hasil |
|---|---|---|
| Total penjualan | `=SUM(F2:F21)` | Rp2.450.000 |
| Rata-rata per transaksi | `=AVERAGE(F2:F21)` | Rp122.500 |
| Transaksi terbesar | `=MAX(F2:F21)` | Rp480.000 |
| Transaksi terkecil | `=MIN(F2:F21)` | Rp15.000 |
| Banyak transaksi | `=COUNT(F2:F21)` | 20 |

### D.2 Menganalisis per Produk dengan SUMIF
Untuk mengetahui pendapatan tiap produk, gunakan **SUMIF**:
```
=SUMIF(C2:C21; "Kopi"; F2:F21)
```
Arti: jumlahkan kolom Total (F2:F21) hanya untuk baris yang berisi "Kopi" di kolom C.

### D.3 Filter Data (Menyaring Baris)
1. Klik salah satu sel di dalam tabel.
2. Klik menu **Data** → **Filter**.
3. Muncul ikon dropdown di setiap header → klik untuk memfilter.
4. Contoh filter yang berguna:
   - Tampilkan hanya produk "Kopi".
   - Tampilkan transaksi dengan Total > 100.000 (filter angka → Number Filters → Greater Than).
   - Urutkan Total dari terbesar (Sort → Largest to Smallest).

> 💡 **Tips:** Filter tidak menghapus data — hanya menyembunyikan baris yang tidak sesuai. Matikan filter dengan klik tombol Filter lagi.

---

## E. Conditional Formatting — Menyorot Data Penting 🎨

**Conditional Formatting** memberi warna otomatis pada sel yang memenuhi aturan tertentu, sehingga pola langsung terlihat.

### Langkah:
1. Blok kolom Total (F2:F21).
2. Menu **Home** → **Conditional Formatting** → **Highlight Cell Rules**.
3. Pilih aturan, misalnya **Greater Than** → ketik `100000` → pilih warna (Green Fill with Dark Green Text).
4. Klik OK — semua transaksi di atas Rp100.000 otomatis menyala hijau. ✅

### Aturan Lain yang Berguna
- **Less Than** 50.000 → merah (transaksi kecil).
- **Top/Bottom Rules** → 10 item teratas.
- **Data Bars** → panjang batang dalam sel.

---

## F. Menyajikan dengan Grafik 📊

Setelah analisis, buat laporan visual:
1. **Pendapatan per Produk:** buat tabel ringkas (Produk → Total) menggunakan SUMIF, lalu buat **Column chart**.
2. **Tren Harian:** buat tabel Total per tanggal, lalu buat **Line chart**.
3. **Proporsi Pendapatan:** buat **Pie chart** untuk melihat produk penyumbang terbesar.

### Contoh Kesimpulan Laporan
- Produk paling laris: **Jus** (60% pendapatan) → sarankan stok diperbanyak.
- Transaksi terbesar terjadi di hari **Sabtu** → butuh kasir tambahan.
- Ada 5 transaksi di bawah Rp50.000 → bisa ditawari paket hemat.

---

## G. Contoh Soal & Penyelesaian 📝

**Contoh 1:** Tuliskan rumus untuk menghitung total pendapatan toko dari 20 transaksi di kolom F2:F21.
**Pembahasan:** `=SUM(F2:F21)`.

**Contoh 2:** Bagaimana cara menampilkan hanya transaksi dengan Total lebih dari Rp100.000 tanpa menghapus baris lain?
**Pembahasan:** Gunakan **Data → Filter**, lalu pada dropdown kolom Total pilih Number Filters → **Greater Than** → 100000. Baris lain disembunyikan sementara.

**Contoh 3:** Tuliskan rumus SUMIF untuk menjumlahkan pendapatan produk "Kopi" bila Produk di C2:C21 dan Total di F2:F21.
**Pembahasan:** `=SUMIF(C2:C21;"Kopi";F2:F21)`.

**Contoh 4:** Data menunjukkan total penjualan = Rp2.450.000 dan ada 20 transaksi. Berapa rata-rata per transaksi?
**Pembahasan:** `=AVERAGE(F2:F21)` atau `=2450000/20` = **Rp122.500**.

---

## H. Miskonsepsi yang Sering Terjadi 🚫

| Miskonsepsi | Fakta yang Benar |
|---|---|
| "Filter menghapus data" | Filter hanya **menyembunyikan** baris; data tetap ada |
| "SUMIF sama dengan SUM" | SUMIF menjumlahkan **bersyarat** (produk tertentu); SUM menjumlahkan semua |
| "Cukup membuat tabel tanpa kesimpulan" | Tujuan analisis adalah **menarik kesimpulan** untuk pengambilan keputusan |
| "Grafik selalu menambah pemahaman" | Grafik harus dipilih sesuai data agar benar-benar informatif |
| "Kondisional formatting hanya untuk dekorasi" | Ini membantu **mendeteksi pola/outlier** secara visual |

---

## I. Tantangan Praktik (Mengaplikasi) 🎯

**Tantangan 1 — Data Mini:** Buat 10 data penjualan kecil (Produk, Qty, Harga) dengan kolom Total berisi rumus. Hitung SUM dan AVERAGE.

**Tantangan 2 — Filter & Format:** Terapkan filter untuk menampilkan produk tertentu, lalu gunakan Conditional Formatting (Greater Than) pada kolom Total.

**Tantangan 3 — Laporan Lengkap:** Buat laporan satu halaman berisi: tabel ringkas pendapatan per produk (SUMIF), column chart, pie chart, dan **3 kesimpulan** yang bisa diambil pemilik toko.

---

## J. Rangkuman Kunci 🔑

1. Studi kasus menggabungkan seluruh kemampuan Excel dalam satu alur kerja nyata.
2. Ringkasan data: **SUM, AVERAGE, MAX, MIN, COUNT**.
3. **SUMIF** menjumlahkan dengan syarat tertentu (per produk).
4. **Filter** menyaring tampilan data tanpa menghapusnya.
5. **Conditional Formatting** menyorot sel yang memenuhi aturan.
6. Sajikan hasil dengan **grafik** yang tepat dan tarik **kesimpulan**.
7. Keputusan terbaik lahir dari data, bukan sekadar perasaan.

---

## K. Glosarium 📖

| Istilah | Arti |
|---|---|
| **Studi kasus** | Penerapan materi pada masalah nyata |
| **SUMIF** | Penjumlahan bersyarat |
| **Filter** | Menyaring baris data sementara |
| **Conditional Formatting** | Pemformatan otomatis berdasarkan aturan |
| **Outlier** | Data yang jauh berbeda dari kebanyakan |
| **Kesimpulan** | Pemaknaan hasil analisis |

---

## L. Refleksi (Merefleksi) 🔍

- Keterampilan Excel apa yang paling berguna menurutmu untuk analisis data nyata?
- Apa kesimpulan paling menarik yang kamu dapat dari data yang kamu olah?
- Kesulitan apa yang kamu temui saat menggabungkan rumus, filter, dan grafik?
- Bagaimana cara kerja analisis data ini mirip dengan cara kamu mengambil keputusan sehari-hari?
- **Skala pemahaman diri:** ____/10
- Data nyata apa yang ingin kamu analisis sendiri di luar kelas?

---

**MGMP Informatika SMAN 6 Cimahi — Fase E (Kelas X) Semester 2**