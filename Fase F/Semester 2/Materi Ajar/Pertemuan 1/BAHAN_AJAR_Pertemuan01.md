# BAHAN AJAR – PERTEMUAN 1 (S2)
## Big Data & Sumber Data Terbuka

| TP | BK, AD — Pengolahan Data Bervolume Besar |
|---|---|

---

### A. REVIEW BIG DATA 5V

| V | Definisi | Contoh |
|---|---|---|
| **Volume** | Ukuran data yang sangat besar — dari terabyte (TB) hingga petabyte (PB) | YouTube: 500 jam video diunggah setiap menit |
| **Velocity** | Kecepatan data masuk dan perlu diproses — real-time atau near-real-time | Twitter: 6.000 tweet per detik, Gojek: 1 juta transaksi/hari |
| **Variety** | Keragaman format data — terstruktur (tabel), semi-terstruktur (JSON), tidak terstruktur (gambar, video) | Data media sosial: teks → gambar → video → lokasi |
| **Veracity** | Kualitas dan kepercayaan data — data valid vs data noise | Data sensor: akurat; data survey online: rawan bias |
| **Value** | Nilai/manfaat yang diperoleh dari data setelah diolah | Prediksi cuaca → pertanian lebih baik; analisis belanja → rekomendasi produk |

---

### B. SUMBER DATA

#### 1. Open Data

> Data yang tersedia untuk publik — bebas diakses, digunakan, dan dibagikan.

**Ciri Open Data:**
- Akses gratis
- Lisensi terbuka (Creative Commons, Open Data Commons)
- Format machine-readable (CSV, JSON, XML)
- Metadata lengkap

**Portal Open Data di Indonesia:**

| Portal | URL | Jenis Data |
|---|---|---|
| **Satu Data Indonesia** | data.go.id | Pendidikan, kependudukan, ekonomi, kesehatan |
| **BMKG** | data.bmkg.go.id | Cuaca, gempa, iklim |
| **BPS** | bps.go.id | Statistik nasional, inflasi, tenaga kerja |
| **Kemendikbud** | data.kemdikbud.go.id | Sekolah, guru, siswa, nilai |
| **Data Jakarta** | data.jakarta.go.id | Data provinsi DKI Jakarta |
| **BEI** | idx.co.id | Data saham & emiten |

**Internasional:**

| Portal | URL | Jenis Data |
|---|---|---|
| **World Bank** | data.worldbank.org | Ekonomi global |
| **Kaggle** | kaggle.com | Dataset untuk ML |
| **UN Data** | data.un.org | Data PBB |

#### 2. Public Data vs Private Data

| Aspek | Public Data | Private Data |
|---|---|---|
| Akses | Terbuka (bisa gratis/berbayar) | Terbatas, perlu izin |
| Contoh | Data BPS, jurnal akademik | Data pelanggan, data medis |
| Penggunaan | Bisa untuk riset dengan atribusi | Butuh persetujuan (informed consent) |
| Regulasi | UU KIP (Keterbukaan Informasi Publik) | UU PDP (Perlindungan Data Pribadi) |

#### 3. Illegal Data

> Data yang diperoleh, digunakan, atau disebarkan melanggar hukum.

**Contoh:**
- Data bocor dari peretasan (database e-commerce)
- Data pribadi yang dijual tanpa izin
- Scraping data pribadi dari media sosial untuk tujuan komersial tanpa izin
- Dataset berisi konten ilegal

**Dampak:**
- Pidana (UU ITE pasal 30–35)
- Denda administratif (UU PDP: hingga 2% dari pendapatan)
- Kerusakan reputasi

---

### C. DATA.GO.ID — SATU DATA INDONESIA

Portal resmi Open Data Pemerintah Indonesia.

#### Cara Menggunakan:

| Langkah | Cara |
|---|---|
| 1. Buka | `data.go.id` |
| 2. Cari | Gunakan kata kunci (misal: "pendidikan", "penduduk") |
| 3. Filter | Gunakan filter: instansi, kategori, format, lisensi |
| 4. Lihat | Klik dataset → baca metadata (deskripsi, sumber, update) |
| 5. Download | Pilih format CSV atau JSON |
| 6. Olah | Buka di Google Sheets / Python |

#### Contoh Dataset:

| Dataset | Instansi | Baris | Kolom |
|---|---|---|---|
| Jumlah Penduduk per Provinsi 2025 | BPS | 34 | 5 |
| Data Sekolah per Provinsi | Kemendikbud | 200.000+ | 15 |
| Realisasi APBN | Kemenkeu | 10.000+ | 20 |
| Indeks Harga Konsumen | BPS | 500+ | 10 |

---

### D. ETIKA PENGGUNAAN DATA

#### Prinsip Etika

| Prinsip | Pertanyaan Kunci |
|---|---|
| **Izin (Consent)** | Apakah saya punya izin untuk menggunakan data ini? |
| **Transparansi** | Apakah pengguna data tahu data mereka digunakan? |
| **Tujuan** | Apakah saya menggunakan data sesuai tujuan awal? |
| **Privasi** | Apakah data pribadi dilindungi? |
| **Akuntabilitas** | Siapa yang bertanggung jawab jika terjadi pelanggaran? |
| **Keadilan** | Apakah penggunaan data menimbulkan bias/diskriminasi? |

#### Kasus Etika

| Kasus | Analisis |
|---|---|
| **Casual** — Menjual data pengguna tanpa izin ke pihak ketiga | Melanggar UU PDP, bisa didenda 2% dari pendapatan |
| **Cambridge Analytica** (2018) | Data 87 juta pengguna Facebook digunakan untuk iklan politik tanpa izin → Facebook didenda $5 miliar |
| **Scraping LinkedIn** (2019) | Perusahaan hiQ scrape data profil LinkedIn — pengadilan putuskan data publik boleh di-scrape |

---

### E. STUDI KASUS: APAKAH DATA INI LEGAL?

| Skenario | Legal? | Alasan |
|---|---|---|
| Download dataset penduduk dari data.go.id | ✅ | Open data, lisensi terbuka |
| Menggunakan foto Instagram tanpa izin untuk riset | ❌ | Ilegal — butuh izin pemilik |
| Menggunakan dataset Titanic dari Kaggle | ✅ | Publik, lisensi terbuka |
| Database pasien bocor di forum hacker | ❌ | Illegal — hasil peretasan |
| Data cuaca BMKG untuk tugas sekolah | ✅ | Open data, API publik |
| Scrape data LinkedIn untuk analisis pasar | ⚠️ | Grey area — tergantung yurisdiksi |

---

### F. RANGKUMAN

| Konsep | Poin Penting |
|---|---|
| Big Data 5V | Volume, Velocity, Variety, Veracity, Value |
| Open Data | data.go.id, BMKG, BPS — bebas akses |
| Private Data | Butuh izin — dilindungi UU PDP |
| Illegal Data | Melanggar hukum — pidana |
| Etika Data | Izin, tujuan, privasi, akuntabilitas |

---

**MGMP Informatika SMAN 6 Cimahi**
