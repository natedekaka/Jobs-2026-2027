# BAHAN AJAR – PERTEMUAN 3 (S1)
## Fungsi Statistik & Logika
*Mengacu pada Panduan Mapel 2025; INFORMATIKA Fase D-F — pendekatan Pembelajaran Mendalam (Memahami → Mengaplikasi → Merefleksi)*



### 🧠 Memahami — Membangun Pemahaman Awal

## A. Tujuan Pembelajaran
Setelah mempelajari materi ini, siswa mampu:
1. Menggunakan fungsi AVERAGEIF, COUNTIF, SUMIF (1 kriteria)
2. Menggunakan fungsi AVERAGEIFS, COUNTIFS, SUMIFS (banyak kriteria)
3. Menerapkan logika AND/OR dalam IF
4. Menggunakan IFERROR untuk menangani error

## B. Fungsi dengan 1 Kriteria (IF version)
**COUNTIF — menghitung jumlah cell yang memenuhi kriteria**
Sintaks: =COUNTIF(range, kriteria)
- =COUNTIF(B2:B50,"Lulus") → hitung berapa "Lulus"
- =COUNTIF(C2:C50,">=75") → hitung nilai >=75
- =COUNTIF(D2:D50,"XI-A") → hitung siswa kelas XI-A
- =COUNTIF(E2:E50,"*IT*") → hitung sel berisi kata "IT" (wildcard)

**SUMIF — menjumlahkan nilai yang memenuhi kriteria**
Sintaks: =SUMIF(range_kriteria, kriteria, range_sum)
- =SUMIF(A2:A50,"XI-A",B2:B50) → total nilai XI-A
- =SUMIF(C2:C50,">=75",D2:D50) → total penjualan untuk qty>=75
- =SUMIF(E2:E50,"Kopi",F2:F50) → total penjualan Kopi

**AVERAGEIF — rata-rata yang memenuhi kriteria**
Sintaks: =AVERAGEIF(range, kriteria)
- =AVERAGEIF(B2:B50,"Lulus",C2:C50) → rata nilai yang lulus
- =AVERAGEIF(A2:A50,"XI-A",B2:B50) → rata-rata kelas XI-A
- =AVERAGEIF(C2:C50,">=70",D2:D50) → rata nilai siswa >=70

## C. Fungsi dengan Banyak Kriteria (IFS version)
**COUNTIFS — menghitung dengan banyak syarat sekaligus**
Sintaks: =COUNTIFS(range1, krit1, range2, krit2, ...)
- =COUNTIFS(A2:A50,"XI-A",B2:B50,"L") → siswa XI-A laki-laki
- =COUNTIFS(C2:C50,">=70",D2:D50,"<=100") → nilai 70-100
- =COUNTIFS(E2:E50,"Produk A",F2:F50,">10") → transaksi Produk A qty>10

**SUMIFS — menjumlahkan dengan banyak syarat**
Sintaks: =SUMIFS(sum_range, krit_range1, krit1, krit_range2, krit2)
- =SUMIFS(D2:D50,A2:A50,"XI-A",B2:B50,"L") → total nilai XI-A laki-laki
- =SUMIFS(F2:F50,E2:E50,"Kopi",C2:C50,">=2024") → penjualan kopi tahun 2024+
- =SUMIFS(F2:F50,E2:E50,"Kopi",G2:G50,">100000") → penjualan kopi >100rb

**AVERAGEIFS — rata-rata dengan banyak syarat**
Sintaks: =AVERAGEIFS(avg_range, krit_range1, krit1, krit_range2, krit2)
- =AVERAGEIFS(D2:D50,A2:A50,"XI-A",B2:B50,"L") → rata-rata nilai XI-A laki-laki
- =AVERAGEIFS(C2:C50,D2:D50,">=70",E2:E50,"Lulus") → rata nilai lulus >=70
- =AVERAGEIFS(F2:F50,G2:G50,">=2024",H2:H50,"Barat") → rata penjualan 2024 wilayah Barat

**Perbedaan penting:**
| Fungsi | Urutan Argumen | Cocok Untuk |
|--------|---------------|-------------|
| SUMIF | range_kriteria, kriteria, sum_range | 1 kriteria |
| SUMIFS | sum_range, range_kriteria1, krit1, ... | 2+ kriteria |
| COUNTIF | range, kriteria | 1 kriteria |
| COUNTIFS | range1, krit1, range2, krit2, ... | 2+ kriteria |
| AVERAGEIF | range, kriteria, avg_range | 1 kriteria |
| AVERAGEIFS | avg_range, range_kriteria1, krit1, ... | 2+ kriteria |

## D. Logika AND, OR, dan NOT dalam IF
**AND — semua syarat harus terpenuhi:**
=IF(AND(C2>=70,D2>=75),"LULUS","TIDAK LULUS")
- Contoh: =IF(AND(nilai>=70,absen>=80),"Lulus","Tidak Lulus")
- Bisa 2+ syarat: AND(syarat1, syarat2, syarat3, ...)

**OR — minimal 1 syarat terpenuhi:**
=IF(OR(C2>=70,D2>=75),"LULUS","TIDAK LULUS")
- Contoh: =IF(OR(hari="Sabtu",hari="Minggu"),"Libur","Masuk")
- Berguna untuk: kategorisasi fleksibel

**NOT — kebalikan:**
=IF(NOT(C2="Tidak Lulus"),"Naik Kelas","Tinggal Kelas")
- =IF(NOT(ISBLANK(A2)), A2, "") → jika tidak kosong, tampilkan isi

**Kombinasi AND+OR:**
=IF(AND(OR(C2>=70,D2>=75),E2="Aktif"),"Lulus","Tidak Lulus")
- Berguna untuk kasus kompleks dengan banyak kondisi

## E. IFERROR — Menangani Error
Berfungsi untuk mengganti pesan error (#N/A, #DIV/0!, #VALUE!, #REF!, #NAME?) dengan teks kustom.
Sintaks: =IFERROR(nilai, nilai_jika_error)

Contoh umum:
- =IFERROR(VLOOKUP(A2,tabel,2,FALSE),"Data tidak ditemukan")
- =IFERROR(A2/B2,0) → jika B2=0, hasil 0 bukan #DIV/0!
- =IFERROR(1/0,"Tidak bisa dibagi nol")
- =IFERROR(AVERAGEIFS(...),0) → jika tidak ada data, hasil 0

**Penting:** IFERROR menangkap SEMUA jenis error — gunakan spesifik bila perlu (IFNA untuk #N/A saja).

## F. Studi Kasus — Analisis Data Sekolah
Buat tabel 30 baris: | Kelas | Gender | Nilai | Absen | Status |
Latihan:
1. Hitung siswa XI-A yang lulus: =COUNTIFS(A:A,"XI-A",E:E,"Lulus")
2. Rata-rata nilai XI-A Laki-laki: =AVERAGEIFS(C:C,A:A,"XI-A",B:B,"L")
3. Total nilai yang >=70: =SUMIF(C:C,">=70",C:C)
4. VLOOKUP aman: =IFERROR(VLOOKUP("ADI",A:E,3,FALSE),"Tidak ketemu")

## G. Tantangan
1. (COUNTIFS) Hitung jumlah siswa perempuan di XI-B yang lulus
2. (SUMIFS) Total penjualan kategori Minuman di toko A
3. (IFERROR) Buat VLOOKUP dengan pesan error kustom
4. (IF+AND) Buat formula: jika nilai>=70 DAN absen>=80 maka 'Lulus' else 'Tidak'


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
**MGMP Informatika SMAN 6 Cimahi — Fase F (Kelas XII) S1 Pert 3**
