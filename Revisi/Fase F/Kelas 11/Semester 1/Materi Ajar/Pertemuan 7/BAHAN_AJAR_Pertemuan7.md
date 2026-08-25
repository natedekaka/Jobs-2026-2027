# BAHAN AJAR – PERTEMUAN 7 (S1)
## Flowchart — Percabangan
*Mengacu pada Panduan Mapel 2025; INFORMATIKA Fase D-F — pendekatan Pembelajaran Mendalam (Memahami → Mengaplikasi → Merefleksi)*

| Informasi | Keterangan |
|---|---|
| **Fase / Kelas** | F / Kelas XI |
| **Alokasi Waktu** | 5 JP × 45 menit (225 menit) |
| **Elemen CP** | Algoritma dan Pemrograman (AP) |
| **Tujuan Pembelajaran** | Menjelaskan konsep percabangan, menggambar flowchart IF-THEN-ELSE, IF bertingkat, dan penggunaan logika AND/OR dalam keputusan |
| **Materi Prasyarat** | Pertemuan 5–6 — Simbol flowchart dan struktur urutan |

---

## A. Kisah Pemantik 🎬

> **"Keputusan di Pintu Gerbang"**
>
> Satpam sekolah bertugas menjaga pintu masuk. Setiap pagi ia menanyakan satu pertanyaan: *"Apakah kamu membawa kartu pelajar?"* Jika ya, silakan masuk. Jika tidak, kamu harus lapor ke guru piket dulu. Keputusan ini berulang setiap hari dengan dua kemungkinan jalan keluar — inilah **percabangan**!
>
> **Pertanyaan pemantik:** Keputusan dua arah apa yang sering kamu hadapi dalam sehari? Bagaimana komputer memutuskan antara "ya" dan "tidak"?

---

## B. Konsep Percabangan (Branching)

**Percabangan** memungkinkan algoritma mengambil keputusan berdasarkan kondisi tertentu. Dalam flowchart, percabangan digambarkan dengan simbol **belah ketupat (decision)**.

**Karakteristik simbol keputusan:**
- Masuk dari atas
- Pertanyaan/kondisi ditulis di dalam simbol (misal: `usia >= 17?`)
- **Dua jalur keluar**: **Ya** (True) dan **Tidak** (False)

```
           ┌──────────────────┐
   masuk ─▶│   kondisi?       │
           └───┬────────┬─────┘
               │ Ya     │ Tidak
               ▼        ▼
           [aksi Ya] [aksi Tidak]
```

---

## C. Flowchart IF Sederhana

**Contoh 1 — Cek Usia:**
```
┌─────────┐
│  START  │
└────┬────┘
     ▼
┌──────────────┐
│ INPUT usia   │
└────┬─────────┘
     ▼
   ┌───────────────┐
   │ usia >= 17?   │
   └──┬───────┬────┘
    Ya│       │Tidak
      ▼       ▼
┌──────────┐ ┌──────────────────┐
│ OUTPUT   │ │ OUTPUT "Belum    │
│ "Cukup   │ │ cukup umur"      │
│ umur"    │ └────┬─────────────┘
└────┬─────┘      │
     ▼            ▼
   ┌─────────┐
   │   END   │
   └─────────┘
```

---

## D. Flowchart IF-THEN-ELSE

**Contoh 2 — Cek Genap/Ganjil:**
Start → input angka → `angka MOD 2 == 0?` → **Ya** → output "Genap" → End; **Tidak** → output "Ganjil" → End.

**Contoh 3 — Cek Kelulusan:**
Start → input nilai → `nilai >= 70?` → **Ya** → output "Lulus" → End; **Tidak** → output "Tidak Lulus" → End.

---

## E. Flowchart IF Bertingkat (ELIF)

**Contoh 4 — Predikat Nilai:**
```
┌─────────┐
│  START  │
└────┬────┘
     ▼
┌──────────────┐
│ INPUT nilai  │
└────┬─────────┘
     ▼
   ┌──────────────┐
   │ nilai >= 85? │
   └──┬──────┬────┘
    Ya│      │Tidak
      ▼      ▼
 ┌────────┐ ┌──────────────┐
 │ "A"    │ │ nilai >= 70? │
 └────────┘ └──┬──────┬────┘
              Ya│      │Tidak
                ▼      ▼
             ┌────┐ ┌──────────────┐
             │"B" │ │ nilai >= 55? │
             └────┘ └──┬──────┬────┘
                      Ya│      │Tidak
                        ▼      ▼
                     ┌────┐ ┌────┐
                     │"C" │ │"D" │
                     └────┘ └────┘
```

**Contoh 5 — Kategori Usia:** usia ≤ 5 → "Balita"; usia ≤ 12 → "Anak"; usia ≤ 17 → "Remaja"; selain itu → "Dewasa".

---

## F. Flowchart dengan Logika AND / OR

**Contoh 6 — Cek Kesehatan (AND):**
Start → input suhu → input batuk → `suhu > 37.5 AND batuk == "ya"?` → **Ya** → "Periksa dokter"; **Tidak** → "Sehat".

**Contoh 7 — Cek Hari Libur (OR):**
Start → input hari → `hari == "Sabtu" OR hari == "Minggu"?` → **Ya** → "Libur"; **Tidak** → "Masuk".

> 💡 **Ingat:** **AND** = kedua kondisi harus benar; **OR** = salah satu saja sudah cukup.

---

## G. Contoh Soal & Penyelesaian 📝

**Contoh 1:** Buat flowchart: input angka → cetak "Positif", "Negatif", atau "Nol"!
**Jawaban:** Start → input angka → `angka > 0?` → Ya → "Positif"; Tidak → `angka < 0?` → Ya → "Negatif"; Tidak → "Nol". (IF bertingkat dua tingkat.)

**Contoh 2:** Buat flowchart cek tahun kabisat: habis dibagi 4 **DAN** (tidak habis dibagi 100 **ATAU** habis dibagi 400)!
**Jawaban:** Start → input tahun → `tahun MOD 4 == 0?` → Tidak → "Bukan kabisat"; Ya → `tahun MOD 100 != 0 OR tahun MOD 400 == 0?` → Ya → "Kabisat"; Tidak → "Bukan kabisat". Tracing: 2024 → 2024 MOD 4 = 0, 2024 MOD 100 = 24 ≠ 0 → **Kabisat**. 1900 → MOD 4 = 0, MOD 100 = 0, MOD 400 = 300 ≠ 0 → **bukan kabisat**.

**Contoh 3:** Buat flowchart mencari terbesar dari 3 angka!
**Jawaban:** Start → input a, b, c → `a > b?` → Ya → `a > c?` → Ya → max = a; Tidak → max = c; Tidak → `b > c?` → Ya → max = b; Tidak → max = c → output max → End. (Nested/IF bersarang.)

**Contoh 4:** Input nilai dan absen; jika nilai ≥ 70 **DAN** absen ≥ 80 maka "Lulus"!
**Jawaban:** Start → input nilai → input absen → `nilai >= 70 AND absen >= 80?` → Ya → "Lulus"; Tidak → "Tidak Lulus". Tracing: nilai=75, absen=90 → **Lulus**; nilai=75, absen=70 → **Tidak Lulus** (karena absen < 80).

**Contoh 5:** Input suhu: > 37,5 demam; 36,5–37,5 normal; < 36,5 hipotermia!
**Jawaban:** Start → input suhu → `suhu > 37.5?` → Ya → "Demam"; Tidak → `suhu >= 36.5?` → Ya → "Normal"; Tidak → "Hipotermia".

---

## H. Miskonsepsi / Kesalahan Umum 🚫

| Miskonsepsi / Kesalahan | Fakta yang Benar |
|---|---|
| Decision hanya punya 1 cabang keluar | Wajib **2 cabang**: Ya dan Tidak |
| Menulis kondisi bukan pertanyaan jelas | Tulis eksplisit: `nilai >= 70?`, bukan "lulus?" |
| Mengabaikan salah satu cabang saat tracing | Tracing harus menelusuri **kedua** cabang |
| Salah memakai AND vs OR | AND: dua-duanya benar; OR: salah satu cukup |
| Percabangan digambar dengan persegi | Percabangan wajib **belah ketupat** |

---

## I. Tantangan Praktik (Mengaplikasi) 🎯

**Tantangan 1 — Genap/Ganjil (mudah):** Buat flowchart: input angka → output "Genap" atau "Ganjil".

**Tantangan 2 — Kelulusan (sedang):** Buat flowchart: input nilai → "Lulus" (≥ 70) atau "Tidak Lulus".

**Tantangan 3 — Terbesar 3 Angka (sulit):** Buat flowchart mencari angka terbesar dari 3 angka yang diinput, lalu tracing dengan a=7, b=12, c=9.

**Tantangan 4 — Predikat (paling sulit):** Buat flowchart predikat nilai A (≥85), B (≥70), C (≥55), D (<55), lalu tracing nilai 92, 70, dan 40.

---

## J. Rangkuman Kunci 🔑

- **Percabangan** memungkinkan algoritma mengambil keputusan.
- Decision digambar dengan **belah ketupat**, keluar 2 cabang: **Ya/Tidak**.
- Struktur: IF sederhana, **IF-THEN-ELSE**, **IF bertingkat**, dan logika **AND/OR**.
- IF bertingkat diuji dari kondisi paling ketat ke paling longgar.
- **AND** butuh semua benar; **OR** cukup salah satu benar.

---

## K. Glosarium 📖

| Istilah | Arti |
|---|---|
| **Branching** | Percabangan alur berdasarkan kondisi |
| **Decision** | Simbol belah ketupat untuk keputusan |
| **IF-THEN-ELSE** | Struktur: jika kondisi benar lakukan X, jika tidak lakukan Y |
| **Nested IF** | IF di dalam IF (bertingkat/bersarang) |
| **Operator AND** | Benar jika kedua kondisi benar |
| **Operator OR** | Benar jika salah satu kondisi benar |

---

## L. Refleksi (Merefleksi) 🔍

- Konsep apa yang paling penting kamu pelajari hari ini?
- Mengapa simbol keputusan harus keluar 2 cabang?
- Bagian mana yang masih sulit dipahami?
- **Skala pemahaman diri:** ____/10
- Apa yang ingin kamu pelajari lebih lanjut?

---

**MGMP Informatika SMAN 6 Cimahi — Fase F (Kelas XI) Semester 1**