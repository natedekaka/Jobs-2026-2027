# BAHAN AJAR – PERTEMUAN 3 (S2)
## Workshop — Pengumpulan Data
*Mengacu pada Panduan Mapel 2025; INFORMATIKA Fase D-F — pendekatan Pembelajaran Mendalam (Memahami → Mengaplikasi → Merefleksi)*

| Informasi | Keterangan |
|---|---|
| **Fase / Kelas** | F / Kelas XII |
| **Alokasi Waktu** | 5 JP × 45 menit (225 menit) |
| **Elemen CP** | PLB (Praktik Lintas Bidang) |
| **Tujuan Pembelajaran** | Menyebarkan instrumen pengumpulan data, mengekspor data Google Form ke Excel, membersihkan data mentah, dan menyusun data siap analisis |
| **Materi Prasyarat** | Proposal & instrumen siap (Pertemuan 2); dasar-dasar Excel (S1) |

---

## A. Kisah Pemantik 🎬

> **"Data Kotor, Analisis Kacau"**
>
> Kelompok Bima semangat mengumpulkan 40 responden dalam semalam. Ketika data dibuka di Excel, ternyata isinya berantakan: ada baris kosong, jawaban "asdfgh" di kolom nama, kelas yang ditulis "XI A", "XI-A", dan "11A", serta beberapa jawaban yang tidak relevan. Analis kelompoknya bingung, *"Pivot Table-nya kok angkanya aneh?"*
>
> Gurunya tersenyum, *"Seperti memasak — bahan yang kotor akan membuat masakan tidak enak. Sebelum menganalisis, data harus dibersihkan dulu."* Setelah memahami *data cleaning*, kelompok Bima merapikan data dan analisisnya menjadi masuk akal.
>
> **Pertanyaan pemantik:**
> 1. Mengapa data yang baru diambil dari survei tidak bisa langsung dianalisis?
> 2. Apa bahayanya jika data yang dianalisis kotor atau tidak konsisten?
> 3. Mengapa kita perlu menghapus kolom nama/timestamp saat cleaning?

---

## B. Konsep Inti: Kualitas Data Menentukan Kualitas Analisis

**Data mentah (raw data)** adalah data yang baru keluar dari Google Form — biasanya masih kotor. **Data bersih (clean data)** adalah data yang siap dianalisis. Alur pengelolaan data: **Kumpulkan → Ekspor → Bersihkan → Siap Analisis**.

| Istilah | Arti | Contoh |
|---|---|---|
| **Raw data** | Data mentah hasil survei | Hasil download Google Form |
| **Data cleaning** | Proses merapikan data | Hapus duplikat, perbaiki format |
| **Variabel** | Kolom data yang diukur | Kelas, jumlah buku/bulan |
| **Responden** | Orang yang mengisi survei | Siswa, guru, warga sekitar |
| **Outlier** | Data yang jauh menyimpang | Jawaban "999" pada skala 1–5 |

> 💡 **Ingat:** Sampah masuk, sampah keluar (*garbage in, garbage out*). Kualitas analisis tidak akan lebih baik dari kualitas datanya.

---

## C. Workshop 1: Pengumpulan Data

### C.1 Memilih Sumber Data

| Sumber | Kelebihan | Kekurangan | Cocok Untuk |
|---|---|---|---|
| Survei Google Form | Cepat, banyak responden | Jawaban bisa asal-asalan | Opini, minat, kebiasaan |
| Observasi langsung | Data akurat, terukur | Butuh waktu | Jumlah, frekuensi |
| Wawancara | Data mendalam | Responden sedikit | Kualitatif |
| Data sekunder (BPS, artikel) | Gratis, kredibel | Tidak spesifik | Data pendukung |

### C.2 Langkah Penyebaran Survei
1. Pastikan Google Form sudah diuji coba dan linknya berfungsi.
2. Buka tab *Send* → salin link atau kode QR.
3. Sebarkan ke target responden:
   - Grup kelas via WhatsApp.
   - Posting di story Instagram.
   - Minta guru membagikan ke kelas lain.
4. Target minimal **30 responden** dalam satu minggu.
5. Pantau jumlah responden di tab *Responses*.

### C.3 Etika Mengumpulkan Data
- Informasikan tujuan survei di deskripsi form.
- Jangan memaksa; jawaban bersifat sukarela.
- Jaga privasi: nama boleh dibuat opsional/anonim.
- Gunakan data hanya untuk keperluan proyek.

---

## D. Ekspor Data Google Form ke Excel

1. Buka Google Form → tab **Responses**.
2. Klik ikon **Google Sheets** (hijau) → *Create new spreadsheet*.
3. Data responden otomatis masuk ke Sheet.
4. Unduh sebagai Excel: **File → Download → Microsoft Excel (.xlsx)**.

> 💡 **Tips:** Simpan salinan asli sebagai sheet "Data_Mentah" agar data awal tetap ada sebagai arsip.

---

## E. Data Cleaning di Excel

### E.1 Masalah Umum pada Data Survei

| Masalah | Contoh | Cara Mengatasi |
|---|---|---|
| Kolom tidak berguna | Timestamp, email, nama | Hapus kolom (atau ganti nama dengan ID) |
| Jawaban kosong | Baris tanpa isi | Filter → cek → hapus jika perlu |
| Jawaban tidak valid | Nama "asdfgh" | Hapus baris |
| Format tidak konsisten | "XI-A", "11 A", "11A" | Standarkan satu format |
| Duplikat responden | Isi identik berulang | Conditional Formatting → Duplicates |

### E.2 Langkah Cleaning
1. Buat salinan sheet: "Data_Mentah" (asli) dan "Data_Bersih" (hasil edit).
2. Hapus kolom timestamp, email, nama (jika tidak dibutuhkan).
3. Pastikan header singkat dan jelas: "Kelas", "Buku/bulan", "Genre".
4. Perbaiki format tidak konsisten (mis. gunakan *Find & Replace*).
5. Gunakan **Conditional Formatting → Highlight Cells Rules → Duplicate Values** untuk mendeteksi duplikat.
6. Sort data (Data → Sort) untuk melihat anomali seperti outlier.

### E.3 Menyusun Data Siap Analisis (Tidy Data)

| ID | Kelas | Genre | Buku/bulan | Waktu_baca (jam) | Alasan_baca |
|---|---|---|---|---|---|
| 1 | XI-A | Fiksi | 3 | 2 | Hiburan |
| 2 | XI-B | Nonfiksi | 1 | 0,5 | Tugas |

**Aturan penting data rapi (tidy data):**
- 1 baris = 1 responden.
- 1 kolom = 1 variabel.
- Tidak ada merged cells.
- Tipe data konsisten (angka dibaca sebagai angka).
- Gunakan **Format as Table (Ctrl+T)** agar range otomatis terpilih di Pivot.

---

## F. Contoh Soal & Penyelesaian 📝

**Soal 1:** Sebutkan 3 jenis masalah umum pada data survei Google Form dan solusinya.
**Pembahasan:** (1) Kolom tidak berguna (timestamp/nama) → hapus atau ganti ID; (2) jawaban tidak valid ("asdfgh") → hapus baris; (3) format tidak konsisten ("XI-A" vs "11A") → standarkan format dengan Find & Replace.

**Soal 2:** Mengapa data survei perlu disimpan dalam dua sheet: "Data_Mentah" dan "Data_Bersih"?
**Pembahasan:** Sheet "Data_Mentah" menyimpan data asli sebagai arsip dan bukti audit, sedangkan "Data_Bersih" digunakan untuk analisis. Jika terjadi kesalahan saat cleaning, kelompok bisa kembali ke data mentah tanpa harus mengulang survei.

**Soal 3:** Tuliskan aturan "tidy data" yang harus dipatuhi agar Pivot Table bekerja dengan benar.
**Pembahasan:** (1) 1 baris = 1 responden; (2) 1 kolom = 1 variabel; (3) tidak ada merged cells; (4) tipe data konsisten; (5) gunakan Format as Table agar range otomatis terdeteksi.

---

## G. Kesalahan Umum dalam Pengumpulan Data 🚫

| Kesalahan | Akibat | Solusi |
|---|---|---|
| Langsung menganalisis data mentah | Hasil aneh/tidak valid | Lakukan data cleaning dulu |
| Responden kurang dari 30 | Data tidak representatif | Sebar ke lebih banyak grup |
| Menghapus data mentah asli | Tidak ada bukti audit | Simpan sheet "Data_Mentah" |
| Mengisi form tanpa uji coba | Pertanyaan ambigu | Uji coba ke 2–3 orang dulu |
| Kolom nama dipaksakan | Melanggar privasi, responden ragu | Buat opsional/anonim |

---

## H. Tantangan Praktik (Mengaplikasi) 🎯

**Milestone Minggu 3 (Pengumpulan Data):**
- [ ] **Tingkat 1 (Dasar):** Finalisasi Google Form dan sebar ke minimal 30 responden; pantau di tab Responses.
- [ ] **Tingkat 2 (Menengah):** Ekspor data ke Excel; buat sheet "Data_Mentah" dan "Data_Bersih".
- [ ] **Tingkat 3 (Mahir):** Selesaikan data cleaning penuh (hapus kolom tak perlu, perbaiki format, hapus duplikat/outlier) sehingga data siap dianalisis di Pertemuan 4.

---

## I. Rangkuman Kunci 🔑

1. Kualitas analisis ditentukan oleh kualitas data: **garbage in, garbage out**.
2. Sumber data: survei, observasi, wawancara, dan data sekunder.
3. Target responden minimal 30 dan harus dikumpulkan secara etis.
4. Data diekspor dari Google Form melalui tab Responses → Google Sheets.
5. **Data cleaning** meliputi: hapus kolom tak berguna, perbaiki format, hapus duplikat/outlier.
6. Data rapi (tidy): 1 baris = 1 responden, 1 kolom = 1 variabel, tanpa merged cells.

---

## J. Glosarium 📖

| Istilah | Arti |
|---|---|
| **Raw data** | Data mentah yang baru keluar dari survei |
| **Data cleaning** | Proses merapikan dan memvalidasi data |
| **Responden** | Orang yang mengisi instrumen survei |
| **Tidy data** | Data dengan struktur rapi: 1 baris = 1 observasi |
| **Outlier** | Data yang menyimpang jauh dari mayoritas |
| **Likert** | Skala sikap, mis. 1–5 dari Sangat Tidak Setuju s.d. Sangat Setuju |

---

## K. Refleksi (Merefleksi) 🔍

- Masalah data apa yang paling sering kamu temukan saat cleaning dan bagaimana mengatasinya?
- Apakah jumlah responden kelompokmu sudah cukup dan data sudah bersih?
- Mengapa etika (privasi, kejujuran) penting dalam pengumpulan data?
- **Skala pemahaman diri:** ____/10
- Apa satu perbaikan yang akan kamu lakukan jika survei harus diulang?

---

**MGMP Informatika SMAN 6 Cimahi — Fase F (Kelas XII) Semester 2**