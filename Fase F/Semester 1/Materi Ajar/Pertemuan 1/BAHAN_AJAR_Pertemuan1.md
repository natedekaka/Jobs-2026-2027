# BAHAN AJAR – PERTEMUAN 1
## Konsep Engineering Process & SDLC

| TP | BK — Proses Rekayasa |
|---|---|

---

### A. APA ITU ENGINEERING PROCESS?

**Engineering Process (Proses Rekayasa)** adalah serangkaian langkah terstruktur dan sistematis yang digunakan untuk merancang, membangun, menguji, meluncurkan, dan menyempurnakan program atau produk teknologi digital.

Setiap produk digital yang kalian gunakan sehari-hari — TikTok, Instagram, Gojek, Google Classroom — melewati proses ini sebelum akhirnya bisa kalian gunakan.

#### Analogi: Membangun Rumah

| Membangun Rumah | Membangun Aplikasi |
|---|---|
| Arsitek membuat denah | **Analysis & Design** |
| Tukang membangun | **Implementation (coding)** |
| Quality control memeriksa | **Testing** |
| Serah terima kunci | **Deployment** |
| Perbaikan bocor, cat ulang | **Maintenance** |

> Tanpa proses yang terstruktur, hasilnya akan **berantakan** dan **tidak sesuai kebutuhan**!

---

### B. SDLC — SOFTWARE DEVELOPMENT LIFE CYCLE

**SDLC** adalah kerangka kerja yang menggambarkan tahapan-tahapan dalam pengembangan perangkat lunak.

---

### C. TUJUH TAHAPAN SDLC

#### Tahap 1: Planning (Perencanaan)

| Pertanyaan Kunci | Output |
|---|---|
| • Apa tujuan aplikasi ini? | Dokumen rencana proyek |
| • Siapa target penggunanya? | Timeline / jadwal |
| • Berapa anggaran yang tersedia? | Estimasi biaya |
| • Kapan harus selesai? | |

**Contoh:** "Kita akan membuat aplikasi presensi siswa berbasis mobile. Target: 500 siswa SMAN 6 Cimahi. Deadline: 3 bulan."

#### Tahap 2: Analysis (Analisis Kebutuhan)

| Pertanyaan Kunci | Output |
|---|---|
| • Apa saja yang dibutuhkan pengguna? | Spesifikasi kebutuhan (SRS) |
| • Fitur apa yang paling penting? | User story |
| • Bagaimana alur kerja pengguna? | Use case diagram |

**Teknik penggalian kebutuhan:**
- **Wawancara**: tanya langsung ke pengguna
- **Observasi**: lihat bagaimana pengguna bekerja
- **Kuesioner**: sebarkan angket ke banyak calon pengguna
- **Studi dokumen**: pelajari sistem yang sudah ada

**Contoh:** "Berdasarkan wawancara dengan guru BK: fitur yang dibutuhkan adalah scan QR, laporan bulanan, notifikasi orang tua."

#### Tahap 3: Design (Perancangan)

| Aktivitas | Output |
|---|---|
| • Wireframe (kerangka tampilan) | Mockup aplikasi |
| • Desain database | ERD (Entity Relationship Diagram) |
| • Arsitektur sistem | Diagram arsitektur |
| • Alur pengguna | User flow |

**Contoh:** Membuat wireframe halaman login, dashboard guru, form presensi.

#### Tahap 4: Implementation (Implementasi / Coding)

| Aktivitas | Teknologi |
|---|---|
| • Menulis kode program | Python, JavaScript, PHP, dll. |
| • Membuat database | MySQL, PostgreSQL |
| • Integrasi komponen | API, library |

**Version Control** — penting untuk melacak perubahan kode:
- **Git** — sistem version control paling populer
- **GitHub/GitLab** — platform hosting Git

#### Tahap 5: Testing (Pengujian)

| Jenis Testing | Deskripsi |
|---|---|
| **Unit Test** | Menguji fungsi/komponen terkecil |
| **Integration Test** | Menguji antar komponen |
| **UAT (User Acceptance Test)** | Pengguna mencoba langsung |
| **Performance Test** | Menguji beban & kecepatan |

**Tujuan:** Menemukan **bug** (kesalahan) sebelum aplikasi dipakai.

#### Tahap 6: Deployment (Peluncuran)

| Aktivitas | Contoh |
|---|---|
| • Rilis ke server produksi | Upload ke Play Store / App Store |
| • Migrasi data | Pindahkan data dari sistem lama |
| • Pelatihan pengguna | Sosialisasi ke guru & siswa |

**Strategi Deployment:**
- **Staging**: uji coba di lingkungan yang mirip produksi
- **Production**: rilis resmi ke pengguna
- **Canary**: rilis bertahap ke sebagian pengguna

#### Tahap 7: Maintenance (Pemeliharaan)

| Aktivitas | Contoh |
|---|---|
| • Perbaikan bug | Memperbaiki error yang muncul |
| • Penambahan fitur | Tambah fitur laporan PDF |
| • Pembaruan keamanan | Update library, patch keamanan |
| • Optimasi | Mempercepat loading, hemat memori |

> **Penting:** SDLC bukanlah proses satu arah! Sering kali kita **kembali** ke tahap sebelumnya (iterasi) untuk menyempurnakan produk.

---

### D. CONTOH PENERAPAN SDLC

#### Studi Kasus: Aplikasi Gojek

| Tahap | Penerapan pada Gojek |
|---|---|
| **Planning** | Ide: "Buat aplikasi yang menghubungkan pengemudi ojek dengan penumpang" |
| **Analysis** | Wawancara: penumpang butuh cepat, pengemudi butuh order |
| **Design** | Desain fitur: pilih lokasi, pilih driver, tracking, pembayaran |
| **Implementation** | Coding aplikasi iOS, Android, backend |
| **Testing** | Uji coba order, tracking, pembayaran |
| **Deployment** | Rilis di Play Store & App Store |
| **Maintenance** | Tambah GoFood, GoSend, GoPay — terus berkembang! |

#### Studi Kasus: Aplikasi TikTok

| Tahap | Penerapan pada TikTok |
|---|---|
| **Planning** | "Aplikasi video pendek dengan algoritma rekomendasi" |
| **Analysis** | Pengguna ingin konten sesuai minat, mudah dibuat |
| **Design** | For You Page, swipe up/down, efek filter |
| **Implementation** | AI recommendation algorithm, video processing |
| **Testing** | Uji coba rekomendasi konten, performa video |
| **Deployment** | Rilis global |
| **Maintenance** | Tambah TikTok Shop, TikTok LIVE, efek AR |

---

### E. MENGAPA SDLC PENTING?

| Tanpa SDLC | Dengan SDLC |
|---|---|
| Fitur tidak sesuai kebutuhan | Kebutuhan terpetakan dengan baik |
| Banyak bug & error | Testing sistematis |
| Terlambat rilis | Jadwal terencana |
| Biaya membengkak | Anggaran terkontrol |
| Sulit dikembangkan | Mudah dimaintenance |

---

### F. RANGKUMAN

| Tahap | Aktivitas Utama | Output |
|---|---|---|
| 1. **Planning** | Tentukan tujuan, jadwal, biaya | Rencana proyek |
| 2. **Analysis** | Wawancara, kuesioner, observasi | Spesifikasi kebutuhan |
| 3. **Design** | Wireframe, desain database | Mockup, ERD |
| 4. **Implementation** | Coding, database | Source code, database |
| 5. **Testing** | Unit test, UAT | Laporan pengujian |
| 6. **Deployment** | Rilis ke pengguna | Aplikasi live |
| 7. **Maintenance** | Perbaikan, tambah fitur | Update versi |

> **Ingat:** SDLC = **S**iklus — bukan garis lurus! Produk terus disempurnakan.

---

**MGMP Informatika SMAN 6 Cimahi**
