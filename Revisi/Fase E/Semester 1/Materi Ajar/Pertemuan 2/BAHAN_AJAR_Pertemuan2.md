# BAHAN AJAR – PERTEMUAN 2 (S1)
## Software & Sistem Operasi
*Mengacu pada Panduan Mapel 2025; INFORMATIKA Fase D-F — pendekatan Pembelajaran Mendalam (Memahami → Mengaplikasi → Merefleksi)*

| Informasi | Keterangan |
|---|---|
| **Fase / Kelas** | E / Kelas X |
| **Alokasi Waktu** | 2 JP × 45 menit (90 menit) |
| **Elemen CP** | Sistem Komputer (SK) |
| **Tujuan Pembelajaran** | Membedakan hardware dan software; mengklasifikasikan jenis software; menjelaskan peran sistem operasi dan cara kerja komputer saat menjalankan aplikasi |
| **Materi Prasyarat** | Perangkat keras komputer (Pertemuan 1): INPUT–PROSES–OUTPUT–STORAGE |

---

## A. Kisah Pemantik 🎬

> **"Komputer yang Tidak Pernah Tidur"**
>
> Pukul 23.00, Toko Online Jaya masih melayani ratusan pembeli. Seorang pelayan mencatat pesanan, kasir menghitung total, dan petugas gudang menyiapkan barang. Tiga orang dengan tugas berbeda — tapi semuanya bekerja **di bawah satu aturan dan satu bos** yang mengatur giliran mereka.
>
> Di dalam komputermu, pekerjaan itu dilakukan oleh **sistem operasi**: satu "bos" yang mengatur kapan keyboard boleh masuk, kapan CPU menghitung, dan kapan layar menampilkan hasil — tanpa pernah lelah.
>
> **Pertanyaan pemantik:** Apa jadinya jika di komputer tidak ada "bos" yang mengatur semua pekerjaan? Coba bayangkan keyboard, monitor, dan CPU bekerja sendiri-sendiri tanpa koordinasi!

---

## B. Apa Itu Software?

**Software (perangkat lunak)** adalah kumpulan instruksi atau program yang memberitahu hardware apa yang harus dilakukan. Software tidak bisa disentuh karena hanya berupa data dan kode, sedangkan **hardware** bisa dilihat dan disentuh.

| Istilah | Bentuk | Contoh |
|---|---|---|
| **Hardware** | Fisik, bisa disentuh | Keyboard, monitor, HDD |
| **Software** | Kode/instruksi, tidak terlihat | Windows, Word, Chrome |

> 💡 **Ingat:** Hardware adalah "tubuh" dan software adalah "jiwa". Tanpa software, komputer hanyalah tumpukan besi yang diam.

---

## C. Klasifikasi Software

Software terbagi menjadi **tiga jenis utama**:

### C.1 Sistem Operasi (OS)
Software utama yang mengelola seluruh hardware dan software di komputer. Ia adalah "jembatan" antara pengguna dan perangkat keras.

| OS | Perangkat | Kelebihan |
|---|---|---|
| Windows 11 | PC/Laptop | User friendly, banyak software |
| macOS | MacBook | Stabil, desain premium |
| Linux (Ubuntu) | PC/Laptop | Open source, ringan |
| Android | HP/Tablet | Terbanyak pengguna |
| iOS | iPhone/iPad | Aman, eksklusif Apple |

### C.2 Aplikasi (Application Software)
Program yang membantu menyelesaikan tugas spesifik pengguna.

| Aplikasi | Kegunaan |
|---|---|
| Microsoft Word | Mengetik dokumen |
| Google Chrome | Browsing internet |
| Zoom | Video conference |
| Canva | Desain grafis |
| Excel | Spreadsheet |

### C.3 Utility
Program pendukung yang menjaga dan merawat sistem.

| Utility | Fungsi |
|---|---|
| Windows Defender | Antivirus |
| File Explorer | Manajemen file |
| Task Manager | Monitor kinerja |
| Disk Cleanup | Bersihkan file sampah |
| CCleaner | Optimasi sistem |

> 💡 **Tips mengingat:** OS = "bos" yang mengatur, Aplikasi = "pekerja" yang menyelesaikan tugas, Utility = "tukang servis" yang merawat mesin.

---

## D. Sistem Operasi yang Paling Populer

1. **Windows** — dominan di PC (±70% pengguna), mudah digunakan.
2. **Android** — OS mobile terbanyak (±70% smartphone dunia).
3. **iOS** — khusus Apple, sistem tertutup namun aman.
4. **macOS** — khusus Mac, desain premium.

| OS | Digunakan di | Sifat |
|---|---|---|
| Windows | PC/Laptop umum | Terbuka untuk banyak merek |
| Android | Berbagai merek HP | Open source (Google) |
| iOS | iPhone/iPad | Tertutup (eksklusif Apple) |
| macOS | MacBook/iMac | Tertutup (eksklusif Apple) |

---

## E. Cara Kerja Komputer: Dari Klik hingga Tampil

Saat kamu mengklik ikon Word, terjadi kerja sama antar komponen:

1. **User** mengklik ikon aplikasi (misalnya Word).
2. **OS** mengambil data aplikasi dari **storage** (HDD/SSD).
3. **CPU** memproses instruksi aplikasi.
4. **RAM** menyimpan data sementara selama aplikasi berjalan.
5. Hasil ditampilkan di **monitor** (output).

```
User klik ikon Word
        │
        ▼
 OS memuat program dari STORAGE (HDD/SSD)
        │
        ▼
 CPU memproses + RAM menyimpan sementara
        │
        ▼
 Tampil jendela Word di MONITOR (output)
```

> 💡 **Fakta menarik:** Jendela Word yang terbuka di layar itu sebenarnya "salinan" yang dimuat ke RAM. Jika RAM penuh, komputer akan terasa lambat karena harus memuat ulang dari storage.

---

## F. Contoh Soal & Penyelesaian 📝

**Contoh 1:** Jelaskan perbedaan antara sistem operasi dan aplikasi!
**Jawaban:** Sistem operasi mengelola seluruh hardware dan software serta menjadi jembatan antara pengguna dan komputer (contoh: Windows). Aplikasi adalah program untuk tugas spesifik yang berjalan di atas OS (contoh: Word, Chrome). Aplikasi tidak bisa berjalan tanpa OS.

**Contoh 2:** Sebutkan 3 contoh sistem operasi beserta perangkatnya!
**Jawaban:**
1. **Windows 11** — untuk PC/Laptop.
2. **Android** — untuk HP/Tablet berbagai merek.
3. **iOS** — khusus iPhone/iPad.

**Contoh 3:** Mengapa Windows lebih populer daripada Linux di kalangan umum?
**Jawaban:** Karena Windows lebih mudah digunakan (user friendly), memiliki dukungan software/game paling banyak, dan sudah terpasang di mayoritas komputer yang dijual, sehingga pengguna tidak perlu repot menginstal sendiri.

---

## G. Miskonsepsi yang Sering Terjadi 🚫

| Miskonsepsi | Fakta yang Benar |
|---|---|
| "Software bisa disentuh seperti flashdisk" | Software adalah kode yang **tidak bisa disentuh**; flashdisk adalah hardware |
| "Game dan aplikasi adalah sistem operasi" | Game/aplikasi adalah **application software**, bukan OS |
| "Linux itu OS khusus server" | Linux juga populer untuk PC dan Android, bersifat open source |
| "Antivirus termasuk aplikasi biasa" | Antivirus termasuk **utility software** yang merawat sistem |

---

## H. Tantangan Praktik (Mengaplikasi) 🎯

**Tantangan 1 — Klasifikasi Cepat:** Kategorikan software berikut ke dalam OS/Aplikasi/Utility: Windows 11, Google Chrome, Microsoft Word, Windows Defender, Android, Adobe Photoshop, File Explorer, Zoom.

**Tantangan 2 — Bedah Task Manager:**
1. Tekan `Ctrl + Shift + Esc` untuk membuka Task Manager.
2. Catat: jumlah proses berjalan = ___, CPU terpakai = ___%, RAM terpakai = ___%.
3. Pilih satu aplikasi → klik kanan → **End task**. Aplikasi apa yang kamu tutup? ____

**Tantangan 3 — Riset OS di HP:** Periksa sistem operasi di HP-mu (Pengaturan → Tentang Ponsel). Catat nama OS, versi, dan RAM yang terpasang. Setelah itu, jelaskan hubungan RAM dengan kelancaran aplikasi berdasarkan cara kerja komputer pada bagian E!

---

## I. Rangkuman Kunci 🔑

1. **Software** = kumpulan instruksi (tidak terlihat); **hardware** = fisik (terlihat).
2. Tiga jenis software: **sistem operasi, aplikasi, utility**.
3. **OS** adalah jembatan antara user dan hardware yang mengatur segalanya.
4. OS populer: **Windows, Android, iOS, macOS, Linux**.
5. Saat aplikasi dibuka: **storage → CPU/RAM → monitor**.
6. RAM yang penuh membuat komputer lambat karena aplikasi harus dimuat ulang dari storage.

---

## J. Glosarium 📖

| Istilah | Arti |
|---|---|
| **Software** | Perangkat lunak — kumpulan instruksi/kode |
| **Sistem Operasi (OS)** | Software utama pengelola hardware & software |
| **Application Software** | Aplikasi untuk tugas spesifik pengguna |
| **Utility** | Program pendukung/perawatan sistem |
| **Open Source** | Kode sumber terbuka, bebas dipakai & dimodifikasi |
| **Task Manager** | Utilitas Windows untuk memantau proses & kinerja |
| **RAM** | Memori sementara tempat aplikasi berjalan |

---

## K. Refleksi (Merefleksi) 🔍

- Apa konsep paling penting yang kamu pelajari hari ini?
- Bagaimana bedanya hardware dan software dalam satu kalimat versimu sendiri?
- OS apa yang ada di komputer sekolahmu, dan mengapa OS itu dipilih?
- **Skala pemahaman diri:** ____/10
- Apa yang ingin kamu pelajari lebih lanjut tentang software?

---

**MGMP Informatika SMAN 6 Cimahi — Fase E (Kelas X) Semester 1**