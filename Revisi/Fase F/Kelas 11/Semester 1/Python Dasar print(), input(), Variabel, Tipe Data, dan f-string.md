## Python Dasar: `print()`, `input()`, Variabel, Tipe Data, dan f-string

------

## A. INFORMASI UMUM

| Komponen                             | Keterangan                                                   |
| ------------------------------------ | ------------------------------------------------------------ |
| **Satuan Pendidikan**                | SMA NEGERI 6 CIMAHI                                          |
| **Mata Pelajaran**                   | Informatika                                                  |
| **Fase / Kelas / Semester** / **TP** | Fase F / Kelas XI / Semester Ganjil / 2026-2026              |
| **Elemen CP**                        | Algoritma dan Pemrograman (AP)                               |
| **Materi Pokok**                     | Pengenalan Python Dasar: fungsi `print()`, `input()`, variabel, tipe data, dan f-string |
| **Alokasi Waktu**                    | 1 pertemuan / 5 JP (5 × 45 menit = 225 menit)                |
| **Moda Pembelajaran**                | Tatap muka (luring) berbantuan komputer / laptop / HP        |
| **Model Pembelajaran**               | Discovery Learning + praktik coding (plugged) dengan scaffolding |
| **Pendekatan**                       | Saintifik, berdiferensiasi, kontekstual                      |
| **Metode**                           | Demonstrasi, tanya jawab, latihan terbimbing, unjuk kerja, refleksi |
| **Penyusun**                         | Daniarsyah S.Kom                                             |
| **Tahun**                            | 2026                                                         |

### 1. Capaian Pembelajaran (Cuplikan Elemen AP Fase F)

Peserta didik mampu mengembangkan program komputer terstruktur dalam notasi algoritma atau kode sumber berdasarkan strategi algoritmik yang tepat; mengembangkan, memelihara, dan menyempurnakan kode sumber program dengan memperhatikan kualitasnya.

### 2. Tujuan Pembelajaran

Setelah mengikuti pembelajaran, peserta didik mampu:

1. Menjelaskan fungsi `print()` dan `input()` serta peran variabel dalam program Python.
2. Menerapkan aturan penamaan variabel yang sahih dan gaya penulisan yang rapi.
3. Membedakan tipe data dasar Python (`str`, `int`, `float`, `bool`) serta melakukan konversi tipe data.
4. Menggunakan f-string untuk menampilkan keluaran yang terformat, mudah dibaca, dan bermakna.
5. Menyusun program interaktif sederhana yang menerima masukan pengguna, menyimpan data ke variabel, dan menampilkan hasil dengan `print()` serta f-string.

### 3. Kompetensi Awal

Peserta didik sudah:

- mengenal konsep algoritma sederhana (langkah-langkah menyelesaikan masalah);
- mampu mengoperasikan komputer (membuka file, mengetik, menyimpan);
- idealnya sudah menginstal Python 3.x dan editor (VS Code / Thonny / IDLE / Google Colab sebagai alternatif), untuk media HP menggunakan pydroid 3 atau web online

### 4. Profil Pelajar Pancasila

- **Bernalar kritis**: menganalisis error, membedakan tipe data, dan memperbaiki kode.
- **Mandiri**: menyelesaikan latihan coding secara bertahap.
- **Bergotong royong**: berpasangan saat debugging (pair programming).
- **Kreatif**: merancang keluaran program yang informatif dengan f-string.

### 5. Target Peserta Didik

Peserta didik kelas XI dengan keragaman kemampuan:

- **Siap belajar** (mahir): diberikan tantangan tambahan (format angka, multi-input).
- **Berkembang**: mengikuti alur terbimbing + contoh.
- **Perlu dukungan**: mendapat scaffolding, template kode, dan pendampingan.

### 6. Sarana dan Prasarana

- Laptop/PC/HP + Python 3.10+ (atau Google Colab / Replit, Web Online)
- Proyektor / layar
- Papan tulis / slide
- LKPD cetak atau digital
- Koneksi internet (opsional)
- File contoh: `biodata.py`

### 7. Pemahaman Bermakna

Program komputer “berbicara” dengan pengguna melalui keluaran (`print`) dan “mendengar” melalui masukan (`input`). Variabel adalah wadah bernama untuk menyimpan data. Tipe data menentukan cara data diproses. f-string membuat pesan program lebih manusiawi, rapi, dan mudah dipahami.

### 8. Pertanyaan Pemantik

1. Bagaimana cara komputer “menyapa” kita dan “mendengar” jawaban kita?
2. Mengapa `2 + 3` hasilnya 5, tetapi `"2" + "3"` hasilnya `"23"`?
3. Bagaimana menampilkan kalimat seperti: *Halo, Nate! Nilai akhirmu 87.50* tanpa merangkai string secara manual dan berantakan?

------

## B. PERSIAPAN PEMBELAJARAN

- Pastikan interpreter Python berjalan (`python --version`).
- Siapkan 3 file starter: `01_print.py`, `02_variabel.py`, `03_biodata.py`.
- Siapkan asesmen diagnostik singkat (5 butir, 5 menit).
- Siapkan rubrik unjuk kerja dan kunci LKPD.
- Atur tempat duduk pair-programming (2 siswa / 1 perangkat jika perlu).

------

## C. KEGIATAN PEMBELAJARAN

**Total 225 menit.** Istirahat mikro 3–5 menit disisipkan di pergantian JP.

### JP 1 — Pendahuluan & Fungsi `print()` (0–45 menit)

**Pendahuluan (15 menit)**

- Salam, doa, presensi, ice breaking: “Kalau program bisa bicara, kalimat pertama apa yang ingin kamu cetak?”
- Asesmen diagnostik singkat (lisan/tertulis, 5 butir):
  1. Apa itu program?
  2. Apa bedanya data angka dan teks?
  3. Pernahkah menulis kode?
  4. Apa fungsi tombol *Run*?
  5. Apa yang terjadi jika mengetik `print(Halo)` tanpa tanda kutip?
- Menyampaikan tujuan, alur 5 JP, dan kriteria keberhasilan.
-  Apersepsi: manusia berkomunikasi; program juga butuh “suara” (`print`) dan “telinga” (`input`).

**Kegiatan Inti JP 1 (30 menit)**

- Demonstrasi program pertama:

```
print("Halo, dunia!")
print("Selamat datang di kelas Informatika.")
print("Python", "itu", "menyenangkan")
print("Baris 1\nBaris 2")
```

- Eksplorasi parameter sederhana: beberapa argumen, `sep`, `end`.

```
print("A", "B", "C", sep="-")
print("Lanjut...", end=" ")
print("di baris yang sama")
```

- Latihan cepat (individu, 8 menit):
  1. Cetak nama sekolah dalam 2 baris.
  2. Cetak `Informatika-Fase-F` menggunakan `sep`.
  3. Prediksi output sebelum dijalankan (think–pair–share).

**Indikator keberhasilan JP 1:** siswa mampu menjalankan `print()` tanpa error sintaks dasar.

------

### JP 2 — Variabel (45–90 menit)

**Kegiatan Inti JP 2**

- Analogi: variabel = kotak berlabel. Isi kotak bisa diganti.

```
nama = "Raka"
umur = 16
print(nama)
print(umur)
nama = "Sinta"   # isi kotak diganti
print(nama)
```

- Aturan identifier:
  - boleh huruf, angka, underscore;
  - tidak boleh diawali angka;
  - tidak boleh keyword (`if`, `class`, `print` sebagai nama variabel dihindari);
  - case-sensitive (`Nama` ≠ `nama`);
  - gaya disarankan: `snake_case`.
- Latihan prediksi:

```
x = 10
y = x
x = 20
print(x, y)   # prediksi?
```

- Praktik terbimbing: buat 4 variabel (`nama_lengkap`, `kelas`, `hobi`, `kota`) lalu cetak.

**Asesmen formatif JP 2:** siswa memperbaiki 3 nama variabel yang salah (`1nama`, `nama siswa`, `class`).

------

### JP 3 — Tipe Data & Konversi (90–135 menit)

**Kegiatan Inti JP 3**

- Empat tipe dasar yang wajib dikuasai di pertemuan ini:

| Tipe    | Contoh literal   | Makna          | Fungsi cek |
| ------- | ---------------- | -------------- | ---------- |
| `str`   | `"11"` / `'A'`   | teks           | `type()`   |
| `int`   | `11`             | bilangan bulat | `type()`   |
| `float` | `11.5`           | pecahan        | `type()`   |
| `bool`  | `True` / `False` | logika         | `type()`   |

```
a = "17"
b = 17
c = 17.0
d = True
print(type(a), type(b), type(c), type(d))
```

- Insight kunci: `input()` **selalu** menghasilkan `str`.

```
angka = input("Umur: ")     # hasilnya string
# print(angka + 1)          # error
angka = int(angka)
print(angka + 1)
```

- Konversi: `int()`, `float()`, `str()`, `bool()`.
- Demonstrasi error klasik: `ValueError` saat `int("tujuh")`.
- Latihan:
  1. Ubah `"3.14"` menjadi `float`.
  2. Ubah `25` menjadi string lalu gabungkan dengan `" tahun"`.
  3. Jelaskan mengapa `"10" + "2"` ≠ `10 + 2`.

**Checkpoint:** siswa dapat menyebutkan tipe sebuah nilai dan memilih fungsi konversi yang tepat.

------

### JP 4 — `input()` dan f-string (135–180 menit)

**Kegiatan Inti JP 4**

- `input(prompt)`: prompt adalah pesan untuk pengguna.

```
nama = input("Masukkan nama: ")
mapel = input("Mata pelajaran favorit: ")
```

- Masalah perangkaian string lama:

```
print("Halo, " + nama + ". Mapel favoritmu " + mapel + ".")
```

- Solusi modern: **f-string** (Python 3.6+):

```
print(f"Halo, {nama}. Mapel favoritmu {mapel}.")
```

- Fitur f-string yang diajarkan di pertemuan ini:
  - sisipan variabel: `f"Halo, {nama}"`
  - ekspresi di dalam `{}`: `f"Tahun depan umurmu {umur + 1}"`
  - format angka: `f"Nilai: {nilai:.2f}"`

```
harga = 15000
jumlah = 3
print(f"Total bayar: Rp{harga * jumlah:,}")
```

- Latihan berpasangan (15 menit): program sapaan + prediksi umur tahun depan + format 2 desimal.

**Kesalahan yang dicegah guru:**

- lupa prefiks `f`;
- memakai `F` atau tidak menaruh variabel di `{}`;
- mengira `input()` langsung bertipe `int`.

------

### JP 5 — Proyek Mini, Asesmen, Penutup (180–225 menit)

**Proyek unjuk kerja (25 menit):**
*Program Kartu Identitas Digital Siswa*

Spesifikasi wajib:

1. Meminta minimal 5 data: nama, NIS, kelas, tinggi badan (cm), cita-cita.
2. Tinggi badan dikonversi ke `float`.
3. Tampilkan kartu identitas rapi memakai f-string (minimal 6 baris keluaran).
4. Tampilkan juga tinggi dalam meter (`tinggi / 100`) dengan 2 desimal.
5. Simpan file `kartu_identitas.py`.

Contoh kerangka:

```
print("=== KARTU IDENTITAS DIGITAL ===")
nama = input("Nama lengkap : ")
nis = input("NIS          : ")
kelas = input("Kelas        : ")
tinggi_cm = float(input("Tinggi (cm)  : "))
cita = input("Cita-cita    : ")

tinggi_m = tinggi_cm / 100
print("\n---------- HASIL ----------")
print(f"Nama      : {nama}")
print(f"NIS       : {nis}")
print(f"Kelas     : {kelas}")
print(f"Tinggi    : {tinggi_cm:.0f} cm ({tinggi_m:.2f} m)")
print(f"Cita-cita : {cita}")
print("---------------------------")
```

**Asesmen sumatif singkat (10 menit):** 8 soal (terlampir).
**Refleksi & penutup (10 menit):**

- Siswa mengisi 3-2-1: 3 hal dipelajari, 2 hal masih bingung, 1 aplikasi di kehidupan nyata.
- Guru merangkum 5 kata kunci: **print – input – variabel – tipe data – f-string**.
- Teaser pertemuan berikutnya: operator dan ekspresi.
- Doa penutup.

------

## D. ASESMEN

### 1. Diagnostik (awal)

5 pertanyaan konsep (tidak dinilai angka, untuk pemetaan).

### 2. Formatif

- Observasi keaktifan dan debugging.
- Prediksi output (think–pair–share).
- Koreksi nama variabel dan tipe data.
- Checklist proses coding.

### 3. Sumatif (akhir pertemuan)

**A. Pilihan ganda / isian singkat (skor 40)**

1. Output `print("A", "B", sep=":")` adalah …  
2. Hasil `type(input("x: "))` selalu …  
3. Nama variabel yang sah: `nilai_siswa` / `2nilai` / `nilai siswa`  
4. Konversi `"12.5"` ke pecahan memakai fungsi …  
5. Perbedaan `"7" + "3"` dan `7 + 3` …  
6. f-string ditandai dengan … di depan string.  
7. `print(f"{3.14159:.2f}")` menampilkan …  
8. Keyword tidak boleh dijadikan nama variabel. Contoh keyword: …

**B. Unjuk kerja program (skor 60)** — lihat rubrik.

### Rubrik Unjuk Kerja (skala 4)

| Aspek                   | 4 (Sangat Baik)                    | 3 (Baik)                           | 2 (Cukup)             | 1 (Perlu Bimbingan) |
| ----------------------- | ---------------------------------- | ---------------------------------- | --------------------- | ------------------- |
| Fungsionalitas          | Semua input–proses–output berjalan | Berjalan dengan 1 kekurangan minor | Berjalan sebagian     | Banyak error        |
| Variabel & tipe data    | Nama jelas, konversi tepat         | Ada konversi, nama cukup           | Konversi kurang tepat | Acak / error tipe   |
| f-string                | Digunakan dengan format rapi       | Digunakan dasar                    | Campur concatenasi    | Tidak dipakai       |
| Keterbacaan kode        | Rapi, ada komentar singkat         | Cukup rapi                         | Berantakan            | Sulit dibaca        |
| Kemandirian & debugging | Mandiri, error ditangani           | Sedikit bantuan                    | Banyak bantuan        | Belum selesai       |

**Nilai akhir pertemuan** = (Tes tertulis × 40%) + (Unjuk kerja × 60%)

### Kriteria Ketuntasan

Tuntas jika nilai akhir ≥ 75 dan program mini dapat dijalankan.

------

## E. DIFERENSIASI, PENGAYAAN, DAN REMEDIAL

**Diferensiasi konten**

- Mahir: tambah format `:,` pada angka, hitung BMI sederhana, atau validasi input tidak kosong.
- Berkembang: ikuti spesifikasi wajib.
- Perlu dukungan: template kode berlubang (fill-in-the-blank).

**Pengayaan**

- Cetak tabel nilai 3 mapel dengan f-string rata kanan.
- Eksperimen `sep`, `end`, dan escape character (`\n`, `\t`).

**Remedial**

- Ulangi 4 langkah: `print` → variabel → `type`/`int` → f-string dengan pendampingan.
- Latihan 5 soal prediksi output.
- Video/micro-demo 10 menit, lalu buat ulang program sapaan.

------

## F. REFLEKSI

**Refleksi peserta didik**

1. Bagian mana yang paling mudah dan paling sulit?
2. Kapan kamu akan memakai f-string di program berikutnya?
3. Jika `input()` menghasilkan string, apa yang harus kamu lakukan sebelum berhitung?

**Refleksi guru**

- Apakah alokasi 5 JP cukup untuk unjuk kerja?
- Apakah perangkat dan instalasi Python menjadi hambatan?
- Siswa mana yang perlu pair-programming di pertemuan berikutnya?
- Apakah contoh kontekstual (biodata, uang saku, nilai) sudah relevan?

------

## G. LAMPIRAN

### Lampiran 1 — LKPD Peserta Didik

**LKPD 01: Python Dasar (print, input, variabel, tipe data, f-string)**
Nama: __________ Kelas: __________ Kelompok: __________

**Kegiatan 1 — Prediksi sebelum menjalankan**
Tulis prediksi, lalu cek dengan komputer.

| No   | Kode                        | Prediksiku | Hasil aktual | Catatan |
| ---- | --------------------------- | ---------- | ------------ | ------- |
| 1    | `print("SMA", 11, sep="-")` |            |              |         |
| 2    | `x = "5"; print(x + x)`     |            |              |         |
| 3    | `x = 5; print(x + x)`       |            |              |         |
| 4    | `print(type(3.0))`          |            |              |         |

**Kegiatan 2 — Perbaiki kode rusak**

```
1nama = input(Masukkan nama)
Umur = input("Umur: ")
print("Halo " + 1nama + " umur " + Umur + 1)
```

Tulis versi benar di bawah ini.

**Kegiatan 3 — Mini program**
Kerjakan *Kartu Identitas Digital* sesuai spesifikasi. Tempel cuplikan kode dan screenshot output.

**Kegiatan 4 — Refleksi 3-2-1**
3 dipelajari:
2 masih bingung:
1 rencana perbaikan:

------

### Lampiran 2 — Bahan Ajar Ringkas (untuk siswa)

**1. `print()`**
Menampilkan data ke layar.
`print(objek1, objek2, sep=" ", end="\n")`

**2. Variabel**
Nama yang merujuk pada nilai di memori.
`nama = "Laila"` artinya: simpan teks `Laila` ke wadah `nama`.

**3. Tipe data dasar**

- `str` : teks
- `int` : bilangan bulat
- `float` : pecahan
- `bool` : `True` / `False`

Cek tipe: `type(nilai)`
Ubah tipe: `int()`, `float()`, `str()`, `bool()`

**4. `input()`**
`data = input("Pesan: ")`
Hasilnya selalu `str`. Konversi dulu jika akan dihitung.

**5. f-string**

```
nama = "Bima"
nilai = 88.456
print(f"Siswa {nama} memperoleh {nilai:.2f}")
```

Wajib ada huruf `f` di depan tanda kutip.

**Tips anti-error**

- String harus dalam tanda kutip.
- Jangan menamai variabel dengan `print`, `input`, `int`.
- Baca pesan error dari baris paling bawah.

------

### Lampiran 3 — Kunci Jawaban Terpilih

- `print("A", "B", sep=":")` → `A:B`
- `type(input(...))` → `<class 'str'>`
- Variabel sah: `nilai_siswa`
- `"12.5"` → `float("12.5")`
- `"7"+"3"` = `"73"` (gabungan teks); `7+3` = `10`
- f-string: prefiks `f`
- `{3.14159:.2f}` → `3.14`
- Contoh keyword: `if`, `for`, `class`, `True`

Kode rusak LKPD versi benar:

```
nama = input("Masukkan nama: ")
umur = int(input("Umur: "))
print(f"Halo {nama}, tahun depan umur {umur + 1}")
```

------

### Lampiran 4 — Glosarium

- **Identifier**: nama yang diberikan ke variabel/fungsi.
- **Assignment**: pemberian nilai ke variabel memakai `=`.
- **Dynamic typing**: tipe variabel mengikuti nilainya.
- **Casting / konversi**: mengubah tipe data.
- **Prompt**: teks petunjuk pada `input()`.
- **f-string**: literal string terformat dengan prefiks `f`.
- **Syntax error**: kesalahan aturan penulisan kode.
- **Runtime error**: kesalahan saat program dijalankan (contoh: `int("abc")`).

------

### Lampiran 5 — Daftar Pustaka

- Keputusan Kepala BSKAP Nomor 032/H/KR/2024 tentang Capaian Pembelajaran pada Pendidikan Anak Usia Dini, Jenjang Pendidikan Dasar, dan Jenjang Pendidikan Menengah pada Kurikulum Merdeka.
- Pusat Kurikulum dan Pembelajaran. *Panduan Pembelajaran dan Asesmen*. Kemendikbudristek.
- Buku Panduan Guru Informatika SMA Kelas XI, Kurikulum Merdeka.
- Python Software Foundation. *The Python Tutorial* — Input and Output. https://docs.python.org/3/tutorial/inputoutput.html
- Python Software Foundation. *Built-in Functions* (`print`, `input`, `int`, `float`, `str`, `type`). https://docs.python.org/3/library/functions.html

------

## H. CATATAN IMPLEMENTASI UNTUK GURU

1. Jika laboratorium terbatas, gunakan **pair programming** atau Google Colab.
2. Jangan memulai dengan teori panjang; 5 menit konsep → langsung ketik.
3. Biasakan siswa **memprediksi output** sebelum menekan Run; ini melatih berpikir komputasional.
4. Simpan portofolio file `.py` siswa sebagai bukti asesmen autentik.
5. Pertemuan ini adalah fondasi. Pastikan konversi `input()` → `int`/`float` benar-benar dikuasai sebelum masuk operator, percabangan, dan perulangan.

Modul ini siap dipakai, digandakan ke format sekolah (kop surat, identitas guru, dan logo), serta dapat dipecah menjadi dua pertemuan jika 5 JP dalam satu hari terlalu padat bagi karakteristik kelas.