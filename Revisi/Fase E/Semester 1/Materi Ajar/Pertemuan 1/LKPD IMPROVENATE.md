# LEMBAR KERJA PRAKTIK (LKP)
**Mata Pelajaran:** Informatika (Fase F - Kelas XII)
**Materi:** Review Excel Dasar & Pengolahan Data
**Waktu:** 2 s.d 5  Jam Pelajaran

## Tujuan Praktik
1. Siswa mampu menginput dan memformat tabel data secara profesional.
2. Siswa mampu menerapkan fungsi aritmatika, logika (IF), dan pencarian (VLOOKUP).
3. Siswa mampu menganalisis data sederhana menggunakan fungsi statistik dasar.

---

## BAGIAN 1: PERSIAPAN DATA
**Instruksi:** 
Blok dan *Copy* data mentah di dalam kotak kode di bawah ini, lalu *Paste* di cell **A1** pada lembar kerja Excel Anda yang masih kosong.

```text
No	Nama	Nilai Ujian	Kode Kelas	Kehadiran (%)
1	Adi Pratama	88	12A	95%
2	Budi Santoso	72	12B	80%
3	Citra Kirana	55	12A	60%
4	Dedi Kurniawan	90	12B	100%
5	Eka Putri	68	12A	75%
6	Fani Anindya	75	12B	88%
7	Gilang Ramadhan	82	12A	92%
8	Hana Safitri	45	12B	50%
9	Ivan Setiawan	95	12A	98%
10	Julia Perez	70	12B	85%
11	Kevin Sanjaya	60	12A	70%
12	Lina Marlina	85	12B	90%
13	Mario Teguh	78	12A	82%
14	Nisa Aulia	50	12B	65%
15	Omar Bakri	92	12A	96%
```
*(Buat juga Tabel Referensi di cell **I1:J3** untuk kebutuhan VLOOKUP)*
```text
Kode Kelas	Nama Kelas
12A	XII IPA 1
12B	XII IPS 1
```

---

## BAGIAN 2: TUGAS FORMAT TABEL PROFESIONAL
Lakukan langkah-langkah berikut agar tabel data Anda rapi dan profesional:
1. **Format as Table:** Blok range `A1:E16`, tekan **`Ctrl + T`** (pastikan *My table has headers* tercentang). Pilih *Style* tabel yang Anda sukai pada tab *Table Design*.
2. **Freeze Panes:** Pergi ke tab **View** > **Freeze Panes** > **Freeze Top Row** (Agar header tetap terlihat saat di-scroll).
3. **Wrap Text:** Blok baris header (A1:E1), lalu klik **Wrap Text** di tab *Home* agar teks panjang terlihat utuh.
4. **Number Format:** Blok kolom `Kehadiran (%)` (E2:E16), pastikan formatnya adalah **Percentage** dengan 0 decimal.
5. **Merge & Center:** Blok `A1` sampai `E1` di *sheet* baru (atau di atas tabel), ketik "DATA NILAI SISWA KELAS XII", lalu **Merge & Center** dan **Bold**. *(Catatan: Jangan merge area data utama).*

---

## BAGIAN 3: PENERAPAN FORMULA (FUNGSI DASAR & LOGIKA)
Tambahkan 3 kolom baru di sebelah kanan tabel (Kolom F, G, H) dengan header: **Huruf Mutu**, **Status**, dan **Nama Kelas**.

**Tugas 1: Huruf Mutu (Kolom F)**
Gunakan fungsi **IF Bertingkat** untuk menentukan huruf mutu berdasarkan Nilai Ujian (Kolom C):
* 85 - 100 = "A"
* 70 - 84 = "B"
* 55 - 69 = "C"
* 0 - 54 = "D"
> *Tulis formula di F2 dan salin ke bawah (F16).*

**Tugas 2: Status Kelulusan (Kolom G)**
Gunakan fungsi **IF** untuk menentukan status kelulusan. KKM adalah 70.
* Jika Nilai >= 70, maka "LULUS"
* Jika tidak, maka "TIDAK LULUS"
> *Tulis formula di G2 dan salin ke bawah (G16).*

**Tugas 3: Pencarian Data (Kolom H)**
Gunakan fungsi **VLOOKUP** untuk memunculkan "Nama Kelas" berdasarkan "Kode Kelas" (Kolom D). Gunakan tabel referensi di `I2:J3`.

* *Tantangan Tambahan:* Bungkus VLOOKUP Anda dengan **IFERROR** agar jika kode salah/tidak ditemukan, muncul teks "Kode Salah".
> *Tulis formula di H2 dan salin ke bawah (H16).*

---

## BAGIAN 4: STATISTIK & TANTANGAN (CHALLENGE)
Di bawah tabel data Anda (misal mulai baris 18), buatlah **Laporan Rekapitulasi** dengan menggunakan fungsi aritmatika dan statistik:

1. **Rata-rata Nilai Kelas:** Hitung rata-rata dari seluruh Nilai Ujian.
2. **Nilai Tertinggi & Terendah:** Cari nilai maksimum dan minimum dari ujian.
3. **Selisih Nilai:** Hitung selisih antara nilai tertinggi dan terendah.
4. **Jumlah Siswa:** Hitung berapa banyak siswa yang datanya terisi (gunakan COUNTA pada kolom Nama).
5. **Jumlah yang Lulus:** Hitung berapa siswa yang berstatus "LULUS" (Gunakan COUNTIF).
6. **Rata-rata Per Kelas (Tantangan):** Hitung rata-rata nilai khusus untuk siswa yang berada di kelas "12A" (Gunakan AVERAGEIF).

---

## BAGIAN 5: REFLEKSI DIRI
Jawablah pertanyaan berikut di dalam sebuah *Text Box* atau di *Sheet* baru bernama "Refleksi":
1. Apa perbedaan mendasar antara fungsi `COUNT` dan `COUNTA` berdasarkan praktik yang baru saja Anda lakukan?
2. Mengapa penggunaan *Format as Table (Ctrl+T)* lebih disarankan daripada hanya memberi *border* manual pada tabel?
3. Kesalahan apa yang paling sering Anda temui saat menulis rumus `VLOOKUP` dan bagaimana cara mengatasinya?

---
---

## KUNCI JAWABAN / PANDUAN FORMULA (Untuk Guru / Evaluasi Mandiri)

**1. Huruf Mutu (Cell F2)**
```excel
=IF(C2>=85,"A",IF(C2>=70,"B",IF(C2>=55,"C","D")))
```
*(Alternatif untuk Excel 2019+ bisa menggunakan `=IFS(C2>=85,"A", C2>=70,"B", C2>=55,"C", TRUE,"D")`)*

**2. Status (Cell G2)**
```excel
=IF(C2>=70,"LULUS","TIDAK LULUS")
```

**3. Nama Kelas dengan IFERROR (Cell H2)**

```excel
=IFERROR(VLOOKUP(D2,$I$2:$J$3,2,FALSE),"Kode Salah")
```
*(Catatan: Jangan lupa gunakan `$` / Absolute Reference pada tabel referensi `I2:J3` agar tidak bergeser saat di-copy ke bawah).*

**4. Rekapitulasi Statistik (Contoh penempatan di cell B18 dst)**
* **Rata-rata Nilai:** `=AVERAGE(C2:C16)`
* **Nilai Tertinggi:** `=MAX(C2:C16)`
* **Nilai Terendah:** `=MIN(C2:C16)`
* **Selisih Nilai:** `=MAX(C2:C16)-MIN(C2:C16)`
* **Jumlah Siswa:** `=COUNTA(B2:B16)`
* **Jumlah Lulus:** `=COUNTIF(G2:G16,"LULUS")`
* **Rata-rata Kelas 12A:** `=AVERAGEIF(D2:D16,"12A",C2:C16)`

---
