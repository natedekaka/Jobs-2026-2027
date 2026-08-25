# BAHAN AJAR – PERTEMUAN 15 (S2)
## PAS & Portofolio
*Mengacu pada Panduan Mapel 2025; INFORMATIKA Fase D-F — pendekatan Pembelajaran Mendalam (Memahami → Mengaplikasi → Merefleksi)*

| Informasi | Keterangan |
|---|---|
| **Fase / Kelas** | F / Kelas XI |
| **Alokasi Waktu** | 5 JP × 45 menit (225 menit) |
| **Elemen CP** | Praktik Lintas Bidang (PLB) |
| **Tujuan Pembelajaran** | Menghadapi Penilaian Akhir Semester, memahami kisi-kisi PAS, dan menyusun portofolio karya Semester 2 |
| **Materi Prasyarat** | Seluruh materi Semester 2 (Pertemuan 1-14) |

---

## A. Skenario Ujian 🎬

> **"Pameran Karya Akhir Tahun"**
>
> Di akhir tahun, sekolah mengadakan pameran: setiap siswa memamerkan karya terbaiknya sepanjang semester. Ada yang memamerkan program buatan, ada yang memajang hasil praktikum jaringan. Semua karya itu menjadi **portofolio** — bukti bahwa belajar benar-benar menghasilkan karya nyata.
>
> Sebelum pameran, ada **PAS** (Penilaian Akhir Semester) yang menguji seluruh kompetensi. Hari ini kamu akan memahami format PAS, berlatih dengan contoh soal, dan merapikan portofolio terbaikmu.
>
> **Pertanyaan pemantik:** Karya apa saja yang bisa kamu banggakan dari Semester 2 ini? Bagaimana portofolio bisa menunjukkan perkembangan belajarmu kepada orang lain?

---

## B. Panduan PAS 🧭

| Aspek | Keterangan |
|---|---|
| **Durasi** | 225 menit (5 JP) |
| **Format** | Pilihan ganda (PG) + esai |
| **Ruang lingkup** | Seluruh materi Semester 2: Python (Pertemuan 1-10) dan Jaringan & Keamanan (Pertemuan 11-13) |
| **Skor** | Gabungan nilai PG dan esai |
| **Tips** | Pahami kisi-kisi, latihan contoh soal, dan kelola waktu |

**Format PAS:**

| Sesi | Durasi | Jenis Soal |
|---|---|---|
| A | ±60 menit | Pilihan ganda |
| B | ±45 menit | Esai (termasuk menulis program) |

---

## C. Kisi-Kisi PAS 📋

| Materi | Jumlah Soal (PG) | Esai |
|---|---|---|
| Python dasar (print, variabel, tipe data) | 4 | - |
| Operator (aritmatika, logika) | 3 | - |
| IF Percabangan | 3 | 1 |
| FOR & WHILE | 3 | 1 |
| List & Tuple | 3 | - |
| Fungsi | 3 | 1 |
| Program (kalkulator, nilai, kuis) | 3 | - |
| Jaringan (dasar, perangkat, topologi) | 4 | - |
| Keamanan Digital (malware, phishing) | 4 | - |

**Fokus utama yang harus dikuasai:**
1. Menulis program dengan input → proses → output.
2. Percabangan `if/elif/else` dan perulangan `for`/`while`.
3. Fungsi dengan parameter dan `return`.
4. Konsep jaringan: IP, DNS, perangkat, topologi, WiFi.
5. Keamanan digital: password, 2FA, phishing, malware.

---

## D. Contoh Soal Pilihan Ganda 📝

**Soal 1:** Sintaks yang benar untuk mencetak teks di Python adalah...
a) `print "Halo"`  b) `print("Halo")`  c) `PRINT("Halo")`  d) `echo("Halo")`
**Jawaban: b** — Python peka huruf besar/kecil, fungsi ditulis `print`.

**Soal 2:** Hasil dari `10 % 3` adalah...
a) 1  b) 3  c) 3.33  d) 30
**Jawaban: a** — `%` adalah sisa bagi; `10 = 3*3 + 1`.

**Soal 3:** Kata kunci untuk percabangan adalah...
a) `for`  b) `while`  c) `if`  d) `def`
**Jawaban: c** — `if` (dengan `elif`/`else`) untuk percabangan.

**Soal 4:** Perangkat yang menghubungkan perangkat dalam satu jaringan lokal adalah...
a) modem  b) switch  c) router  d) BTS
**Jawaban: b** — switch menghubungkan perangkat dalam satu LAN.

**Soal 5:** Ancaman yang menyamar sebagai program baik untuk mencuri data adalah...
a) virus  b) worm  c) trojan  d) ransomware
**Jawaban: c** — trojan menyamar sebagai program baik.

**Soal 6:** Untuk mengulang blok kode selama kondisi bernilai `True`, digunakan...
a) `if`  b) `while`  c) `print`  d) `range`
**Jawaban: b** — `while` mengulang selama kondisi benar.

---

## E. Contoh Soal Esai ✍️

**Esai 1:** Buat program yang menerima input 3 angka lalu mencetak angka terbesar!

**Jawaban:**
```python
a = float(input("Angka 1: "))
b = float(input("Angka 2: "))
c = float(input("Angka 3: "))

terbesar = a
if b > terbesar:
    terbesar = b
if c > terbesar:
    terbesar = c
print("Terbesar:", terbesar)
```

**Output (jika input 12, 45, 7):**
```
Terbesar: 45.0
```

**Esai 2:** Buat fungsi `faktorial(n)` yang menghitung `n!` menggunakan perulangan!

**Jawaban:**
```python
def faktorial(n):
    hasil = 1
    for i in range(1, n + 1):
        hasil *= i
    return hasil

print(faktorial(5))
```

**Output:**
```
120
```

**Esai 3:** Jelaskan perbedaan LAN dan WAN beserta contohnya!

**Jawaban acuan:** LAN (Local Area Network) adalah jaringan dengan cakupan kecil seperti satu gedung atau lab komputer, contohnya jaringan WiFi di sekolah. WAN (Wide Area Network) mencakup area sangat luas bahkan antar negara, contohnya internet. LAN cepat dan mudah dikelola; WAN membutuhkan infrastruktur besar dan menghubungkan banyak LAN.

---

## F. Portofolio Semester 2 📁

Portofolio adalah kumpulan karya terbaik yang menunjukkan perkembangan belajarmu.

| No | Karya | Format |
|---|---|---|
| 1 | Program Python (Kalkulator / To-Do List) | `.ipynb` (Colab) |
| 2 | Program Python (BMI / Nilai / Kuis) | `.ipynb` (Colab) |
| 3 | Tugas Jaringan (gambar topologi, hasil ping/tracert) | `.pdf` |

**Langkah menyusun portofolio:**
1. Pilih 3 karya terbaikmu.
2. Pastikan setiap program **dapat dijalankan tanpa error**.
3. Beri nama file yang jelas, misal `Kalkulator_NamaSiswa.ipynb`.
4. Sertakan catatan singkat: tujuan program, fitur, dan hasil uji.
5. Simpan di satu folder `Portofolio_Informatika_S2`.

**Aspek penilaian portofolio:**

| Aspek | Bobot |
|---|---|
| Kelengkapan | 30% |
| Kebenaran kode | 30% |
| Kreativitas | 20% |
| Refleksi diri | 20% |

---

## G. Contoh Soal Latihan Tambahan 🎯

**Latihan 1:** Tulis program yang menerima nilai sebuah siswa dan mencetak "Lulus" jika ≥ 70, selain itu "Tidak Lulus".

```python
nilai = float(input("Nilai: "))
if nilai >= 70:
    print("Lulus")
else:
    print("Tidak Lulus")
```

**Latihan 2:** Tulis program yang mencetak bilangan genap 1-20 menggunakan `for` dan `range`.

```python
for i in range(2, 21, 2):
    print(i, end=" ")
```

**Latihan 3:** Buat list 5 nama teman, lalu cetak nama pada indeks ke-3.

```python
teman = ["Andi", "Budi", "Citra", "Dewi", "Eka"]
print(teman[3])
```
**Output:**
```
Dewi
```

---

## H. Miskonsepsi & Kesalahan Umum 🚫

| Miskonsepsi / Kesalahan | Fakta yang Benar |
|---|---|
| "PAS hanya menguji hafalan" | PAS menguji pemahaman dan kemampuan menulis program |
| "Portofolio cukup satu karya" | Kumpulkan minimal 3 karya terbaik dengan format yang diminta |
| "Program yang sudah jalan tidak perlu diuji lagi" | Selalu uji ulang sebelum dikumpulkan |
| "Esai cukup satu kalimat" | Susun jawaban runtut: definisi → contoh → saran |
| "Menyalin pekerjaan teman tidak masalah" | Plagiarisme merugikan dirimu dan melanggar kejujuran |
| "Terlambat mengumpulkan portofolio tidak apa-apa" | Kelola waktu; portofolio adalah bagian nilai |

---

## I. Tantangan Praktik (Mengaplikasi) 🎯

**Tantangan 1 — Simulasi PAS (Mudah):** Kerjakan 10 soal PG contoh dalam batas waktu, lalu periksa sendiri dengan pembahasan.

**Tantangan 2 — Latihan Esai (Sedang):** Kerjakan ketiga contoh esai (angka terbesar, faktorial, LAN vs WAN) secara mandiri dalam batas waktu.

**Tantangan 3 — Audit Program (Sedang):** Periksa 3 program terbaikmu: pastikan tidak error, input/output sesuai, dan beri komentar penjelasan.

**Tantangan 4 — Susun Portofolio (Sulit):** Pilih dan rapi kan 3 karya terbaik, lengkapi dengan catatan tujuan, fitur, dan hasil uji.

**Tantangan 5 — Refleksi Akhir (Sulit):** Tulis refleksi satu paragraf: apa yang sudah kamu kuasai, apa yang masih sulit, dan rencanamu di semester berikutnya.

---

## J. Rangkuman Kunci 🔑

- **PAS** menguji seluruh materi Semester 2: Python dan Jaringan & Keamanan.
- Format PAS: pilihan ganda + esai (termasuk menulis program).
- Kuasai kisi-kisi: Python dasar, operator, percabangan, perulangan, list, fungsi, jaringan, keamanan.
- **Portofolio** berisi minimal 3 karya terbaik dengan format yang diminta.
- Program portofolio harus bebas error dan disertai catatan singkat.
- Jaga kejujuran: kerjakan sendiri dan susun jawaban esai secara runtut.

---

## K. Glosarium 📖

| Istilah | Arti |
|---|---|
| **PAS** | Penilaian Akhir Semester |
| **Portofolio** | Kumpulan karya terbaik sebagai bukti belajar |
| **Pilihan Ganda** | Soal dengan pilihan jawaban |
| **Esai** | Soal uraian jawaban |
| **Kisi-kisi** | Ringkasan materi yang diujikan |
| **Plagiarisme** | Menyalin karya orang lain tanpa izin |
| **Refleksi** | Perenungan terhadap proses belajar |

---

## L. Refleksi (Merefleksi) 🔍

- Karya apa yang paling kamu banggakan dari Semester 2 ini dan mengapa?
- Bagaimana portofolio membantu kamu melihat perkembangan belajar selama satu semester?
- Apa target belajarmu untuk semester berikutnya?
- **Skala pemahaman diri:** ____/10
- Apa pesan atau saran untuk dirimu sendiri di tahun ajaran ini?

---

**MGMP Informatika SMAN 6 Cimahi — Fase F (Kelas XI) Semester 2**