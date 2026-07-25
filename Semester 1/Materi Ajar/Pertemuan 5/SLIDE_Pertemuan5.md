---
marp: true
theme: uncover
class: invert
---

# PERTEMUAN 5
## Mesin Pencari Tingkat Lanjut
### Informatika – Fase E / Kelas X
#### SMA Negeri 6 Cimahi

---

## Review — Pertemuan 4

### Sistem Operasi
- **5 peran OS**: Proses, Memori, File, I/O, Antarmuka
- **Praktik**: Task Manager, File Explorer, CLI

> Sekarang kita bahas bagaimana **memanfaatkan internet secara cerdas**

---

## Apersepsi

**Coba cari `cara membuat kue nastar` di Google...**

Dalam **0,5 detik** muncul **jutaan hasil**.

> Bagaimana caranya Google tahu mana yang paling relevan?
> Apa bedanya kalau pakai tanda kutip?

---

# TUJUAN PEMBELAJARAN

1. ✅ Memahami cara kerja mesin pencari
2. ✅ Menggunakan **operator pencarian** (AND, OR, NOT, `""`, `site:`, `filetype:`)
3. ✅ Membandingkan **Google vs Bing vs DuckDuckGo**
4. ✅ Merancang query yang efektif

---

# CARA KERJA MESIN PENCARI

---

## Crawling → Indexing → Ranking

```
         Crawling              Indexing             Ranking
            │                     │                     │
            ▼                     ▼                     ▼
    ┌──────────────┐    ┌──────────────┐    ┌──────────────┐
    │   Googlebot  │    │    Indeks    │    │  Algoritma   │
    │  Menjelajahi │───→│  Katalog kata│───→│  PageRank +  │
    │  miliaran    │    │  kunci dari  │    │  200+ faktor │
    │  halaman web │    │  setiap web  │    │  relevansi   │
    └──────────────┘    └──────────────┘    └──────────────┘
```

---

## Crawling

**Web Crawler / Spider / Googlebot**

- Program otomatis yang menjelajahi web
- Mengikuti link dari satu halaman ke halaman lain
- Mengunjungi miliaran halaman setiap hari

> Seperti kamu browsing dari satu situs ke situs lain, tapi 24/7

---

## Indexing

**Menyusun Katalog Raksasa**

Setiap kata di setiap halaman dicatat beserta:
- Lokasinya (URL)
- Posisinya di halaman
- Metadata (judul, deskripsi)

> Seperti indeks di belakang buku — kamu bisa langsung tahu di halaman berapa kata tertentu berada

---

## Ranking

**Menentukan Urutan Hasil**

Faktor yang memengaruhi peringkat:
| Faktor | Pengaruh |
|---|---|
| PageRank (link masuk) | Tinggi |
| Kata kunci di judul | Tinggi |
| Kecepatan loading | Sedang |
| Mobile-friendly | Sedang |
| Freshness (kebaruan) | Rendah-Sedang |

---

# OPERATOR PENCARIAN

---

## 1. Tanda Kutip "..."

| Query | Hasil |
|---|---|
| `sistem komputer` | Kata sistem DAN komputer (tidak harus berurutan) |
| `"sistem komputer"` | Frasa PERSIS "sistem komputer" berurutan |

### Contoh:
- `"global warming"` → hanya halaman dengan frasa tepat itu
- `pemanasan global` → halaman dengan kata pemanasan DAN global (di mana saja)

---

## 2. AND, OR, NOT

| Operator | Contoh | Fungsi |
|---|---|---|
| **AND** | (otomatis) | Semua kata harus ada |
| `OR` / `\|` | `motor OR mobil` | Salah satu kata boleh muncul |
| `-` (NOT) | `kucing -anggora` | Kata setelah minus DILEWATKAN |

### Contoh:
- `sejarah AND budaya` → sama dengan `sejarah budaya`
- `film komedi OR horor` → film komedi ATAU horor
- `ikan -hiu` → ikan tapi bukan hiu

---

## 3. site: — Batasi Domain

| Query | Hasil |
|---|---|
| `site:kemendikbud.go.id kurikulum` | Hanya dari domain kemendikbud |
| `polusi site:ac.id` | Hanya dari universitas Indonesia |
| `covid site:who.int` | Hanya dari WHO |

> **Berguna untuk**: sumber terpercaya, riset akademik, info pemerintah

---

## 4. filetype: — Batasi Format

| Query | Hasil |
|---|---|
| `informatika filetype:pdf` | Hanya file PDF |
| `laporan filetype:xlsx` | Hanya file Excel |
| `proposal filetype:docx` | Hanya file Word |

> **Berguna untuk**: mencari jurnal, laporan, dokumen resmi

---

## 5. Operator Lainnya

| Operator | Contoh | Fungsi |
|---|---|---|
| `intitle:` | `intitle:von neumann` | Kata di judul halaman |
| `related:` | `related:kompas.com` | Situs serupa |
| `..` | `smartphone 3..7 juta` | Rentang harga |
| `after:` | `pemilu after:2024-01-01` | Setelah tanggal |

---

## Demo Langsung!

**Coba di browser masing-masing:**

1. `"sistem komputer" filetype:pdf`
2. `"sistem komputer" filetype:pdf site:ac.id`
3. `intitle:"sistem operasi" linux`
4. `smartphone 3..7 juta 2024`

---

# PRAKTIK 3 IN 1

---

## Praktik 1: Tanpa vs Dengan Operator

Buka Google, cari dan catat perbedaannya:

| Query | Jumlah Hasil |
|---|---|
| `sejarah komputer` | |
| `"sejarah komputer"` | |
| `"sejarah komputer" filetype:pdf` | |
| `"sejarah komputer" filetype:pdf site:ac.id` | |

---

## Praktik 2: Variabel Ganda

### Skenario:
> Cari jurnal tentang **dampak media sosial terhadap kesehatan mental remaja**, format **PDF**, dari **situs universitas (.ac.id)**

**Rancang query-nya!**

```
_______________________________________________
```

---

## Praktik 3: Google vs Bing vs DuckDuckGo

Topik: `"kecerdasan buatan" "pendidikan" filetype:pdf site:ac.id`

| Aspek | Google | Bing | DuckDuckGo |
|---|---|---|---|
| Jumlah hasil | | | |
| Hasil #1 | | | |
| Skor (1–5) | | | |

---

## Diskusi

1. **Operator mana yang paling berguna?**
2. **Apakah Google selalu lebih baik?**
3. **Kapan pakai tanda kutip?**

---

## Rangkuman

| No | Poin Penting |
|---|---|
| 1 | Mesin pencari: **Crawl → Index → Rank** |
| 2 | `"..."` = frasa tepat, `-` = kecualikan, `OR` = alternatif |
| 3 | `site:` = batasi domain, `filetype:` = batasi format |
| 4 | Google, Bing, DuckDuckGo punya kelebihan masing-masing |
| 5 | **Query yang baik** → hasil tepat di halaman pertama |

---

## Tugas Rumah

| Strategi | Query | Jumlah Hasil |
|---|---|---|
| Sederhana | | |
| Pakai operator | | |
| Mesin lain | | |

> Cari 1 topik pelajaran dengan **3 strategi berbeda**!

---

## Pertemuan Berikutnya

### Ekosistem Periksa Fakta & Membaca Lateral
> Bagaimana membedakan berita benar dan hoaks?

---

# Terima Kasih

### MGMP Informatika SMAN 6 Cimahi

> "Informasi adalah kekuatan. Tapi seperti kekuatan lainnya, yang terpenting adalah bagaimana menggunakannya."
