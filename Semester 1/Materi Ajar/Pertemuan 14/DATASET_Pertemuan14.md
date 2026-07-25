# DATASET PERTEMUAN 14 — DATA SISWA
## Konsep Kualitas Data & GIGO

File: `DATASET_Pertemuan14.csv` — gunakan untuk praktik identifikasi data bermasalah.

| Nama | Kelas | Tgl Lahir | No HP | Nilai | Alamat |
|---|---|---|---|---|---|
| Andi Pratama | X-1 | 15-03-2009 | 08123456789 | 85 | Cimahi |
| Budi Santoso | X-1 | 2009-05-20 | 08234567890 | | Cimahi |
| Cici Dewi Lestari | X-2 | 20/05/2009 | 08345678901 | 95 | |
| Andi Pratama | X-1 | 15-03-2009 | 08123456789 | 85 | Cimahi |
| Dedi Supriadi | X-3 | 01-01-1900 | 08456789 | 200 | Bandung |
| Euis | X-1 | 10-10-2009 | 08567ABCD | Tujuhpuluh | Cimahi |
| Fitri Handayani | X-2 | 30-02-2009 | 08678901234 | 80 | Cimahi |
| Gunawan | x-1 | 05-07-2009 | 08789012345 | 90 | Cimahi |
| Hesti Nurjanah | X-2 | 12-12-2009 | | 85 | 
| Indra | X-1 | 25-01-2009 | 08901234567 | 75 | Bandung |
| Joko Susilo | X-3 | 2009-03-15 | 08912345678 | 88 | Jakarta |
| Budi Santoso | X-1 | 2009-05-20 | 08234567890 | | Cimahi |
| Kurnia | X-2 | 03-03 | 08123456780 | -5 | Cimahi |
| Lilis Suryani | X-1 | 18-08-2009 | 08111111111 | AB | Cimahi |
| Budi Santoso | X-1 | 2009-05-20 | 08234567890 | | Cimahi |

---

### Panduan Masalah (untuk guru)

| Baris | Nama | Field | Masalah | Jenis | Keterangan |
|---|---|---|---|---|---|
| 1 | Andi | — | — | — | Data benar |
| 2 | Budi | Tgl Lahir | Format YYYY-MM-DD | Format | Tidak konsisten |
| 2 | Budi | Nilai | Kosong | Missing | |
| 3 | Cici | Tgl Lahir | Format DD/MM/YYYY | Format | |
| 3 | Cici | Alamat | Kosong | Missing | |
| 4 | Andi | — | Duplikat baris 1 | Duplicate | |
| 5 | Dedi | Tgl Lahir | 01-01-1900 | Invalid | Default/tidak valid |
| 5 | Dedi | No HP | Hanya 8 digit | Outlier/Format | Seharusnya 12+ digit |
| 5 | Dedi | Nilai | 200 | Outlier | Maks 100 |
| 6 | Euis | Nama | Inisial saja? | Inkonsistensi | |
| 6 | Euis | No HP | Ada huruf | Format | |
| 6 | Euis | Nilai | "Tujuhpuluh" (teks) | Format | |
| 7 | Fitri | Tgl Lahir | 30-02-2009 | Invalid | Feb maks 28 |
| 8 | Gunawan | Kelas | "x-1" (kecil) | Inkonsistensi | |
| 9 | Hesti | No HP | Kosong | Missing | |
| 9 | Hesti | Alamat | Kosong | Missing | |
| 11 | Joko | Tgl Lahir | Format YYYY-MM-DD | Format | |
| 12 | Budi | — | Duplikat baris 2 | Duplicate | |
| 13 | Kurnia | Tgl Lahir | "03-03" tanpa tahun | Missing/Format | |
| 13 | Kurnia | Nilai | -5 | Invalid/Outlier | |
| 14 | Lilis | Nilai | "AB" | Format | |
| 15 | Budi | — | Duplikat baris 2 & 12 | Duplicate | Tripel! |

**Total masalah: ~20 temuan dalam 15 baris data.**

---

**MGMP Informatika SMAN 6 Cimahi**
