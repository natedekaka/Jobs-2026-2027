# BAHAN AJAR – PERTEMUAN 1 (S1)
## Review Excel
*Mengacu pada Panduan Mapel 2025; INFORMATIKA Fase D-F — pendekatan Pembelajaran Mendalam (Memahami → Mengaplikasi → Merefleksi)*



### 🧠 Memahami — Membangun Pemahaman Awal

## A. Tujuan Pembelajaran
Setelah mempelajari materi ini, siswa mampu:
1. Menjelaskan fungsi dasar Excel (SUM, AVERAGE, MAX, MIN, COUNT, COUNTA, IF, VLOOKUP)
2. Menerapkan fungsi-fungsi tersebut dalam studi kasus data nilai
3. Membuat format tabel profesional (Table, Freeze Panes, Wrap Text, Number Format)

## B. Review: Mengapa Excel Penting?
Microsoft Excel adalah tools pengolah data paling banyak digunakan di dunia — dari administrasi sekolah, UMKM, hingga perusahaan multinasional. Di K12, kita akan memperdalam kompetensi Excel yang sudah dipelajari di K11.

## C. Daftar Fungsi Dasar Excel
**Fungsi Aritmatika (SUM, AVERAGE, MAX, MIN, COUNT, COUNTA)**
Fungsi aritmatika digunakan untuk perhitungan dasar:
- SUM(range): menjumlahkan angka dalam range
  - Contoh: =SUM(A1:A10) akan menjumlahkan A1 sampai A10
  - Catatan: cell kosong atau teks diabaikan, bukan dianggap 0
- AVERAGE(range): menghitung rata-rata
  - =AVERAGE(B2:B20) → jumlah semua angka dibagi jumlah cell berisi angka
  - Hati-hati: cell kosong TIDAK dihitung, tapi cell berisi 0 TETAP dihitung
- MAX(range): nilai tertinggi dalam range
  - =MAX(C1:C50) → mengembalikan angka terbesar
  - Bisa juga untuk teks (urutan alfabet), tapi jarang digunakan
- MIN(range): nilai terendah dalam range
  - =MIN(C1:C50) → mengembalikan angka terkecil
- COUNT(range): menghitung jumlah cell berisi angka
  - =COUNT(D2:D100) → hasilnya integer
  - Tidak menghitung cell teks atau kosong
- COUNTA(range): menghitung semua cell yang tidak kosong
  - =COUNTA(A1:A100) → menghitung berapa baris data yang terisi

**Fungsi Logika (IF)**
=IF(logika, nilai_benar, nilai_salah)
- Logika: perbandingan (>, <, >=, <=, =, <>)
- Contoh: =IF(D2>=70,"LULUS","TIDAK LULUS")
- IF bertingkat: =IF(D2>=85,"A",IF(D2>=70,"B",IF(D2>=55,"C","D")))
  - Maksimal 64 IF bertingkat di Excel
  - Alternatif: gunakan IFS (Excel 2019+)

**Fungsi Pencarian (VLOOKUP)**
=VLOOKUP(nilai_cari, tabel, kolom_ke, FALSE)
- FALSE = exact match, TRUE = approximate match
- Contoh: =VLOOKUP("ADI", A2:B20, 2, FALSE)
- Syarat: data yang dicari harus di kolom PERTAMA tabel
- Jika tidak ditemukan: #N/A — gunakan IFERROR untuk menanganinya
- Alternatif: INDEX+MATCH atau XLOOKUP (Excel 2021+)

## D. Studi Kasus — Data Nilai Siswa
Buat tabel berikut di Excel:
| No | Nama | Nilai | Huruf Mutu | Status |
Keterangan:
1. Huruf Mutu: =IF(C2>=85,"A",IF(C2>=70,"B",IF(C2>=55,"C","D")))
   - 85-100 = A (Sangat Baik)
   - 70-84 = B (Baik)
   - 55-69 = C (Cukup)
   - 0-54 = D (Kurang)
2. Status: =IF(C2>=70,"LULUS","TIDAK LULUS") — KKM 70
3. Rata-rata kelas: =AVERAGE(C2:C16)
4. Jumlah lulus: =COUNTIF(E2:E16,"LULUS")
5. Jumlah tidak lulus: =COUNTIF(E2:E16,"TIDAK LULUS")
6. Nilai tertinggi: =MAX(C2:C16)
7. Nilai terendah: =MIN(C2:C16)
8. Jumlah siswa: =COUNTA(A2:A16)

## E. Format Tabel Profesional
Langkah-langkah membuat tabel rapi:
1. Select range → Ctrl+T (atau Insert → Table)
   - Otomatis: header bold, filter dropdown, alternating row colors
   - Bisa ganti style di Table Design tab
2. Number Format: Home → Number
   - General: default
   - Number: desimal (2 angka)
   - Currency: Rp
   - Percentage: %
   - Date: DD/MM/YYYY
3. Freeze Panes: View → Freeze Panes
   - Freeze Top Row: baris header tetap terlihat saat scroll
   - Freeze First Column: kolom pertama tetap terlihat
   - Freeze Panes: baris dan kolom tertentu tetap
4. Wrap Text: Home → Wrap Text
   - Berguna untuk teks panjang dalam cell sempit
5. Merge & Center: untuk judul tabel
   - Hati-hati: jangan merge pada area data — akan mengganggu formula

## F. Tantangan (Challenge)
1. Buat tabel 15 siswa dengan 2 kelas berbeda
2. Tambahkan kolom: predikat (A/B/C/D), status, ranking
3. Selisih nilai tertinggi dan terendah: =MAX(range)-MIN(range)
4. Jumlah siswa per predikat: =COUNTIF(range,"A")
5. Rata-rata per kelas: =AVERAGEIF(kelas_range,"XI-A",nilai_range)

## G. Refleksi
Mengapa format tabel yang rapi penting? Bagaimana presentasi data yang baik mempengaruhi pembaca?


### 🔧 Mengaplikasi — Praktik & Penerapan

### Latihan Pemahaman
1. Jelaskan konsep utama yang telah dipelajari dengan bahasamu sendiri!
2. Berikan 2 contoh penerapan dalam kehidupan sehari-hari!
3. Diskusikan dengan teman: bagaimana materi ini dapat membantu menyelesaikan masalah nyata?

### 🔍 Merefleksi — Refleksi & Evaluasi

- Apa konsep paling penting yang kamu pelajari hari ini?
- Bagaimana konsep ini terkait dengan materi sebelumnya?
- Skala pemahaman diri: ___/10
- Apa yang ingin kamu pelajari lebih lanjut?

---
**MGMP Informatika SMAN 6 Cimahi — Fase F (Kelas XII) S1 Pert 1**
