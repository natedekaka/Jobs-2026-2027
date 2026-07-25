# BAHAN AJAR – PERTEMUAN 14
## Big Data & Data Mining

| TP | BK, AP — Pengolahan Data Bervolume Besar |
|---|---|

---

### A. APA ITU BIG DATA?

**Big Data** adalah kumpulan data yang sangat besar, cepat berubah, dan beragam sehingga tidak dapat diproses menggunakan alat pengolahan data tradisional (Excel, SQL biasa).

#### Analogi: Perpustakaan

| Data Biasa | Big Data |
|---|---|
| Buku di perpustakaan sekolah | Seluruh buku di Perpustakaan Nasional |
| Dicari manual dengan katalog | Dicari dengan sistem digital |
| Data kelas: 36 siswa | Data seluruh pelajar Indonesia: 53 juta |

---

### B. 5V BIG DATA

#### 1. Volume — Jumlah Data

Data yang dihasilkan setiap menit di dunia:

| Platform | Data per Menit |
|---|---|
| YouTube | 500 jam video diupload |
| TikTok | 167 juta video ditonton |
| Google | 5,6 juta pencarian |
| Email | 241 juta email terkirim |
| WhatsApp | 69 juta pesan terkirim |

#### 2. Velocity — Kecepatan

Data mengalir dengan sangat cepat dan harus diproses secara real-time.

| Platform | Kecepatan Data |
|---|---|
| Twitter | 6.000 tweet/detik |
| Instagram | 1.000 post/detik |
| Sensor IoT | 1.000 data/detik |
| Bursa saham | 1 juta transaksi/detik |

#### 3. Variety — Keragaman

Big Data tidak hanya teks, tapi juga:

| Jenis Data | Contoh |
|---|---|
| **Struktur** | Tabel database, Excel |
| **Semi-struktur** | JSON, XML, HTML |
| **Tidak terstruktur** | Gambar, video, audio, teks bebas |

#### 4. Veracity — Kebenaran

Tidak semua data akurat. Data perlu divalidasi.

| Masalah | Contoh |
|---|---|
| Data tidak akurat | Sensor rusak → suhu -10°C di padang pasir |
| Data duplikat | 2 akun untuk 1 orang |
| Data hoax | Berita palsu menyebar di media sosial |
| Data tidak lengkap | Alamat tidak diisi saat registrasi |

#### 5. Value — Nilai

Big Data hanya berguna jika menghasilkan nilai.

| Data | Nilai |
|---|---|
| Data pembelian | Rekomendasi produk "Pelanggan juga membeli" |
| Data GPS | Prediksi macet → rute alternatif |
| Data kesehatan | Deteksi dini penyakit |
| Data nilai siswa | Prediksi siswa berpotensi drop out |

---

### C. SUMBER BIG DATA

```
                    ┌──────────────────┐
                    │   SUMBER BIG     │
                    │      DATA        │
                    └──────────────────┘
         ┌──────────────┬──────────────┐
         ▼              ▼              ▼
   ┌──────────┐   ┌──────────┐   ┌──────────┐
   │  MEDIA   │   │    IoT   │   │   BISNIS │
   │  SOSIAL  │   │          │   │          │
   ├──────────┤   ├──────────┤   ├──────────┤
   │Facebook  │   │Sensor    │   │E-commerce│
   │Instagram │   │GPS       │   │Transaksi │
   │TikTok    │   │Smartwatch│   │Logistik  │
   │Twitter   │   │CCTV      │   │Keuangan  │
   │YouTube   │   │Smart home│   │Kesehatan │
   └──────────┘   └──────────┘   └──────────┘
```

---

### D. DATA MINING

**Data Mining** adalah proses menemukan pola, hubungan, dan insight yang berguna dari data besar.

#### Proses KDD (Knowledge Discovery in Databases)

```
┌──────────┐   ┌──────────┐   ┌──────────┐   ┌──────────┐   ┌──────────┐
│Selection │──▶│Preproces│──▶│Transfor- │──▶│   Data   │──▶│Interpre- │
│          │   │  sing   │   │  mation  │   │  Mining  │   │  tation  │
├──────────┤   ├──────────┤   ├──────────┤   ├──────────┤   ├──────────┤
│Pilih data│   │Bersihkan│   │Ubah      │   │Terapkan  │   │Analisis  │
│relevan   │   │data     │   │format    │   │algoritma │   │hasil     │
└──────────┘   └──────────┘   └──────────┘   └──────────┘   └──────────┘
```

**Contoh KDD — Analisis Data Siswa Terlambat**

| Tahap | Aktivitas | Contoh |
|---|---|---|
| **Selection** | Pilih data absensi 1 tahun | Hanya data kehadiran pagi |
| **Preprocessing** | Hapus data libur, hari besar | — |
| **Transformation** | Kategorikan waktu terlambat | ≤15', ≤30', >30' |
| **Data Mining** | Cari pola keterlambatan | Senin & Kamis terbanyak |
| **Interpretation** | Rekomendasi kegiatan | "Rapat guru Senin pagi → siswa libur" |

---

### E. TEKNIK DATA MINING

#### 1. Klasifikasi

Mengelompokkan data ke dalam **kategori yang sudah ditentukan**.

```
Data: Email
        │
        ▼
   ┌────────┐
   │ SPAM?  │
   └────────┘
     │       │
     ▼       ▼
   SPAM    BUKAN SPAM
```

**Contoh:**
- Spam filter → Spam / Bukan
- Diagnosa penyakit → Positif / Negatif
- Kelulusan → Lulus / Tidak Lulus

**Algoritma:** Decision Tree, Naive Bayes, SVM

#### 2. Klastering

Mengelompokkan data ke dalam **kelompok alami (tidak ada label)**.

```
Data: Pelanggan
        │
        ▼
  ┌─────┴─────┐
  ▼           ▼
Klaster 1   Klaster 2
(Pembeli     (Pembeli
 setia)      kadang2)
```

**Contoh:**
- Segmentasi pelanggan
- Pengelompokan berita
- Analisis perilaku siswa

**Algoritma:** K-Means, DBSCAN

#### 3. Asosiasi (Market Basket Analysis)

Menemukan **hubungan antar item** — "Jika A, maka B".

**Contoh terkenal:**
- "Diaper → Beer" — Walmart menemukan pembeli popok juga cenderung beli bir
- "Beli roti → beli selai"
- "Beli laptop → beli mouse"

**Metrik:**

| Metrik | Rumus | Arti |
|---|---|---|
| **Support** | (A & B) / Total transaksi | Seberapa sering A dan B muncul bersama |
| **Confidence** | (A & B) / A | Jika beli A, seberapa mungkin beli B |
| **Lift** | Confidence / (B / Total) | Seberapa signifikan hubungannya |

#### 4. Regresi

Memprediksi **nilai numerik** berdasarkan data historis.

**Contoh:**
- Prediksi harga rumah berdasarkan luas, lokasi, kamar
- Prediksi nilai ujian berdasarkan jam belajar
- Prediksi cuaca / suhu

---

### F. ETIKA & PRIVASI BIG DATA

| Risiko | Contoh | Solusi |
|---|---|---|
| **Pelanggaran privasi** | Data kesehatan bocor | Enkripsi, akses terbatas |
| **Bias algoritma** | AI diskriminasi ras/gender | Data training yang beragam |
| **Manipulasi** | Iklan politik tertarget | Regulasi, transparansi |
| **Pengawasan massal** | CCTV + AI + data pribadi | Batasan hukum |

---

### G. RANGKUMAN

| Konsep | Inti |
|---|---|
| **Big Data** | Data sangat besar, cepat, beragam |
| **5V** | Volume, Velocity, Variety, Veracity, Value |
| **Data Mining** | Menemukan pola dari data besar |
| **KDD** | 5 tahap: Selection → Preprocessing → Transformation → Mining → Interpretation |
| **Klasifikasi** | Kelompok ke kategori yang sudah ada |
| **Klastering** | Kelompok alami tanpa label |
| **Asosiasi** | "Jika A maka B" — hubungan antar item |
| **Regresi** | Prediksi nilai numerik |

---

**MGMP Informatika SMAN 6 Cimahi**
