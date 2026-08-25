# BAHAN AJAR – PERTEMUAN 11 (S1)
## Pseudocode — Perulangan
*Mengacu pada Panduan Mapel 2025; INFORMATIKA Fase D-F — pendekatan Pembelajaran Mendalam (Memahami → Mengaplikasi → Merefleksi)*

| Informasi | Keterangan |
|---|---|
| **Fase / Kelas** | F / Kelas XI |
| **Alokasi Waktu** | 5 JP × 45 menit (225 menit) |
| **Elemen CP** | Algoritma dan Pemrograman (AP) |
| **Tujuan Pembelajaran** | Menulis perulangan FOR dan WHILE dalam pseudocode, membedakan kapan menggunakan keduanya, serta menyusun pseudocode dengan akumulasi |
| **Materi Prasyarat** | Pertemuan 9–10 — Dasar pseudocode dan percabangan |

---

## A. Kisah Pemantik 🎬

> **"Menyapu Halaman Sekolah"**
>
> Setiap pagi, petugas kebersihan menyapu halaman dengan pola yang sama: sapu 3 lapis dari kiri ke kanan, buang sampah ke tong, lalu kembali ke titik awal. Ia tidak perlu menghafal 10 instruksi berbeda — cukup satu pola yang **diulang**. Begitu juga program: perulangan menghemat penulisan dan membuat kode lebih ringkas.
>
> **Pertanyaan pemantik:** Kapan kamu tahu sebuah pekerjaan harus diulang dengan jumlah pasti, dan kapan diulang "sampai suatu kondisi tercapai"?

---

## B. Perulangan FOR

**FOR** digunakan jika **jumlah perulangan sudah diketahui** sejak awal.

```
FOR i = 1 TO 5
    OUTPUT i
ENDFOR
```
Output: 1 2 3 4 5

**FOR dengan langkah (step):**
```
FOR i = 2 TO 10 STEP 2
    OUTPUT i
ENDFOR
```
Output: 2 4 6 8 10

---

## C. Perulangan WHILE

**WHILE** digunakan jika perulangan **berhenti berdasarkan kondisi**, dan banyaknya belum diketahui.

```
i = 1
WHILE i <= 5
    OUTPUT i
    i = i + 1
ENDWHILE
```
Output: 1 2 3 4 5

> 💡 **Perhatian:** dalam WHILE, update counter (`i = i + 1`) **harus ada di dalam blok**, jika tidak akan terjadi *infinite loop*.

---

## D. FOR vs WHILE

| Aspek | FOR | WHILE |
|---|---|---|
| Jumlah iterasi | Diketahui sejak awal | Tergantung kondisi |
| Counter otomatis | Ya (i = 1 TO 10) | Manual (i = i + 1) |
| Risiko infinite loop | Rendah | Tinggi (jika lupa update) |
| Contoh penggunaan | Cetak 1–100 | Tebak angka sampai benar |

---

## E. Contoh Pseudocode Perulangan

**Menjumlah 1–5 (akumulasi):**
```
START
    jumlah = 0
    FOR i = 1 TO 5
        jumlah = jumlah + i
    ENDFOR
    OUTPUT jumlah
END
```
Hasil: **15**

**Faktorial n!:**
```
START
    INPUT n
    faktorial = 1
    FOR i = 1 TO n
        faktorial = faktorial * i
    ENDFOR
    OUTPUT faktorial
END
```
Tracing: n = 5 → faktorial = 1×2×3×4×5 = **120**.

**WHILE — Tebak Angka:**
```
START
    rahasia = 7
    INPUT tebakan
    WHILE tebakan != rahasia
        OUTPUT "Salah, coba lagi"
        INPUT tebakan
    ENDWHILE
    OUTPUT "Benar!"
END
```

**Rata-rata N nilai:**
```
START
    INPUT n
    total = 0
    FOR i = 1 TO n
        INPUT nilai
        total = total + nilai
    ENDFOR
    rata = total / n
    OUTPUT rata
END
```

---

## F. Contoh Soal & Penyelesaian 📝

**Contoh 1:** Tulis pseudocode mencetak bilangan genap 2–10!
**Jawaban:**
```
FOR i = 2 TO 10 STEP 2
    OUTPUT i
ENDFOR
```
Output: 2 4 6 8 10.

**Contoh 2:** Tulis pseudocode menghitung faktorial 5 (5×4×3×2×1)!
**Jawaban:**
```
faktorial = 1
FOR i = 1 TO 5
    faktorial = faktorial * i
ENDFOR
OUTPUT faktorial
```
Hasil: 1×2×3×4×5 = **120**.

**Contoh 3:** Tulis pseudocode WHILE: tebak angka sampai benar!
**Jawaban:**
```
rahasia = 7
INPUT tebakan
WHILE tebakan != rahasia
    OUTPUT "Salah"
    INPUT tebakan
ENDWHILE
OUTPUT "Benar!"
```

**Contoh 4:** Tulis pseudocode mencetak bilangan 10 sampai 1 (mundur)!
**Jawaban:**
```
FOR i = 10 TO 1 STEP -1
    OUTPUT i
ENDFOR
```
Output: 10 9 8 ... 1.

**Contoh 5:** Tulis pseudocode WHILE menghitung mundur dari n sampai "Go!"!
**Jawaban:**
```
INPUT n
WHILE n > 0
    OUTPUT n
    n = n - 1
ENDWHILE
OUTPUT "Go!"
```
Tracing: n=3 → 3, 2, 1, "Go!".

---

## G. Miskonsepsi / Kesalahan Umum 🚫

| Miskonsepsi / Kesalahan | Fakta yang Benar |
|---|---|
| Lupa menulis ENDFOR/ENDWHILE | Penutup wajib ada untuk tiap blok perulangan |
| Update counter di luar WHILE | `i = i + 1` harus **di dalam** blok WHILE |
| Menggunakan FOR untuk jumlah tak tentu | FOR untuk jumlah pasti; tak tentu pakai WHILE |
| Akumulator di-reset di dalam loop | `total = 0` dipasang **sebelum** loop |
| Step salah arah pada FOR mundur | FOR mundur gunakan `STEP -1` |

---

## H. Tantangan Praktik (Mengaplikasi) 🎯

**Tantangan 1 — Cetak 1–10 (mudah):** Tulis pseudocode FOR mencetak 1 sampai 10, dan versi WHILE-nya.

**Tantangan 2 — Jumlah Genap (sedang):** Tulis pseudocode menghitung jumlah bilangan genap 1–50. (Jawaban: 650.)

**Tantangan 3 — Faktorial (sulit):** Tulis pseudocode menerima n dan menghitung n! beserta tracing untuk n = 6.

**Tantangan 4 — Menu Berulang (paling sulit):** Tulis pseudocode WHILE menu: tampilkan menu 1–4, jalankan proses sesuai pilihan, ulang sampai pilihan == 4 (keluar).

---

## I. Rangkuman Kunci 🔑

- **FOR** = jumlah perulangan pasti, counter otomatis, diakhiri **ENDFOR**.
- **WHILE** = berhenti berdasarkan kondisi, update counter manual, diakhiri **ENDWHILE**.
- **Akumulator** (`total = total + i`) diinisialisasi sebelum loop.
- Hindari **infinite loop** dengan selalu mengubah kondisi di dalam WHILE.
- FOR/WHILE bisa dipakai untuk mencetak, menjumlah, menghitung faktorial, dan rata-rata.

---

## J. Glosarium 📖

| Istilah | Arti |
|---|---|
| **FOR loop** | Perulangan dengan jumlah iterasi pasti |
| **WHILE loop** | Perulangan berdasarkan kondisi |
| **ENDFOR / ENDWHILE** | Penutup blok perulangan |
| **Counter** | Variabel penghitung iterasi |
| **Akumulator** | Variabel penampung jumlah kumulatif |
| **Infinite loop** | Perulangan tak berujung karena kondisi tak berubah |

---

## K. Refleksi (Merefleksi) 🔍

- Konsep apa yang paling penting kamu pelajari hari ini?
- Kapan kamu memilih FOR dan kapan WHILE?
- Bagian mana yang masih sulit dipahami?
- **Skala pemahaman diri:** ____/10
- Apa yang ingin kamu pelajari lebih lanjut?

---

**MGMP Informatika SMAN 6 Cimahi — Fase F (Kelas XI) Semester 1**