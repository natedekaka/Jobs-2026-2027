# BAHAN AJAR – PERTEMUAN 4 (S2)
## Grafik Dasar
*Mengacu pada Panduan Mapel 2025; INFORMATIKA Fase D-F — pendekatan Pembelajaran Mendalam (Memahami → Mengaplikasi → Merefleksi)*

| Informasi | Keterangan |
|---|---|
| **Fase / Kelas** | E / Kelas X |
| **Alokasi Waktu** | 2 JP × 45 menit (90 menit) |
| **Elemen CP** | Analisis Data (AD) / Teknik Informatika dan Komunikasi (TIK) |
| **Tujuan Pembelajaran** | Memilih jenis grafik yang tepat, membuat grafik dari data di Excel, serta memformat dan memindahkan grafik agar informatif dan menarik |
| **Materi Prasyarat** | Rumus dasar, fungsi SUM/AVERAGE, dan referensi sel (Pertemuan 1–3) |

---

## A. Kisah Pemantik 🎬

> **"Angka yang Tidak Ada yang Baca"**
>
> Tim OSIS menyusun laporan kegiatan dan menyerahkan tumpukan tabel angka kepada kepala sekolah. Kepala sekolah mengerutkan kening — datanya benar, tapi sulit dibaca sekilas. Keesokan harinya, mereka mengubah tabel itu menjadi **grafik batang** berwarna. Sekarang, hanya dengan sekali lihat, siapa pun paham kegiatan mana yang paling banyak peminatnya. Angka "bercerita" lewat grafik! 📈
>
> **Pertanyaan pemantik:** Pernahkah kamu melihat tabel panjang lalu kesulitan memahami polanya? Kapan sebuah gambar lebih cepat menjelaskan daripada seratus baris angka?

---

## B. Mengapa Data Perlu Dijadikan Grafik? 📊

**Grafik (chart)** adalah representasi visual data. Dengan grafik, pola, perbandingan, dan tren langsung terlihat tanpa membaca angka satu per satu.

| Keuntungan Grafik | Contoh |
|---|---|
| Membandingkan antar kategori | Penjualan per produk |
| Menunjukkan tren waktu | Penjualan per bulan |
| Menampilkan proporsi | Pangsa pasar tiap merek |
| Komunikasi cepat & menarik | Presentasi, laporan, rapor |

---

## C. Jenis-Jenis Grafik dan Kegunaannya 📈

| Jenis Grafik | Kegunaan | Contoh Data yang Cocok |
|---|---|---|
| **Column** (batang tegak) | Membandingkan kategori | Penjualan per produk |
| **Bar** (batang mendatar) | Perbandingan dengan label panjang | Ranking 10 besar sekolah |
| **Line** (garis) | Tren / perubahan sepanjang waktu | Penjualan per bulan |
| **Pie** (lingkaran) | Proporsi/persentase dari keseluruhan | Pangsa pasar, persentase anggaran |
| **Area** | Tren dengan penekanan volume | Kenaikan pengguna aplikasi |

### Memilih Grafik yang Tepat
| Data yang Kamu Punya | Grafik Terbaik |
|---|---|
| Nilai per kategori (tidak berurutan waktu) | Column / Bar |
| Data berurutan waktu | Line |
| Bagian dari keseluruhan (jumlahnya 100%) | Pie |
| Membandingkan banyak kategori | Bar / Column |

> ⚠️ **Hati-hati dengan Pie:** gunakan hanya jika total semua bagian = 100% dan kategori tidak terlalu banyak (maksimal ±7 bagian).

---

## D. Cara Membuat Grafik di Excel 🛠️

### Langkah-Langkah:
1. **Siapkan data** dalam bentuk tabel dengan judul kolom (header).
2. **Blok seluruh data** termasuk header (mis. `A1:C7`).
3. Klik menu **Insert** → grup **Charts**.
4. Pilih jenis grafik: Column, Line, Pie, dll.
5. Grafik muncul di worksheet, siap diformat.

### Contoh Data dan Hasilnya
| Bulan | Penjualan (Rp) |
|---|---|
| Januari | 5.000.000 |
| Februari | 7.000.000 |
| Maret | 6.500.000 |

→ Blok A1:B4 → Insert → **Line** → grafik garis menunjukkan penjualan naik di Februari, turun sedikit di Maret.

> 💡 **Tips:** Pilih **Recommended Charts** jika bingung; Excel akan menyarankan grafik yang cocok dengan data.

---

## E. Memformat Grafik agar Menarik ✨

Setelah grafik dibuat, format agar mudah dibaca:

| Elemen Grafik | Fungsi | Cara Menambah |
|---|---|---|
| **Chart Title** | Judul grafik | Klik grafik → ikon `+` → Chart Title |
| **Axis Titles** | Label sumbu X dan Y | Ikon `+` → Axis Titles |
| **Legend** | Keterangan warna/pattern | Ikon `+` → Legend |
| **Data Labels** | Menampilkan nilai di atas bar/titik | Ikon `+` → Data Labels |
| **Gridlines** | Garis bantu pembaca | Ikon `+` → Gridlines |
| **Chart Style** | Variasi warna & tampilan | Tab **Chart Design** → galeri style |
| **Quick Layout** | Tata letak siap pakai | Tab Chart Design → Quick Layout |

### Memindahkan Grafik
1. Klik grafik → tab **Chart Design** → **Move Chart**.
2. Pilih **New Sheet** untuk menampilkan grafik di sheet sendiri, atau **Object in** untuk menaruhnya di sheet yang sama.
3. Cara lain: klik dan **seret** grafik ke posisi yang diinginkan.

### Menyesuaikan Ukuran
- Klik grafik lalu tarik titik-titik sudutnya (handle).
- Ubah warna bar dengan klik dua kali pada bar → tab **Format** → **Shape Fill**.

---

## F. Contoh Soal & Penyelesaian 📝

**Contoh 1:** Data penjualan per bulan selama 6 bulan. Jenis grafik apa yang paling tepat dan mengapa?
**Pembahasan:** **Line chart**, karena datanya berurutan berdasarkan waktu dan kita ingin melihat **tren** kenaikan/penurunan bulan ke bulan.

**Contoh 2:** Sebutkan langkah membuat grafik column dari data A1:B5.
**Pembahasan:** Blok A1:B5 (termasuk header) → Insert → Charts → pilih **Column**. Grafik batang akan muncul menampilkan perbandingan nilai tiap baris.

**Contoh 3:** Apa fungsi Data Labels pada grafik?
**Pembahasan:** Data Labels menampilkan **nilai angka** langsung di atas setiap bar/titik, sehingga pembaca tidak perlu memperkirakan dari skala sumbu.

**Contoh 4:** Kapan grafik Pie tidak disarankan?
**Pembahasan:** Pie tidak disarankan bila bagian-bagiannya tidak berjumlah 100% atau jumlah kategorinya terlalu banyak (lebih dari ±7), karena potongan menjadi terlalu kecil dan sulit dibedakan.

---

## G. Miskonsepsi yang Sering Terjadi 🚫

| Miskonsepsi | Fakta yang Benar |
|---|---|
| "Semua data bisa pakai pie chart" | Pie hanya untuk proporsi dari total 100% |
| "Line chart untuk membandingkan kategori" | Line paling cocok untuk **tren waktu**; kategori pakai Column/Bar |
| "Grafik tidak perlu judul" | Judul sangat penting agar pembaca tahu isi grafik |
| "Blok data tidak perlu menyertakan header" | Header dibutuhkan agar Excel tahu nama kategori/seri |
| "Data labels hanya mempercantik" | Data labels menampilkan nilai aktual sehingga akurat |

---

## H. Tantangan Praktik (Mengaplikasi) 🎯

**Tantangan 1 — Grafik Pertama:** Buat data penjualan 5 produk dalam satu bulan, lalu buat **column chart** lengkap dengan judul, label sumbu, dan data labels.

**Tantangan 2 — Grafik Tren:** Buat data suhu kota selama 7 hari, lalu buat **line chart** untuk menunjukkan tren suhu.

**Tantangan 3 — Analisis Proporsi:** Buat data pengeluaran bulanan (makanan, transport, pendidikan, hiburan) yang totalnya 100%, lalu buat **pie chart**. Tambahkan keterangan persentase pada setiap bagian.

---

## I. Rangkuman Kunci 🔑

1. **Grafik** membuat data lebih mudah dipahami secara visual.
2. Pilih grafik sesuai data: kategori → **Column/Bar**, waktu → **Line**, proporsi → **Pie**.
3. Langkah membuat grafik: siapkan data → blok → **Insert → Chart**.
4. Lengkapi dengan **judul, label sumbu, legend, dan data labels**.
5. Grafik bisa dipindahkan ke **New Sheet** atau di dalam sheet yang sama.
6. Gunakan **Chart Design** dan **Format** untuk mempercantik grafik.
7. Grafik yang baik membantu komunikasi data lebih cepat dan meyakinkan.

---

## J. Glosarium 📖

| Istilah | Arti |
|---|---|
| **Chart / Grafik** | Representasi visual data |
| **Column chart** | Grafik batang tegak untuk perbandingan |
| **Line chart** | Grafik garis untuk tren |
| **Pie chart** | Grafik lingkaran untuk proporsi |
| **Data Labels** | Nilai angka yang ditampilkan pada grafik |
| **Legend** | Keterangan warna/seri pada grafik |
| **Axis** | Sumbu X (horizontal) dan Y (vertikal) |

---

## K. Refleksi (Merefleksi) 🔍

- Kapan kamu akan memakai grafik batang, garis, dan lingkaran dalam hidupmu?
- Grafik apa yang paling sering kamu lihat di berita atau media sosial?
- Apa kesulitan yang kamu temui saat membuat atau memformat grafik?
- Bagian mana yang masih perlu kamu perbaiki?
- **Skala pemahaman diri:** ____/10
- Data apa yang ingin kamu visualisasikan selanjutnya?

---

**MGMP Informatika SMAN 6 Cimahi — Fase E (Kelas X) Semester 2**