---
marp: true
theme: uncover
class: invert
---

# PERTEMUAN 4
## Sistem Operasi & Perannya
### Informatika – Fase E / Kelas X
#### SMA Negeri 6 Cimahi

---

## Review — Pertemuan 3

### Simulasi Eksekusi Program
- **READ** = mengambil data dari memori (data tetap ada)
- **WRITE** = menulis data ke memori (data lama terganti)
- **Siklus**: Fetch → Decode → Execute → Store

> Tugas: alur IPO menghitung rata-rata 3 nilai — kumpulkan!

---

## Apersepsi

### Siapa "manajer" di dalam komputer?

Kita bisa membuka **Chrome, Word, Spotify, dan Calculator** secara bersamaan.

> Siapa yang mengatur agar semua aplikasi itu bisa jalan bersama tanpa saling ganggu?

---

# TUJUAN PEMBELAJARAN

1. ✅ Menjelaskan **pengertian & fungsi** sistem operasi
2. ✅ Mengidentifikasi **jenis-jenis** sistem operasi
3. ✅ Menjelaskan **5 peran utama** OS
4. ✅ Mendemonstrasikan fitur OS: **Task Manager**, **File Explorer**, **CLI**

---

# APA ITU SISTEM OPERASI?

---

## Definisi

**Sistem Operasi (OS)** adalah perangkat lunak sistem yang:

- Mengelola **sumber daya hardware** (CPU, RAM, disk)
- Menyediakan **layanan** untuk program aplikasi
- Menjadi **jembatan** antara hardware dan pengguna

| Tanpa OS | Dengan OS |
|---|---|
| Harus koding langsung ke hardware | Panggil API yang sudah disediakan OS |
| Setiap aplikasi harus punya driver sendiri | OS menyediakan driver universal |
| Sangat rumit | Relatif mudah |

---

## Model Lapisan Bawang

```
┌─────────────────────────────────────┐
│          PENGGUNA (User)           │
│     (Aplikasi: Chrome, Word, Game) │
├─────────────────────────────────────┤
│         SISTEM OPERASI              │
│     ┌───────────────────────┐       │
│     │       KERNEL          │       │
│     │   (Inti OS)           │       │
│     └───────────────────────┘       │
├─────────────────────────────────────┤
│            HARDWARE                 │
│      (CPU, RAM, HDD, I/O)          │
└─────────────────────────────────────┘
```

---

## Jenis-Jenis Sistem Operasi

| Jenis | Contoh | Untuk |
|---|---|---|
| 🖥️ **Desktop** | Windows, macOS, Linux | PC, laptop |
| 📱 **Mobile** | Android, iOS | HP, tablet |
| 🖧 **Server** | Ubuntu Server, Windows Server | Web server, database |
| 📺 **Embedded** | Firmware, RTOS | TV, AC, router |
| 🏭 **Real-Time** | VxWorks, QNX | Medis, mobil, pesawat |

---

# 5 PERAN UTAMA OS

---

## 1. Manajemen Proses

**Proses** = program yang sedang dijalankan

### Tugas OS:
- Membuat & menghapus proses
- **Scheduling**: menggilir CPU antar proses
- Menangani sinkronisasi

### Ilustrasi:
```
CPU: |A|B|C|A|B|C|A|B|C|...
     1 ms per giliran
```
> Pengguna merasa semua aplikasi jalan BERSAMAAN

---

## 2. Manajemen Memori

OS mengatur alokasi **RAM** untuk setiap proses.

```
RAM 8 GB:
┌────────────────────────┐
│ OS          (2 GB)    │
├────────────────────────┤
│ Chrome      (1.5 GB)  │
├────────────────────────┤
│ Word        (500 MB)  │
├────────────────────────┤
│ FREE        (4 GB)    │
└────────────────────────┘
```

**Virtual Memory**: OS bisa pakai hard disk sebagai "RAM tambahan" (swap file)

---

## 3. Manajemen File

OS menyediakan **sistem file** — cara data diatur di disk.

```
C:\
├── Users\
│   ├── Andi\Documents\
│   └── Budi\Documents\
├── Program Files\
└── Windows\
```

| Operasi | Contoh |
|---|---|
| Buat file | Save, New |
| Baca file | Open |
| Ubah file | Edit, Rename |
| Hapus file | Delete |
| Atur izin | Read-only, Hidden |

---

## 4. Manajemen Perangkat I/O

OS mengatur komunikasi dengan hardware melalui **driver**.

| Perangkat | Driver |
|---|---|
| Keyboard | keyboard.sys |
| Printer | printer driver |
| VGA | graphics driver |
| WiFi | network driver |

> OS membuat semua hardware "terlihat sama" bagi aplikasi

---

## 5. Antarmuka Pengguna

### GUI vs CLI

| Aspek | GUI | CLI |
|---|---|---|
| Interaksi | Klik & drag | Ketik perintah |
| Kemudahan | Mudah | Butuh hafalan |
| Kecepatan | Lambat | Cepat |
| Sumber daya | Berat | Ringan |

**GUI** = Graphical User Interface (Windows, macOS)
**CLI** = Command Line Interface (CMD, Terminal)

---

# PRAKTIK 3 IN 1

---

## Praktik 1: Task Manager

**Buka Ctrl+Shift+Esc**

1. Lihat tab **Processes** — aplikasi apa yang jalan?
2. Lihat tab **Performance** — % CPU dan RAM
3. Buka Chrome + Word + Calculator
4. Amati perubahan grafik!

> Catat di LKPD!

---

## Praktik 2: File Explorer

**Jelajahi struktur folder:**

1. `C:\` — apa saja isinya?
2. `C:\Users\Namamu`
3. Buat folder `Latihan_OS` di Desktop
4. Buat file `test.txt`, tulis nama kamu
5. Ubah jadi **Hidden**

> System file = OS yang membuat semua ini mungkin

---

## Praktik 3: CLI

**Buka CMD (Windows) atau Terminal (Linux)**

| Perintah | Fungsi |
|---|---|
| `dir` / `ls` | Lihat isi folder |
| `cd ..` | Naik folder |
| `mkdir nama` | Buat folder |
| `echo teks > file.txt` | Buat file |
| `del file.txt` | Hapus file |

> Coba sendiri, catat hasilnya di LKPD!

---

## Refleksi

### Diskusi:
1. Apa yang terjadi pada % CPU saat buka Chrome?
2. Kenapa RAM tidak pernah kosong?
3. Kapan CLI lebih berguna dari GUI?

### Tulis:
- Skala pemahaman: ___ / 10
- Satu hal baru yang kamu pelajari tentang OS

---

## Rangkuman

| No | Poin Penting |
|---|---|
| 1 | **OS** = manager sumber daya komputer |
| 2 | **Model bawang**: User → Aplikasi → OS → Hardware |
| 3 | **5 peran**: Proses, Memori, File, I/O, Antarmuka |
| 4 | **Task Manager** = jendela untuk melihat kerja OS |
| 5 | **CLI** = cara komunikasi teks dengan OS |

---

## Tugas Rumah

### Amati komputermu di rumah!

| Kondisi | CPU (%) | RAM (%) |
|---|---|---|
| Idle (diam) | | |
| Browsing 5+ tab | | |
| Main game (opsional) | | |

> Tulis laporan singkat (1 paragraf)!

---

## Pertemuan Berikutnya

### 🎯 Bagian 2: Literasi Digital & Informasi
> Mesin Pencari Tingkat Lanjut — Boolean search, operator pencarian

---

# Terima Kasih

### MGMP Informatika SMAN 6 Cimahi

> "Sistem Operasi adalah fondasi yang membuat pengalaman komputasi modern terasa mulus."
