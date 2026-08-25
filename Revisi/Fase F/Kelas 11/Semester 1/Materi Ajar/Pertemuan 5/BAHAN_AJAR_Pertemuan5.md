# BAHAN AJAR – PERTEMUAN 5 (S1)
## Notasi Algoritma & Flowchart
*Mengacu pada Panduan Mapel 2025; INFORMATIKA Fase D-F — pendekatan Pembelajaran Mendalam (Memahami → Mengaplikasi → Merefleksi)*

| Informasi | Keterangan |
|---|---|
| **Fase / Kelas** | F / Kelas XI |
| **Alokasi Waktu** | 5 JP × 45 menit (225 menit) |
| **Elemen CP** | Algoritma dan Pemrograman (AP) |
| **Tujuan Pembelajaran** | Menjelaskan fungsi flowchart, mengidentifikasi simbol-simbol flowchart standar, menggambar flowchart sederhana, dan melakukan tracing untuk memeriksa kebenaran alur |
| **Materi Prasyarat** | Pertemuan 1–4 — Algoritma dan 4 pilar Computational Thinking |

---

## A. Kisah Pemantik 🎬

> **"Resep yang Sulit Dipahami"**
>
> Andi menulis resep masakan dalam 3 paragraf teks panjang. Ibunya kesulitan membacanya karena harus mencari-cari di mana langkah "aduk" dan "diamkan". Lalu Andi menggambar **peta langkah** dengan kotak-kotak dan panah: setiap kotak satu langkah, panah menunjukkan urutan, belah ketupat untuk keputusan "apakah sudah matang?". Ibunya langsung paham!
>
> **Pertanyaan pemantik:** Apa keuntungan menyampaikan alur dengan gambar daripada teks panjang? Pernahkah kamu melihat diagram alur (flowchart) dalam kehidupan sehari-hari?

---

## B. Apa Itu Flowchart?

**Flowchart** adalah representasi grafis dari algoritma menggunakan simbol-simbol standar. Flowchart memudahkan pembacaan alur logika karena **visual** — kita tidak perlu membaca teks panjang untuk memahami urutan langkah.

**Mengapa Flowchart Penting?**
1. Memvisualisasikan algoritma sebelum coding
2. Memudahkan komunikasi antar programmer
3. Membantu menemukan error logika (debugging)
4. Dokumentasi program yang mudah dipahami

---

## C. Simbol-Simbol Dasar Flowchart

| Simbol | Nama | Fungsi |
|---|---|---|
| ○ Oval / Terminator | **Mulai (Start)** atau **Selesai (End)** program |
| ▱ Jajar Genjang | **Input** (membaca data) atau **Output** (menampilkan hasil) |
| ▭ Persegi Panjang | **Proses** — operasi/perhitungan/assignment |
| ◇ Belah Ketupat | **Keputusan** — percabangan/kondisi (Ya/Tidak) |
| → Garis Panah | Menunjukkan **arah aliran** |
| ○ Lingkaran (kecil) | **Konektor** — penghubung antar bagian/halaman |

---

## D. Aturan Penulisan Flowchart

1. Satu simbol → satu aktivitas (jangan digabung)
2. Menggunakan kata kerja yang jelas: "Masukkan kopi", bukan "Kopi"
3. Garis alir tidak boleh putus
4. Hindari garis bersilangan — gunakan konektor jika perlu
5. Setiap **decision** harus memiliki 2 cabang: **Ya** dan **Tidak**
6. Mulai dengan Start dan akhiri dengan End

---

## E. Contoh Flowchart — Membuat Kopi

```
┌─────────┐
│  START  │
└────┬────┘
     ▼
┌────────────────────────────────────┐
│ Siapkan cangkir, kopi, gula, air   │
│ panas, dan sendok                  │
└────┬───────────────────────────────┘
     ▼
┌──────────────────────────────┐
│ Masukkan kopi instan ke dalam │
│ cangkir                       │
└────┬─────────────────────────┘
     ▼
┌──────────────────────┐
│ Masukkan gula sesuai │
│ selera (1–2 sendok)  │
└────┬─────────────────┘
     ▼
┌──────────────────────┐
│ Tuang air panas      │
└────┬─────────────────┘
     ▼
┌──────────────────────┐
│ Aduk hingga rata     │
└────┬─────────────────┘
     ▼
┌─────────┐
│  END    │
└─────────┘
```

---

## F. Tracing — Mengecek Kebenaran Flowchart

**Tracing** adalah simulasi menjalankan flowchart langkah demi langkah untuk memastikan alurnya benar.

**Langkah Tracing:**
1. Mulai dari Start
2. Ikuti setiap langkah dengan memberi nilai pada variabel
3. Catat perubahan di setiap langkah
4. Pastikan output sesuai yang diharapkan

**Contoh Tracing — Flowchart "Hitung Luas":**
1. Start
2. Input panjang = 5, lebar = 3
3. Luas = 5 × 3 = **15**
4. Output "Luas = 15"
5. End ✅

---

## G. Contoh Soal & Penyelesaian 📝

**Contoh 1:** Gambarkan simbol flowchart untuk Terminal, I/O, Proses, dan Decision!
**Jawaban:** Terminal = **oval** (mulai/selesai); I/O = **jajar genjang** (input/output); Proses = **persegi panjang** (perhitungan); Decision = **belah ketupat** (percabangan Ya/Tidak).

**Contoh 2:** Buat flowchart "Membeli Es Jeruk" minimal 6 langkah!
**Jawaban:** Start → siapkan uang → datang ke penjual → pilih ukuran es jeruk (besar/kecil) → bayar dan terima es jeruk → ucapkan terima kasih → End.

**Contoh 3:** Diberikan flowchart "Login": Start → input user/pass → cek → jika benar "Selamat datang" → End. Jika salah → apa yang harus ditambahkan?
**Jawaban:** Harus ada cabang **Tidak** dari decision "user/pass benar?": kembali ke "input user/pass" (loop) atau menampilkan pesan "Login gagal" lalu **end**. Tanpa cabang tersebut, flowchart tidak lengkap karena keputusan butuh 2 jalan keluar.

**Contoh 4:** Tracing flowchart dengan input nilai = 75. Jika nilai ≥ 70 → "Lulus", jika tidak → "Remedial". Apa outputnya?
**Jawaban:** Karena 75 ≥ 70, cabang Ya diambil → output **"Lulus"**. Jika nilai diubah menjadi 60, outputnya "Remedial".

**Contoh 5:** Buat flowchart konversi suhu: input Celcius, hitung Fahrenheit = C × 9/5 + 32, lalu output!
**Jawaban:** Start → input C → F = C × 9/5 + 32 → output F → End. Contoh: C=25 → F = 25 × 9/5 + 32 = **77**.

---

## H. Miskonsepsi / Kesalahan Umum 🚫

| Miskonsepsi / Kesalahan | Fakta yang Benar |
|---|---|
| Tidak ada Start/End | Algoritma tidak jelas batas mulainya |
| Tidak ada input | Data tidak jelas berasal dari mana |
| Decision hanya 1 cabang | Keputusan wajib memiliki 2 cabang: Ya dan Tidak |
| Garis alir tidak jelas/bersilangan | Alur menjadi ambigu — gunakan konektor |
| Proses tidak terdefinisi | "Hitung" tanpa jelas hitung apa → salah |
| Dua aktivitas dalam satu simbol | Satu simbol = satu aktivitas |

---

## I. Tantangan Praktik (Mengaplikasi) 🎯

**Tantangan 1 — Simbol (mudah):** Gambar dan beri nama 4 simbol dasar flowchart di bukumu.

**Tantangan 2 — Flowchart Sederhana (sedang):** Buat flowchart "menyikat gigi" minimal 6 langkah tanpa percabangan.

**Tantangan 3 — Flowchart I/O (sulit):** Buat flowchart menghitung rata-rata 3 nilai: input nilai1, nilai2, nilai3 → rata = (n1+n2+n3)/3 → output.

**Tantangan 4 — Tracing (paling sulit):** Gambar flowchart "hitung luas lingkaran" (π × r²), lalu lakukan tracing dengan r = 7 (π = 3,14) dan tulis hasil di setiap langkah.

---

## J. Rangkuman Kunci 🔑

- **Flowchart** = representasi visual algoritma dengan simbol standar.
- 5 simbol utama: **Terminal (oval), I/O (jajar genjang), Proses (persegi), Decision (belah ketupat), Garis alir (panah)**.
- Aturan: 1 simbol = 1 aktivitas, decision harus punya 2 cabang, garis tidak putus.
- **Tracing** = simulasi menjalankan flowchart untuk memeriksa kebenaran.
- Flowchart lebih mudah dipahami daripada teks panjang.

---

## K. Glosarium 📖

| Istilah | Arti |
|---|---|
| **Flowchart** | Diagram alir berbasis simbol untuk menggambarkan algoritma |
| **Terminal** | Simbol oval untuk mulai/selesai |
| **Decision** | Simbol belah ketupat untuk percabangan kondisi |
| **Tracing** | Menelusuri alur flowchart dengan nilai konkret |
| **Konektor** | Simbol lingkaran penghubung antar bagian |
| **Assignment** | Proses pemberian nilai ke variabel (misal: luas = p × l) |

---

## L. Refleksi (Merefleksi) 🔍

- Konsep apa yang paling penting kamu pelajari hari ini?
- Apa keuntungan flowchart dibanding teks untuk menyampaikan alur?
- Bagian mana yang masih sulit dipahami?
- **Skala pemahaman diri:** ____/10
- Apa yang ingin kamu pelajari lebih lanjut tentang flowchart?

---

**MGMP Informatika SMAN 6 Cimahi — Fase F (Kelas XI) Semester 1**