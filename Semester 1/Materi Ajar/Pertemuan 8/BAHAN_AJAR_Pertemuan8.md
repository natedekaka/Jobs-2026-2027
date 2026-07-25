# BAHAN AJAR – PERTEMUAN 8
## Perangkat Teknologi untuk Produktivitas

| TP | LD 2.4 |
|---|---|

---

### A. PENGOLAH KATA — Fitur Lanjut (Word / Google Docs)

#### 1. Mail Merge (Surat Massal)

Mail merge memungkinkan kamu membuat banyak dokumen personal (sertifikat, surat, label) dari satu template + satu data.

**Langkah:**
1. **Siapkan data** di Excel/Sheets: Nama, Kelas, Jabatan, Nilai (dll)
2. **Buat template** di Word/Docs: tulis surat, sisipkan `<<Nama>>`, `<<Kelas>>` dll
3. **Mail Merge**: Mailings → Select Recipients → Use Existing List → pilih file Excel
4. **Insert Merge Field**: tempatkan field di posisi yang tepat
5. **Preview Results**: lihat hasil
6. **Finish & Merge**: cetak semua atau edit individual

**Contoh template:**
```
Yth. <<Nama>>
Siswa kelas <<Kelas>>
SMAN 6 Cimahi

Dengan hormat,
Kami mengundang Saudara <<Nama>> sebagai <<Jabatan>>
untuk menghadiri rapat OSIS pada ...
```

#### 2. Daftar Isi Otomatis

| Langkah | Cara |
|---|---|
| 1. Gunakan **Heading Styles** | Heading 1, Heading 2, Heading 3 |
| 2. Insert Table of Contents | References → Table of Contents |
| 3. Update jika ada perubahan | Klik kanan → Update Field |

#### 3. Header & Footer

- Berbeda untuk halaman ganjil-genap (untuk buku)
- Section break untuk format berbeda dalam satu dokumen

#### 4. Track Changes & Comments

- **Review → Track Changes**: setiap edit tercatat
- **Comment**: beri catatan tanpa mengubah teks

---

### B. SPREADSHEET — Fitur Lanjut (Excel / Google Sheets)

#### 1. Rumus Dasar yang Wajib Dikuasai

| Rumus | Fungsi | Contoh |
|---|---|---|
| `=SUM(A1:A10)` | Menjumlahkan range | =SUM(B2:B11) |
| `=AVERAGE(A1:A10)` | Rata-rata | =AVERAGE(C2:C11) |
| `=IF(logika, nilai_benar, nilai_salah)` | Kondisional | `=IF(B2>=75,"LULUS","TIDAK LULUS")` |
| `=VLOOKUP(nilai, tabel, kolom)` | Pencarian vertikal | `=VLOOKUP(D2,Sheet2!A:B,2)` |
| `=COUNTIF(range, kriteria)` | Menghitung sesuai kriteria | `=COUNTIF(B2:B11,">75")` |

#### 2. Conditional Formatting

Format sel otomatis berdasarkan nilainya.

**Langkah:**
1. Pilih range → Format → Conditional formatting
2. Atur aturan:
   - `Cell is greater than 85` → warna hijau
   - `Cell is less than 55` → warna merah
3. Hasil: angka berubah warna otomatis

#### 3. Grafik / Chart

| Langkah | Cara |
|---|---|
| Pilih data | Range yang ingin dibuat grafik |
| Insert → Chart | Pilih jenis: batang, garis, lingkaran |
| Customize | Judul, sumbu, warna, label |

#### 4. Data Validation

Membatasi input — misal hanya angka 0–100 di kolom nilai:
- Data → Data Validation → Number between 0–100

---

### C. PRESENTASI — Fitur Lanjut (PowerPoint / Google Slides)

#### 1. Slide Master

**Slide Master** = template master yang mengontrol semua slide.

**Langkah:**
1. View → Slide Master
2. Edit satu kali (font, background, logo)
3. **Semua slide berubah otomatis**
4. Jika ingin slide tertentu berbeda, gunakan **Layout** yang berbeda

#### 2. Hyperlink & Navigasi Interaktif

| Tujuan | Cara |
|---|---|
| Link ke slide lain | Select text → Insert Link → Place in This Document → pilih slide |
| Link ke web | Insert Link → URL |
| Tombol navigasi | Insert → Shapes → pilih bentuk → link ke slide |

**Contoh:**
- Slide 1 (Daftar Isi): link ke slide 2, 3, 4, 5
- Slide 2–5: tombol "Kembali ke Daftar Isi"

#### 3. Animasi & Transisi

| Fitur | Fungsi |
|---|---|
| **Animasi** | Gerakan pada elemen di dalam slide (muncul, hilang, bergerak) |
| **Transisi** | Efek pergantian antar slide |
| **Trigger** | Animasi muncul saat diklik (bukan otomatis) |

**Tips:** Animasi secukupnya — terlalu banyak mengganggu fokus.

---

### D. KOLABORASI DARING — Google Workspace

Google Docs, Sheets, dan Slides mendukung kolaborasi real-time.

| Fitur | Cara | Manfaat |
|---|---|---|
| **Share** | Klik Share → masukkan email anggota | Bisa diedit bersama |
| **Permission** | Viewer / Commenter / Editor | Kontrol akses |
| **Real-time editing** | Beberapa orang edit bersamaan | Tidak perlu bolak-balik file |
| **Version history** | File → Version history → See history | Lihat siapa mengubah apa |
| **Comments** | Select teks → Comment → @mention | Diskusi dalam dokumen |
| **Suggesting mode** | Klik ikon pensil → Suggesting | Saran tanpa mengubah asli |

---

### E. Rangkuman

1. **Mail Merge** menghemat waktu — buat banyak surat/sertifikat dari 1 template + data.
2. **Daftar isi otomatis** dari heading styles — update 1 klik.
3. **Conditional formatting** mewarnai otomatis — data langsung terbaca.
4. **Slide master** mengubah semua slide dalam 1 edit.
5. **Hyperlink + navigasi** membuat presentasi interaktif.
6. **Google Workspace** memungkinkan kolaborasi real-time.

---

**MGMP Informatika SMAN 6 Cimahi**
