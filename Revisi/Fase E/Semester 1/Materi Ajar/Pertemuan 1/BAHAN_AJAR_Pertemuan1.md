# BAHAN AJAR – PERTEMUAN 1 (S1)
## Perangkat Keras Komputer
*Mengacu pada Panduan Mapel 2025; INFORMATIKA Fase D-F — pendekatan Pembelajaran Mendalam (Memahami → Mengaplikasi → Merefleksi)*

| Informasi | Keterangan |
|---|---|
| **Fase / Kelas** | E / Kelas X |
| **Alokasi Waktu** | 2 JP × 45 menit (90 menit) |
| **Elemen CP** | Sistem Komputer (SK) |
| **Tujuan Pembelajaran** | Mengenali perangkat keras komputer beserta fungsi dan pengelompokannya |
| **Materi Prasyarat** | Tidak ada (materi pertama) |

---

## A. Kisah Pemantik 🎬

> **"Komputer di Dapur"**
>
> Bu Ratna baru membuka warung makan dengan menu digital. Setiap hari ia menerima pesanan, mengolah bahan, menyajikan makanan, dan mencatat semua pesanan di bukunya. Tanpa ia sadari, warung Bu Ratna bekerja **persis seperti komputer**!
>
> - Pelanggan memesan menu → **INPUT**
> - Bu Ratna memasak sesuai pesanan → **PROSES**
> - Makanan disajikan ke pelanggan → **OUTPUT**
> - Semua pesanan dicatat di buku → **STORAGE**
>
> **Pertanyaan pemantik:** Jika satu komponen ini hilang (misal Bu Ratna lupa mencatat pesanan), apa yang terjadi pada warungnya? Kaitkan jawabanmu dengan cara kerja komputer!

---

## B. Apa Itu Perangkat Keras (Hardware)?

**Hardware** adalah seluruh komponen **fisik** komputer yang dapat **dilihat dan disentuh**, seperti keyboard, monitor, CPU, dan printer. Hardware adalah "tubuh" komputer, sedangkan software (perangkat lunak) adalah "jiwa" atau "otak ide" yang menjalankan tubuh tersebut.

| Istilah | Arti | Contoh |
|---|---|---|
| **Hardware** | Perangkat keras (fisik) | Keyboard, mouse, monitor, HDD |
| **Software** | Perangkat lunak (program) | Windows, Microsoft Word, Google Chrome |
| **Brainware** | Pengguna / orang yang mengoperasikan | Kamu! |

> 💡 **Ingat:** Komputer tidak bisa bekerja sendiri. Ia butuh **hardware** untuk bekerja, **software** untuk diatur, dan **brainware** (kamu) untuk memerintah.

---

## C. Skema Komputer: INPUT – PROSES – OUTPUT – STORAGE

Setiap komputer bekerja mengikuti alur sederhana berikut:

```
┌─────────┐    ┌─────────┐    ┌─────────┐
│  INPUT  │───▶│ PROSES  │───▶│ OUTPUT  │
└─────────┘    └─────────┘    └─────────┘
                    │
                    ▼
              ┌─────────┐
              │ STORAGE │
              └─────────┘
```

| Fungsi | Peran | Contoh | Analogi Warung |
|---|---|---|---|
| **INPUT** | Memasukkan data | Keyboard, mouse, scanner, mikrofon, webcam | Pelanggan memesan |
| **PROSES** | Mengolah data | CPU, chipset, GPU | Koki memasak |
| **OUTPUT** | Menampilkan hasil | Monitor, speaker, printer, proyektor | Makanan disajikan |
| **STORAGE** | Menyimpan data | HDD, SSD, flashdisk, DVD | Buku catatan pesanan |

**Kesalahan umum:** Banyak siswa mengira monitor termasuk perangkat input. **Salah!** Monitor hanya menampilkan hasil (output), bukan memasukkan data. Begitu juga layar sentuh — jika bisa disentuh, barulah menjadi perangkat input.

---

## D. CPU — Otak Komputer 🧠

**CPU (Central Processing Unit)** adalah komponen utama yang menjalankan semua instruksi dan perhitungan. CPU disebut "otak" komputer karena semua proses berlangsung di sini.

| Komponen CPU | Fungsi |
|---|---|
| **ALU (Arithmetic Logic Unit)** | Melakukan operasi matematika (+, −, ×, ÷) dan logika (lebih besar, sama dengan) |
| **Control Unit** | Mengatur aliran data dan mengendalikan seluruh bagian komputer |
| **Register** | Memori super cepat di dalam CPU untuk penyimpanan sementara |

> 💡 **Fakta menarik:** Kecepatan CPU diukur dalam **GHz** (gigahertz). Satu prosesor modern bisa menjalankan **miliaran instruksi per detik**! Bandingkan dengan kecepatanmu menulis satu kalimat.

---

## E. Jenis-Jenis Perangkat Keras

### E.1 Perangkat Input
| Perangkat | Fungsi |
|---|---|
| Keyboard | Mengetik teks, angka, dan perintah |
| Mouse | Menggerakkan kursor dan memilih objek |
| Scanner | Memindai dokumen/cetak menjadi digital |
| Mikrofon | Merekam suara |
| Webcam | Merekam gambar bergerak (video) |
| Joystick / Gamepad | Mengendalikan permainan |

### E.2 Perangkat Output
| Perangkat | Fungsi |
|---|---|
| Monitor | Menampilkan hasil dalam bentuk visual |
| Speaker | Mengeluarkan suara/audio |
| Printer | Mencetak ke kertas |
| Proyektor | Menampilkan tampilan ke layar besar |

### E.3 Perangkat Penyimpanan (Storage)
| Perangkat | Kapasitas | Kecepatan | Kelebihan |
|---|---|---|---|
| **HDD** | 500 GB – 2 TB | Lambat | Kapasitas besar, harga murah |
| **SSD** | 128 GB – 1 TB | Cepat | Boot dan transfer sangat cepat |
| **Flashdisk** | 8 GB – 256 GB | Sedang | Portabel, mudah dibawa |
| **DVD** | ±4,7 GB | Lambat | Murah, namun mulai ditinggalkan |
| **Memory Card** | 16 GB – 512 GB | Sedang | Untuk HP/kamera |

### HDD vs SSD — Mana yang Lebih Baik?

| Aspek | HDD | SSD |
|---|---|---|
| Cara kerja | Piringan berputar + jarum baca | Chip memori (tanpa bagian bergerak) |
| Kecepatan | Lambat | Sangat cepat |
| Ketahanan guncangan | Rentan rusak | Tahan guncangan |
| Harga per GB | Murah | Mahal |
| Ideal untuk | Data besar (file, backup) | Sistem operasi dan program |

> 💡 **Tips:** Laptop dengan **SSD** bisa menyala dalam hitungan detik, sedangkan yang masih HDD bisa memakan 1–2 menit!

---

## F. Contoh Soal & Penyelesaian 📝

**Contoh 1:** Sebutkan 3 contoh perangkat input beserta fungsinya!
**Jawaban:**
1. **Keyboard** — mengetik teks dan angka.
2. **Mouse** — menggerakkan kursor.
3. **Scanner** — memindai dokumen menjadi file digital.

**Contoh 2:** Mengapa CPU disebut "otak komputer"?
**Jawaban:** Karena CPU (terutama bagian ALU dan Control Unit) mengendalikan semua perhitungan dan instruksi, sehingga seluruh bagian komputer bekerja sesuai perintah. Tanpa CPU, data tidak dapat diolah.

**Contoh 3:** Jelaskan perbedaan HDD dan SSD!
**Jawaban:** HDD menyimpan data pada piringan berputar sehingga lebih lambat, sedangkan SSD menggunakan chip memori tanpa bagian bergerak sehingga jauh lebih cepat, lebih awet, dan tidak berisik. SSD lebih mahal per kapasitas yang sama.

---

## G. Miskonsepsi yang Sering Terjadi 🚫

| Miskonsepsi | Fakta yang Benar |
|---|---|
| "Monitor adalah perangkat input" | Monitor **hanya output**; untuk input, sentuh layarnya (touchscreen) |
| "Flashdisk termasuk perangkat proses" | Flashdisk termasuk **storage** (penyimpanan) |
| "Komputer bisa bekerja tanpa software" | Tanpa software, hardware tidak punya perintah untuk dijalankan |
| "Semakin besar RAM = semakin cepat *boot*" | RAM mempercepat kerja banyak aplikasi; boot lebih dipengaruhi SSD |

---

## H. Tantangan Praktik (Mengaplikasi) 🎯

**Tantangan 1 — Skema Komputer:** Gambarlah skema INPUT → PROSES → OUTPUT dengan kotak STORAGE di bawah PROSES. Tuliskan **2 contoh** di setiap kotak.

**Tantangan 2 — Observasi Lab:** Amati komputer di laboratorium sekolahmu. Catat:
- Merk dan tipe CPU: _______________
- Jenis penyimpanan (HDD/SSD): _______________
- 1 perangkat input tambahan selain keyboard dan mouse: _______________

**Tantangan 3 — Berpikir Kritis:** Warung Bu Ratna kehabisan kertas untuk mencatat pesanan (storage hilang). Apa solusi yang bisa dilakukan agar pesanan tetap tercatat? Hubungkan dengan cara kerja komputer modern.

---

## I. Rangkuman Kunci 🔑

1. **Hardware** = komponen fisik komputer yang bisa dilihat dan disentuh.
2. Alur kerja komputer: **INPUT → PROSES → OUTPUT → (STORAGE)**.
3. **CPU** adalah otak komputer, terdiri atas ALU, Control Unit, dan Register.
4. Perangkat input (keyboard, mouse), output (monitor, printer), dan storage (HDD, SSD).
5. **SSD lebih cepat** daripada HDD karena tidak ada bagian yang berputar.
6. Komputer bekerja optimal jika hardware, software, dan brainware saling mendukung.

---

## J. Glosarium 📖

| Istilah | Arti |
|---|---|
| **Hardware** | Perangkat keras — komponen fisik komputer |
| **CPU** | Central Processing Unit — otak komputer |
| **ALU** | Arithmetic Logic Unit — bagian CPU untuk perhitungan & logika |
| **SSD** | Solid State Drive — penyimpanan cepat tanpa bagian bergerak |
| **HDD** | Hard Disk Drive — penyimpanan berbasis piringan berputar |
| **Storage** | Media penyimpanan data permanen |

---

## K. Refleksi (Merefleksi) 🔍

- Konsep apa yang paling penting kamu pelajari hari ini?
- Bagaimana konsep INPUT–PROSES–OUTPUT terhubung dengan kehidupan sehari-harimu (selain komputer)?
- Bagian mana yang masih sulit dipahami?
- **Skala pemahaman diri:** ____/10
- Apa yang ingin kamu pelajari lebih lanjut tentang komputer?

---

**MGMP Informatika SMAN 6 Cimahi — Fase E (Kelas X) Semester 1**