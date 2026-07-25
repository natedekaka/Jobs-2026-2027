# BAHAN AJAR – PERTEMUAN 1
## Pengantar Sistem Komputer

| Mata Pelajaran | Informatika |
|---|---|
| Fase / Kelas | E / X |
| TP | BK 1.5 |
| Semester | 1 (Ganjil) |

---

### A. Apa Itu Sistem Komputer?

**Sistem komputer** adalah kumpulan dari komponen-komponen yang saling berhubungan dan bekerja sama untuk menerima data (input), memproses data (process), menyimpan data (storage), dan menghasilkan informasi (output).

Sistem komputer terdiri dari tiga elemen utama:

```
┌─────────────────────────────────────────────────────┐
│                   SISTEM KOMPUTER                    │
├──────────────┬──────────────────┬───────────────────┤
│   HARDWARE   │    SOFTWARE      │      BRAINWARE    │
│  (Perangkat  │   (Program &     │   (Pengguna/SDM)  │
│     Keras)   │    Aplikasi)     │                   │
└──────────────┴──────────────────┴───────────────────┘
```

- **Hardware** → Perangkat keras yang bisa dilihat dan disentuh
- **Software** → Program yang menjalankan hardware
- **Brainware** → Manusia yang mengoperasikan komputer

---

### B. Komponen-Komponen Sistem Komputer

#### 1. Input Device (Perangkat Masukan)

Berfungsi untuk menerima data dari luar dan mengirimkannya ke CPU.

| Perangkat | Fungsi |
|---|---|
| Keyboard | Mengetik teks, perintah, angka |
| Mouse | Menggerakkan kursor, memilih objek |
| Microphone | Merekam suara |
| Scanner | Memindai gambar/dokumen |
| Webcam | Menangkap gambar/video |
| Touchscreen | Layar sentuh (input sekaligus output) |

#### 2. Process Device (Perangkat Pemrosesan)

Komponen utama yang memproses data, yaitu **CPU (Central Processing Unit)**.

**CPU** terdiri dari tiga bagian:
- **ALU (Arithmetic Logic Unit):** melakukan perhitungan matematika dan logika
- **Control Unit (CU):** mengatur dan mengontrol semua operasi dalam komputer
- **Register:** memori berukuran kecil di dalam CPU untuk penyimpanan sementara data yang sedang diproses

Ilustrasi sederhana:

```
 Input ──→ CPU ──→ Output
             │
             ↓
           Memori
```

#### 3. Memory (Memori)

Tempat penyimpanan data sementara maupun permanen.

| Jenis Memori | Fungsi | Karakteristik |
|---|---|---|
| **RAM** (Random Access Memory) | Menyimpan data dan program yang sedang berjalan | Volatile (hilang saat mati), cepat |
| **ROM** (Read Only Memory) | Menyimpan instruksi dasar untuk booting | Non-volatile, hanya bisa dibaca |
| **Cache Memory** | Memori kecil berkecepatan tinggi di dalam CPU | Sangat cepat, terbatas |

#### 4. Storage Device (Perangkat Penyimpanan)

Penyimpanan data secara permanen.

| Perangkat | Kapasitas | Karakteristik |
|---|---|---|
| **Hard Disk Drive (HDD)** | Besar (256 GB–10 TB) | Lambat, murah, mekanik |
| **Solid State Drive (SSD)** | Sedang (128 GB–2 TB) | Cepat, mahal, non-mekanik |
| **Flashdisk / USB Drive** | 8 GB–256 GB | Portabel |
| **Memory Card / SD Card** | 8 GB–512 GB | Untuk kamera/HP |
| **Cloud Storage** | Tergantung layanan (Google Drive, iCloud, dll) | Akses online |

#### 5. Output Device (Perangkat Keluaran)

Berfungsi untuk menampilkan atau mengeluarkan hasil pemrosesan data.

| Perangkat | Fungsi |
|---|---|
| Monitor | Menampilkan gambar/video |
| Speaker | Mengeluarkan suara |
| Printer | Mencetak dokumen ke kertas |
| Proyektor | Memproyeksikan tampilan ke layar besar |

---

### C. Analogi Sistem Komputer dengan Tubuh Manusia

Untuk memudahkan pemahaman, sistem komputer dapat dianalogikan dengan tubuh manusia:

| Komputer | Manusia | Penjelasan |
|---|---|---|
| Keyboard, Mouse | Mata, Telinga, Kulit | Menerima input dari lingkungan |
| CPU (Otak) | Otak Besar | Memproses informasi |
| RAM | Memori Jangka Pendek | Mengingat hal yang sedang dikerjakan |
| Hard Disk | Memori Jangka Panjang | Menyimpan kenangan/pengetahuan |
| Monitor, Speaker | Mulut, Tangan | Mengeluarkan hasil/output |
| Software | Pengetahuan / skill | Cara melakukan sesuatu |
| Listrik | Energi / Makanan | Sumber tenaga |

---

### D. Cara Kerja Sederhana Sistem Komputer

Proses kerja komputer mengikuti alur **Input → Proses → Output → Storage**.

```
                 ┌───────────────┐
                 │   INPUT       │
                 │ (Keyboard,    │
                 │  Mouse, dll)  │
                 └───────┬───────┘
                         │
                         ▼
                 ┌───────────────┐
          ┌──────│    CPU       │──────┐
          │      │  (Proses)    │      │
          │      └───────┬───────┘      │
          │              │              │
          ▼              ▼              ▼
   ┌──────────┐   ┌────────────┐  ┌──────────┐
   │ OUTPUT   │   │ MEMORY     │  │ STORAGE  │
   │(Monitor, │   │ (RAM)      │  │ (Hard    │
   │ Speaker) │   │ Sementara  │  │  Disk)   │
   └──────────┘   └────────────┘  │ Permanen │
                                  └──────────┘
```

**Contoh sederhana: Mengetik di Microsoft Word**

1. **Input:** User menekan tombol 'A' di keyboard
2. **Proses:** CPU menerima sinyal, menerjemahkan ke kode ASCII (65), mengirim ke RAM
3. **Output:** Monitor menampilkan huruf 'A' di layar
4. **Storage:** Saat user klik "Save", data dari RAM ditulis ke Hard Disk

---

### E. Klasifikasi Komputer Berdasarkan Ukuran

| Jenis | Ukuran | Contoh | Kegunaan |
|---|---|---|---|
| **Supercomputer** | Sangat besar | IBM Summit | Riset ilmiah, prakiraan cuaca |
| **Mainframe** | Besar | IBM zSeries | Bank, perusahaan besar |
| **Server** | Sedang-besar | Dell PowerEdge | Melayani jaringan |
| **Personal Computer (PC)** | Meja | Desktop, Laptop | Penggunaan pribadi |
| **Mobile Device** | Genggam | Smartphone, Tablet | Komunikasi, hiburan |
| **Embedded System** | Sangat kecil | Arduino, Smartwatch | Perangkat khusus |

---

### F. Rangkuman

1. **Sistem komputer** terdiri dari hardware, software, dan brainware.
2. **Komponen utama:** Input → Proses (CPU) → Output + Storage.
3. **CPU** adalah otak komputer yang terdiri dari ALU, Control Unit, dan Register.
4. **RAM** bersifat sementara (volatile), **Hard Disk** bersifat permanen (non-volatile).
5. Setiap aktivitas di komputer melibatkan alur Input-Proses-Output-Storage.

---

### G. Glosarium

| Istilah | Arti |
|---|---|
| **CPU** | Central Processing Unit – unit pemrosesan pusat |
| **RAM** | Random Access Memory – memori akses acak |
| **ROM** | Read Only Memory – memori hanya baca |
| **HDD** | Hard Disk Drive – piringan penyimpanan magnetik |
| **SSD** | Solid State Drive – penyimpanan berbasis chip |
| **ALU** | Arithmetic Logic Unit – unit aritmatika dan logika |
| **Input** | Data yang dimasukkan ke sistem |
| **Output** | Hasil keluaran dari sistem |
| **Brainware** | Manusia yang mengoperasikan komputer |
| **Hardware** | Perangkat keras komputer |

---

**MGMP Informatika SMAN 6 Cimahi**
