# DATASET PROYEK — PERTEMUAN 15
## Validasi, Verifikasi & Data Cleansing

File: `DATASET_Proyek_15.csv` — 25 baris data kotor untuk dibersihkan.

| Nama | Kelas | Tgl Lahir | No HP | Nilai | Alamat |
|---|---|---|---|---|---|
| Andi Pratama | X-1 | 15-03-2009 | 08123456789 | 85 | Cimahi |
| Budi Santoso | X-1 | 2009-05-20 | 08234567890 | | Cimahi |
| Cici Dewi Lestari | X-2 | 20/05/2009 | 08345678901 | 95 | |
| Andi Pratama | X-1 | 15-03-2009 | 08123456789 | 85 | Cimahi |
| Dedi Supriadi | X-3 | 01-01-1900 | 08456789 | 200 | Bandung |
| Euis Julaeha | X-1 | 10-10-2009 | 08567ABCD | Tujuhpuluh | Cimahi |
| Fitri Handayani | X-22 | 30-02-2009 | 08678901234 | 80 | Cimahi |
| Gunawan Wibisono | x-1 | 05-07-2009 | 08789012345 | 90 | Cimahi |
| Hesti Nurjanah | X-2 | 12-12-2009 | | 85 | |
| Indra Lesmana | X-1 | 25-01-2009 | 08901234567 | 75 | Bandung |
| Joko Susilo | X-3 | 2009-03-15 | 08912345678 | 88 | Jakarta |
| Budi Santoso | X-1 | 2009-05-20 | 08234567890 | | Cimahi |
| Kurnia Sari | X-2 | 03-03 | 08123456780 | -5 | Cimahi |
| Lilis Suryani | X-1 | 18-08-2009 | 08111111111 | AB | Cimahi |
| Budi Santoso | X-1 | 2009-05-20 | 08234567890 | | Cimahi |
| Maman Abdurrahman | X-2 | 15-03-2009 | 08123456789 | 88 | Cimahi |
| Neni Rahmawati | X-1 | 2008-13-01 | 08223344556 | 92 | |
| Oki Setiawan | x-3 | 07-07-2009 | 08334455667 | -10 | Bandung |
| Putri Amelia | X-2 | 25-12-2009 | 08445566778 | 78 | Cimahi |
| Qiandra | X-1 | 13- | 08556677889 | | |
| Rudi Hartono | X-2 | 14-10-2009 | 0866778899 | 85 | Bandung |
| Siti Nurhaliza | X-1 | 30-04-2009 | 08778899001 | 95 | Jakarta |
| Tono Suhartono | X-3 | 22-08-2009 | 08889900112 | 55 | Cimahi |
| Budi Santoso | X-1 | 2009-05-20 | 08234567890 | | Cimahi |
| Vina Wulandari | X-2 | 2009-11-11 | 08001122334 | 82 | |

---

### Panduan Masalah (untuk guru)

| Baris | Nama | Masalah Utama | Jenis |
|---|---|---|---|
| 2 | Budi | Format tanggal YYYY-MM-DD, Nilai kosong | Format + Missing |
| 3 | Cici | Format tanggal DD/MM/YYYY, Alamat kosong | Format + Missing |
| 4 | Andi | Duplikat baris 1 | Duplicate |
| 5 | Dedi | Tgl lahir 01-01-1900 (default), No HP 8 digit, Nilai 200 | Invalid + Format + Outlier |
| 6 | Euis | No HP ada huruf, Nilai teks "Tujuhpuluh" | Format |
| 7 | Fitri | Kelas "X-22" (tidak valid), Tgl 30-02-2009 | Invalid + Invalid |
| 8 | Gunawan | Kelas "x-1" | Inkonsistensi |
| 9 | Hesti | No HP kosong, Alamat kosong | Missing |
| 11 | Joko | Format tanggal YYYY-MM-DD | Format |
| 12 | Budi | Duplikat baris 2 | Duplicate |
| 13 | Kurnia | Tgl lahir tanpa tahun "03-03", Nilai -5 | Missing + Invalid |
| 14 | Lilis | Nilai "AB" (teks) | Format |
| 15 | Budi | Duplikat baris 2 & 12 | Duplicate |
| 16 | Maman | Nama panjang, data valid | ✅ |
| 17 | Neni | Tgl "2008-13-01" (bulan 13), Alamat kosong | Invalid + Missing |
| 18 | Oki | Kelas "x-3", Nilai -10 | Inkonsistensi + Invalid |
| 20 | Qiandra | Tgl lahir "13-" (tidak lengkap), Nilai kosong | Missing |
| 21 | Rudi | No HP 10 digit (valid sih, tapi beda variasi) | — |
| 22 | Siti | Data valid | ✅ |
| 24 | Budi | Duplikat baris 2, 12, 15 | Duplicate (4×!) |
| 25 | Vina | Format tanggal YYYY-MM-DD | Format |

**Estimasi masalah: ~25+ masalah dalam 25 baris data.**

---

**MGMP Informatika SMAN 6 Cimahi**
