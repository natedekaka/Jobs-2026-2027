# BAHAN AJAR – PERTEMUAN 2 (S2)
## Rumus & Referensi
*Mengacu pada Panduan Mapel 2025; INFORMATIKA Fase D-F — pendekatan Pembelajaran Mendalam (Memahami → Mengaplikasi → Merefleksi)*

| Informasi | Keterangan |
|---|---|
| **Fase / Kelas** | E / Kelas X |
| **Alokasi Waktu** | 2 JP × 45 menit (90 menit) |
| **Elemen CP** | Analisis Data (AD) / Teknik Informatika dan Komunikasi (TIK) |
| **Tujuan Pembelajaran** | Menulis rumus dengan operator aritmatika, menggunakan fungsi dasar, serta memahami perbedaan referensi sel relatif, absolut, dan semi-absolut |
| **Materi Prasyarat** | Pengenalan Excel: sel, range, dan fungsi SUM/AVERAGE/COUNT (Pertemuan 1) |

---

## A. Kisah Pemantik 🎬

> **"Kesalahan 50 Juta karena Rumus Disalin"**
>
> Seorang kasir toko harus menghitung total harga 50 produk. Ia membuat rumus `=B2*C2` di baris pertama, lalu **menyalin** rumus itu ke 49 baris lainnya. Besok paginya, semua total menjadi Rp0! Ternyata, saat rumus disalin, referensi selnya **ikut berubah** dan menunjuk ke sel yang salah. Kasir itu baru sadar setelah belajar tentang **referensi relatif dan absolut** di Excel. 😅
>
> **Pertanyaan pemantik:** Mengapa rumus yang sama bisa memberikan hasil berbeda setelah disalin? Pernahkah kamu menyalin rumus di Excel (atau aplikasi lain) dan hasilnya tiba-tiba aneh?

---

## B. Dasar Rumus Excel 🧮

**Rumus (formula)** di Excel selalu diawali dengan tanda **`=`**. Rumus bisa berisi angka, operator, alamat sel, dan fungsi.

### B.1 Urutan Perhitungan (Prioritas Operator)
Excel menghitung mengikuti aturan matematika: **dalam kurung → pangkat → kali/bagi → tambah/kurang**.

| Contoh Rumus | Hasil | Penjelasan |
|---|---|---|
| `=5+3*2` | 11 | Perkalian dulu: 3×2=6, lalu +5 |
| `=(5+3)*2` | 16 | Kurung dulu: 5+3=8, lalu ×2 |
| `=2^3+1` | 9 | Pangkat dulu: 8, lalu +1 |
| `=10-4/2` | 8 | Bagi dulu: 4÷2=2, lalu 10−2 |

---

## C. Operator Aritmatika ✖️

| Operator | Fungsi | Contoh | Hasil |
|---|---|---|---|
| `+` | Penjumlahan | `=5+3` | 8 |
| `-` | Pengurangan | `=10-4` | 6 |
| `*` | Perkalian | `=6*7` | 42 |
| `/` | Pembagian | `=15/3` | 5 |
| `^` | Pangkat | `=2^3` | 8 |
| `%` | Persen | `=50*10%` | 5 |

> ⚠️ **Ingat:** di Excel perkalian ditulis `*`, bukan `x`; pembagian ditulis `/`, bukan `:`.

---

## D. Fungsi Dasar dan Cara Menuliskannya 📊

Fungsi adalah rumus siap pakai yang bisa langsung dipakai setelah tanda `=`.

| Fungsi | Kegunaan | Contoh | Keterangan |
|---|---|---|---|
| `=SUM(range)` | Jumlah | `=SUM(A1:A10)` | Menjumlahkan angka pada range |
| `=AVERAGE(range)` | Rata-rata | `=AVERAGE(B2:B20)` | Rata-rata angka pada range |
| `=MAX(range)` | Tertinggi | `=MAX(C1:C10)` | Nilai terbesar |
| `=MIN(range)` | Terendah | `=MIN(C1:C10)` | Nilai terkecil |
| `=COUNT(range)` | Banyak angka | `=COUNT(D2:D50)` | Hitung sel berisi angka |

### Contoh Gabungan Rumus dan Fungsi
| Nama | Nilai 1 | Nilai 2 | Total | Rata-rata |
|---|---|---|---|---|
| Andi | 80 | 90 | `=B2+C2` | `=AVERAGE(B2:C2)` |

Hasil di kolom D: `=B2+C2` = 170; kolom E: `=AVERAGE(B2:C2)` = 85.

> 💡 **Tips:** Excel menampilkan hasil langsung, tapi rumusnya bisa dilihat di **Formula Bar** atau dengan menekan **Ctrl+`**.

---

## E. Referensi Sel: Relatif, Absolut, Semi-Absolut 🔗

**Referensi sel** adalah alamat sel yang dipakai dalam rumus. Saat rumus disalin, cara referensi berperilaku menentukan hasilnya.

| Jenis | Contoh | Saat disalin ke bawah/kanan | Kegunaan |
|---|---|---|---|
| **Relatif** | `A1` | Ikut berubah mengikuti posisi baru | Perhitungan berulang per baris |
| **Absolut** | `$A$1` | Selalu tetap, tidak berubah | Angka tetap (diskon, kurs, persen) |
| **Semi-absolut (kolom tetap)** | `$A1` | Kolom tetap, baris berubah | Rumus per kolom |
| **Semi-absolut (baris tetap)** | `A$1` | Baris tetap, kolom berubah | Rumus per baris |

### Contoh Nyata: Rumus Diskon
Buat tabel:

| A (Produk) | B (Harga) | C (Harga Diskon) |
|---|---|---|
| Buku | 50.000 | `=B2*$D$1` |
| Pulpen | 10.000 | `=B3*$D$1` |

Di sel `D1` ketik **0,9** (diskon 10%, bayar 90%). Saat rumus di C2 disalin ke C3:
- `B2` (relatif) → berubah menjadi `B3` ✅
- `$D$1` (absolut) → **tetap** `$D$1` ✅ (diskon selalu diambil dari D1)

Jika `$D$1` ditulis tanpa `$` (yaitu `D1`), saat disalin ke C3 akan menjadi `D2` (kosong) → hasil salah! 💥

### Cara Membuat Referensi Absolut
Ketik `=B2*D1`, lalu tekan **F4** → otomatis berubah menjadi `=B2*$D$1`. Tekan F4 berulang untuk memilih jenis referensi.

---

## F. Contoh Soal & Penyelesaian 📝

**Contoh 1:** Berapa hasil dari `=10-2*3`? Jelaskan urutan perhitungannya.
**Pembahasan:** Perkalian dihitung lebih dulu: `2*3=6`, lalu `10-6=4`. Hasilnya **4**.

**Contoh 2:** Tuliskan rumus untuk menghitung rata-rata nilai sel B2 sampai B10 dan nilai tertingginya.
**Pembahasan:**
- Rata-rata: `=AVERAGE(B2:B10)`
- Tertinggi: `=MAX(B2:B10)`

**Contoh 3:** Tabel di bawah ini: di C2 ditulis `=B2*$D$1` dengan D1=0,5. Bila rumus disalin ke C3, apa hasilnya jika B3=8000?
**Pembahasan:** Karena `$D$1` absolut (tetap), rumus menjadi `=B3*$D$1` = `8000*0,5` = **4000**. Referensi `B2` berubah relatif menjadi `B3`, sedangkan `$D$1` tetap.

**Contoh 4:** Mengapa `=10/5+2` menghasilkan 4, bukan (10/7)?
**Pembahasan:** Pembagian dikerjakan sebelum penjumlahan: `10/5=2`, lalu `2+2=4`. Untuk hasil berbeda, gunakan kurung: `=10/(5+2)` = 1,43.

---

## G. Miskonsepsi yang Sering Terjadi 🚫

| Miskonsepsi | Fakta yang Benar |
|---|---|
| "Tanda perkalian di Excel adalah `x`" | Gunakan `*` |
| "`$` hanyalah tanda mata uang" | `$` di depan alamat sel menandakan referensi **absolut** |
| "Menyalin rumus selalu menghasilkan nilai sama" | Referensi **relatif** berubah saat disalin, hasil bisa berbeda |
| "`=A1+A2+A3` lebih baik daripada `=SUM(A1:A3)`" | Keduanya valid; `SUM` lebih ringkas dan mudah diperluas |
| "Tanpa kurung, Excel menghitung kiri ke kanan" | Excel mengikuti prioritas operator: kurung → pangkat → kali/bagi → tambah/kurang |

---

## H. Tantangan Praktik (Mengaplikasi) 🎯

**Tantangan 1 — Kalkulator Rumus:** Buat 5 rumus di Excel yang masing-masing memakai operator +, −, ×, ÷, dan pangkat. Verifikasi hasilnya dengan kalkulator.

**Tantangan 2 — Tabel Belanja:** Buat tabel 6 barang dengan kolom Nama, Harga, Qty, dan Subtotal (`=Harga*Qty`). Tambahkan baris TOTAL menggunakan SUM.

**Tantangan 3 — Rumus Diskon:** Buat tabel dengan kolom Harga dan Diskon. Letakkan besaran diskon (mis. 15%) di satu sel absolut (`$D$1`). Isi kolom Harga Setelah Diskon dengan `=Harga*$D$1`, lalu salin ke semua baris. Uji dengan mengubah nilai di `D1` — perhatikan semua baris ikut berubah.

---

## I. Rangkuman Kunci 🔑

1. Rumus selalu diawali **`=`** dan mengikuti prioritas operator (kurung → pangkat → kali/bagi → tambah/kurang).
2. Operator dasar: `+`, `-`, `*`, `/`, `^`.
3. Fungsi dasar: `SUM`, `AVERAGE`, `MAX`, `MIN`, `COUNT`.
4. Referensi **relatif** (A1) berubah saat disalin; referensi **absolut** (`$A$1`) tetap.
5. Semi-absolut `$A1` atau `A$1` mengunci salah satu komponen.
6. Gunakan **F4** untuk mengubah referensi menjadi absolut.
7. Referensi absolut sangat penting untuk angka tetap seperti diskon atau kurs.

---

## J. Glosarium 📖

| Istilah | Arti |
|---|---|
| **Rumus / Formula** | Perhitungan yang diawali tanda `=` |
| **Operator** | Simbol perhitungan (+, −, ×, ÷, ^) |
| **Fungsi** | Rumus siap pakai (SUM, AVERAGE, dll.) |
| **Referensi relatif** | Alamat sel yang berubah saat rumus disalin (A1) |
| **Referensi absolut** | Alamat sel yang tetap saat disalin (`$A$1`) |
| **Semi-absolut** | Salah satu bagian tetap ($A1 atau A$1) |
| **F4** | Tombol pintas untuk mengunci referensi sel |

---

## K. Refleksi (Merefleksi) 🔍

- Apa perbedaan paling penting antara referensi relatif dan absolut?
- Dalam kehidupan nyata, kapan kamu butuh angka yang "tidak boleh berubah" (seperti diskon atau tarif)?
- Bisakah kamu menemukan contoh rumusmu sendiri yang menghasilkan kesalahan saat disalin?
- Bagian mana yang masih membingungkan?
- **Skala pemahaman diri:** ____/10
- Apa yang ingin kamu latih lebih lanjut?

---

**MGMP Informatika SMAN 6 Cimahi — Fase E (Kelas X) Semester 2**