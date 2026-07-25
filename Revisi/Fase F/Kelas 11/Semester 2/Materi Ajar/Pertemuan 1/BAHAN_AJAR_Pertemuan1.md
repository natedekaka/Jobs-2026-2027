# BAHAN AJAR – PERTEMUAN 1 (S2)
## Pengenalan Python & Google Colab
*Mengacu pada Panduan Mapel 2025; INFORMATIKA Fase D-F — pendekatan Pembelajaran Mendalam (Memahami → Mengaplikasi → Merefleksi)*



### 🧠 Memahami — Membangun Pemahaman Awal

## A. Tujuan Pembelajaran
Setelah mempelajari materi ini, siswa mampu:
1. Menjelaskan apa itu Python dan kegunaannya
2. Mengakses dan menggunakan Google Colab
3. Menulis program Python pertama dengan print()
4. Membaca dan memahami pesan error sederhana

## B. Apa Itu Python?
Python adalah bahasa pemrograman tingkat tinggi (high-level) yang dirancang untuk mudah dibaca dan ditulis. Dibuat oleh Guido van Rossum pada tahun 1991. Nama Python diambil dari acara komedi Monty Python's Flying Circus.

**Karakteristik Python:**
1. **Mudah dibaca** — sintaks mirip bahasa Inggris, menggunakan indentasi
2. **Interpreted** — kode dijalankan baris per baris (tanpa kompilasi)
3. **Dinamis** — tidak perlu deklarasi tipe data
4. **Multipurpose** — bisa untuk web, data, AI, game, otomatisasi
5. **Open source** — gratis dan punya komunitas besar

**Bidang Penggunaan Python:**
- Web Development: Django, Flask
- Data Science & Analisis: Pandas, NumPy
- Artificial Intelligence: TensorFlow, PyTorch
- Otomatisasi: script untuk tugas repetitif
- Pendidikan: bahasa pemrograman pertama

## C. Google Colab
Kita akan menggunakan Google Colaboratory (Colab) — platform online gratis.

**Kelebihan Colab:**
1. Tidak perlu install apa pun (cukup browser)
2. Gratis dengan akses GPU/TPU
3. File otomatis tersimpan di Google Drive
4. Bisa kolaborasi real-time

**Langkah Akses:**
1. Buka browser → colab.research.google.com
2. Login dengan akun Gmail
3. Klik File → New Notebook
4. Mulai menulis kode di cell

**Shortcut Penting:**
| Shortcut | Fungsi |
|----------|--------|
| Shift+Enter | Jalankan cell dan pindah ke cell berikutnya |
| Ctrl+Enter | Jalankan cell tanpa pindah |
| Alt+Enter | Jalankan cell dan buat cell baru |
| Ctrl+M B | Tambah cell code di bawah |

## D. Program Pertama
```python
print("Hello, World!")
```

**Variasi print():**
```python
print(123)                 # mencetak angka
print("Halo", "dunia")    # mencetak beberapa nilai
print("Hasil:", 5 + 3)    # campur teks dan angka
```

## E. Tanda Kutip
- Teks bisa pakai " " atau ' '
```python
print("Pakai kutip dua")
print('Pakai kutip satu')
```

## F. Komentar
```python
# ini komentar satu baris
print("Halo")  # komentar di samping kode

'''
Ini komentar multi-baris
untuk dokumentasi
'''
```

## G. Error Itu Wajar!
```python
print("Halo       # SyntaxError: EOL
print(halo)       # NameError: not defined
prnt("Halo")      # NameError: prnt not defined
```


### 🔧 Mengaplikasi — Praktik & Penerapan

## H. Latihan
1. Tulis print("Namamu") — ganti dengan nama sendiri
2. Tulis print dengan 3 teks berbeda dalam satu perintah
3. Coba buat error dengan sengaja, baca pesannya
4. Ganti nama notebook: klik judul → ganti
5. Simpan: File → Save a copy in Drive


### 🔍 Merefleksi — Refleksi & Evaluasi

- Apa konsep paling penting yang kamu pelajari hari ini?
- Bagaimana konsep ini terkait dengan materi sebelumnya?
- Skala pemahaman diri: ___/10
- Apa yang ingin kamu pelajari lebih lanjut?

---
**MGMP Informatika SMAN 6 Cimahi — Fase F (Kelas XI) S2 Pert 1**
