# BAHAN AJAR – PERTEMUAN 17 (S1)
## PAS - Ujian Praktik Excel
*Mengacu pada Panduan Mapel 2025; INFORMATIKA Fase D-F — pendekatan Pembelajaran Mendalam (Memahami → Mengaplikasi → Merefleksi)*



### 🧠 Memahami — Membangun Pemahaman Awal

## A. Tujuan: PAS — Ujian Praktik Excel
Ujian praktik mengukur kemampuan Excel fungsi teks dan tanggal.

## B. Format Ujian Praktik
| Sesi | Durasi | Soal | Bobot |
|------|--------|------|-------|
| Praktik | 60 menit | 3 soal | 100% |


### 🔧 Mengaplikasi — Praktik & Penerapan

## C. Soal 1: Data Siswa (40 poin)
Buat tabel 10 siswa dengan struktur berikut:
| NIS | Nama Lengkap | Kelas | Tgl Lahir | Usia | Email Sekolah |
|-----|-------------|-------|-----------|------|--------------|
| 2025001 | Andi Prasetyo | XI-A | 15/03/2008 | formula | formula |

**Kolom yang menggunakan formula:**
1. Usia: =DATEDIF(C2, TODAY(), "Y") & " tahun"
2. Email: =LOWER(LEFT(B2,1)) & "." & LOWER(MID(B2, FIND(" ",B2)+1, 99)) & "@sma6.sch.id"
   - Contoh: andi.prasetyo@sma6.sch.id
3. Kelas: =IF(MID(A2,8,1)="1","XI-A",IF(MID(A2,8,1)="2","XI-B","XI-C"))

**Kriteria:**
- Semua formula benar (20 poin)
- Format rapi, Freeze Panes (10 poin)
- Table style (10 poin)

## D. Soal 2: Validasi Data (30 poin)
Buat tabel validasi 10 baris:
| Data | Jenis | Validasi | Keterangan |
|------|-------|----------|------------|
| 2025001 | NIS | =IF(LEN(A2)=7,"Valid","Tidak Valid") | |
| andi@ | Email | =IF(ISNUMBER(FIND("@",B2)),"Valid","Tidak Valid") | |

Buat 5 jenis validasi berbeda:
1. NIS: panjang harus 7 digit
2. Email: harus mengandung "@"
3. Nama: harus huruf kapital semua
4. Tanggal: tahun harus 2008-2009
5. Nilai: range 0-100

## E. Soal 3: Laporan Otomatis (30 poin)
Buat laporan dengan fungsi tanggal:
1. Tanggal hari ini: =TODAY()
2. Nama bulan: =TEXT(TODAY(), "MMMM")
3. Tahun ini: =YEAR(TODAY())
4. Hari ini ke-: =TEXT(TODAY(), "DDDD")
5. Selisih dari 1 Januari: =DATEDIF(DATE(YEAR(TODAY()),1,1), TODAY(), "D")
6. Akhir tahun: =DATE(YEAR(TODAY()),12,31)
7. Sisa hari: =E6 - TODAY()

## F. Rubrik
| Aspek | Bobot |
|-------|-------|
| Kebenaran formula | 40% |
| Kerapian format | 30% |
| Kelengkapan | 20% |
| Efisiensi (tidak manual) | 10% |


### 🔍 Merefleksi — Refleksi & Evaluasi

- Apa konsep paling penting yang kamu pelajari hari ini?
- Bagaimana konsep ini terkait dengan materi sebelumnya?
- Skala pemahaman diri: ___/10
- Apa yang ingin kamu pelajari lebih lanjut?

---
**MGMP Informatika SMAN 6 Cimahi — Fase F (Kelas XI) S1 Pert 17**
