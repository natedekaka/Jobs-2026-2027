# BAHAN AJAR – PERTEMUAN 3 (S1)
## Fungsi Statistik & Logika
*Mengacu pada Panduan Mapel 2025; INFORMATIKA Fase D-F — pendekatan Pembelajaran Mendalam (Memahami → Mengaplikasi → Merefleksi)*

| Informasi | Keterangan |
|---|---|
| **Fase / Kelas** | F / Kelas XII |
| **Alokasi Waktu** | 5 JP × 45 menit (225 menit) |
| **Elemen CP** | Analisis Data (AD) |
| **Tujuan Pembelajaran** | Menggunakan fungsi statistik bersyarat (COUNTIF, SUMIF, AVERAGEIF dan versi IFS), serta logika AND/OR/NOT dan IFERROR untuk analisis data |
| **Materi Prasyarat** | Fungsi dasar Excel (SUM, AVERAGE, IF, VLOOKUP) dan Pivot Table |

---

## A. Kisah Pemantik 🎬

> **"Beasiswa yang Harus Tepat Sasaran"**
>
> Sekolah ingin memilih calon penerima beasiswa. Syaratnya rumit: siswa kelas XII-A yang nilainya **di atas 80** dan **tidak pernah absen** pada semester lalu. Tata usaha mengeluarkan daftar 300 siswa. Menghitung satu per satu akan memakan waktu berhari-hari — dan satu kesalahan bisa membuat siswa yang layak tidak terpilih. Staf TU pun bertanya, *"Apakah ada rumus Excel yang bisa menghitung dengan banyak syarat sekaligus?"*
>
> **Pertanyaan pemantik:** Bagaimana komputer "membaca" sebuah syarat seperti *kelas = XII-A* *dan* *nilai ≥ 80*? Apa perbedaan logika **AND** dan **OR** dalam menentukan siapa yang lulus seleksi?

---

## B. Konsep Dasar: Menghitung dengan Syarat

Fungsi-fungsi ini menghitung, menjumlahkan, atau merata-rata data **yang memenuhi kriteria tertentu** — bukan seluruh data.

| Istilah | Arti | Contoh |
|---|---|---|
| **Kriteria** | Syarat yang harus dipenuhi | `"XI-A"`, `">=75"`, `"L"` |
| **Range** | Area sel yang diperiksa | `A2:A50` |
| **Sum_range** | Area yang dijumlahkan | `F2:F50` |
| **Wildcard** | Karakter `*` dan `?` untuk pola | `"*IT*"` |
| **IFS (banyak syarat)** | Keluarga fungsi dengan 2+ kriteria | `COUNTIFS`, `SUMIFS` |

> 💡 **Ingat perbedaan penting:** Pada fungsi **IF** (1 syarat), range kriteria ditulis **dulu baru sum_range** (`SUMIF(range, kriteria, sum_range)`). Pada fungsi **IFS** (banyak syarat), **sum_range ditulis paling depan** (`SUMIFS(sum_range, range1, krit1, ...)`).

---

## C. Fungsi dengan Satu Kriteria

**COUNTIF — menghitung sel yang memenuhi kriteria**
```
=COUNTIF(range, kriteria)
=COUNTIF(B2:B50,"Lulus")     → berapa sel berisi "Lulus"
=COUNTIF(C2:C50,">=75")      → berapa nilai ≥ 75
=COUNTIF(E2:E50,"*IT*")      → berapa sel mengandung kata "IT"
```

**SUMIF — menjumlahkan nilai yang memenuhi kriteria**
```
=SUMIF(range_kriteria, kriteria, range_sum)
=SUMIF(A2:A50,"XI-A",B2:B50)        → total nilai kelas XI-A
=SUMIF(E2:E50,"Kopi",F2:F50)        → total penjualan produk Kopi
```

**AVERAGEIF — rata-rata nilai yang memenuhi kriteria**
```
=AVERAGEIF(range_kriteria, kriteria, range_rata)
=AVERAGEIF(B2:B50,"Lulus",C2:C50)  → rata-rata nilai siswa yang lulus
=AVERAGEIF(A2:A50,"XI-A",B2:B50)   → rata-rata nilai kelas XI-A
```

---

## D. Fungsi dengan Banyak Kriteria (Versi IFS)

**COUNTIFS — menghitung dengan banyak syarat**
```
=COUNTIFS(range1, krit1, range2, krit2, ...)
=COUNTIFS(A2:A50,"XI-A",B2:B50,"L")      → siswa XI-A laki-laki
=COUNTIFS(C2:C50,">=70",D2:D50,"<=100")  → nilai 70–100
```

**SUMIFS — menjumlahkan dengan banyak syarat**
```
=SUMIFS(sum_range, range_krit1, krit1, range_krit2, krit2, ...)
=SUMIFS(D2:D50,A2:A50,"XI-A",B2:B50,"L")     → total nilai XI-A laki-laki
=SUMIFS(F2:F50,E2:E50,"Kopi",C2:C50,">=2024") → penjualan Kopi sejak 2024
```

**AVERAGEIFS — rata-rata dengan banyak syarat**
```
=AVERAGEIFS(rata_range, range_krit1, krit1, range_krit2, krit2, ...)
=AVERAGEIFS(D2:D50,A2:A50,"XI-A",B2:B50,"L") → rata-rata nilai XI-A laki-laki
=AVERAGEIFS(F2:F50,G2:G50,">=2024",H2:H50,"Barat") → rata penjualan 2024 wilayah Barat
```

| Fungsi | Urutan Argumen | Cocok Untuk |
|---|---|---|
| SUMIF | range, kriteria, sum_range | 1 kriteria |
| SUMIFS | sum_range, range1, krit1, ... | 2+ kriteria |
| COUNTIF | range, kriteria | 1 kriteria |
| COUNTIFS | range1, krit1, range2, krit2, ... | 2+ kriteria |
| AVERAGEIF | range, kriteria, avg_range | 1 kriteria |
| AVERAGEIFS | avg_range, range1, krit1, ... | 2+ kriteria |

---

## E. Logika AND, OR, NOT dan IFERROR

### E.1 AND — semua syarat harus terpenuhi
```
=IF(AND(C2>=70, D2>=75), "LULUS", "TIDAK LULUS")
```
Nilai LULUS hanya jika **kedua** syarat benar (nilai ≥ 70 **dan** absen ≥ 80).

### E.2 OR — minimal satu syarat terpenuhi
```
=IF(OR(hari="Sabtu", hari="Minggu"), "Libur", "Masuk")
```
Hasil "Libur" jika **salah satu** kondisi benar.

### E.3 NOT — kebalikan dari suatu kondisi
```
=IF(NOT(C2="Tidak Lulus"), "Naik Kelas", "Tinggal Kelas")
```

### E.4 Kombinasi AND + OR
```
=IF(AND(OR(C2>=70,D2>=75), E2="Aktif"), "Lulus", "Tidak Lulus")
```
Berguna untuk keputusan dengan banyak kondisi yang kompleks.

### E.5 IFERROR — menangani error
```
=IFERROR(nilai, nilai_jika_error)
=IFERROR(VLOOKUP(A2,tabel,2,FALSE),"Data tidak ditemukan")
=IFERROR(A2/B2, 0)   → menghindari #DIV/0! jika B2 = 0
```
IFERROR menangkap **semua** jenis error (`#N/A`, `#DIV/0!`, `#VALUE!`, `#REF!`, `#NAME?`). Jika hanya ingin menangani `#N/A` (misal dari VLOOKUP), gunakan **IFNA** yang lebih spesifik.

---

## F. Contoh Soal & Penyelesaian 📝

**Contoh 1:** Tuliskan rumus menghitung jumlah siswa kelas "XI-A" pada kolom A2:A50!
**Jawaban:** `=COUNTIF(A2:A50,"XI-A")`

**Contoh 2:** Tuliskan rumus total penjualan produk "Kopi" (produk di kolom E, total di kolom F, 50 baris)!
**Jawaban:** `=SUMIF(E2:E50,"Kopi",F2:F50)`

**Contoh 3:** Tuliskan rumus rata-rata nilai siswa XI-A laki-laki (kelas di kolom A, gender di kolom B, nilai di kolom C)!
**Jawaban:** `=AVERAGEIFS(C2:C50,A2:A50,"XI-A",B2:B50,"L")`

**Contoh 4:** Buat formula: siswa LULUS jika nilai ≥70 **dan** absen ≥80, selain itu TIDAK LULUS!
**Jawaban:** `=IF(AND(C2>=70,D2>=80),"LULUS","TIDAK LULUS")`

**Contoh 5:** Bagaimana menghindari tampilan `#N/A` saat VLOOKUP tidak menemukan data?
**Jawaban:** Gunakan `=IFERROR(VLOOKUP(A2,tabel,2,FALSE),"Data tidak ditemukan")` atau `=IFNA(...)` untuk error `#N/A` saja.

**Contoh 6:** Apa perbedaan urutan argumen SUMIF dan SUMIFS?
**Jawaban:** SUMIF: `(range, kriteria, sum_range)`; SUMIFS: `(sum_range, range1, krit1, ...)`. Pada SUMIFS, **range yang dijumlahkan ditulis paling awal**.

---

## G. Miskonsepsi yang Sering Terjadi 🚫

| Miskonsepsi | Fakta yang Benar |
|---|---|
| "SUMIF dan SUMIFS urutan argumennya sama" | Urutan **berbeda**; pada SUMIFS sum_range ditulis paling depan |
| "Kriteria harus selalu berupa teks" | Kriteria bisa angka, teks, atau ekspresi seperti `">=75"` |
| "COUNTIF menghitung sel berisi 0" | Ya, 0 dihitung; sel kosong tidak |
| "AND dan OR memiliki hasil yang sama" | **AND** butuh semua syarat benar; **OR** cukup satu syarat benar |
| "IFERROR hanya untuk #N/A" | IFERROR menangkap **semua** error; gunakan IFNA bila hanya untuk #N/A |

---

## H. Tantangan Praktik (Mengaplikasi) 🎯

**Tantangan 1 — Satu Kriteria (30 menit):** Buat data 30 siswa (Kelas, Gender, Nilai, Absen, Status). Gunakan COUNTIF, SUMIF, dan AVERAGEIF untuk masing-masing satu kriteria.

**Tantangan 2 — Banyak Kriteria (45 menit):** Gunakan COUNTIFS, SUMIFS, dan AVERAGEIFS untuk: (a) siswa XI-A yang Lulus, (b) total nilai XI-A perempuan, (c) rata-rata nilai siswa lulus dengan absen ≥ 80.

**Tantangan 3 — Logika (45 menit):** Buat kolom Keputusan dengan IF+AND (nilai ≥70 DAN absen ≥80 = Lulus) dan kolom Alternatif dengan IF+OR (nilai ≥70 ATAU absen ≥85).

**Tantangan 4 — Antisipasi Error (40 menit):** Buat VLOOKUP dari tabel lain dan bungkus dengan IFERROR. Hitung rata-rata dengan AVERAGEIFS dan tangani hasil kosong agar tampil 0.

---

## I. Rangkuman Kunci 🔑

1. **COUNTIF/SUMIF/AVERAGEIF** bekerja untuk **satu kriteria**.
2. **COUNTIFS/SUMIFS/AVERAGEIFS** bekerja untuk **banyak kriteria** — ingat urutan argumen yang berbeda.
3. **AND** = semua syarat benar; **OR** = minimal satu syarat benar; **NOT** = kebalikan.
4. **IFERROR** mengganti pesan error dengan teks pilihan; **IFNA** khusus `#N/A`.
5. Kriteria bisa berupa teks, angka, atau ekspresi perbandingan (`">=75"`, `"*IT*"`).
6. Fungsi bersyarat ini adalah kunci analisis data dengan syarat ganda di dunia kerja.

---

## J. Glosarium 📖

| Istilah | Arti |
|---|---|
| **Kriteria** | Syarat yang harus dipenuhi oleh data agar dihitung |
| **Wildcard** | Karakter `*`/`?` untuk mencocokkan pola teks |
| **COUNTIF(S)** | Menghitung sel yang memenuhi satu/banyak kriteria |
| **SUMIF(S)** | Menjumlahkan nilai yang memenuhi satu/banyak kriteria |
| **AVERAGEIF(S)** | Merata-rata nilai yang memenuhi satu/banyak kriteria |
| **AND / OR / NOT** | Operator logika untuk menggabungkan kondisi |
| **IFERROR / IFNA** | Fungsi penangan error |

---

## K. Refleksi (Merefleksi) 🔍

- Dalam situasi nyata apa kamu membutuhkan fungsi bersyarat, bukan sekadar SUM biasa?
- Apa yang membedakan logika AND dan OR dalam pengambilan keputusan sehari-hari?
- Kesulitan apa yang paling sering kamu temui saat menulis fungsi bersyarat?
- **Skala pemahaman diri:** ____/10
- Data apa di sekitarmu yang bisa dianalisis dengan fungsi ini?

---

**MGMP Informatika SMAN 6 Cimahi — Fase F (Kelas XII) Semester 1**