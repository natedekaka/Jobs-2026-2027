# MODUL AJAR INFORMATIKA – FASE E (KELAS X)

## Informasi Umum

| Komponen | Deskripsi |
|---|---|
| **Mata Pelajaran** | Informatika |
| **Fase / Kelas** | E / X |
| **Semester** | 2 (Genap) |
| **Pertemuan ke-** | 1 |
| **Alokasi Waktu** | 2 JP × 45 menit (90 menit) |
| **Tahun Pelajaran** | 2026/2027 |
| **Satuan Pendidikan** | **SMA Negeri 6 Cimahi** |

---

## Profil Pelajar Pancasila

| Dimensi | Indikator |
|---|---|
| Bernalar Kritis | Menganalisis struktur data dalam kehidupan sehari-hari |
| Kreatif | Membuat mind map struktur data |
| Mandiri | Merefleksikan perkembangan belajar dari S1 ke S2 |

---

## Sarana & Prasarana

| Sarana | Keterangan |
|---|---|
| Lab komputer / laptop | 1 unit per 2 siswa (untuk Python nanti) |
| Proyektor / LCD | Untuk presentasi |
| Kartu/alat peraga | Untuk simulasi array (kertas/karton) |

---

## Tujuan Pembelajaran (TP 1.1)

| TP | Indikator Ketercapaian Tujuan Pembelajaran (IKTP) |
|---|---|
| **BK 1.1:** Memahami konsep struktur data dasar dan hubungannya dengan algoritma | 1.1.1 Menjelaskan pengertian struktur data dan mengapa penting<br>1.1.2 Mengidentifikasi struktur data dalam kehidupan sehari-hari<br>1.1.3 Menjelaskan konsep array/list: indeks, elemen, alokasi memori berurutan<br>1.1.4 Menganalisis kemiripan array dengan daftar dalam kehidupan nyata |

---

## Peta Kompetensi

```
Pertemuan 1 S2 — Pendahuluan & Konsep Struktur Data (Array/List)
│
├── Pendahuluan (15 menit)
│   ├── Selamat datang S2: review hasil S1 & gambaran S2
│   ├── Apersepsi: "Apa itu data? Bagaimana komputer menyimpannya?"
│   └── Analogi: lemari arsip, daftar belanja, rak buku
│
├── Inti (60 menit)
│   ├── Memahami (20 menit)
│   │   ├── Definisi struktur data
│   │   ├── Array: definisi, indeks, elemen
│   │   └── Analogi & contoh nyata
│   │
│   ├── Mengaplikasi (30 menit)
│   │   ├── [15'] Simulasi array dengan kartu
│   │   └── [15'] Mind map struktur data
│   │
│   └── Merefleksi (10 menit)
│       └── Presentasi mind map + refleksi
│
└── Penutup (15 menit)
```

---

## Langkah Pembelajaran

### Pembukaan (15 menit)

| Kegiatan | Waktu |
|---|---|
| 1. Salam, doa, cek kehadiran | 2 menit |
| 2. **Selamat datang semester 2**: Review singkat hasil S1 — nilai PAS, portofolio, pencapaian kelas. | 5 menit |
| 3. **Gambaran S2**: "Semester 2 kita akan jadi **problem solver** — belajar struktur data, algoritma, pseudocode, dan Python!" Tunjukkan roadmap 15 pertemuan | 5 menit |
| 4. **Apersepsi**: "Bayangkan kamu punya 1000 buku. Bagaimana cara menyimpannya agar mudah dicari kembali? Itulah yang dipelajari di struktur data!" | 3 menit |

### Inti (60 menit)

#### Memahami (berkesadaran, menggembirakan) — 20 menit

1. **Apa itu Struktur Data? (5 menit)**
   - **Definisi**: Cara komputer menyusun, menyimpan, dan mengelola data agar efisien
   - **Analogi**: Rak buku (struktur data) → cara buku disusun (array, stack, queue) → memudahkan cari buku (algoritma)
   - **Mengapa penting?**: Data → butuh struktur → baru diproses dengan algoritma
   - **Tiga struktur data dasar S2**: Array/List, Stack, Queue

2. **Array/List — Struktur Data Paling Dasar (10 menit)**

   | Konsep | Penjelasan | Analogi |
   |---|---|---|
   | **Array** | Kumpulan data dengan tipe sama, disimpan berurutan di memori | Deretan loker bernomor |
   | **Indeks** | Posisi data dalam array, dimulai dari 0 | Nomor loker |
   | **Elemen** | Data yang disimpan di setiap posisi | Isi setiap loker |
   | **Ukuran tetap** | Array punya kapasitas tetap (fixed size) | Loker tetap 10 pintu |

   **Ilustrasi array nilai [85, 90, 78, 92, 88]:**
   ```
   Indeks:    0    1    2    3    4
            ┌────┬────┬────┬────┬────┐
   Nilai:   │ 85 │ 90 │ 78 │ 92 │ 88 │
            └────┴────┴────┴────┴────┘
   ```

3. **Contoh Array dalam Kehidupan (5 menit)**
   | Contoh | Array |
   |---|---|
   | Daftar nilai ulangan | Array of integers |
   | Daftar nama siswa | Array of strings |
   | Nomor kursi di bus | Array of integers (0–49) |
   | Tanggal dalam sebulan | Array 31 elemen |
   | Pixel gambar | Array 2 dimensi |

#### Mengaplikasi (bermakna, menggembirakan) — 30 menit

4. **Aktivitas 1: Simulasi Array dengan Kartu (15 menit) — Berpasangan**

   **Alat:** 10 kartu/kertas kecil bernomor 0–9

   **Tugas:**
   | Langkah | Kegiatan |
   |---|---|
   | 1. Urutkan 10 kartu secara berjajar | Buat "array" dengan indeks 0–9 |
   | 2. Guru menyebut indeks → siswa tunjuk kartu | Latihan mengakses elemen via indeks |
   | 3. Guru menyebut nilai → siswa cari di indeks berapa | Latihan konsep indeks |
   | 4. Ambil kartu posisi 3 → apa yang terjadi dengan posisi lain? | Diskusi: "Hapus" dari array |

   **Diskusi:**
   - "Bagaimana rasanya mencari kartu di posisi tertentu?"
   - "Apa yang terjadi jika ingin menyisipkan kartu baru di tengah?"
   - "Kenapa array disebut struktur data paling sederhana?"

5. **Aktivitas 2: Mind Map Struktur Data (15 menit) — Individu**

   **Tugas:** Buat mind map (di kertas / canva / draw.io) tentang struktur data yang mencakup:

   ```
                    ┌──────────────┐
                    │ STRUKTUR DATA │
                    └──────────────┘
                           │
            ┌──────────────┼──────────────┐
            │              │              │
        ┌──────┐      ┌──────┐      ┌──────┐
        │Array │      │Stack │      │Queue │
        │/List │      │LIFO  │      │FIFO  │
        └──────┘      └──────┘      └──────┘
            │              │              │
    ┌───────┼───────┐ ┌───┴───┐   ┌───┴───┐
    │Definisi│Contoh │ │Push Pop│  │Enqueue │
    │Indeks  │nyata  │ │Undo   │  │Dequeue │
    │Elemen  │       │ │Browser│  │Antrian │
    └───────┴───────┘ └───────┘   └───────┘
   ```

   **Diferensiasi:**
   - **Pemula**: Fokus pada array saja, minimal 5 cabang
   - **Mahir**: Tambahkan perbandingan array, stack, queue (persamaan & perbedaan)

#### Merefleksi (berkesadaran, bermakna) — 10 menit

6. **Presentasi Mind Map (5 menit)**
   - 3 siswa presentasi mind mapnya @1,5 menit
   - Tunjukkan: definisi, contoh array favorit, kesamaan dengan kehidupan

7. **Refleksi Individu (5 menit)**
   - "Apa perbedaan utama menyimpan data di array vs di buku catatan?"
   - "Satu analogi array yang paling membantu pemahamanmu"
   - Skala pemahaman: ___ / 10

### Penutup (15 menit)

| Kegiatan | Waktu |
|---|---|
| 1. Rangkuman: "Array = kumpulan data dengan indeks. Indeks dimulai dari 0. Elemen diakses via indeks." | 3 menit |
| 2. Tanya jawab | 5 menit |
| 3. **Tugas**: Cari 3 contoh array di kehidupan sehari-hari selain dari materi — tulis di buku | 3 menit |
| 4. Sampaikan pertemuan depan: **Stack (Tumpukan)** — bawa 5 buku/kardus kecil untuk simulasi | 2 menit |
| 5. Doa & salam | 2 menit |

---

## Asesmen

### Rubrik Formatif

| Kriteria | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| **Simulasi array** | Tidak ikut | Ikut pasif | Ikut aktif | Aktif + menjelaskan ke pasangan |
| **Mind map** | Tidak buat | Minimal (3 cabang) | Lengkap (≥5 cabang) | Lengkap + perbandingan + rapi |
| **Contoh array** | Tidak bisa | 1 contoh | 2 contoh | 3 contoh + analisis |

---

**MGMP Informatika SMAN 6 Cimahi**
