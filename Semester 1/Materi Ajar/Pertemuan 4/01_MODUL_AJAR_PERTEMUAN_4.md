# MODUL AJAR INFORMATIKA – FASE E (KELAS X)

## Informasi Umum

| Komponen | Deskripsi |
|---|---|
| **Mata Pelajaran** | Informatika |
| **Fase / Kelas** | E / X |
| **Semester** | 1 (Ganjil) |
| **Pertemuan ke-** | 4 |
| **Alokasi Waktu** | 2 JP × 45 menit (90 menit) |
| **Tahun Pelajaran** | 2026/2027 |
| **Satuan Pendidikan** | **SMA Negeri 6 Cimahi** |

---

## Profil Pelajar Pancasila

| Dimensi | Indikator |
|---|---|
| Bernalar Kritis | Menganalisis peran sistem operasi dalam pengelolaan sumber daya komputer |
| Mandiri | Menjelajahi fitur sistem operasi secara mandiri (Task Manager, File Explorer, CLI) |
| Gotong Royong | Berdiskusi dan berbagi temuan dalam praktik eksplorasi OS |

---

## Sarana & Prasarana

| Sarana | Keterangan |
|---|---|
| Lab komputer / laptop | 1 unit per 2 siswa (untuk praktik) |
| Proyektor / LCD | Untuk demo guru |
| Sistem Operasi | Windows 10/11 atau Linux (mint/ubuntu) |
| Aplikasi | Task Manager, File Explorer/Terminal, pengolah teks (Notepad) |
| LKPD & Bahan Ajar | Dicetak |

---

## Tujuan Pembelajaran (TP 1.7)

| TP | Indikator Ketercapaian Tujuan Pembelajaran (IKTP) |
|---|---|
| **BK 1.7:** Memahami peran sistem operasi | 1.7.1 Menjelaskan pengertian dan fungsi sistem operasi<br>1.7.2 Mengidentifikasi jenis-jenis sistem operasi (desktop, mobile, embedded, server)<br>1.7.3 Menjelaskan peran OS dalam pengelolaan memori, proses, file, dan antarmuka pengguna<br>1.7.4 Mendemonstrasikan penggunaan fitur dasar OS (Task Manager, File Explorer, CLI) |

---

## Peta Kompetensi (Pertemuan 4)

```
Pertemuan 4 — Sistem Operasi & Perannya
│
├── Pendahuluan (10 menit)
│   ├── Review pertemuan 3 (simulasi IPO)
│   └── Apersepsi: "Siapa yang mengatur semua proses di komputer?"
│
├── Inti (65 menit)
│   ├── Memahami (25 menit)
│   │   ├── Definisi & sejarah OS
│   │   ├── Model lapisan bawang sistem komputer
│   │   ├── Jenis-jenis OS (desktop, mobile, embedded, server)
│   │   └── 5 peran utama OS
│   │
│   ├── Mengaplikasi (30 menit)
│   │   ├── Praktik 1: Task Manager (mengamati proses & memori)
│   │   ├── Praktik 2: File Explorer (navigasi file system)
│   │   └── Praktik 3: CLI sederhana (command line)
│   │
│   └── Merefleksi (10 menit)
│       └── Diskusi hasil praktik
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
| 2. **Review**: "Kemarin kita simulasi eksekusi program. Siapa yang mengatur urutan instruksi di CPU?" (jawaban: Control Unit). "Tapi siapa yang mengatur seluruh program yang berjalan BERSAMAAN di komputer?" (jawaban: Sistem Operasi) | 5 menit |
| 3. **Apersepsi**: Guru bertanya — "Komputer bisa menjalankan banyak aplikasi sekaligus: Chrome, Word, Spotify. Siapa yang mengatur agar semuanya berjalan lancar tanpa saling mengganggu?" | 3 menit |

### Inti (65 menit)

#### Memahami (berkesadaran, menggembirakan) — 25 menit

1. **Apa Itu Sistem Operasi? (5 menit)**
   - Definisi: **Sistem Operasi (OS)** adalah perangkat lunak sistem yang mengelola sumber daya hardware dan software komputer, serta menyediakan layanan umum untuk program aplikasi.
   - OS adalah **jembatan antara hardware, software, dan pengguna**
   - Contoh: Windows, macOS, Linux, Android, iOS

2. **Model Lapisan Bawang Sistem Komputer (7 menit)**
   - Guru menggambar/modelkan sistem komputer sebagai lapisan bawang:

     ```
     ┌─────────────────────────────────────┐
     │          PENGGUNA (User)            │
     │    (Aplikasi: Chrome, Word, Game)   │
     ├─────────────────────────────────────┤
     │         SISTEM OPERASI              │
     │  (Windows, Linux, macOS, Android)   │
     ├─────────────────────────────────────┤
     │            HARDWARE                 │
     │  (CPU, RAM, HDD, Keyboard, Monitor) │
     └─────────────────────────────────────┘
     ```

   - Penjelasan setiap lapisan:
     - **Lapisan 1 — Hardware**: Komponen fisik (CPU, RAM, dll) — bahasa mesin
     - **Lapisan 2 — Sistem Operasi**: Menyembunyikan kompleksitas hardware, menyediakan API untuk aplikasi
     - **Lapisan 3 — Pengguna/Aplikasi**: Berinteraksi dengan OS melalui GUI atau CLI

3. **Jenis-Jenis Sistem Operasi (5 menit)**

   | Jenis | Contoh | Karakteristik |
   |---|---|---|
   | **Desktop** | Windows, macOS, Linux (Ubuntu) | GUI, multitasking, untuk PC/laptop |
   | **Mobile** | Android, iOS | Touchscreen, portabel, hemat daya |
   | **Server** | Ubuntu Server, Windows Server | Tahan lama, headless, fokus layanan jaringan |
   | **Embedded** | RTOS, firmware TV/AC/kulkas | Tertanam di perangkat khusus, sumber daya terbatas |
   | **Real-Time** | VxWorks | Respon dalam waktu yang terjamin (sistem medis, pesawat) |

4. **Lima Peran Utama Sistem Operasi (8 menit)**

   | Peran | Deskripsi | Analogi |
   |---|---|---|
   | **1. Manajemen Proses** | Mengatur eksekusi program: menjadwalkan giliran CPU antar aplikasi | Seperti manajer yang mengatur jadwal kerja karyawan |
   | **2. Manajemen Memori** | Mengalokasikan dan membebaskan RAM untuk program yang berjalan | Seperti petugas parkir yang mengatur slot parkir |
   | **3. Manajemen File** | Mengatur penyimpanan, pembacaan, dan penulisan file di disk | Seperti pustakawan yang mengatur katalog buku |
   | **4. Manajemen Perangkat I/O** | Mengatur komunikasi dengan hardware (keyboard, printer, dll) | Seperti penerjemah antar dua bahasa |
   | **5. Antarmuka Pengguna** | Menyediakan cara interaksi pengguna dengan komputer (GUI/CLI) | Seperti resepsionis yang membantu pengunjung |

   - **Multitasking**: OS menjalankan banyak aplikasi secara bergantian dalam milidetik — pengguna merasa semua berjalan bersamaan
   - **Scheduling**: OS menggunakan algoritma penjadwalan (Round Robin, Priority, dll) untuk menentukan proses mana yang jalan duluan

#### Mengaplikasi (bermakna, menggembirakan) — 30 menit

5. **Praktik 1: Task Manager — Mengamati Proses & Memori (10 menit)**
   - **Langkah**:
     1. Buka Task Manager (Ctrl+Shift+Esc di Windows)
     2. Lihat tab **Processes**: aplikasi apa saja yang berjalan?
     3. Lihat tab **Performance**: berapa % CPU dan RAM yang terpakai?
     4. Coba buka beberapa aplikasi (Chrome, Word, Calculator) — amati perubahan grafik CPU/RAM
     5. Pilih satu proses → klik kanan → **End Task** (dan lihat aplikasinya tertutup)
   - **Hasil**: Siswa mencatat di LKPD jumlah proses, % CPU, % RAM sebelum dan sesudah membuka aplikasi baru

   **Alternatif untuk Linux**: Buka `System Monitor` atau `htop` di terminal

6. **Praktik 2: File Explorer — Navigasi File System (10 menit)**
   - **Langkah**:
     1. Buka File Explorer / Windows Explorer
     2. Jelajahi struktur folder: `C:\`, `C:\Users\[nama]`, `C:\Program Files`
     3. Buat folder baru, rename, hapus
     4. Cari file dengan ekstensi `.txt`, `.docx`, `.jpg`
   - **Konsep**: OS menyediakan sistem file hierarkis (folder di dalam folder), hak akses file (read-only, hidden), dan path

7. **Praktik 3: CLI Dasar — Command Line Interface (10 menit)**
   - **Langkah**:
     1. Buka Command Prompt (Windows: `cmd` / Linux: `terminal`)
     2. Coba perintah dasar:

        | Perintah | Fungsi | Windows | Linux |
        |---|---|---|---|
        | Lihat isi folder | `dir` | `ls` |
        | Pindah folder | `cd folder` | `cd folder` |
        | Buat folder | `mkdir namafolder` | `mkdir namafolder` |
        | Hapus file | `del file.txt` | `rm file.txt` |
        | Bersihkan layar | `cls` | `clear` |
        | Matikan komputer | `shutdown /s` | `shutdown -h now` |

     3. Siswa mencoba sendiri dan mencatat hasil di LKPD
   - **Penjelasan**: CLI adalah cara berinteraksi dengan OS tanpa GUI — lebih cepat dan lebih kuat untuk tugas tertentu

#### Merefleksi (berkesadaran, bermakna) — 10 menit

8. **Diskusi Hasil Praktik (5 menit)**
   - "Apa yang terjadi pada % CPU saat kalian membuka Chrome?"
   - "Kenapa RAM tidak pernah kosong?"
   - "Apa beda navigasi file via GUI (File Explorer) vs CLI (Command Prompt)?"
   - "Kapan CLI lebih berguna daripada GUI?"

9. **Refleksi Individu (5 menit)**
   - Menulis di LKPD:
     - "Apa fungsi OS yang paling menarik menurutmu?"
     - "Apa beda manajemen proses dan manajemen memori?"
     - "Skala 1–10, seberapa paham kamu tentang OS hari ini?"

### Penutup (15 menit)

| Kegiatan | Waktu |
|---|---|
| 1. Rangkuman: "OS adalah lapisan tengah yang mengelola hardware untuk aplikasi — tanpanya, kita harus Coding langsung ke hardware" | 3 menit |
| 2. Tanya jawab | 5 menit |
| 3. Menyampaikan pertemuan depan: Bagian 2 — Literasi Digital & Informasi | 2 menit |
| 4. **Tugas**: Buka Task Manager di rumah/lab dan amati proses apa saja yang berjalan saat komputer idle vs saat main game/browsing. Catat perbedaannya! | 3 menit |
| 5. Doa & salam | 2 menit |

---

## Asesmen

### 1. Asesmen Formatif — Laporan Praktik

| Kriteria | Skor (1–4) |
|---|---|
| Kelengkapan data Task Manager (sebelum & sesudah) | |
| Hasil eksplorasi File Explorer (struktur folder) | |
| Hasil percobaan CLI (min 3 perintah) | |
| Refleksi dan analisis | |

### 2. Kuis Tertulis (5 menit — exit ticket)

1. Apa fungsi Sistem Operasi?
2. Sebutkan 2 jenis sistem operasi!
3. Apa perbedaan manajemen proses dan manajemen memori?
4. Apa kepanjangan CLI?

---

## Lampiran

| Kode | Nama File | Deskripsi |
|---|---|---|
| LKPD-04 | LKPD_Pertemuan4 | Lembar praktik Task Manager, File Explorer, CLI |
| BA-04 | Bahan_Ajar_Pertemuan4 | Materi OS, model lapisan bawang, jenis OS, peran OS |
| AS-04 | Asesmen_Pertemuan4 | Rubrik + kuis |
| SL-04 | Slide_Pertemuan4 | Slide presentasi |

---

**MGMP Informatika SMAN 6 Cimahi**
