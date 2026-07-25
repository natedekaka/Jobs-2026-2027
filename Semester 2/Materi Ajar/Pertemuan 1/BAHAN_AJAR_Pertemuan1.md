# BAHAN AJAR – PERTEMUAN 1
## Konsep Struktur Data & Array

| TP | BK 1.1 |
|---|---|

---

### A. APA ITU STRUKTUR DATA?

**Struktur data** adalah cara komputer menyusun, menyimpan, dan mengelola data agar dapat digunakan secara efisien.

```
Data Mentah → Struktur Data → Algoritma → Solusi
```

#### Analogi: Perpustakaan

| Konsep | Analogi Perpustakaan |
|---|---|
| **Data** | Buku |
| **Struktur Data** | Cara buku disusun (berdasarkan genre, abjad, nomor) |
| **Algoritma** | Cara mencari buku (lihat rak A, cari abjad, dll) |

Tanpa struktur data, komputer akan kesulitan mengelola data — seperti perpustakaan tanpa rak, buku hanya ditumpuk di lantai.

#### Tiga Struktur Data Dasar Semester 2

| Struktur Data | Prinsip | Analogi |
|---|---|---|
| **Array / List** | Berurutan, indeks | Deretan loker, daftar belanja |
| **Stack** | LIFO (Last In First Out) | Tumpukan piring, undo |
| **Queue** | FIFO (First In First Out) | Antrian kasir, antrian printer |

---

### B. ARRAY — STRUKTUR DATA PALING DASAR

#### Definisi

Array adalah kumpulan elemen data dengan **tipe yang sama** yang disimpan secara **berurutan di memori**, di mana setiap elemen bisa diakses langsung melalui **indeks**.

#### Karakteristik Array

| Karakteristik | Keterangan |
|---|---|
| **Ukuran tetap** | Jumlah elemen ditentukan saat dibuat |
| **Indeks dimulai dari 0** | Elemen pertama: indeks 0 |
| **Tipe data seragam** | Semua elemen harus tipe sama (semua angka / semua teks) |
| **Akses acak (random access)** | Bisa langsung akses indeks tertentu tanpa perlu baca dari awal |
| **Alokasi memori berurutan** | Elemen bersebelahan di memori — cepat diakses |

#### Ilustrasi Array

**Array nilai ulangan 5 siswa:**
```
Indeks:    0     1     2     3     4
         ┌─────┬─────┬─────┬─────┬─────┐
Nilai:   │ 85  │ 90  │ 78  │ 92  │ 88  │
         └─────┴─────┴─────┴─────┴─────┘
```

- `nilai[0]` = 85 (data siswa pertama)
- `nilai[2]` = 78 (data siswa ketiga)
- `nilai[4]` = 88 (data siswa kelima)

#### Array dalam Kehidupan Sehari-hari

| Contoh | Array | Indeks |
|---|---|---|
| Daftar nama siswa | `["Andi", "Budi", "Cici"]` | 0, 1, 2 |
| Nomor kursi bioskop | `[1, 2, 3, ..., 50]` | 0–49 |
| Tanggal dalam sebulan | `[1, 2, 3, ..., 31]` | 0–30 |
| Skor game tertinggi | `[9800, 7500, 6200, 5000]` | 0, 1, 2, 3 |
| Warna lampu lalu lintas | `["merah", "kuning", "hijau"]` | 0, 1, 2 |

#### Operasi Dasar Array

| Operasi | Cara | Contoh |
|---|---|---|
| **Akses** | `nama_array[indeks]` | `nilai[2]` → 78 |
| **Ubah** | `nama_array[indeks] = nilai_baru` | `nilai[2] = 80` |
| **Cari** | Telusuri dari indeks 0 sampai ketemu | Cari nilai 92 → indeks 3 |

---

### C. PERBANDINGAN: ARRAY VS VARIABEL BIASA

| Aspek | Variabel Biasa | Array |
|---|---|---|
| Jumlah data | 1 nilai | Banyak nilai |
| Cara akses | Panggil nama | Panggil nama + indeks |
| Contoh | `nama = "Andi"` | `nama[0] = "Andi"`<br>`nama[1] = "Budi"` |
| Kegunaan | Data tunggal | Data jamak/berulang |

---

### D. MENGAPA STRUKTUR DATA PENTING?

| Alasan | Penjelasan |
|---|---|
| **Efisiensi** | Memori dan waktu proses lebih optimal |
| **Organisasi** | Data terstruktur, mudah dicari |
| **Skalabilitas** | Bisa menangani data besar (ribuan, jutaan) |
| **Dasar algoritma** | Semua algoritma butuh struktur data |

---

### E. RANGKUMAN

1. **Struktur data** = cara menyusun data di komputer
2. **Array** = kumpulan data sejenis dengan indeks (mulai dari 0)
3. Keuntungan array: akses cepat via indeks, penyimpanan berurutan
4. Contoh array: daftar nilai, daftar nama, nomor kursi

---

**MGMP Informatika SMAN 6 Cimahi**
