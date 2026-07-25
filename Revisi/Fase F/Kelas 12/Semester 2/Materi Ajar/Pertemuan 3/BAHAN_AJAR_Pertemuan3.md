# BAHAN AJAR – PERTEMUAN 3 (S2)
## Workshop — Pengumpulan Data
*Mengacu pada Panduan Mapel 2025; INFORMATIKA Fase D-F — pendekatan Pembelajaran Mendalam (Memahami → Mengaplikasi → Merefleksi)*



### 🧠 Memahami — Membangun Pemahaman Awal

## A. Tujuan Pembelajaran
Setelah mempelajari materi ini, siswa mampu:
1. Membuat dan menyebarkan Google Form untuk pengumpulan data
2. Mengekspor data Google Form ke Excel
3. Membersihkan data mentah (data cleaning) di Excel
4. Menyusun data siap analisis

## B. Workshop 1: Pengumpulan Data

**Sumber Data yang Tersedia:**
| Sumber | Kelebihan | Kekurangan | Cocok Untuk |
|--------|-----------|------------|-------------|
| Survei Google Form | Cepat, banyak responden | Jawaban asal-asalan | Opini, minat, kebiasaan |
| Observasi langsung | Data akurat | Butuh waktu | Jumlah, frekuensi |
| Wawancara | Data mendalam | Sedikit responden | Kualitatif |
| Data sekunder (BPS, artikel) | Gratis, kredibel | Tidak spesifik | Data pendukung |

**Langkah Survei:**
1. Buka Google Form yang sudah jadi
2. Klik "Send" → dapatkan link
3. Sebarkan ke target responden:
   - Grup kelas via WA
   - Posting di story IG
   - Minta guru share ke kelas lain
4. Target: minimal 30 responden dalam 1 minggu
5. Monitor jumlah responden: Responses tab

## C. Ekspor Data ke Excel
1. Buka Google Form → Responses tab
2. Klik ikon Google Sheets (hijau) → Create new spreadsheet
3. Data akan otomatis masuk ke Sheet
4. Download sebagai Excel: File → Download → Microsoft Excel (.xlsx)

## D. Data Cleaning di Excel
Data dari Google Form biasanya perlu dibersihkan:

**Masalah Umum:**
1. **Timestamp:** tidak perlu untuk analisis → hapus kolom
2. **Nama:** bisa dihapus demi privasi → ganti dengan ID
3. **Jawaban kosong:** filter → cek → hapus baris jika perlu
4. **Jawaban tidak valid:** "asdf" sebagai nama → hapus
5. **Format waktu:** gunakan Date format → sesuaikan

**Langkah Cleaning:**
1. Buat copy data (sheet "Data_Mentah" + "Data_Bersih")
2. Hapus kolom timestamp, email, nama (jika perlu)
3. Pastikan header singkat: "Kelas", "Buku/bulan", "Genre"
4. Data Validation: batasi input
5. Conditional Formatting: Highlight Cells Rules → Duplicates
6. Sort data (Data → Sort) untuk lihat anomali

## E. Menyusun Data Siap Analisis
Setelah dibersihkan, format data:
| ID | Kelas | Genre | Buku/bulan | Waktu_baca (jam) | Alasan_baca |
|----|-------|-------|------------|------------------|-------------|
| 1 | XI-A | Fiksi | 3 | 2 | Hiburan |

**Aturan Penting:**
- 1 baris = 1 responden
- 1 kolom = 1 variabel
- Tidak ada merged cells
- Tipe data konsisten
- Gunakan Data → Format as Table (Ctrl+T)


### 🔧 Mengaplikasi — Praktik & Penerapan

## F. Tugas Pertemuan 3
1. Finalisasi Google Form
2. Sebarkan ke minimal 30 responden
3. Ekspor data ke Excel
4. Bersihkan data (sheet Data_Bersih)

**Ceklist:**
- [ ] Google Form sudah disebar
- [ ] Minimal 30 responden
- [ ] Data sudah di Excel
- [ ] Data sudah dibersihkan


### 🔍 Merefleksi — Refleksi & Evaluasi

- Apa konsep paling penting yang kamu pelajari hari ini?
- Bagaimana konsep ini terkait dengan materi sebelumnya?
- Skala pemahaman diri: ___/10
- Apa yang ingin kamu pelajari lebih lanjut?

---
**MGMP Informatika SMAN 6 Cimahi — Fase F (Kelas XII) S2 Pert 3**
