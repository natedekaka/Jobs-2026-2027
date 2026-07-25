# BAHAN AJAR – PERTEMUAN 5
## Mesin Pencari Tingkat Lanjut

| Mata Pelajaran | Informatika |
|---|---|
| Fase / Kelas | E / X |
| TP | LD 2.1 |
| Semester | 1 (Ganjil) |

---

### A. Cara Kerja Mesin Pencari

#### Crawling
Mesin pencari menggunakan program otomatis bernama **web crawler** atau **spider** untuk menjelajahi halaman-halaman web di internet. Crawler mengikuti tautan (link) dari satu halaman ke halaman lainnya — mirip seperti kita browsing dari satu situs ke situs lain.

#### Indexing
Setelah halaman di-crawl, mesin pencari menyusun **indeks** — yaitu katalog raksasa berisi kata-kata dan lokasinya di setiap halaman web.

> **Analogi**: Crawling = memotret setiap halaman buku di perpustakaan. Indexing = membuat katalog judul, pengarang, dan kata kunci dari setiap buku.

#### Ranking
Saat kamu mengetik query, mesin pencari melihat ke indeks dan menentukan halaman mana yang paling relevan menggunakan algoritma. Google menggunakan **PageRank** (berdasarkan jumlah dan kualitas link yang mengarah ke halaman tersebut) plus ratusan faktor lainnya.

```
 Crawling        Indexing         Ranking         Results
 (robot)      (database)      (algoritma)      (halaman)
    │              │               │               │
    ▼              ▼               ▼               ▼
   Web         Katalog         Skor 0-100     10 hasil
  1T+ hlm       kata kunci     relevansi       teratas
```

---

### B. Operator Pencarian Google

#### 1. Tanda Kutip — Pencarian Frasa Tepat
Gunakan `"..."` untuk mencari kata dalam urutan yang persis sama.

| Query | Hasil |
|---|---|
| `sistem komputer` | Mencari halaman dengan kata sistem DAN komputer (tidak harus berurutan) |
| `"sistem komputer"` | Mencari halaman dengan frasa "sistem komputer" tepat berurutan |

#### 2. AND, OR, NOT ( -, | )

| Operator | Contoh | Penjelasan |
|---|---|---|
| **AND** (otomatis) | `sejarah budaya indonesia` | Semua kata harus ada (default) |
| **OR** ( `|` ) | `motor \| mobil` | Salah satu kata boleh ada |
| **NOT** ( `-` ) | `ikan -hiu` | Kata setelah tanda minus DILEWATKAN |

#### 3. site: — Batasi Domain

| Query | Hasil |
|---|---|
| `kurikulum merdeka site:kemendikbud.go.id` | Hanya dari domain kemendikbud |
| `polusi site:.ac.id` | Hanya dari domain akademik Indonesia |
| `covid site:.gov` | Hanya dari domain pemerintah |

#### 4. filetype: — Batasi Format File

| Query | Hasil |
|---|---|
| `informatika filetype:pdf` | Hanya file PDF |
| `laporan keuangan filetype:xlsx` | Hanya file Excel |
| `presentasi produk filetype:ppt` | Hanya file PowerPoint |

#### 5. intitle: — Kata di Judul Halaman

| Query | Hasil |
|---|---|
| `intitle:von neumann` | Kata "von neumann" ada di judul halaman |
| `intitle:"sistem operasi" linux` | Frasa di judul + kata "linux" di manapun |

#### 6. allinurl: — Kata di URL

| Query | Hasil |
|---|---|
| `allinurl:login` | Halaman login |
| `allinurl:admin` | Halaman admin (sering dipakai security researcher) |

#### 7. intext: — Kata di Isi Halaman

| Query | Hasil |
|---|---|
| `intext:password` | Halaman yang mengandung kata "password" di teksnya |

#### 8. related: — Situs Serupa

| Query | Hasil |
|---|---|
| `related:kompas.com` | Situs berita serupa kompas |
| `related:youtube.com` | Situs berbagi video serupa |

#### 9. .. — Rentang Angka

| Query | Hasil |
|---|---|
| `smartphone 3..7 juta` | HP dengan harga 3–7 juta |
| `film 2018..2023` | Film rilis 2018–2023 |

#### 10. before:/after: — Rentang Waktu

| Query | Hasil |
|---|---|
| `pemilu after:2024-01-01` | Halaman setelah 1 Jan 2024 |
| `bencana before:2023-12-31` | Halaman sebelum 31 Des 2023 |

---

### C. Perbandingan Mesin Pencari

| Aspek | Google | Bing | DuckDuckGo |
|---|---|---|---|
| **Pendiri** | Larry Page, Sergey Brin | Microsoft | Gabriel Weinberg |
| **Market share** | ~90% | ~4% | ~0,5% |
| **Pelacakan** | Melacak & menyimpan riwayat | Melacak | **Zero tracking** |
| **Iklan** | Berdasarkan riwayat pencarian | Berdasarkan riwayat | Berdasarkan kata kunci saja |
| **Fitur khas** | Featured Snippet, Knowledge Graph | Rewards points, video preview | !bang shortcuts, tema |
| **Hasil pencarian** | Personalisasi tinggi | Personalisasi sedang | Sama untuk semua |
| **Kecepatan** | Sangat cepat | Cepat | Cepat |

#### Kapan Pakai Yang Mana?

| Situasi | Rekomendasi |
|---|---|
| Ingin hasil paling relevan & personal | Google |
| Ingin hasil tanpa pelacakan privasi | DuckDuckGo |
| Ingin kumpulkan poin reward (Microsoft Rewards) | Bing |
| Riset akademik | Google Scholar |
| Mencari konten video | Google + YouTube |

---

### D. Studi Kasus: Merancang Query Efektif

**Situasi**: Kamu ingin mencari **jurnal ilmiah tentang dampak media sosial terhadap kesehatan mental remaja di Indonesia**, dalam **format PDF**, dari situs **universitas di Indonesia (.ac.id)**, tahun **2020–2025**.

**Query yang dirancang:**

```
"dampak media sosial" "kesehatan mental" remaja site:ac.id filetype:pdf after:2020
```

| Bagian Query | Fungsi |
|---|---|
| `"dampak media sosial"` | Frasa tepat (tidak terpisah) |
| `"kesehatan mental"` | Frasa tepat |
| `remaja` | Kata tambahan |
| `site:ac.id` | Domain akademik Indonesia |
| `filetype:pdf` | Hanya format PDF |
| `after:2020` | Terbit setelah 2020 |

**Latihan**: Ubah query di atas jika kamu ingin mencari di situs pemerintah (`.go.id`), format Word (`.docx`), tentang topik yang sama!

---

### E. Tips Pencarian Efektif

1. **Mulai dengan kata kunci sederhana**, lalu tambahkan operator jika hasil terlalu banyak
2. **Gunakan tanda kutip** untuk nama orang, judul, atau frasa spesifik
3. **Gunakan `-`** untuk mengecualikan topik yang tidak diinginkan
4. **Batasi domain** dengan `site:` untuk sumber terpercaya
5. **Gunakan `filetype:`** jika mencari dokumen (PDF, DOCX, XLSX)
6. **Coba mesin pencari yang berbeda** — Google tidak selalu yang terbaik untuk semua kasus
7. **Manfaatkan fitur Tools** → Time range untuk hasil terbaru

---

### F. Rangkuman

1. Mesin pencari bekerja dalam 3 tahap: **Crawling → Indexing → Ranking**.
2. **Operator pencarian** seperti `".."`, `site:`, `filetype:`, `OR`, `-` membuat pencarian lebih presisi.
3. **Google, Bing, dan DuckDuckGo** punya kelebihan masing-masing — pilih sesuai kebutuhan.
4. **Query yang baik** adalah yang menghasilkan informasi relevan di halaman pertama.

---

### G. Glosarium

| Istilah | Arti |
|---|---|
| **Crawler** | Program yang menjelajahi web untuk mengumpulkan halaman |
| **Indexing** | Proses menyusun katalog kata kunci dari halaman web |
| **Ranking** | Penentuan urutan hasil berdasarkan relevansi |
| **Query** | Kata kunci yang diketik di mesin pencari |
| **Operator Pencarian** | Simbol/kata khusus untuk mempersempit hasil |
| **PageRank** | Algoritma Google yang menilai pentingnya halaman dari link |
| **Featured Snippet** | Kotak jawaban langsung di atas hasil pencarian Google |

---

**MGMP Informatika SMAN 6 Cimahi**
