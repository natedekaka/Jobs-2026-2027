# BAHAN AJAR – PERTEMUAN 16 (S1)
## PAS — Ujian Tulis
*Mengacu pada Panduan Mapel 2025; INFORMATIKA Fase D-F — pendekatan Pembelajaran Mendalam (Memahami → Mengaplikasi → Merefleksi)*

| Informasi | Keterangan |
|---|---|
| **Fase / Kelas** | F / Kelas XI |
| **Alokasi Waktu** | 5 JP × 45 menit (225 menit) |
| **Elemen CP** | Praktik Lintas Bidang (PLB) |
| **Tujuan Pembelajaran** | Mengukur seluruh kompetensi semester 1 (CT, flowchart, pseudocode, Excel) melalui PAS ujian tulis sesuai kisi-kisi |
| **Materi Prasyarat** | Pertemuan 1–15 — Seluruh materi dan review semester 1 |

---

## A. Skenario Ujian 🎬

> **"Menghadapi Pertarungan Akhir"**
>
> Semua materi semester 1 akan diuji hari ini. Tidak ada yang perlu ditakutkan jika kamu sudah memahami **pola**: simbol flowchart, struktur IF/ELSE/FOR/WHILE, dan fungsi Excel. Ingat, ujian menilai pemahaman, bukan hafalan. Baca soal dua kali, kerjakan yang mudah lebih dulu, dan jangan lupa periksa kembali.
>
> **Pertanyaan pemantik:** Apa 3 hal yang paling kamu ingat dari materi semester ini? Bagaimana kamu akan membagi waktu dalam ujian 90 menit?

---

## B. Format Ujian

| Sesi | Durasi | Jenis | Jumlah |
|---|---|---|---|
| **Ujian Tulis** | 90 menit | PG + Esai | **30 PG + 5 Esai** |

**Konversi Nilai:**
| Predikat | Rentang |
|---|---|
| A (Sangat Baik) | 85–100 |
| B (Baik) | 70–84 |
| C (Cukup) | 55–69 |
| D (Kurang) | 0–54 |

**KKM = 70**

---

## C. Kisi-Kisi PAS

| Materi | PG | Esai | Bobot |
|---|---|---|---|
| Flowchart Dasar (simbol, urutan) | 4 | – | 10% |
| Flowchart Percabangan (IF-ELSE, nested) | 4 | 1 | 15% |
| Flowchart Perulangan (FOR, WHILE) | 4 | 1 | 15% |
| Pseudocode Dasar (IF, ELSE, INPUT, OUTPUT) | 4 | – | 10% |
| Pseudocode Percabangan & Perulangan | 3 | 1 | 12% |
| Excel Fungsi Teks (LEFT, RIGHT, MID, LEN) | 4 | 1 | 13% |
| Excel Fungsi Tanggal (TODAY, DATEDIF) | 4 | 1 | 13% |
| Logika Pemrograman (AND, OR, NOT) | 3 | – | 12% |

---

## D. Contoh Soal Pilihan Ganda

1. Simbol belah ketupat dalam flowchart digunakan untuk... **c) keputusan**
2. Hasil `=LEFT("INFORMATIKA", 4)` adalah... **a) INFO**
3. `=DATEDIF(A2, TODAY(), "Y")` menghasilkan... **a) tahun**
4. Kata kunci perulangan dengan jumlah pasti: **b) FOR**
5. Flowchart mencetak 1–5 menggunakan struktur... **c) loop**
6. `=LEN("Excel")` bernilai... **5**
7. `=RIGHT("SMAN 6", 1)` bernilai... **6**
8. WHILE berhenti berdasarkan... **kondisi**
9. Operator yang membutuhkan semua kondisi benar: **AND**
10. Simbol untuk mulai/selesai program: **oval/terminal**

---

## E. Contoh Soal Esai & Penyelesaian

**Esai 1 — Flowchart urutkan:** Input 3 angka → urutkan dari besar ke kecil!
**Jawaban (alur):** Start → input a, b, c → bandingkan berpasangan dan tukar bila perlu (a vs b, lalu a vs c, lalu b vs c) → output a, b, c (terurut besar–kecil) → End.

**Esai 2 — Pseudocode menu:** Menu pilih 1–4, ulang sampai pilih 4 (keluar)!
**Jawaban:**
```
pilihan = 0
WHILE pilihan != 4
    OUTPUT "1. Tambah 2. Lihat 3. Hapus 4. Keluar"
    INPUT pilihan
    IF pilihan == 1 THEN
        OUTPUT "Menambah..."
    ELSE IF pilihan == 2 THEN
        OUTPUT "Melihat..."
    ELSE IF pilihan == 3 THEN
        OUTPUT "Menghapus..."
    ENDIF
ENDWHILE
OUTPUT "Terima kasih"
```

**Esai 3 — Flowchart bilangan prima:** Input n → output "Prima" atau "Bukan"!
**Jawaban (alur):** Start → input n → jika n < 2 → "Bukan"; else → i = 2 → `i <= n/2?` → Ya → `n MOD i == 0?` → Ya → "Bukan" → End; Tidak → i = i + 1 → kembali; Tidak → "Prima" → End.

**Esai 4 — Excel:** Rumus mengambil 3 digit terakhir NIS "2025001"?
**Jawaban:** `=RIGHT("2025001", 3)` → **001**.

**Esai 5 — Excel:** Rumus membuat email dari nama "Andi Prasetyo"?
**Jawaban:**
```
=LOWER(LEFT(B2,1)) & "." & LOWER(MID(B2, FIND(" ",B2)+1, 99)) & "@sma6.sch.id"
```
→ **andi.prasetyo@sma6.sch.id**.

---

## F. Panduan Menjawab Ujian

1. **Baca soal dua kali** sebelum menjawab.
2. Untuk flowchart: gambar simbol dengan benar, beri label panah Ya/Tidak.
3. Untuk pseudocode: perhatikan indentasi dan penutup blok (ENDIF/ENDFOR/ENDWHILE).
4. Untuk Excel: tulis rumus lengkap diawali `=`.
5. Alokasikan waktu: ~1 menit per PG, sisakan ≥ 20 menit untuk esai.
6. Simpan 5 menit terakhir untuk review jawaban.

---

## G. Contoh Soal & Penyelesaian 📝

**Contoh 1:** Apa perbedaan utama FOR dan WHILE dalam pseudocode?
**Jawaban:** FOR dipakai saat jumlah iterasi **diketahui** (counter otomatis); WHILE dipakai saat perulangan **berhenti berdasarkan kondisi** yang bisa berubah, dan counter-nya manual.

**Contoh 2:** Tulis hasil `=MID("INFORMATIKA", 3, 4)`!
**Jawaban:** Mulai dari karakter ke-3 sebanyak 4 karakter → **FORM**.

**Contoh 3:** Gambarkan simbol untuk input, proses, dan keputusan!
**Jawaban:** Input/output = **jajar genjang**; proses = **persegi panjang**; keputusan = **belah ketupat**.

**Contoh 4:** Mengapa flowchart percabangan harus punya 2 cabang keluar?
**Jawaban:** Karena keputusan memiliki dua kemungkinan hasil (benar/salah → Ya/Tidak). Tanpa 2 cabang, alur tidak lengkap dan algoritma tidak dapat dijalankan.

---

## H. Miskonsepsi / Kesalahan Umum 🚫

| Miskonsepsi / Kesalahan | Fakta yang Benar |
|---|---|
| "Menghafal contoh soal cukup untuk PAS" | Soal bervariasi; kuasai **pola** dan konsep |
| "Pseudocode tidak butuh ENDIF/ENDFOR" | Setiap blok wajib ditutup |
| "Cukup menjawab PG, esai bisa dilewati" | Esai menyumbang bobot besar dan menilai pemahaman |
| "Flowchart boleh tanpa label Ya/Tidak" | Label penting agar alur jelas |
| "Lupa menulis `=` pada rumus Excel" | Semua rumus wajib diawali `=` |

---

## I. Tantangan Praktik (Mengaplikasi) 🎯

**Tantangan 1 — Latihan PG (mudah):** Kerjakan 10 contoh PG di bagian D tanpa melihat kunci.

**Tantangan 2 — Latihan Esai Flowchart (sedang):** Gambar flowchart urutkan 3 angka besar–kecil di selembar kertas.

**Tantangan 3 — Latihan Esai Pseudocode (sulit):** Tulis pseudocode menu berulang dan cek bilangan prima.

**Tantangan 4 — Simulasi Penuh (paling sulit):** Kerjakan seluruh contoh PAS (30 PG + 5 esai) dalam 90 menit, lalu nilai sendiri.

---

## J. Rangkuman Kunci 🔑

- PAS tulis: **30 PG + 5 esai, 90 menit, KKM 70**.
- Kisi-kisi meliputi flowchart, pseudocode, Excel, dan logika AND/OR.
- Kunci esai: gambar flowchart dengan simbol benar, pseudocode berindentasi, rumus Excel lengkap.
- Baca dua kali, kerjakan mudah dulu, review jawaban.

---

## K. Glosarium 📖

| Istilah | Arti |
|---|---|
| **PAS** | Penilaian Akhir Semester |
| **Kisi-kisi** | Rincian materi dan bobot soal ujian |
| **KKM** | Kriteria Ketuntasan Minimal |
| **Esai** | Soal uraian yang menuntut jawaban lengkap |
| **PG** | Pilihan Ganda |

---

## L. Refleksi (Merefleksi) 🔍

- Materi mana yang menurutmu paling banyak keluar di PAS?
- Bagian mana yang paling sulit kamu jawab?
- Apa yang akan kamu lakukan berbeda jika ada kesempatan belajar ulang?
- **Skala pemahaman diri:** ____/10
- Target apa untuk semester depan?

---

**MGMP Informatika SMAN 6 Cimahi — Fase F (Kelas XI) Semester 1**