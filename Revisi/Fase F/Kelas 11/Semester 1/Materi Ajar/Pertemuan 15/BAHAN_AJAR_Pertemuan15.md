# BAHAN AJAR – PERTEMUAN 15 (S1)
## Review Semester 1
*Mengacu pada Panduan Mapel 2025; INFORMATIKA Fase D-F — pendekatan Pembelajaran Mendalam (Memahami → Mengaplikasi → Merefleksi)*

| Informasi | Keterangan |
|---|---|
| **Fase / Kelas** | F / Kelas XI |
| **Alokasi Waktu** | 5 JP × 45 menit (225 menit) |
| **Elemen CP** | Praktik Lintas Bidang (PLB) |
| **Tujuan Pembelajaran** | Mengulang dan mengintegrasikan seluruh materi semester 1 (CT, flowchart, pseudocode, Excel) untuk persiapan PAS |
| **Materi Prasyarat** | Pertemuan 1–14 — Seluruh materi semester 1 |

---

## A. Skenario Kegiatan 🎬

> **"Menyusun Ulang Peta Perjalanan"**
>
> Bayangkan kamu sedang menyiapkan peta perjalanan untuk ujian akhir. Kamu sudah berjalan jauh: mulai dari mengenal algoritma, memecah masalah (dekomposisi), menemukan pola dan abstraksi, lalu menggambar alur dengan flowchart, menulis pseudocode, dan terakhir mengolah data dengan Excel. Hari ini kamu **merangkai ulang seluruh peta itu** agar tidak ada bagian yang terlewat di PAS.
>
> **Pertanyaan pemantik:** Bagian mana dari perjalanan belajar ini yang paling kamu kuasai? Bagian mana yang masih kabur?

---

## B. Peta Materi Semester 1

**Blok 1 — Berpikir Komputasional (Pert 1–4):**
| Pert | Materi | Inti |
|---|---|---|
| 1 | Algoritma | 5 ciri algoritma baik (input, output, definite, finite, effective) |
| 2 | Dekomposisi | Memecah masalah besar menjadi sub-masalah |
| 3 | Pola & Abstraksi | Mencari keteraturan; menyaring informasi esensial |
| 4 | CT Unplugged | Praktik 4 pilar tanpa komputer |

**Blok 2 — Algoritma & Pemrograman (Pert 5–11):**
| Pert | Materi | Inti |
|---|---|---|
| 5–6 | Flowchart | Simbol, urutan (sequence), I/O |
| 7 | Flowchart Percabangan | IF-ELSE, IF bertingkat, AND/OR |
| 8 | Flowchart Perulangan | FOR, WHILE, nested loop, akumulasi |
| 9 | Pseudocode | Struktur START–INPUT–PROSES–OUTPUT–END |
| 10 | Pseudocode Percabangan | IF-THEN-ELSE, ELIF, AND/OR |
| 11 | Pseudocode Perulangan | FOR, WHILE, faktorial, rata-rata |

**Blok 3 — Analisis Data (Pert 12–13):**
| Pert | Materi | Inti |
|---|---|---|
| 12 | Fungsi Lanjut Excel | LEFT, RIGHT, MID, LEN, TODAY, DATEDIF, CONCATENATE |
| 13 | CF & Sort/Filter | Conditional Formatting, sort, filter |

---

## C. Contoh Soal Review & Penyelesaian

**Soal 1 — Flowchart urutan:** Input jam dan menit → konversi ke total menit (jam × 60 + menit).
**Jawaban:** Start → input jam → input menit → total = jam × 60 + menit → output total → End. Tracing: jam=2, menit=15 → **135 menit**.

**Soal 2 — Flowchart percabangan:** Input 3 bilangan → output yang terbesar.
**Jawaban:** Start → input a, b, c → `a > b?` → Ya → `a > c?` → Ya → output a; Tidak → output c; Tidak → `b > c?` → Ya → output b; Tidak → output c → End.

**Soal 3 — Flowchart perulangan:** Cetak bilangan kelipatan 3 dari 3 sampai 30.
**Jawaban:** Start → i = 3 → `i <= 30?` → Ya → output i → i = i + 3 → kembali; Tidak → End. Output: 3, 6, 9, ..., 30.

**Soal 4 — Pseudocode predikat:**
```
INPUT nilai
IF nilai >= 85 THEN
    OUTPUT "A"
ELSE IF nilai >= 70 THEN
    OUTPUT "B"
ELSE IF nilai >= 55 THEN
    OUTPUT "C"
ELSE
    OUTPUT "D"
ENDIF
```

**Soal 5 — Excel data siswa:** Data 10 siswa: NIS, Nama, Tgl Lahir. Buat kolom Usia, Email, dan Status.
- Usia: `=DATEDIF(C2, TODAY(), "Y")`
- Email: `=LOWER(B2) & "@sma6.sch.id"`
- Status: `=IF(D2 >= 16, "SMA", "Belum")`

---

## D. Strategi Ujian PAS

1. **Flowchart:** kuasai 3 simbol utama (proses = persegi, I/O = jajar genjang, decision = belah ketupat) + oval start/end.
2. **Pseudocode:** hafal struktur IF-THEN-ELSE-ENDIF, FOR-ENDFOR, WHILE-ENDWHILE.
3. **Excel:** kuasai LEFT, RIGHT, MID, LEN, DATEDIF, CONCATENATE, IF, TODAY.
4. **Waktu:** kerjakan yang mudah dulu.
5. **Praktik:** gambar flowchart dengan rapi dan beri label pada panah.

---

## E. Contoh Soal & Penyelesaian 📝

**Contoh 1:** Sebutkan 4 pilar berpikir komputasional dan urutannya!
**Jawaban:** **Dekomposisi → Pengenalan Pola → Abstraksi → Algoritma**.

**Contoh 2:** Apa perbedaan flowchart dan pseudocode?
**Jawaban:** Flowchart adalah representasi **visual** dengan simbol standar; pseudocode adalah representasi **teks** mirip bahasa manusia yang terstruktur. Keduanya mendeskripsikan algoritma yang sama.

**Contoh 3:** Kapan menggunakan FOR dan kapan WHILE?
**Jawaban:** FOR jika jumlah perulangan **sudah diketahui** (misal cetak 1–100); WHILE jika berhenti **berdasarkan kondisi** yang bisa berubah (misal sampai tebakan benar).

**Contoh 4:** Apa fungsi `=DATEDIF(A2, TODAY(), "Y")`?
**Jawaban:** Menghitung selisih antara tanggal di A2 dan hari ini dalam satuan **tahun** — biasanya dipakai menghitung usia.

**Contoh 5:** Bagaimana langkah memberi warna merah otomatis pada nilai < 70?
**Jawaban:** Blok range → Home → Conditional Formatting → New Rule → "Format only cells that contain" → less than 70 → Format merah → OK.

---

## F. Miskonsepsi / Kesalahan Umum 🚫

| Miskonsepsi / Kesalahan | Fakta yang Benar |
|---|---|
| "Flowchart dan pseudocode adalah hal berbeda-beda isinya" | Keduanya menggambarkan **algoritma yang sama** dalam bentuk berbeda |
| "WHILE pasti lebih baik dari FOR" | Pilih sesuai kebutuhan: jumlah pasti → FOR, kondisi → WHILE |
| "Dekomposisi = membagi kerja saja" | Inti dekomposisi memecah **masalah**, bukan hanya membagi tugas |
| "Excel sulit karena banyak rumus" | Semua rumus mengikuti pola: `=` + nama fungsi + argumen |
| "Menghafal contoh soal cukup" | Pahami pola agar bisa mengerjakan variasi soal PAS |

---

## G. Tantangan Praktik (Mengaplikasi) 🎯

**Tantangan 1 — Peta Konsep (mudah):** Gambar peta konsep 3 blok materi S1 lengkap dengan kata kunci.

**Tantangan 2 — Flashcard (sedang):** Buat 10 kartu tanya-jawab (simbol flowchart, kata kunci pseudocode, fungsi Excel).

**Tantangan 3 — Soal Campuran (sulit):** Kerjakan 5 soal review di bagian C tanpa membuka catatan.

**Tantangan 4 — Latihan PAS (paling sulit):** Buat 1 soal versimu untuk tiap jenis: flowchart, pseudocode, dan Excel; lalu tukar dan nilai bersama teman.

---

## H. Rangkuman Kunci 🔑

- S1 terdiri dari 3 blok: **CT, Algoritma & Pemrograman, Analisis Data**.
- Flowchart = visual; pseudocode = teks; keduanya menggambarkan algoritma.
- FOR untuk jumlah pasti, WHILE untuk kondisi.
- Excel: fungsi teks + tanggal + CF/Sort/Filter mempercepat analisis data.
- Pahami **pola** agar siap menghadapi variasi soal PAS.

---

## I. Glosarium 📖

| Istilah | Arti |
|---|---|
| **Review** | Mengulang dan merangkum materi |
| **Peta konsep** | Diagram hubungan antar konsep |
| **Flashcard** | Kartu tanya-jawab untuk menghafal |
| **PAS** | Penilaian Akhir Semester |
| **Integrasi** | Menggabungkan materi menjadi satu kesatuan |

---

## J. Refleksi (Merefleksi) 🔍

- Blok materi mana yang paling kamu kuasai?
- Bagian mana yang masih perlu latihan tambahan sebelum PAS?
- Strategi apa yang akan kamu terapkan saat ujian?
- **Skala pemahaman diri:** ____/10
- Apa target nilaimu untuk PAS?

---

**MGMP Informatika SMAN 6 Cimahi — Fase F (Kelas XI) Semester 1**