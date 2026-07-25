# MODUL AJAR INFORMATIKA – FASE E (KELAS X)

## Informasi Umum

| Komponen | Deskripsi |
|---|---|
| **Mata Pelajaran** | Informatika |
| **Fase / Kelas** | E / X |
| **Semester** | 1 (Ganjil) |
| **Pertemuan ke-** | 5 |
| **Alokasi Waktu** | 2 JP × 45 menit (90 menit) |
| **Tahun Pelajaran** | 2026/2027 |
| **Satuan Pendidikan** | **SMA Negeri 6 Cimahi** |

---

## Profil Pelajar Pancasila

| Dimensi | Indikator |
|---|---|
| Bernalar Kritis | Mengevaluasi hasil pencarian dengan operator lanjutan |
| Mandiri | Menjalankan strategi pencarian secara mandiri |
| Gotong Royong | Berdiskusi hasil pencarian dalam kelompok |

---

## Sarana & Prasarana

| Sarana | Keterangan |
|---|---|
| Lab komputer / laptop | 1 unit per siswa (atau 1 per 2 siswa) |
| Koneksi internet | Untuk praktik pencarian |
| Proyektor / LCD | Untuk demo guru |
| Browser | Chrome / Firefox / Edge |
| LKPD & Bahan Ajar | Dicetak |

---

## Tujuan Pembelajaran (TP 2.1)

| TP | Indikator Ketercapaian Tujuan Pembelajaran (IKTP) |
|---|---|
| **LD 2.1:** Memahami penggunaan mesin pencari dengan variabel yang lebih banyak | 2.1.1 Menggunakan operator pencarian (AND, OR, NOT, "", site:, filetype:) untuk mempersempit hasil<br>2.1.2 Membandingkan hasil pencarian antar mesin pencari (Google, Bing, DuckDuckGo)<br>2.1.3 Memilih strategi pencarian terbaik berdasarkan kebutuhan informasi |

---

## Peta Kompetensi

```
Pertemuan 5 — Mesin Pencari Tingkat Lanjut
│
├── Pendahuluan (10 menit)
│   ├── Review OS & transisi ke Literasi Digital
│   └── Apersepsi: "Bagaimana cara mencari info spesifik di internet?"
│
├── Inti (65 menit)
│   ├── Memahami (20 menit)
│   │   ├── Cara kerja mesin pencari (crawling, indexing, ranking)
│   │   ├── Operator pencarian: AND, OR, NOT, "", site:, filetype:, intitle:
│   │   └── Perbandingan Google vs Bing vs DuckDuckGo
│   │
│   ├── Mengaplikasi (35 menit)
│   │   ├── Praktik 1: Tanpa operator vs dengan operator
│   │   ├── Praktik 2: Mencari dengan variabel ganda
│   │   └── Praktik 3: Membandingkan 3 mesin pencari
│   │
│   └── Merefleksi (10 menit)
│       └── Diskusi strategi pencarian terbaik
│
└── Penutup (15 menit)
```

---

## Langkah Pembelajaran

### Pembukaan (10 menit)

| Kegiatan | Waktu |
|---|---|
| 1. Salam, doa, cek kehadiran | 2 menit |
| 2. Review singkat: OS mengelola sumber daya — sekarang kita bahas bagaimana memanfaatkan internet secara cerdas | 3 menit |
| 3. **Apersepsi**: "Coba cari 'cara membuat kue nastar' di Google. Dalam 0,5 detik muncul jutaan hasil. Bagaimana caranya Google tahu mana yang paling relevan?" | 5 menit |

### Inti (65 menit)

#### Memahami (berkesadaran, menggembirakan) — 20 menit

1. **Cara Kerja Mesin Pencari (8 menit)**
   - **Crawling**: Googlebot menjelajahi web, mengikuti link dari halaman ke halaman
   - **Indexing**: Menyusun indeks kata kunci (seperti indeks di buku)
   - **Ranking**: Menentukan urutan hasil berdasarkan relevansi (algoritma PageRank, dll)
   - Ilustrasi:

     ```
     Crawling → Indexing → Ranking → Results
        │           │          │         │
        ▼           ▼          ▼         ▼
     "Memindai"  "Menyusun" "Menilai" "Menampilkan"
       web       katalog    relevansi   hasil
     ```

2. **Operator Pencarian (7 menit)**

   | Operator | Contoh | Fungsi |
   |---|---|---|
   | `"kata tepat"` | `"global warming"` | Mencari frasa PERSIS (tidak dipisah) |
   | `AND` | `sejarah AND komputer` | Kedua kata harus muncul |
   | `OR` | `motor OR mobil` | Salah satu kata muncul |
   | `-` (NOT) | `kucing -anjing` | Mengecualikan kata |
   | `site:` | `site:kemendikbud.go.id kurikulum` | Hanya dari domain tertentu |
   | `filetype:` | `filetype:pdf informatika` | Hanya format file tertentu |
   | `intitle:` | `intitle:arsitektur von neumann` | Kata di judul halaman |
   | `..` (range) | `smartphone 3..7 juta` | Rentang harga/angka |
   | `related:` | `related:kompas.com` | Situs serupa |

3. **Perbandingan Mesin Pencari (5 menit)**

   | Aspek | Google | Bing | DuckDuckGo |
   |---|---|---|---|
   | Pangsa pasar | ~90% | ~4% | ~0,5% |
   | Privasi | Melacak pengguna | Melacak | **Tidak melacak** |
   | Fitur unggulan | Knowledge Graph, featured snippets | Rewards points, video preview | !bang commands, privasi |
   | Kustomisasi | Filter, tools | Filter, tools | Minimalis |

#### Mengaplikasi (bermakna, menggembirakan) — 35 menit

4. **Praktik 1: Tanpa Operator vs Dengan Operator (10 menit)**
   - Siswa mencari dengan dan tanpa operator, membandingkan jumlah hasil
   - Contoh:

     | Tanpa Operator | Dengan Operator | Jumlah Hasil (sebelum) | Jumlah Hasil (sesudah) |
     |---|---|---|---|
     | `sejarah komputer` | `"sejarah komputer" filetype:pdf` | | |
     | `pemanasan global` | `"pemanasan global" site:.ac.id` | | |
     | `korupsi` | `korupsi -politik site:kompas.com` | | |

5. **Praktik 2: Mencari dengan Variabel Ganda (10 menit)**
   - Skenario: "Cari jurnal ilmiah tentang dampak media sosial terhadap kesehatan mental remaja di Indonesia, format PDF, dari situs .ac.id"
   - Siswa merancang query: `"dampak media sosial" "kesehatan mental" remaja site:ac.id filetype:pdf`
   - Evaluasi hasil: apakah sesuai dengan yang diinginkan?

6. **Praktik 3: Membandingkan 3 Mesin Pencari (15 menit)**
   - Semua siswa mencari topik yang SAMA di 3 mesin pencari:
     - Google (google.com)
     - Bing (bing.com)
     - DuckDuckGo (duckduckgo.com)
   - Topik: `"kecerdasan buatan" "pendidikan" site:ac.id filetype:pdf`
   - Catat: jumlah hasil, peringkat 3 besar, relevansi

#### Merefleksi (berkesadaran, bermakna) — 10 menit

7. **Diskusi Kelas (5 menit)**
   - "Operator mana yang paling berguna menurut kalian?"
   - "Apakah hasil pencarian Google selalu lebih baik dari DuckDuckGo? Kenapa?"
   - "Kapan kita perlu menggunakan tanda kutip `" "` dalam pencarian?"

8. **Refleksi Individu (5 menit)**
   - Tulis di LKPD: skala pemahaman, strategi baru yang dipelajari

### Penutup (15 menit)

| Kegiatan | Waktu |
|---|---|
| 1. Rangkuman: "Mesin pencari bukan sekadar kotak ketik — gunakan operator untuk presisi" | 3 menit |
| 2. Tanya jawab | 5 menit |
| 3. Menyampaikan pertemuan depan: Ekosistem Periksa Fakta & Membaca Lateral | 2 menit |
| 4. Tugas: Cari 1 topik pelajaran dengan 3 strategi query berbeda, catat perbedaan hasilnya | 3 menit |
| 5. Doa & salam | 2 menit |

---

## Asesmen

| Kriteria | Skor (1–4) |
|---|---|
| Praktik 1: Membandingkan hasil dengan/tanpa operator | |
| Praktik 2: Merancang query dengan variabel ganda | |
| Praktik 3: Perbandingan 3 mesin pencari | |
| Refleksi | |

---

**MGMP Informatika SMAN 6 Cimahi**
