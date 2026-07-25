# PENILAIAN TENGAH SEMESTER (PTS) GENAP
## INFORMATIKA – FASE F / KELAS XI
### TAHUN PELAJARAN 2026/2027

| | |
|---|---|
| **Hari/Tanggal** | ____________________ |
| **Waktu** | 90 menit |
| **Jumlah Soal** | 20 PG + 4 Esai |
| **Skor Maksimal** | 100 |
| **Materi** | Pengolahan Data (Pert 1–5) |
| **Satuan Pendidikan** | SMA Negeri 6 Cimahi |

---

### PETUNJUK

1. Doa sebelum mengerjakan
2. Tulis nama, kelas di lembar jawab
3. PG: beri tanda silang (X) pada satu jawaban benar
4. Esai: tulis jawaban jelas dan lengkap

---

## BAGIAN A — PILIHAN GANDA (20 Soal × 2 Poin = 40 Poin)

---

**1.** Dalam Big Data 5V, aspek yang menjelaskan kecepatan data masuk dan perlu diproses adalah...

A. Volume
B. Velocity
C. Variety
D. Veracity
E. Value

**2.** Berikut adalah contoh Open Data yang legal untuk digunakan, **kecuali**...

A. Dataset dari data.go.id
B. Dataset publik Kaggle
C. Data cuaca BMKG dari API publik
D. Database pasien rumah sakit yang bocor di internet
E. Data BPS jumlah penduduk

**3.** Menggunakan foto profil Instagram teman untuk dataset machine learning tanpa izin termasuk...

A. Open Data
B. Public Data
C. Illegal Data
D. Private Data (dengan izin)
E. Fair Use

**4.** Dampak missing values dalam dataset adalah...

A. Data menjadi lebih cepat diproses
B. Rata-rata menjadi bias dan jumlah sampel berkurang
C. Dataset otomatis diperbaiki
D. Tidak ada dampak
E. Data menjadi lebih akurat

**5.** Cara mendeteksi data duplikat di Google Sheets adalah...

A. `=ISBLANK(A2)`
B. `=MAX(A2:A100)`
C. Conditional formatting dengan `=COUNTIF(A:A,A1)>1`
D. `=AVERAGE(A2:A100)`
E. `=TRIM(A2)`

**6.** Outlier dalam dataset adalah...

A. Data yang hilang
B. Data yang muncul dua kali
C. Nilai yang sangat berbeda dari mayoritas data
D. Data dengan format salah
E. Data yang sudah dibersihkan

**7.** Fungsi `=PROPER()` di Google Sheets digunakan untuk...

A. Menghapus spasi berlebih
B. Mengubah teks menjadi format judul (huruf besar di awal kata)
C. Mengecek data kosong
D. Menghitung rata-rata
E. Menyaring data

**8.** Tujuan utama data labeling dalam machine learning adalah...

A. Menghapus data duplikat
B. Memberi kategori pada data mentah untuk supervised learning
C. Memperbesar ukuran dataset
D. Mengubah format data
E. Mengompresi data

**9.** Berikut adalah contoh klasifikasi biner, yaitu...

A. Positif / Netral / Negatif
B. Spam / Bukan Spam
C. Sangat Puas / Puas / Cukup / Kurang
D. Merah / Kuning / Hijau
E. SD / SMP / SMA

**10.** Karakteristik dashboard yang baik adalah...

A. Berisi banyak tabel angka
B. Harus di-scroll ke bawah
C. Satu layar, visual, interaktif, fokus pada KPI
D. Tidak perlu filter
E. Hanya satu grafik

**11.** Berikut adalah contoh KPI (Key Performance Indicator) dalam dashboard nilai, **kecuali**...

A. Rata-rata nilai
B. Persentase kelulusan
C. Nama siswa
D. Nilai tertinggi
E. Jumlah siswa

**12.** Prinsip F-shape dalam layout dashboard berarti...

A. Grafik berbentuk huruf F
B. Informasi terpenting di kiri atas, KPI di atas
C. Semua konten di tengah
D. Tidak ada aturan khusus
E. Warna harus merah

**13.** Manakah yang merupakan contoh baris data dalam format CSV?

A. `{"nama": "Budi", "nilai": 85}`
B. `Budi,X-A,85`
C. `<nama>Budi</nama>`
D. `nama: Budi, nilai: 85`
E. `Budi | X-A | 85`

**14.** Tipe data yang **tidak** dikenal dalam JSON adalah...

A. String
B. Number
C. Boolean
D. Date
E. Null

**15.** Fungsi `next(reader)` dalam Python `csv.reader` digunakan untuk...

A. Membaca baris terakhir
B. Melewati baris header
C. Menutup file
D. Menulis baris baru
E. Menghapus baris

**16.** Fungsi Python untuk membaca file JSON adalah...

A. `json.read()`
B. `json.load()`
C. `json.parse()`
D. `json.open()`
E. `json.get()`

**17.** Kelebihan `csv.DictReader` dibanding `csv.reader` adalah...

A. Lebih cepat
B. Bisa mengakses kolom menggunakan nama, bukan indeks
C. Tidak perlu import module
D. Hanya bisa membaca file JSON
E. Otomatis menghapus duplikat

**18.** Langkah yang benar untuk konversi CSV ke JSON adalah...

A. Baca JSON → tulis CSV
B. Baca CSV → parsing tiap baris → tulis JSON
C. Copy-paste manual
D. JSON tidak bisa dikonversi ke CSV
E. Baca CSV → langsung jadi JSON tanpa kode

**19.** Urutan pipeline pengolahan data yang benar adalah...

A. Olah → Cuci → Cari → Visual → Lapor
B. Cari → Cuci → Olah → Visual → Lapor
C. Lapor → Visual → Olah → Cuci → Cari
D. Cuci → Cari → Olah → Visual → Lapor
E. Cari → Olah → Cuci → Visual → Lapor

**20.** Prinsip "consent" dalam etika data berarti...

A. Data harus dienkripsi
B. Pengguna harus memberi izin sebelum datanya digunakan
C. Data harus disimpan di cloud
D. Semua data boleh digunakan untuk riset
E. Data tidak perlu dihapus

---

## BAGIAN B — ESAI (4 Soal × 15 Poin = 60 Poin)

---

**21.** (Data Cleaning — 15 poin)

Seorang guru mengumpulkan data nilai siswa dalam file `nilai_kotor.csv`:

```
Nama,Kelas,Nilai
budi santoso,X-A,85
Budi Santoso,X-A,85
Citra Dewi,X-B,
Adi Pratama,X-C,-10
Dian Kurniawan,X-A,120
Eka Putri,X-B,78
```

Berdasarkan data di atas:
a. Identifikasi **3 masalah kualitas data** yang ditemukan! (3 poin)
b. Untuk setiap masalah, jelaskan **solusi cleaning** yang tepat! (6 poin)
c. Tuliskan **data setelah cleaning** (dalam format CSV)! (6 poin)

---

**22.** (Dashboard — 15 poin)

Kamu diminta membuat dashboard untuk data penjualan di kantin sekolah selama 1 bulan (30 hari). Data yang tersedia: Tanggal, Menu (Nasi Goreng/Mie Ayam/Bakso), Jumlah Terjual, Harga Satuan.

a. Sebutkan **4 KPI** yang akan kamu tampilkan di dashboard! (4 poin)
b. Sebutkan **2 jenis grafik** yang tepat + jelaskan **tujuan** masing-masing! (6 poin)
c. Gambarkan **layout dashboard** (sketsa kotak-kotak dengan posisi judul, KPI, grafik, filter)! (5 poin)

---

**23.** (Python CSV/JSON — 15 poin)

Diberikan file `data_siswa.csv`:

```csv
Nama,Kelas,Nilai
Adi,X-A,85
Budi,X-B,70
Citra,X-A,90
Dian,X-C,65
Eka,X-B,80
```

Tulis kode Python untuk:
a. Membaca file CSV dan mencetak semua data (3 poin)
b. Menghitung rata-rata nilai dan mencetaknya (4 poin)
c. Menyimpan hasil (data + rata-rata) ke file JSON `hasil.json` (4 poin)
d. Memfilter siswa dengan nilai ≥ 75 dan mencetak nama-namanya (4 poin)

---

**24.** (Studi Kasus Pipeline — 15 poin)

Seorang peneliti ingin menganalisis data cuaca dari BMKG untuk memprediksi musim tanam padi di Jawa Barat. Data tersedia di `data.bmkg.go.id` dalam format CSV (100.000 baris, 15 kolom) — berisi suhu, curah hujan, kelembaban, kecepatan angin per hari selama 10 tahun.

Berdasarkan kasus di atas:
a. Jelaskan **5 langkah pipeline** yang harus dilakukan peneliti! (5 poin)
b. Untuk langkah **cleaning**: sebutkan 3 potensi masalah data cuaca dan solusinya! (6 poin)
c. Untuk langkah **visualisasi**: sebutkan 2 jenis grafik yang tepat dan insight yang bisa didapat! (4 poin)

---

### — SELAMAT MENGERJAKAN —

**MGMP Informatika SMAN 6 Cimahi**
