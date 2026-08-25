# BAHAN AJAR – PERTEMUAN 9 (S1)
## Pengenalan Pseudocode
*Mengacu pada Panduan Mapel 2025; INFORMATIKA Fase D-F — pendekatan Pembelajaran Mendalam (Memahami → Mengaplikasi → Merefleksi)*

| Informasi | Keterangan |
|---|---|
| **Fase / Kelas** | F / Kelas XI |
| **Alokasi Waktu** | 5 JP × 45 menit (225 menit) |
| **Elemen CP** | Algoritma dan Pemrograman (AP) |
| **Tujuan Pembelajaran** | Menjelaskan pengertian pseudocode, menulis struktur dasar START-INPUT-PROSES-OUTPUT-END, memahami kata kunci utama, dan menerjemahkan flowchart ke pseudocode |
| **Materi Prasyarat** | Pertemuan 5–8 — Notasi algoritma, flowchart urutan, percabangan, dan perulangan |

---

## A. Kisah Pemantik 🎬

> **"Bahasa Perantara Dua Dunia"**
>
> Seorang arsitek menjelaskan desain rumah kepada tukang bangunan. Ia tidak berbicara langsung dengan bahasa mesin, tapi dengan **gambar dan kata sederhana** yang dipahami keduanya. Dalam dunia pemrograman, *pseudocode* adalah "bahasa perantara" itu — di antara gambar flowchart dan kode komputer.
>
> **Pertanyaan pemantik:** Mengapa lebih mudah merencanakan sesuatu dengan bahasa manusia yang terstruktur daripada langsung menulis kode? Apa yang terjadi jika kita lompat langsung menulis kode tanpa rencana?

---

## B. Apa Itu Pseudocode?

**Pseudocode** adalah notasi algoritma yang mirip dengan **bahasa manusia** tetapi **terstruktur seperti kode program**. Pseudocode **tidak bisa dijalankan langsung** di komputer — fungsinya merencanakan logika sebelum coding.

**Aturan Pseudocode:**
1. Gunakan bahasa Indonesia atau Inggris yang jelas
2. Gunakan indentasi (jedi) untuk menandai blok kode
3. Tulis satu langkah per baris
4. Gunakan kata kunci baku: INPUT, OUTPUT, IF-THEN-ELSE, FOR, WHILE

---

## C. Struktur Dasar Pseudocode

```
START
    INPUT variabel
    PROSES (rumus/logika)
    OUTPUT hasil
END
```

**Kata Kunci Pseudocode:**
| Kata Kunci | Fungsi |
|---|---|
| **START / END** | Menandai awal dan akhir algoritma |
| **INPUT** | Membaca data dari pengguna |
| **OUTPUT** | Menampilkan hasil |
| **IF ... THEN ... ELSE** | Percabangan |
| **FOR / WHILE** | Perulangan |
| **SET / =** | Assignment (pemberian nilai) |

---

## D. Contoh Pseudocode

**Menghitung Luas Persegi Panjang:**
```
START
    INPUT panjang
    INPUT lebar
    luas = panjang * lebar
    OUTPUT luas
END
```

**Konversi Suhu (Celcius → Fahrenheit):**
```
START
    INPUT celcius
    fahrenheit = celcius * 9/5 + 32
    OUTPUT fahrenheit
END
```

**Menghitung Rata-rata 3 Nilai:**
```
START
    INPUT nilai1
    INPUT nilai2
    INPUT nilai3
    rata = (nilai1 + nilai2 + nilai3) / 3
    OUTPUT rata
END
```

---

## E. Pseudocode vs Flowchart vs Kode

| Aspek | Flowchart | Pseudocode | Kode (Python) |
|---|---|---|---|
| Visual | ✅ | ❌ | ❌ |
| Mirip bahasa manusia | ❌ | ✅ | Sebagian |
| Siap di-coding langsung | ❌ | ✅ | ✅ |
| Butuh software khusus | Tidak | Tidak | Ya (interpreter) |

> 💡 **Pipeline standar pembuatan program:** **Flowchart → Pseudocode → Kode (Python/C++)**. Flowchart memetakan alur, pseudocode merinci logika, kode mengeksekusinya.

---

## F. Contoh Soal & Penyelesaian 📝

**Contoh 1:** Tulis pseudocode: input 2 angka, output jumlahnya!
**Jawaban:**
```
START
    INPUT a
    INPUT b
    jumlah = a + b
    OUTPUT jumlah
END
```

**Contoh 2:** Tulis pseudocode menentukan bilangan ganjil/genap!
**Jawaban:**
```
START
    INPUT angka
    IF angka MOD 2 == 0 THEN
        OUTPUT "Genap"
    ELSE
        OUTPUT "Ganjil"
    ENDIF
END
```

**Contoh 3:** Terjemahkan flowchart luas segitiga (0,5 × alas × tinggi) ke pseudocode!
**Jawaban:**
```
START
    INPUT alas
    INPUT tinggi
    luas = 0.5 * alas * tinggi
    OUTPUT luas
END
```

**Contoh 4:** Apa perbedaan pseudocode dengan bahasa pemrograman?
**Jawaban:** Pseudocode tidak terikat sintaks bahasa tertentu, tidak bisa dijalankan komputer, dan lebih mudah dibaca manusia. Bahasa pemrograman punya aturan sintaks ketat dan bisa dieksekusi mesin (diterjemahkan interpreter/compiler).

**Contoh 5:** Tulis pseudocode konversi rupiah ke dolar (kurs 1 USD = 15.000 IDR)!
**Jawaban:**
```
START
    INPUT rupiah
    dollar = rupiah / 15000
    OUTPUT dollar
END
```
Tracing: rupiah = 75.000 → dollar = **5 USD**.

---

## G. Miskonsepsi / Kesalahan Umum 🚫

| Miskonsepsi / Kesalahan | Fakta yang Benar |
|---|---|
| "Pseudocode harus bisa dijalankan komputer" | Pseudocode **tidak dieksekusi** — hanya untuk perencanaan |
| Menulis terlalu mirip kode lengkap | Pseudocode cukup logika, tanpa sintaks rumit |
| Tidak memakai indentasi | Indentasi menandai blok dan membuat logika jelas |
| Lupa START/END | Struktur lengkap membantu pembacaan algoritma |
| Satu baris mencampur banyak langkah | Satu baris = satu instruksi |

---

## H. Tantangan Praktik (Mengaplikasi) 🎯

**Tantangan 1 — Jumlah Dua Angka (mudah):** Tulis pseudocode input 2 angka, output jumlah dan selisihnya.

**Tantangan 2 — Keliling Persegi (sedang):** Tulis pseudocode menghitung keliling persegi (4 × sisi), lalu lakukan tracing dengan sisi = 9.

**Tantangan 3 — Luas Lingkaran (sulit):** Tulis pseudocode menghitung luas lingkaran (π × r², π = 3,14). Tracing dengan r = 10.

**Tantangan 4 — Translasi (paling sulit):** Gambarlah flowchart "input 2 angka → output perkalian", lalu terjemahkan ke pseudocode. Bandingkan hasil keduanya.

---

## I. Rangkuman Kunci 🔑

- **Pseudocode** = notasi algoritma mirip bahasa manusia, terstruktur seperti kode.
- Struktur dasar: **START → INPUT → PROSES → OUTPUT → END**.
- Kata kunci: INPUT, OUTPUT, IF-THEN-ELSE, FOR, WHILE, SET.
- Pseudocode **tidak dijalankan komputer**; fungsinya merencanakan logika.
- Pipeline: **Flowchart → Pseudocode → Kode**.

---

## J. Glosarium 📖

| Istilah | Arti |
|---|---|
| **Pseudocode** | Deskripsi algoritma bergaya bahasa manusia yang terstruktur |
| **Assignment** | Pemberian nilai ke variabel dengan "=" |
| **Indentasi** | Menjorokkan baris untuk menandai blok kode |
| **Sintaks** | Aturan penulisan dalam bahasa pemrograman |
| **Translasi** | Menerjemahkan algoritma antar bentuk (flowchart ↔ pseudocode) |

---

## K. Refleksi (Merefleksi) 🔍

- Konsep apa yang paling penting kamu pelajari hari ini?
- Apa kelebihan pseudocode dibanding flowchart?
- Bagian mana yang masih sulit dipahami?
- **Skala pemahaman diri:** ____/10
- Apa yang ingin kamu pelajari lebih lanjut?

---

**MGMP Informatika SMAN 6 Cimahi — Fase F (Kelas XI) Semester 1**