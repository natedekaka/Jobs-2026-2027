# BAHAN AJAR – PERTEMUAN 15 (S1)
## PAS — Ujian & Portofolio
*Mengacu pada Panduan Mapel 2025; INFORMATIKA Fase D-F — pendekatan Pembelajaran Mendalam (Memahami → Mengaplikasi → Merefleksi)*

| Informasi | Keterangan |
|---|---|
| **Fase / Kelas** | F / Kelas XII |
| **Alokasi Waktu** | 5 JP × 45 menit (225 menit) |
| **Elemen CP** | Praktik Lintas Bidang (PLB) |
| **Tujuan Pembelajaran** | Mengukur kompetensi akhir semester 1 melalui ujian (pilihan ganda dan esai) serta pengumpulan portofolio karya terbaik |
| **Materi Prasyarat** | Seluruh materi Pertemuan 1–14 |

---

## A. Skenario & Instruksi Ujian 📋

> **"Hari Pembuktian"**
>
> Hari ini kamu mengikuti **Penilaian Akhir Semester**. Ujian terdiri dari pilihan ganda dan esai yang mencakup seluruh materi: Excel, konten digital, dan etika/hukum. Selain itu, kamu wajib mengumpulkan **portofolio 3 karya terbaik** semester ini. Inilah puncak perjalanan belajar satu semester — tunjukkan yang terbaik, kelola waktu, dan periksa kembali pekerjaanmu sebelum mengumpulkan.
>
> **Instruksi:** Baca petunjuk dengan teliti. Kerjakan soal mudah lebih dulu, gunakan waktu yang tersisa untuk mengecek jawaban, dan pastikan portofolio sudah dikumpulkan sesuai tenggat.

---

## B. Jadwal dan Ketentuan Ujian

| Sesi | Durasi | Jenis Soal | Jumlah |
|---|---|---|---|
| Sesi 1 | 60 menit | Pilihan Ganda (PG) | 30 soal |
| Sesi 2 | 60 menit | Esai | 5 soal |
| Total | 120 menit | — | 35 soal |

**Ketentuan:**
1. Kerjakan secara **mandiri** dan jujur.
2. Baca setiap soal dengan cermat; perhatikan kata kunci.
3. Kerjakan soal yang mudah terlebih dahulu.
4. Periksa kembali sebelum mengumpulkan.

---

## C. Kisi-Kisi Soal

| Materi | Jumlah PG | Jumlah Esai | Bobot |
|---|---|---|---|
| Excel (Review, Pivot, Fungsi Statistik) | 10 | 2 | 35% |
| Dashboard & Analisis Data | 4 | 1 | 20% |
| Konten Digital (Branding, Hoaks, AI, Produksi) | 8 | 1 | 25% |
| Etika Digital (UU ITE, Hak Cipta, Privasi) | 8 | 1 | 20% |

---

## D. Contoh Soal Pilihan Ganda

1. Fungsi untuk menghitung jumlah sel berisi **angka** adalah... **(COUNT)**
2. Shortcut membuat Table di Excel... **(Ctrl+T)**
3. Area Pivot Table untuk menempatkan data yang dihitung... **(Values)**
4. Pasal UU ITE tentang pencemaran nama baik... **(27 ayat 3)**
5. Sumber foto gratis tanpa kewajiban menyebut sumber... **(Unsplash / Pixabay berlisensi CC0)**

---

## E. Contoh Soal Esai & Pedoman Jawaban

**Soal 1 — Formula:** Buat formula IF bertingkat untuk predikat nilai (A ≥85, B 70–84, C 55–69, D <55)!
**Jawaban:** `=IF(C2>=85,"A",IF(C2>=70,"B",IF(C2>=55,"C","D")))`

**Soal 2 — Verifikasi:** Jelaskan 4 langkah verifikasi hoaks!
**Jawaban:** (1) Baca seluruh berita, bukan hanya judul; (2) cek sumber (penulis, tanggal, domain); (3) cari versi lain di media kredibel; (4) verifikasi gambar/video dengan reverse image search.

**Soal 3 — Hukum:** Sebutkan 3 pasal UU ITE beserta sanksinya!
**Jawaban:** Pasal 27 ayat (3) pencemaran nama baik (hingga 4 tahun); Pasal 28 ayat (1) berita bohong (hingga 6 tahun); Pasal 29 ancaman kekerasan (hingga 4 tahun). (Jawaban pasal lain yang tepat juga diterima.)

**Soal 4 — Kasus:** *"Seorang siswa memposting foto temannya tanpa izin."* Pasal apa yang berpotensi dilanggar? Beri saran!
**Jawaban:** Berpotensi melanggar Pasal 27 ayat (3) UU ITE (pencemaran nama baik) dan hak cipta atas foto; selain itu melanggar privasi. Saran: minta izin sebelum mengunggah, hapus unggahan, dan minta maaf.

---

## F. Contoh Soal & Penyelesaian (Latihan Tambahan) 📝

**Contoh 1:** Tuliskan rumus rata-rata nilai siswa kelas "XII-A" laki-laki (kelas di kolom A, gender di kolom B, nilai di kolom C, 40 baris)!
**Jawaban:** `=AVERAGEIFS(C2:C41,A2:A41,"XII-A",B2:B41,"L")`

**Contoh 2:** Bagaimana membuat dashboard dengan KPI, chart, dan slicer dari data penjualan?
**Jawaban:** Buat pivot (Rows=Produk, Values=Sum Total) → buat chart dari pivot → Insert Slicer untuk Kategori → susun KPI cards (Total, Rata-rata, Produk Terlaris) dalam satu sheet "DASHBOARD".

**Contoh 3:** Sebutkan 5 elemen branding!
**Jawaban:** Logo, warna, tipografi, tone of voice, dan tagline.

**Contoh 4:** Mengapa kita tidak boleh mengambil foto orang dari media sosial tanpa izin?
**Jawaban:** Karena melanggar hak cipta (UU No. 28/2014), hak moral pencipta, dan berpotensi melanggar privasi serta Pasal 27 UU ITE.

**Contoh 5:** Apa saja yang termasuk jejak digital pasif? Beri 3 contoh!
**Jawaban:** Alamat IP, cookie browser, dan data lokasi GPS. (Jawaban lain yang sesuai, misal riwayat pencarian, juga benar.)

---

## G. Kesalahan Umum yang Harus Dihindari 🚫

| Kesalahan | Cara Menghindari |
|---|---|
| Tidak membaca soal sampai selesai | Baca cermat dan tandai kata kunci |
| Salah urutan argumen rumus | Ingat SUMIF vs SUMIFS, AVERAGEIF vs AVERAGEIFS |
| Menyebut pasal tanpa contoh | Hubungkan setiap pasal dengan contoh kasus |
| Lupa konversi nilai/predikat | Hafalkan rentang: A ≥85, B 70–84, C 55–69 |
| Terlalu lama di satu soal | Kerjakan soal mudah lebih dulu |

---

## H. Tantangan Praktik (Mengaplikasi) 🎯

**Tantangan 1 — Drill PG (60 menit):** Kerjakan 20 soal pilihan ganda campuran (Excel, konten, hukum) dan bahas jawaban yang salah.

**Tantangan 2 — Drill Esai (60 menit):** Kerjakan 5 soal esai dari kisi-kisi; mintalah teman untuk saling mengoreksi menggunakan pedoman jawaban.

**Tantangan 3 — Finalisasi Portofolio (60 menit):** Susun folder digital berisi: (1) file Excel dashboard, (2) poster Canva, (3) PDF tugas etika. Periksa kelengkapan dan penamaan file.

**Tantangan 4 — Evaluasi Diri (45 menit):** Lakukan simulasi 30 soal dengan batas waktu; evaluasi hasilnya dan tulis 3 poin perbaikan untuk hari ujian.

---

## I. Rangkuman Kunci 🔑

1. **PAS** = 30 soal PG (60 menit) + 5 soal esai (60 menit).
2. Bobot materi: Excel 35%, Dashboard 20%, Konten Digital 25%, Etika Digital 20%.
3. Hafalkan rumus kunci: `IF` bertingkat, `COUNTIFS/SUMIFS/AVERAGEIFS`, `VLOOKUP+IFERROR`.
4. Kuasai istilah: KPI, slicer, prompt, hoaks, pasal UU ITE, CC, UU PDP.
5. **Portofolio** berisi 3 karya terbaik: Excel, poster, tugas etika.

---

## J. Glosarium 📖

| Istilah | Arti |
|---|---|
| **PAS** | Penilaian Akhir Semester |
| **PG** | Pilihan Ganda |
| **KPI** | Indikator kinerja utama |
| **VLOOKUP** | Fungsi pencarian data |
| **Hoaks** | Informasi palsu yang direkayasa |
| **Portofolio** | Kumpulan karya terbaik siswa |

---

## K. Refleksi (Merefleksi) 🔍

- Bagaimana perasaanmu menghadapi PAS setelah mempelajari semua materi?
- Materi mana yang paling bermanfaat untuk kehidupanmu ke depan?
- Apa yang akan kamu lakukan berbeda pada semester berikutnya?
- **Skala pemahaman diri:** ____/10
- Apa rencanamu setelah semester ini berakhir?

---

**MGMP Informatika SMAN 6 Cimahi — Fase F (Kelas XII) Semester 1**