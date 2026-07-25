# BAHAN AJAR – PERTEMUAN 2
## Model Arsitektur Von Neumann & Input-Proses-Output (IPO)

| Mata Pelajaran | Informatika |
|---|---|
| Fase / Kelas | E / X |
| TP | BK 1.5, 1.6 |
| Semester | 1 (Ganjil) |

---

### A. Sejarah Arsitektur Von Neumann

Pada tahun 1945, seorang matematikawan bernama **John von Neumann** merancang sebuah arsitektur komputer yang menjadi dasar hampir semua komputer modern hingga saat ini. Ide revolusionernya adalah **Stored Program Concept** — yaitu program dan data disimpan di memori yang sama, bukan di-hardware terpisah.

Sebelum Von Neumann, komputer harus di-program ulang secara fisik dengan mengganti kabel dan sakelar. Setelah Von Neumann, instruksi disimpan di memori dan bisa diubah dengan mudah — ini yang memungkinkan kita menjalankan berbagai aplikasi di komputer yang sama.

```
┌─────────────────────────────────────────────────────────┐
│                    VON NEUMANN ARCHITECTURE              │
│                                                         │
│  ┌──────────┐     ┌──────────┐     ┌──────────┐        │
│  │  INPUT   │────→│   CPU    │────→│  OUTPUT  │        │
│  │ DEVICE   │     │──────────│     │  DEVICE  │        │
│  └──────────┘     │ ALU│ CU  │     └──────────┘        │
│                   └────┬──┬──┘                          │
│                        │  │                             │
│                        ▼  ▼                             │
│                   ┌──────────────────┐                  │
│                   │     MEMORI      │                  │
│                   │  (RAM / ROM)    │                  │
│                   └──────────────────┘                  │
│                                                         │
│         SEMUA KOMPONEN TERHUBUNG VIA BUS               │
└─────────────────────────────────────────────────────────┘
```

---

### B. Komponen Utama Arsitektur Von Neumann

#### 1. Central Processing Unit (CPU)

CPU adalah "otak" komputer yang menjalankan instruksi. Terdiri dari:

| Komponen CPU | Fungsi | Analogi |
|---|---|---|
| **ALU** (Arithmetic Logic Unit) | Melakukan operasi aritmatika (+, -, ×, ÷) dan logika (=, >, <, AND, OR) | Kalkulator dalam otak |
| **Control Unit (CU)** | Mengatur dan mengkoordinasikan semua aktivitas komputer — membaca instruksi dari memori, mengontrol ALU, mengatur aliran data | Konduktor orkestra |
| **Register** | Memori kecil berkecepatan sangat tinggi di dalam CPU | Meja kerja (sementara) |

**Cara CPU Bekerja (Siklus Fetch-Decode-Execute):**

```
1. FETCH   → CU mengambil instruksi dari Memori
2. DECODE  → CU menerjemahkan instruksi
3. EXECUTE → CU memerintahkan ALU untuk menjalankan instruksi
4. STORE   → Hasil disimpan kembali ke Memori atau Register
```

#### 2. Memori

Berfungsi menyimpan data dan instruksi. Dalam arsitektur Von Neumann, data dan instruksi berada di ruang memori yang sama (tidak dibedakan).

| Jenis Memori | Fungsi |
|---|---|
| **RAM** (Random Access Memory) | Menyimpan data dan program yang sedang berjalan — isinya hilang saat komputer mati |
| **ROM** (Read Only Memory) | Menyimpan instruksi booting — isinya tetap walau komputer mati |

**Alamat Memori:** Setiap lokasi di memori memiliki alamat unik (seperti nomor rumah). CPU mengakses data berdasarkan alamat ini.

#### 3. Unit Input

Menerima data dari dunia luar ke dalam sistem komputer.

| Contoh | Fungsi |
|---|---|
| Keyboard | Mengetik teks |
| Mouse | Navigasi |
| Mikrofon | Suara |
| Sensor (suhu, cahaya) | Data lingkungan |

#### 4. Unit Output

Menampilkan atau mengirim hasil pemrosesan ke dunia luar.

| Contoh | Fungsi |
|---|---|
| Monitor | Tampilan visual |
| Speaker | Suara |
| Printer | Cetakan kertas |

#### 5. Bus System

**Bus** adalah jalur komunikasi yang menghubungkan semua komponen. Ada tiga jenis bus:

| Bus | Fungsi |
|---|---|
| **Data Bus** | Membawa data antar komponen |
| **Address Bus** | Membawa alamat memori yang akan diakses |
| **Control Bus** | Membawa sinyal kontrol (baca/tulis, clock) |

---

### C. Konsep Input-Proses-Output (IPO)

IPO adalah model kerja dasar komputer yang menggambarkan aliran data:

```
INPUT → PROSES → OUTPUT
           │
           ↓
        STORAGE
```

#### Contoh 1: Mengetik di Aplikasi Catatan

| Tahap | Proses |
|---|---|
| **Input** | User menekan tombol 'H' di keyboard |
| **Proses** | Keyboard mengirim sinyal → CPU menerjemahkan ke kode ASCII (72 = H) → CU menyimpan ke RAM di alamat tertentu |
| **Output** | Monitor menampilkan huruf 'H' di layar pada posisi kursor |
| **Storage** | Saat user klik Save, data dipindahkan dari RAM ke Hard Disk |

#### Contoh 2: Membuka Google Chrome

| Tahap | Proses |
|---|---|
| **Input** | User mengklik ganda ikon Chrome |
| **Proses** | CPU membaca file chrome.exe dari Hard Disk → menyalin ke RAM → CPU mengeksekusi instruksi-instruksi program |
| **Output** | Jendela Chrome muncul di layar |
| **Storage** | Cache dan data sementara disimpan sementara di RAM |

---

### D. Stored Program Concept

Inilah gagasan paling penting dari Von Neumann:

- **Program (instruksi)** dan **data** disimpan di memori yang **sama**
- Komputer bisa mengubah program dengan mudah karena instruksi di memori bisa ditulis ulang
- Tanpa konsep ini, kita harus mengganti hardware untuk menjalankan program berbeda

**Ilustrasi:**

```
MEMORI (berisi campuran data dan instruksi):
┌─────────┬─────────┬─────────┬─────────┬─────────┐
│ Alamat  │ Alamat  │ Alamat  │ Alamat  │ Alamat  │
│   0     │   1     │   2     │   3     │   4     │
│         │         │         │         │         │
│LOAD 5   │LOAD 3   │  ADD    │ STORE 7 │  HALT   │
│(Instruk)│(Instruk)│(Instruk)│(Instruk)│(Instruk)│
├─────────┼─────────┼─────────┼─────────┼─────────┤
│ Alamat  │ Alamat  │         │         │         │
│   5     │   6     │  ...    │  ...    │  ...    │
│         │         │         │         │         │
│  DATA   │  DATA   │         │         │         │
│   7     │   3     │         │         │         │
└─────────┴─────────┴─────────┴─────────┴─────────┘
```

Program menghitung 7 + 3:
1. Ambil data dari alamat 5 (nilai 7) → Register A
2. Ambil data dari alamat 6 (nilai 3) → Register B
3. ALU: A + B = 10
4. Simpan hasil ke alamat 7

---

### E. Perbandingan: Komputer Von Neumann vs Manusia

| Komponen Komputer | Manusia | Penjelasan |
|---|---|---|
| CPU (ALU + CU) | Otak | Memproses, menghitung, mengontrol |
| RAM | Memori jangka pendek | Mengingat hal yang sedang dikerjakan |
| Hard Disk | Memori jangka panjang | Menyimpan kenangan/pengetahuan |
| Keyboard/Mouse | Mata/Telinga | Menerima informasi dari luar |
| Monitor/Speaker | Mulut | Mengeluarkan hasil |
| Bus System | Sistem saraf | Menghantarkan sinyal ke seluruh tubuh |

---

### F. Rangkuman

1. **Arsitektur Von Neumann** adalah dasar semua komputer modern — terdiri dari CPU, Memori, Input, Output, dan Bus.
2. **IPO (Input-Proses-Output)** adalah model aliran data dasar dalam sistem komputer.
3. **Stored Program Concept** memungkinkan program dan data disimpan di memori yang sama.
4. **CPU** bekerja dengan siklus **Fetch → Decode → Execute → Store**.
5. **Bus** menghubungkan semua komponen dan membawa data, alamat, dan sinyal kontrol.

---

### G. Glosarium

| Istilah | Arti |
|---|---|
| **Von Neumann Architecture** | Model arsitektur komputer dengan program tersimpan |
| **Stored Program Concept** | Konsep program dan data disimpan di memori yang sama |
| **ALU** | Arithmetic Logic Unit — bagian CPU untuk perhitungan |
| **Control Unit** | Bagian CPU yang mengatur aliran data dan instruksi |
| **Register** | Memori kecepatan tinggi di dalam CPU |
| **Bus** | Jalur komunikasi antar komponen komputer |
| **Fetch-Decode-Execute** | Siklus kerja CPU dalam menjalankan instruksi |
| **Address** | Alamat unik setiap lokasi di memori |

---

**MGMP Informatika SMAN 6 Cimahi**
