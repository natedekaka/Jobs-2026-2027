# BAHAN AJAR – PERTEMUAN 4
## Sistem Operasi & Perannya

| Mata Pelajaran | Informatika |
|---|---|
| Fase / Kelas | E / X |
| TP | BK 1.7 |
| Semester | 1 (Ganjil) |

---

### A. Definisi Sistem Operasi

**Sistem Operasi (OS)** adalah perangkat lunak sistem yang bertindak sebagai perantara antara **hardware**, **software aplikasi**, dan **pengguna**. OS mengelola semua sumber daya komputer dan menyediakan layanan yang dibutuhkan oleh program aplikasi.

Tanpa OS, setiap program harus berkomunikasi langsung dengan hardware — ini sangat rumit dan tidak praktis.

> **OS = Manager yang mengatur semua sumber daya komputer**

---

### B. Model Lapisan Bawang Sistem Komputer

Sistem komputer dapat digambarkan sebagai lapisan bawang — setiap lapisan menyembunyikan kompleksitas lapisan di bawahnya:

```
                     ┌─────────────────────┐
                     │    PENGGUNA (User)  │
                     │  Manusia yang       │
                     │  menggunakan komputer│
                     └──────────┬──────────┘
                                │
                     ┌──────────▼──────────┐
                     │   APLIKASI (SW)     │
                     │  Chrome, Word, Game │
                     │  Excel, VS Code     │
                     └──────────┬──────────┘
                                │
                     ┌──────────▼──────────┐
                     │  SISTEM OPERASI (OS)│
                     │  Windows, Linux,    │
                     │  macOS, Android     │
                     │                    │
                     │  ┌──────────────┐  │
                     │  │    Kernel    │  │
                     │  │(Inti OS)    │  │
                     │  └──────────────┘  │
                     └──────────┬──────────┘
                                │
                     ┌──────────▼──────────┐
                     │     HARDWARE        │
                     │  CPU, RAM, HDD,     │
                     │  Keyboard, Monitor  │
                     └─────────────────────┘
```

**Penjelasan lapisan:**
1. **Hardware** — Komponen fisik (CPU, RAM, dll). Berkomunikasi dalam bahasa mesin.
2. **Kernel** — Inti dari OS yang berinteraksi langsung dengan hardware. Menangani tugas paling dasar.
3. **Sistem Operasi** — Kernel + utilitas + antarmuka. Menyediakan layanan untuk aplikasi.
4. **Aplikasi** — Program yang digunakan pengguna (browser, office, game).
5. **Pengguna** — Manusia yang menggunakan komputer.

---

### C. Jenis-Jenis Sistem Operasi

| Jenis | Contoh | Ciri Utama | Penggunaan |
|---|---|---|---|
| **Desktop OS** | Windows, macOS, Linux Ubuntu | GUI, multitasking, dukungan hardware luas | PC, laptop |
| **Mobile OS** | Android, iOS | Sentuhan, portabel, hemat daya | Smartphone, tablet |
| **Server OS** | Ubuntu Server, Windows Server, CentOS | Stabil, headless (tanpa GUI), fokus jaringan | Server web, database, cloud |
| **Embedded OS** | RTOS, firmware | Ringan, real-time, tugas spesifik | TV, AC, mobil, IoT |
| **Real-Time OS** | VxWorks, QNX | Respon dalam batas waktu ketat | Medis, militer, industri |

---

### D. Lima Peran Utama Sistem Operasi

#### 1. Manajemen Proses

**Proses** adalah program yang sedang dieksekusi. OS bertanggung jawab untuk:
- Membuat dan menghapus proses
- Menjadwalkan proses (menggilir CPU antar proses)
- Mengatur sinkronisasi antar proses
- Menangani deadlock

**Ilustrasi Scheduling (Round Robin):**

```
Waktu:  →→→→→→→→→→→→→→→→→→→→→→→→→→→
CPU:   |A|B|C|A|B|C|A|B|C|A|B|C|
       1 1 1 1 1 1 1 1 1 1 1 1   (ms)
```

Tiga program (A, B, C) mendapat giliran CPU masing-masing 1 ms secara bergantian. Pengguna merasa ketiganya berjalan bersamaan.

**Status Proses:**

```
NEW ──→ READY ──→ RUNNING ──→ TERMINATED
           │            │
           ↓            ↓
        WAITING     (gunakan CPU)
     (menunggu I/O)
```

#### 2. Manajemen Memori

OS mengelola **RAM** — siapa yang boleh menggunakan berapa banyak, dan di alamat mana.

**Tugas manajemen memori:**
- Melacak bagian memori yang digunakan dan kosong
- Mengalokasikan memori ke proses yang membutuhkan
- Membebaskan memori saat proses selesai
- **Virtual Memory** — menggunakan sebagian hard disk sebagai RAM tambahan (swap file)

**Ilustrasi:**

```
RAM 8 GB:
┌────────────────────────────────┐
│  OS          (2 GB)           │
├────────────────────────────────┤
│  Chrome      (1,5 GB)         │
├────────────────────────────────┤
│  Word        (500 MB)         │
├────────────────────────────────┤
│  Spotify     (300 MB)         │
├────────────────────────────────┤
│  FREE        (3,7 GB)         │
└────────────────────────────────┘
```

#### 3. Manajemen File

OS menyediakan sistem file untuk mengatur data di disk.

**Konsep:**
- **File**: unit penyimpanan data (dokumen, gambar, program)
- **Folder/Directory**: wadah untuk mengelompokkan file
- **Path**: alamat lengkap file dalam sistem (C:\Users\Nama\Dokumen\tugas.docx)
- **Hak akses**: read, write, execute (perizinan)

**Struktur Folder Hierarkis:**

```
C:\
├── Users\
│   ├── Andi\
│   │   ├── Documents\
│   │   ├── Downloads\
│   │   └── Desktop\
│   └── Budi\
├── Program Files\
│   ├── Chrome\
│   └── Microsoft Office\
└── Windows\
    ├── System32\
    └── Temp\
```

#### 4. Manajemen Perangkat I/O

OS mengatur komunikasi antara CPU dan perangkat input/output melalui **driver**.

| Perangkat | Driver | Fungsi |
|---|---|---|
| Keyboard | keyboard.sys | Menerjemahkan sinyal tombol ke karakter |
| Printer | printer driver | Mengubah data ke format cetak |
| VGA | graphics driver | Mengatur tampilan layar |
| WiFi | network driver | Mengelola koneksi nirkabel |

#### 5. Antarmuka Pengguna

OS menyediakan dua cara interaksi:

| Antarmuka | Deskripsi | Contoh |
|---|---|---|
| **GUI** (Graphical User Interface) | Visual — klik, drag, window | Windows Desktop, macOS Aqua, GNOME |
| **CLI** (Command Line Interface) | Berbasis teks — mengetik perintah | Command Prompt, Terminal, PowerShell |

**Perbandingan:**

| Aspek | GUI | CLI |
|---|---|---|
| Kemudahan | Mudah untuk pemula | Butuh hafalan perintah |
| Kecepatan | Lambat untuk tugas kompleks | Cepat untuk tugas berulang |
| Sumber daya | Boros RAM/CPU | Ringan |
| Otomatisasi | Sulit | Mudah (scripting) |

---

### E. Contoh Sistem Operasi dalam Kehidupan Sehari-hari

| Perangkat | Sistem Operasi |
|---|---|
| Laptop Windows | Windows 10 / 11 |
| MacBook | macOS |
| Smartphone Android | Android (versi 13/14) |
| iPhone | iOS |
| Smart TV | WebOS, Tizen |
| Router WiFi | DD-WRT, OpenWRT |
| ATM | Windows XP Embedded / Linux |
| Mobil modern | QNX, Linux Automotive |

---

### F. Rangkuman

1. **Sistem Operasi** adalah perantara hardware, software, dan pengguna.
2. **Model lapisan bawang**: Pengguna → Aplikasi → OS (Kernel) → Hardware.
3. **Lima peran utama OS**: Manajemen Proses, Memori, File, I/O, dan Antarmuka.
4. **Multitasking**: OS menjalankan banyak proses secara bergantian dengan scheduling.
5. **GUI vs CLI**: GUI visual dan mudah, CLI cepat dan bisa di-scripting.

---

### G. Glosarium

| Istilah | Arti |
|---|---|
| **Sistem Operasi** | Software yang mengelola hardware dan menyediakan layanan untuk aplikasi |
| **Kernel** | Inti dari sistem operasi yang berinteraksi langsung dengan hardware |
| **Proses** | Program yang sedang dijalankan di memori |
| **Scheduling** | Penjadwalan giliran proses menggunakan CPU |
| **Multitasking** | Kemampuan menjalankan banyak proses secara bergantian |
| **Virtual Memory** | Penggunaan hard disk sebagai RAM tambahan |
| **Driver** | Software yang menjembatani OS dengan perangkat hardware |
| **GUI** | Graphical User Interface — antarmuka grafis |
| **CLI** | Command Line Interface — antarmuka baris perintah |
| **File System** | Cara OS mengatur dan menyimpan file di disk |

---

**MGMP Informatika SMAN 6 Cimahi**
