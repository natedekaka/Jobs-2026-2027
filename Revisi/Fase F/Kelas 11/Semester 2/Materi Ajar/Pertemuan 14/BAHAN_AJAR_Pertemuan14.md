# BAHAN AJAR – PERTEMUAN 14 (S2)
## PTS — Python & Jaringan
*Mengacu pada Panduan Mapel 2025; INFORMATIKA Fase D-F — pendekatan Pembelajaran Mendalam (Memahami → Mengaplikasi → Merefleksi)*

| Informasi | Keterangan |
|---|---|
| **Fase / Kelas** | F / Kelas XI |
| **Alokasi Waktu** | 5 JP × 45 menit (225 menit) |
| **Elemen CP** | Praktik Lintas Bidang (PLB) |
| **Tujuan Pembelajaran** | Mengukur penguasaan materi Python (Pertemuan 1-9) dan Jaringan (Pertemuan 11-13) melalui Penilaian Tengah Semester |
| **Materi Prasyarat** | Seluruh materi Semester 2 hingga Pertemuan 13 |

---

## A. Skenario Ujian 🎬

> **"Panggung Pertunjukan Tahunan"**
>
> Hari ini adalah pertunjukan besar: **PTS**. Seperti penari yang menampilkan semua gerakan yang telah dilatih, kamu akan menunjukkan seluruh pemahamanmu tentang Python dan jaringan. Ruang ujian hening, waktu terasa cepat — tetapi setiap siswa yang sudah berlatih akan tampil percaya diri.
>
> Ingat: soal PTS terdiri dari **teori pilihan ganda** dan **praktik pemrograman** (Python), serta **teori jaringan**. Kelola waktumu, kerjakan yang mudah dulu, dan jangan panik melihat soal yang sulit.
>
> **Pertanyaan pemantik:** Strategi apa yang akan kamu gunakan saat menghadapi soal praktik pemrograman agar programmu bebas error dan sesuai ketentuan?

---

## B. Panduan PTS 🧭

| Aspek | Keterangan |
|---|---|
| **Durasi** | 225 menit (5 JP) |
| **Bentuk soal** | Pilihan ganda, praktik pemrograman, dan esai |
| **Materi Python** | Pertemuan 1-9 (print, variabel, operator, percabangan, perulangan, list, fungsi, program) |
| **Materi Jaringan** | Pertemuan 11-13 (IP, DNS, perangkat, WiFi, keamanan digital) |
| **Tips sukses** | Baca soal dulu, kerjakan mudah, uji program, periksa kembali |

**Kisi-kisi materi Python:**

| Topik | Contoh Soal |
|---|---|
| Input/Output | Fungsi mencetak output: `print()` |
| Tipe Data | Tipe data teks: `str` |
| Operator | Operator sisa bagi: `%` |
| Percabangan | Struktur pemilihan kondisi: `if/elif/else` |
| Perulangan | Perulangan dengan `range()`: `for` |
| List & Tuple | Tipe data yang bisa diubah: `list` |
| Fungsi | Kata kunci fungsi: `def`, pengembalian nilai: `return` |

**Kisi-kisi materi jaringan & keamanan:**

| Topik | Contoh Soal |
|---|---|
| Perangkat | Perangkat penghubung ke internet: modem/router |
| Skala | Jaringan terluas: WAN |
| Protokol | Protokol web aman: HTTPS |
| IP/DNS | Alamat unik perangkat: IP Address; penerjemah nama: DNS |
| Tools | Alat tes koneksi: ping |
| Keamanan | Ancaman kunci file: ransomware; penipuan mengelabui: phishing |
| WiFi | Frekuensi cepat: 5 GHz; nama jaringan: SSID; keamanan tambahan: 2FA |

---

## C. Contoh Soal Pilihan Ganda (Python) 📝

**Soal 1:** Fungsi yang digunakan untuk mencetak output ke layar adalah...
a) `input()`  b) `print()`  c) `type()`  d) `len()`
**Jawaban: b** — `print()` mencetak teks, angka, dan hasil operasi.

**Soal 2:** Hasil dari `10 % 3` adalah...
a) 1  b) 3  c) 3.33  d) 0
**Jawaban: a** — `%` adalah operator modulus (sisa bagi); `10 = 3*3 + 1`, sisa = 1.

**Soal 3:** Kata kunci untuk mendefinisikan fungsi adalah...
a) `for`  b) `if`  c) `def`  d) `return`
**Jawaban: c** — `def` digunakan untuk mendefinisikan fungsi.

**Soal 4:** Tipe data yang dapat diubah elemennya (mutable) adalah...
a) tuple  b) list  c) int  d) str
**Jawaban: b** — list bersifat mutable; tuple immutable.

**Soal 5:** Alat untuk menulis dan menjalankan Python secara online adalah...
a) Microsoft Word  b) Google Colab  c) Paint  d) Excel
**Jawaban: b** — Google Colab adalah notebook Python online gratis.

---

## D. Contoh Soal Praktik Pemrograman 💻

**Soal 1 (Mudah):** Buat program yang menerima input sebuah angka lalu mencetak "Genap" atau "Ganjil".

```python
angka = int(input("Masukkan angka: "))
if angka % 2 == 0:
    print("Genap")
else:
    print("Ganjil")
```

**Output (jika input 7):**
```
Ganjil
```

**Soal 2 (Sedang):** Buat program yang menghitung rata-rata dari 5 angka yang diinput user.

```python
total = 0
for i in range(5):
    total += float(input(f"Angka ke-{i+1}: "))
print("Rata-rata:", total / 5)
```

**Output (jika input 80, 90, 70, 60, 100):**
```
Rata-rata: 80.0
```

**Soal 3 (Sulit):** Buat program To-Do List sederhana dengan fitur tambah, lihat, dan hapus.

```python
tugas = []
while True:
    print("\n1. Tambah  2. Lihat  3. Hapus  4. Keluar")
    p = input("Pilih: ")
    if p == "1":
        tugas.append(input("Tugas baru: "))
    elif p == "2":
        for i, t in enumerate(tugas, 1):
            print(f"{i}. {t}")
        if not tugas:
            print("[Kosong]")
    elif p == "3":
        no = int(input("Nomor: ")) - 1
        if 0 <= no < len(tugas):
            print(f"'{tugas.pop(no)}' dihapus")
    elif p == "4":
        break
```

---

## E. Contoh Soal Jaringan & Esai 🌐

**Soal Pilihan Ganda (Jaringan):**

**Soal 1:** Perangkat yang menghubungkan jaringan lokal ke internet adalah...
a) switch  b) router  c) kabel UTP  d) monitor
**Jawaban: b** — router menghubungkan antar jaringan termasuk ke internet.

**Soal 2:** Jenis jaringan dengan cakupan paling luas adalah...
a) LAN  b) MAN  c) WAN  d) PAN
**Jawaban: c** — WAN mencakup area sangat luas (antar negara).

**Soal 3:** Ancaman yang mengunci file dan meminta tebusan disebut...
a) virus  b) worm  c) ransomware  d) spyware
**Jawaban: c** — ransomware mengunci file dan meminta tebusan.

**Soal 4:** Nama jaringan WiFi yang tampil pada daftar koneksi disebut...
a) IP  b) DNS  c) SSID  d) router
**Jawaban: c** — SSID adalah nama jaringan WiFi.

**Soal Esai:** "Jelaskan 3 langkah menjaga keamanan akun digitalmu!"
**Jawaban acuan:** (1) Gunakan **password kuat** — minimal 12 karakter, kombinasi huruf besar/kecil, angka, simbol, dan unik tiap akun. (2) Aktifkan **2FA** agar butuh kode tambahan selain password. (3) **Waspada phishing** — jangan klik link mencurigakan dan jangan membagikan data pribadi; verifikasi lewat saluran resmi. (Bonus: rutin **backup** data penting).

---

## F. Strategi Mengerjakan Ujian 🎯

1. **Baca semua soal dulu** — kenali mana yang mudah dan mana yang sulit.
2. **Kerjakan yang mudah dulu** — amankan poin terlebih dahulu.
3. **Program yang benar lebih penting daripada program yang lengkap** — pastikan kode tidak error.
4. **Uji program** dengan contoh input sebelum mengumpulkan.
5. **Esai**: tulis definisi → contoh → saran agar jawaban runtut dan lengkap.
6. **Kelola waktu**: sisihkan waktu di akhir untuk memeriksa kembali jawaban.

---

## G. Miskonsepsi & Kesalahan Umum Saat Ujian 🚫

| Kesalahan Umum | Cara Menghindari |
|---|---|
| Langsung mengetik kode tanpa membaca soal | Baca dan pahami permintaan soal dulu |
| Lupa mengonversi `input()` ke `int`/`float` | Konversi sebelum melakukan perhitungan |
| Indentasi salah pada blok `if`/`for` | Periksa konsistensi indentasi (4 spasi) |
| Tidak menguji program | Jalankan program dengan beberapa contoh input |
| Menghafal kode tanpa memahami logika | Pahami alur input-proses-output, bukan hafalan |
| Panik pada soal sulit | Kerjakan yang mudah dulu, sisanya selanjutnya |

---

## H. Rangkuman Kunci 🔑

- PTS mencakup **Python** (print, variabel, operator, percabangan, perulangan, list, fungsi) dan **Jaringan** (IP, DNS, perangkat, WiFi, keamanan digital).
- Kerjakan soal mudah dulu, uji program, dan kelola waktu dengan baik.
- Pastikan kode bebas error dan sesuai ketentuan soal.
- Untuk esai, susun jawaban: definisi → contoh → saran.

---

## I. Glosarium 📖

| Istilah | Arti |
|---|---|
| **PTS** | Penilaian Tengah Semester |
| **Pilihan Ganda** | Soal dengan pilihan jawaban |
| **Praktik** | Soal menulis program komputer |
| **Esai** | Soal uraian jawaban |
| **Rubrik** | Pedoman penilaian jawaban |
| **Kisi-kisi** | Ringkasan materi yang diujikan |

---

## J. Refleksi (Merefleksi) 🔍

- Soal bagian mana yang terasa paling mudah dan paling sulit? Mengapa?
- Strategi mana yang membantumu menyelesaikan soal praktik?
- Apa yang akan kamu perbaiki untuk menghadapi PAS nanti?
- **Skala pemahaman diri:** ____/10
- Topik apa yang ingin kamu perdalam sebelum Penilaian Akhir Semester?

---

**MGMP Informatika SMAN 6 Cimahi — Fase F (Kelas XI) Semester 2**