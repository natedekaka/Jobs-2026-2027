# MODUL AJAR INFORMATIKA – FASE E (KELAS X)

## Informasi Umum

| Komponen | Deskripsi |
|---|---|
| **Mata Pelajaran** | Informatika |
| **Fase / Kelas** | E / X |
| **Semester** | 1 (Ganjil) |
| **Pertemuan ke-** | 3 |
| **Alokasi Waktu** | 2 JP × 45 menit (90 menit) |
| **Tahun Pelajaran** | 2026/2027 |
| **Satuan Pendidikan** | **SMA Negeri 6 Cimahi** |

---

## Profil Pelajar Pancasila

| Dimensi | Indikator |
|---|---|
| Bernalar Kritis | Menganalisis alur data dari input hingga output dalam studi kasus nyata |
| Kreatif | Merancang simulasi IPO untuk kasus baru |
| Mandiri | Menyelesaikan simulasi dan LKPD secara bertanggung jawab |

---

## Sarana & Prasarana

| Sarana | Keterangan |
|---|---|
| Ruang kelas / Lab komputer | 1 komputer/laptop untuk demo plugged (opsional) |
| Kartu simulasi | Kartu alamat memori, kartu instruksi, kartu data (dicetak dari kertas karton) |
| Papan tulis + spidol warna | Untuk menggambar alur data |
| Alat peraga | Gelas/kotak untuk simulasi stack memori |
| LKPD & Bahan Ajar | Dicetak |

---

## Tujuan Pembelajaran (TP 1.6)

| TP | Indikator Ketercapaian Tujuan Pembelajaran (IKTP) |
|---|---|
| **BK 1.6:** Menyimulasikan dinamika Input-Proses-Output dalam sebuah komputer Von Neumann | 1.6.1 Menjelaskan langkah-langkah aliran data dari input ke output melalui CPU dan memori<br>1.6.2 Melakukan simulasi unplugged pembacaan data dari input, penyimpanan di alamat memori, pemrosesan di CPU, dan pengiriman ke output<br>1.6.3 Menganalisis studi kasus alur IPO pada aplikasi sehari-hari |

---

## Peta Kompetensi (Pertemuan 3)

```
Pertemuan 3 — Simulasi Dinamika IPO
│
├── Review (10 menit)
│   ├── Review diagram Von Neumann (tugas rumah pertemuan 2)
│   └── Apersepsi: "Bagaimana data berjalan di dalam komputer?"
│
├── Inti (65 menit)
│   ├── Memahami (15 menit)
│   │   ├── Konsep alamat memori dan pengalamatan
│   │   ├── Bagaimana CPU membaca/menulis ke memori
│   │   └── Peran clock speed dalam sinkronisasi
│   │
│   ├── Mengaplikasi (35 menit)
│   │   ├── Simulasi 1: "Pos Indonesia" — alamat memori
│   │   └── Simulasi 2: "Eksekusi Program Sederhana" — simulasi lengkap IPO
│   │
│   └── Merefleksi (15 menit)
│       ├── Diskusi hasil simulasi
│       └── Refleksi individu
│
└── Penutup (15 menit)
    ├── Kesimpulan
    ├── Tugas
    └── Doa & salam
```

---

## Langkah Pembelajaran

### Pembukaan (10 menit)

| Kegiatan | Waktu |
|---|---|
| 1. Salam, doa, cek kehadiran | 2 menit |
| 2. **Review tugas**: 3 siswa diminta menunjukkan diagram Von Neumann buatannya — guru memberi apresiasi dan koreksi | 5 menit |
| 3. **Apersepsi**: Guru menunjukkan gelas kosong dan beberapa kertas bertuliskan angka. "Kalau gelas ini adalah memori (RAM), dan kertas ini adalah data — bagaimana cara CPU menaruh data dan mengambilnya kembali?" | 3 menit |

### Inti (65 menit)

#### Memahami (berkesadaran, menggembirakan) — 15 menit

1. **Konsep Alamat Memori (8 menit)**
   - Guru menjelaskan dengan analogi **kompleks perumahan**:
     - Memori = kompleks perumahan (banyak rumah)
     - Alamat memori = nomor rumah (0, 1, 2, 3, ...)
     - Data = orang yang tinggal di rumah
     - CPU = kurir yang mengantar/mengambil barang dari rumah-rumah
   - **Dua operasi dasar CPU terhadap memori**:
     - **READ (Load)**: CPU membaca data dari suatu alamat memori → data disalin ke CPU (data di memori tetap ada)
     - **WRITE (Store)**: CPU menulis data ke suatu alamat memori → data lama dihapus, diganti data baru

   ```
   MEMORI (RAM) — seperti deretan loker:
   ┌─────┬─────┬─────┬─────┬─────┬─────┐
   │  7  │  3  │  0  │  5  │  2  │  9  │
   ├─────┼─────┼─────┼─────┼─────┼─────┤
   │  0  │  1  │  2  │  3  │  4  │  5  │ ← Alamat
   └─────┴─────┴─────┴─────┴─────┴─────┘
   ```

2. **Clock Speed & Sinkronisasi (7 menit)**
   - CPU bekerja berdasarkan **detak clock** (clock cycle)
   - 1 clock cycle = 1 langkah dasar (fetch, decode, execute, dll)
   - Semakin tinggi clock speed (GHz), semakin cepat eksekusi
   - Analogi: **drum dalam marching band** — semua pemain bergerak mengikuti irama drum
   - Guru mendemonstrasikan: tepuk tangan berirama tetap, siswa menjalankan simulasi mengikuti tepukan

#### Mengaplikasi (bermakna, menggembirakan) — 35 menit

3. **Simulasi 1: "Pos Indonesia" — Memahami Alamat Memori (15 menit)**
   - **Persiapan**: Siapkan 10 kartu/kotak bernomor 0–9 di lantai/meja (sebagai memori)
   - Setiap kotak berisi sebuah angka (data)
   - **Peran**:
     - 1 siswa sebagai **CPU** (memegang kartu instruksi)
     - 1 siswa sebagai **Control Unit** (membaca instruksi dan memberi komando)
     - 1 siswa sebagai **ALU** (menghitung jika diperlukan)
     - Siswa lain sebagai **Bus** (mengantarkan data antar komponen) — opsional
   - **Instruksi 1 — READ**: "Baca data dari alamat 3"
     - CU membaca instruksi → mengirim perintah ke Bus → Bus mengambil data dari alamat 3 → dikirim ke CPU
   - **Instruksi 2 — WRITE**: "Tulis angka 15 ke alamat 7"
     - CPU mengirim data 15 → Bus membawanya ke alamat 7 → data lama di alamat 7 diganti

4. **Simulasi 2: "Eksekusi Program Sederhana" (20 menit)**
   - **Skenario**: Program menghitung `(5 + 3) × 2`
   - **Persiapan memori** (data di papan tulis):

     | Alamat | Isi | Keterangan |
     |---|---|---|
     | 0 | LOAD 5 | Instruksi: ambil data dari alamat 5 |
     | 1 | LOAD 6 | Instruksi: ambil data dari alamat 6 |
     | 2 | ADD | Instruksi: jumlahkan kedua data |
     | 3 | STORE 7 | Instruksi: simpan hasil ke alamat 7 |
     | 4 | HALT | Instruksi: berhenti |
     | 5 | 5 | Data |
     | 6 | 3 | Data |
     | 7 | (kosong) | Tempat hasil |
     | 8 | 2 | Data |

   - **Alur simulasi langkah demi langkah**:
     1. **Fetch**: CU membaca alamat 0 → "LOAD 5"
     2. **Decode**: CU menerjemahkan "ambil data dari alamat 5"
     3. **Execute**: Data dari alamat 5 (nilai 5) → Register A di CPU
     4. **Fetch**: CU membaca alamat 1 → "LOAD 6"
     5. **Execute**: Data dari alamat 6 (nilai 3) → Register B di CPU
     6. **Fetch**: CU membaca alamat 2 → "ADD"
     7. **Execute**: ALU menghitung A + B = 5 + 3 = 8
     8. **Fetch**: CU membaca alamat 3 → "STORE 7"
     9. **Execute**: Hasil 8 → ditulis ke alamat 7
     10. **Fetch**: CU membaca alamat 4 → "HALT"
     11. Program selesai.

   - **Peran siswa**:
     - 1 siswa sebagai **PC (Program Counter)** — menunjuk alamat yang sedang diakses
     - 1 siswa sebagai **CU** — membaca instruksi dari memori
     - 1 siswa sebagai **ALU** — menghitung
     - 1 siswa sebagai **Register A** — menyimpan data pertama
     - 1 siswa sebagai **Register B** — menyimpan data kedua
     - 1 siswa sebagai **Memori** — memegang/menulis data di papan

   - Seluruh kelas mengikuti alur dengan panduan LKPD

#### Merefleksi (berkesadaran, bermakna) — 15 menit

5. **Diskusi Hasil Simulasi (8 menit)**
   - Pertanyaan diskusi:
     - "Apa yang terjadi jika alamat 5 tidak berisi data 5 tetapi berisi 100?"
     - "Mengapa kita perlu Register di dalam CPU? Kenapa tidak langsung ambil dari memori setiap kali?"
     - "Dalam simulasi tadi, proses mana yang paling lambat?"
   - Guru menjelaskan **prinsip kerja pipeline** (sedikit gambaran): CPU bisa melakukan fetch instruksi berikutnya sambil mengeksekusi instruksi saat ini

6. **Refleksi Individu (7 menit)**
   - Siswa menulis refleksi di LKPD:
     - "Bagian simulasi mana yang paling seru?"
     - "Apa perbedaan utama READ dengan WRITE?"
     - "Skala 1–10, seberapa paham kamu tentang cara kerja CPU?"

### Penutup (15 menit)

| Kegiatan | Waktu |
|---|---|
| 1. Guru merangkum: "Dinamika IPO melibatkan Fetch → Decode → Execute → Store — data berpindah antara memori dan CPU melalui bus" | 3 menit |
| 2. Tanya jawab / klarifikasi | 5 menit |
| 3. Menyampaikan pertemuan berikutnya: **Sistem Operasi & Perannya** | 2 menit |
| 4. **Tugas**: Tuliskan langkah demi langkah alur IPO untuk kasus "Menghitung rata-rata 3 nilai ulangan" — gunakan format tabel seperti simulasi tadi | 3 menit |
| 5. Doa & salam | 2 menit |

---

## Asesmen

### 1. Asesmen Formatif — Observasi Simulasi

| Indikator | 1 (Perlu Perbaikan) | 2 (Cukup) | 3 (Baik) | 4 (Sangat Baik) |
|---|---|---|---|---|
| Memahami peran dalam simulasi | Tidak paham peran | Paham setelah dijelaskan ulang | Paham peran dan menjalankan dengan benar | Paham peran dan mampu menjelaskan ke teman |
| Mengikuti urutan Fetch-Decode-Execute | Urutan kacau | Urutan benar dengan bimbingan | Urutan benar mandiri | Urutan benar dan tepat waktu |
| Memahami perbedaan READ dan WRITE | Tidak bisa membedakan | Bisa membedakan tapi belum tepat | Bisa membedakan dengan benar | Bisa membedakan dan memberi contoh |

### 2. Asesmen Formatif — LKPD

| Kriteria | Skor (1–4) |
|---|---|
| Kelengkapan tabel alur simulasi | |
| Kebenaran analisis studi kasus | |
| Refleksi (jujur dan relevan) | |

---

## Lampiran

| Kode | Nama File | Deskripsi |
|---|---|---|
| LKPD-03 | LKPD_Pertemuan3 | Lembar Kerja (tabel simulasi, studi kasus, refleksi) |
| BA-03 | Bahan_Ajar_Pertemuan3 | Materi: alamat memori, siklus eksekusi, simulasi program |
| AS-03 | Asesmen_Pertemuan3 | Instrumen observasi + rubrik |
| SL-03 | Slide_Pertemuan3 | Presentasi + panduan simulasi |

---

**MGMP Informatika SMAN 6 Cimahi**
