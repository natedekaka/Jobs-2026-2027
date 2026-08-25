# BAHAN AJAR – PERTEMUAN 9 (S1)
## Word — Mail Merge & Daftar Isi
*Mengacu pada Panduan Mapel 2025; INFORMATIKA Fase D-F — pendekatan Pembelajaran Mendalam (Memahami → Mengaplikasi → Merefleksi)*

| Informasi | Keterangan |
|---|---|
| **Fase / Kelas** | E / Kelas X |
| **Alokasi Waktu** | 2 JP × 45 menit (90 menit) |
| **Elemen CP** | Teknologi Informasi dan Komunikasi (TIK) |
| **Tujuan Pembelajaran** | Membuat banyak dokumen serupa sekaligus (mail merge) dari data Excel; membuat daftar isi otomatis berbasis heading styles; memperbarui daftar isi |
| **Materi Prasyarat** | Layout & header/footer (P8); pengenalan Excel untuk menyiapkan data penerima |

---

## A. Kisah Pemantik 🎬

> **"100 Undangan dalam 1 Malam"**
>
> Panitia perpisahan kelas X harus membuat **100 undangan** untuk orang tua — dengan nama dan alamat yang berbeda-beda. Jika ditulis satu per satu, mereka butuh semalaman dan tangan pegal. Padahal acaranya besok!
>
> Seorang anggota yang paham **mail merge** menyelesaikannya dalam **15 menit**: satu template undangan, satu file Excel berisi 100 nama, lalu tinggal klik — semua undangan jadi dengan nama masing-masing.
>
> **Pertanyaan pemantik:** Pernahkah kamu mengerjakan tugas berulang yang membosankan (menulis hal yang sama berkali-kali)? Bagaimana cara otomatisasi bisa membantu pekerjaan seperti itu?

---

## B. Apa Itu Mail Merge?

**Mail Merge** adalah fitur Word untuk membuat **banyak dokumen serupa dengan data yang berbeda** dari satu template. Cocok untuk surat undangan, sertifikat, dan label alamat.

| Komponen | Peran |
|---|---|
| **Dokumen utama (template)** | Teks yang sama untuk semua penerima |
| **Data source (Excel)** | Data yang berbeda per penerima |
| **Merge fields** | Tempat "lubang" di template yang diisi data |
| **Hasil merge** | Dokumen akhir per penerima |

---

## C. Langkah Membuat Mail Merge

1. **Siapkan data** — buat file Excel berisi kolom: Nama, Alamat, Kota, Nilai, dll.
2. **Siapkan template** — buat dokumen Word berisi teks utama undangan/sertifikat.
3. **Jalankan wizard:**
   - Klik **References → Start Mail Merge → Step by Step Mail Merge Wizard**.
   - Pilih tipe **Letters**.
   - **Select recipients → Use existing list** → pilih file Excel.
   - **Insert Merge Fields**: klik tempat yang diinginkan → pilih field (misal `<<Nama>>`).
   - **Preview Results** untuk melihat hasil sebelum dicetak.
   - **Finish & Merge**: cetak langsung atau buat dokumen terpisah (**Edit Individual Documents**).

> 💡 **Urutan jangan terbalik:** Data Excel harus **disimpan dan ditutup** (atau minimal kolom pertama berisi nama kolom) sebelum dihubungkan ke Word.

---

## D. Field yang Sering Digunakan

| Field | Isi |
|---|---|
| `<<Nama>>` | Nama penerima |
| `<<Alamat>>` | Alamat penerima |
| `<<Kota>>` | Kota |
| `<<Tanggal>>` | Tanggal surat |
| `<<Nilai>>` | Nilai (untuk rapor/sertifikat) |

```
Contoh template sertifikat:
"Sertifikat ini diberikan kepada
        <<Nama>>
atas keberhasilan menyelesaikan pelatihan dengan nilai <<Nilai>>."
```

---

## E. Daftar Isi Otomatis (Table of Contents)

Daftar isi otomatis dibuat berdasarkan **heading styles**:

1. Terapkan style **Heading 1** (bab), **Heading 2** (subbab), **Heading 3** (sub-subbab) pada judul dokumen.
2. Klik **References → Table of Contents** → pilih format yang diinginkan.
3. Daftar isi terbentuk otomatis lengkap dengan nomor halaman.

> 💡 **Kunci sukses:** Jangan buat daftar isi manual — jika halaman berubah, daftar manual harus ditulis ulang. Dengan heading styles, cukup **update**.

---

## F. Update Daftar Isi Secara Berkala

Setelah mengedit dokumen:

- Klik pada area daftar isi → **Update Table**.
- Pilih salah satu:
  - **Update page numbers only** — jika hanya halaman yang berubah.
  - **Update entire table** — jika ada judul baru/diubah.

---

## G. Contoh Soal & Penyelesaian 📝

**Contoh 1:** Apa fungsi Mail Merge?
**Jawaban:** Mail Merge membuat **banyak dokumen serupa dengan data berbeda** sekaligus dari satu template dan satu data source (Excel), misal 100 undangan dengan nama yang berbeda-beda.

**Contoh 2:** Sebutkan 3 langkah utama membuat Mail Merge!
**Jawaban:**
1. Siapkan data di Excel (Nama, Alamat, Kota, dll).
2. Buat template dokumen di Word.
3. Jalankan wizard (**References → Start Mail Merge**) → hubungkan data → Insert Merge Field → Preview → Finish & Merge.

**Contoh 3:** Bagaimana cara membuat daftar isi otomatis dan mengapa perlu Update Table?
**Jawaban:** Beri **heading styles** (Heading 1/2/3) pada judul, lalu **References → Table of Contents**. **Update Table** perlu dilakukan setelah dokumen berubah agar nomor halaman dan judul di daftar isi tetap sesuai.

---

## H. Miskonsepsi yang Sering Terjadi 🚫

| Miskonsepsi | Fakta yang Benar |
|---|---|
| "Daftar isi dibuat dengan mengetik manual" | Daftar isi otomatis dari **heading styles** jauh lebih cepat & akurat |
| "Mail Merge hanya untuk surat" | Bisa untuk **sertifikat, label, rapor, email massal** |
| "Data Excel tidak perlu rapi" | Kolom harus **bernama jelas** agar merge field cocok |
| "Setelah jadi, daftar isi tidak perlu di-update" | Setiap ada perubahan halaman/judul, lakukan **Update Table** |

---

## I. Tantangan Praktik (Mengaplikasi) 🎯

**Tantangan 1 — Undangan Kelas:** Buat file Excel berisi 5 nama teman + alamat. Buat template undangan, lalu jalankan mail merge sehingga dihasilkan 5 undangan dengan nama & alamat berbeda.

**Tantangan 2 — Sertifikat Nilai:** Buat data 5 siswa (Nama, Nilai, Kelas) di Excel. Buat sertifikat berisi `<<Nama>>` dan nilai `<<Nilai>>`, lalu **Preview Results** untuk mengecek kebenarannya.

**Tantangan 3 — Laporan + Daftar Isi:** Buat dokumen 3 bab (masing-masing 2 subbab) menggunakan Heading 1/2. Sisipkan daftar isi otomatis, lalu tambah satu bab baru dan lakukan **Update entire table**. Periksa apakah daftar isi bertambah.

---

## J. Rangkuman Kunci 🔑

1. **Mail Merge** = membuat dokumen massal dari satu template + data Excel.
2. Urutan: **data Excel → template Word → wizard → merge fields → preview → finish**.
3. Field ditandai tanda `<<...>>`, misal `<<Nama>>`.
4. **Daftar isi otomatis** dibangun dari **heading styles**.
5. Setelah edit dokumen, selalu **Update Table** (page numbers only / entire table).

---

## K. Glosarium 📖

| Istilah | Arti |
|---|---|
| **Mail Merge** | Fitur pembuatan dokumen massal dengan data berbeda |
| **Template** | Dokumen utama yang dipakai sebagai pola |
| **Data Source** | Sumber data (file Excel) |
| **Merge Field** | Penanda tempat data disisipkan (`<<...>>`) |
| **Heading Style** | Gaya judul (Heading 1/2/3) yang dipakai daftar isi |
| **Table of Contents** | Daftar isi otomatis |
| **Update Table** | Memperbarui daftar isi setelah perubahan |

---

## L. Refleksi (Merefleksi) 🔍

- Pekerjaan apa di sekolah atau rumah yang bisa dihemat dengan mail merge?
- Mengapa heading styles penting untuk daftar isi otomatis?
- Apa keuntungan daftar isi otomatis dibanding daftar isi manual?
- **Skala pemahaman diri:** ____/10
- Apa yang ingin kamu pelajari lebih lanjut tentang otomatisasi dokumen?

---

**MGMP Informatika SMAN 6 Cimahi — Fase E (Kelas X) Semester 1**