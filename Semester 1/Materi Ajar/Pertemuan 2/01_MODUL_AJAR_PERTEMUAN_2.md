# MODUL AJAR INFORMATIKA – FASE E (KELAS X)

## Informasi Umum

| Komponen | Deskripsi |
|---|---|
| **Mata Pelajaran** | Informatika |
| **Fase / Kelas** | E / X (Sepuluh) |
| **Semester** | 1 (Ganjil) |
| **Pertemuan ke-** | 2 |
| **Alokasi Waktu** | 2 JP × 45 menit (90 menit) |
| **Tahun Pelajaran** | 2026/2027 |
| **Satuan Pendidikan** | **SMA Negeri 6 Cimahi** |

---

## Profil Pelajar Pancasila

| Dimensi | Indikator |
|---|---|
| Bernalar Kritis | Menganalisis alur data dalam arsitektur Von Neumann |
| Kreatif | Merancang simulasi sederhana alur IPO |
| Mandiri | Menyelesaikan LKPD secara bertanggung jawab |

---

## Sarana & Prasarana

| Sarana | Keterangan |
|---|---|
| Ruang kelas / Lab komputer | Dilengkapi proyektor/LCD |
| Kartu/kertas simulasi | Untuk simulasi unplugged (kartu alamat memori, instruksi) |
| Papan tulis / whiteboard | Untuk gambar diagram Von Neumann |
| Alat tulis | Spidol warna, sticky notes |
| LKPD & Bahan Ajar | Dicetak atau digital |

---

## Tujuan Pembelajaran (TP 1.5, 1.6)

| TP | Indikator Ketercapaian Tujuan Pembelajaran (IKTP) |
|---|---|
| **BK 1.5:** Memahami model komputer Von Neumann | 1.5.1 Menjelaskan arsitektur Von Neumann dan komponen utamanya (Input, CPU, Memori, Output)<br>1.5.2 Menggambarkan diagram blok arsitektur Von Neumann |
| **BK 1.6:** Menyimulasikan dinamika Input-Proses-Output dalam sebuah komputer Von Neumann | 1.6.1 Menjelaskan alur data dari input hingga output<br>1.6.2 Melakukan simulasi sederhana alur IPO secara unplugged |

---

## Peta Kompetensi (Pertemuan 2)

```
Pertemuan 2 — Model Von Neumann & IPO
│
├── Bagian 1: Pendahuluan & Review (15 menit)
│   ├── Review pertemuan 1
│   ├── Apersepsi: "Bagaimana data bergerak di dalam komputer?"
│   └── Tujuan pembelajaran hari ini
│
├── Bagian 2: Inti (60 menit)
│   ├── Memahami (20 menit)
│   │   ├── Sejarah singkat arsitektur Von Neumann
│   │   ├── Diagram blok: Input → CPU (ALU+CU) → Memori → Output
│   │   └── Konsep program tersimpan (stored program concept)
│   │
│   ├── Mengaplikasi (25 menit)
│   │   ├── Simulasi unplugged: "Manusia Komputer"
│   │   └── LKPD: menggambar & menjelaskan alur IPO
│   │
│   └── Merefleksi (15 menit)
│       ├── Diskusi hasil simulasi
│       └── Refleksi individu
│
└── Bagian 3: Penutup (15 menit)
    ├── Kesimpulan
    ├── Tugas & tindak lanjut
    └── Doa & salam
```

---

## Langkah Pembelajaran

### Pembukaan (15 menit)

| Kegiatan | Waktu |
|---|---|
| 1. Salam, doa, cek kehadiran | 2 menit |
| 2. **Review kilat**: Guru menunjuk 2–3 siswa untuk menyebutkan 1 komponen komputer dan fungsinya (dari pertemuan 1) | 5 menit |
| 3. **Apersepsi**: "Kalau kalian mengetik di keyboard, bagaimana huruf itu bisa muncul di layar? Coba tebak jalurnya!" | 5 menit |
| 4. Menyampaikan tujuan pembelajaran pertemuan ini | 3 menit |

### Bagian Inti (60 menit)

#### Memahami (berkesadaran, menggembirakan) — 20 menit

1. **Paparan Konsep – Arsitektur Von Neumann (10 menit)**
   - Guru menjelaskan dengan slide/diagram:
     - **Sejarah singkat**: John von Neumann (1945) — arsitektur yang masih dipakai komputer modern
     - **Komponen utama Von Neumann**:
       - **CPU** (ALU + Control Unit)
       - **Memori** (menyimpan data dan instruksi)
       - **Unit Input**
       - **Unit Output**
       - **Bus** (jalur data antar komponen)
     - **Konsep Program Tersimpan (Stored Program Concept)**: instruksi dan data disimpan di memori yang sama
   - Guru menggambar diagram Von Neumann di papan tulis secara bertahap:

     ```
     ┌──────────┐     ┌─────────────────────┐     ┌──────────┐
     │  INPUT   │────→│        CPU          │────→│  OUTPUT  │
     │(Keyboard)│     │  ┌───────┬───────┐  │     │(Monitor) │
     └──────────┘     │  │ ALU  │  CU   │  │     └──────────┘
                      │  └───┬───┴───┬───┘  │
                      └──────┼───────┼──────┘
                             │       │
                             ▼       ▼
                      ┌──────────────────┐
                      │     MEMORI      │
                      │  (RAM/ROM)      │
                      └──────────────────┘
     ```

2. **Penjelasan Alur IPO (10 menit)**
   - Guru menjelaskan dengan contoh konkret:
     - **Contoh 1 — Menekan tombol 'A'**:
       1. Keyboard mengirim sinyal ke CPU
       2. CPU menerjemahkan sinyal ke kode ASCII
       3. Data disimpan di RAM
       4. Hasil dikirim ke monitor
     - **Contoh 2 — Membuka aplikasi**:
       1. Klik ikon (Input)
       2. CPU membaca instruksi dari Hard Disk ke RAM
       3. CPU mengeksekusi instruksi
       4. Tampilan aplikasi muncul di layar (Output)
   - Perkenalkan istilah **Bus**: jalur yang menghubungkan komponen

#### Mengaplikasi (bermakna, menggembirakan) — 25 menit

3. **Simulasi Unplugged: "Manusia Komputer" (15 menit)**
   - 5 siswa maju ke depan, masing-masing memerankan:
     - **Siswa A**: Unit Input (membaca kartu perintah)
     - **Siswa B**: Control Unit (mengatur jalannya proses)
     - **Siswa C**: ALU (melakukan perhitungan)
     - **Siswa D**: Memori (menyimpan data sementara di papan tulis)
     - **Siswa E**: Unit Output (mengumumkan hasil)
   - Guru memberikan kartu instruksi: "Hitung 5 + 3"
   - Alur simulasi:
     1. Input membaca: "Hitung 5 + 3"
     2. Control Unit menginstruksikan ALU untuk menghitung
     3. ALU menghitung → hasil "8"
     4. Hasil disimpan di Memori
     5. Output mengumumkan: "Hasilnya adalah 8"
   - Ulangi dengan instruksi berbeda (misal: "Cari nilai terbesar dari [7, 2, 9]")
   - Siswa yang tidak maju mengamati dan mencatat alur di LKPD

4. **Mengerjakan LKPD (10 menit)**
   - Siswa secara individu mengerjakan LKPD:
     - Menggambar diagram Von Neumann
     - Menjelaskan alur IPO untuk 2 studi kasus
     - Menjawab soal analisis

#### Merefleksi (berkesadaran, bermakna) — 15 menit

5. **Diskusi Hasil Simulasi (8 menit)**
   - Tanya jawab:
     - "Apa yang terjadi jika Memori (siswa D) tidak bekerja?"
     - "Apa peran Control Unit dalam simulasi tadi?"
     - "Mengapa data harus melewati CPU dulu sebelum ke output?"
   - Guru memberikan penguatan konsep

6. **Refleksi Individu (7 menit)**
   - Siswa menulis di buku catatan/LKPD:
     - "Apa beda arsitektur Von Neumann dengan sistem komputer biasa?"
     - "Saya paham/belum paham tentang..."
     - "Skala 1–10, seberapa paham saya hari ini?"

### Penutup (15 menit)

| Kegiatan | Waktu |
|---|---|
| 1. Guru merangkum: "Arsitektur Von Neumann = Input → CPU (ALU+CU) → Memori → Output" | 3 menit |
| 2. Tanya jawab / klarifikasi | 5 menit |
| 3. Menyampaikan pertemuan berikutnya: "Simulasi Dinamika IPO — kita akan praktik langsung!" | 2 menit |
| 4. **Tugas**: Baca bahan ajar pertemuan 2 dan buat diagram Von Neumann versi kalian sendiri di kertas A4 (dikumpulkan pertemuan depan) | 3 menit |
| 5. Doa & salam | 2 menit |

---

## Asesmen

### 1. Asesmen Formatif — Observasi Simulasi

| Indikator | Perlu Perbaikan (1) | Cukup (2) | Baik (3) | Sangat Baik (4) |
|---|---|---|---|---|
| Memahami peran masing-masing komponen | Tidak paham perannya | Paham perannya sendiri | Paham peran sendiri + kaitannya | Memandu teman yang lain |
| Menjalankan simulasi sesuai urutan IPO | Urutan kacau | Urutan benar dengan bantuan | Urutan benar mandiri | Urutan benar + menjelaskan ke teman |
| Kerja sama tim | Tidak mau bekerja sama | Kerja sama pasif | Aktif berkontribusi | Memimpin kelompok |

### 2. Asesmen Formatif — LKPD

| Kriteria | Skor (1–4) |
|---|---|
| Diagram Von Neumann lengkap dan benar | |
| Penjelasan alur IPO logis dan tepat | |
| Jawaban analisis tepat | |
| **Total (3–12)** | |

---

## Lampiran

| Kode | Nama File | Deskripsi |
|---|---|---|
| LKPD-02 | LKPD_Pertemuan2 | Lembar Kerja Peserta Didik |
| BA-02 | Bahan_Ajar_Pertemuan2 | Materi bacaan arsitektur Von Neumann & IPO |
| AS-02 | Asesmen_Pertemuan2 | Instrumen asesmen formatif |
| SL-02 | Slide_Pertemuan2 | Materi presentasi |

---

**MGMP Informatika SMAN 6 Cimahi**
