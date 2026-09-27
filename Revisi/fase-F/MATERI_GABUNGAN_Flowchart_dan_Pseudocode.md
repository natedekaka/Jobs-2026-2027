# MATERI GABUNGAN — Flowchart & Pseudocode
## Rangkuman Pertemuan 5–11 | Informatika Fase F (Kelas XI) Semester 1
*Algoritma dan Pemrograman (AP) — ringkasan konsep yang mudah dipahami dan dijelaskan*

| Informasi | Keterangan |
|---|---|
| **Fase / Kelas** | F / Kelas XI |
| **Elemen CP** | Algoritma dan Pemrograman (AP) |
| **Cakupan Materi** | Pertemuan 5–11: Notasi Algoritma, Flowchart (Urutan, Percabangan, Perulangan), Pseudocode (Dasar, Percabangan, Perulangan) |
| **Pola Belajar** | Memahami → Mengaplikasi → Merefleksi |

---

## Daftar Isi

1. Peta Materi (Gambaran Besar)
2. Bagian 1 — Apa Itu Flowchart?
3. Bagian 2 — Struktur Urutan (Sequence) & I/O
4. Bagian 3 — Percabangan (Branching)
5. Bagian 4 — Perulangan (Loop)
6. Bagian 5 — Apa Itu Pseudocode?
7. Bagian 6 — Pseudocode Percabangan
8. Bagian 7 — Pseudocode Perulangan
9. Bagian 8 — Flowchart vs Pseudocode vs Kode
10. Contoh Soal Gabungan & Penyelesaian
11. Rangkuman Kunci
12. Glosarium

---

## 1. Peta Materi (Gambaran Besar)

> **Satu cerita panjang:** Algoritma adalah *rencana langkah*. Kita bisa menuliskannya dalam DUA bentuk yang saling melengkapi:
> - **Flowchart** = rencana dalam bentuk **gambar/simbol** (agar mudah terlihat alurnya)
> - **Pseudocode** = rencana dalam bentuk **teks terstruktur** (agar mudah dibaca seperti kode)

```
PERTEMUAN 5       PERTEMUAN 6-8              PERTEMUAN 9       PERTEMUAN 10-11
Algoritma   -->   FLOWCHART                 --> PSEUDOCODE    --> PSEUDOCODE
& Simbol          (urutan, cabang, ulang)      (dasar)           (cabang & ulang)
```

| Pertemuan | Topik | Pertanyaan Kunci |
|---|---|---|
| 5 | Notasi Algoritma & Flowchart | Simbol apa saja dasar flowchart? |
| 6 | Flowchart Urutan & I/O | Bagaimana membaca input dan menampilkan output? |
| 7 | Flowchart Percabangan | Bagaimana komputer memilih antara Ya/Tidak? |
| 8 | Flowchart Perulangan | Bagaimana menjalankan langkah berulang kali? |
| 9 | Pengenalan Pseudocode | Bagaimana menulis algoritma seperti teks terstruktur? |
| 10 | Pseudocode Percabangan | Bagaimana menulis IF-THEN-ELSE dalam teks? |
| 11 | Pseudocode Perulangan | Bagaimana menulis FOR dan WHILE dalam teks? |

---

# BAGIAN 1 — APA ITU FLOWCHART? (Pertemuan 5)

## 1.1 Pengertian

**Flowchart** adalah representasi grafis dari algoritma menggunakan simbol-simbol standar. Karena berbentuk **gambar**, alur logika langsung terlihat tanpa harus membaca teks panjang.

**Kenapa penting?**
1. Memvisualisasikan algoritma sebelum coding
2. Memudahkan komunikasi antar programmer
3. Membantu menemukan error logika (debugging)
4. Menjadi dokumentasi program yang mudah dipahami

## 1.2 Simbol Dasar Flowchart

| Simbol | Bentuk | Fungsi |
|---|---|---|
| **Terminal** | Oval | Mulai (Start) / Selesai (End) |
| **I/O** | Jajar genjang | Input (membaca data) / Output (menampilkan hasil) |
| **Proses** | Persegi panjang | Operasi / perhitungan / assignment |
| **Decision** | Belah ketupat | Percabangan / keputusan (Ya / Tidak) |
| **Garis alir** | Panah | Menunjukkan arah aliran |
| **Konektor** | Lingkaran kecil | Penghubung antar bagian / halaman |

> **KUNCI BENTUK** — Hafalkan bentuk ini, semua diagram di materi ini memakainya:

```
   ╭──────────╮      ╱════════════╲      ┌──────────────┐      ╱──────────────╲
   │  START / │     ║  INPUT /   ║      │    PROSES    │     ╱   kondisi      ╲
   │   END    │     ║  OUTPUT    ║      │ perhitungan  │    │      ( ? )       │
   ╰──────────╯      ╲════════════╱      └──────────────┘     ╲              ╱
    Oval = mulai            Jajar genjang     Persegi panjang    ╲──────────────╱
    & selesai               = input & output  = proses/hitungan  Belah ketupat =
                                                                 percabangan Ya/Tidak
```

## 1.3 Aturan Penulisan Flowchart

1. Satu simbol → satu aktivitas (jangan digabung)
2. Gunakan kata kerja yang jelas: "Masukkan kopi", bukan "Kopi"
3. Garis alir tidak boleh putus
4. Hindari garis bersilangan → pakai konektor
5. Setiap **decision** wajib punya 2 cabang: **Ya** dan **Tidak**
6. Mulai dengan **Start** dan akhiri dengan **End**

## 1.4 Contoh Flowchart — Membuat Kopi

*Semua langkahnya adalah proses (persegi panjang), tanpa input/output, jadi cukup oval di awal dan akhir.*

```
╭──────────╮
│  START   │
╰────┬─────╯
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
╭──────────╮
│   END    │
╰──────────╯
```

## 1.5 Tracing — Mengecek Kebenaran Algoritma

**Tracing** = mensimulasikan jalannya flowchart/pseudocode langkah demi langkah dengan **nilai konkret**, lalu mencatat perubahan tiap variabel.

**Langkah:**
1. Mulai dari Start
2. Masukkan nilai pada variabel input
3. Catat hasil perhitungan di setiap langkah
4. Pastikan output akhir sesuai harapan

**Contoh tracing — Hitung Luas:**
| Langkah | Variabel | Nilai |
|---|---|---|
| 1. Start | – | – |
| 2. Input | panjang = 5, lebar = 3 | 5, 3 |
| 3. Proses | luas = 5 × 3 | **15** |
| 4. Output | "Luas = 15" | 15 |
| 5. End | ✅ | Selesai |

> 💡 **TIPS MENGAJAR:** Minta siswa membawa nilai nyata (misal r=7) dan "menjalankan" flowchart dengan pensil — coret variabel seraya bergerak di gambar.

---

# BAGIAN 2 — STRUKTUR URUTAN & I/O (Pertemuan 6)

## 2.1 Struktur Urutan (Sequence)

**Urutan (sequence)** adalah struktur paling sederhana: langkah dieksekusi **berurutan dari atas ke bawah** tanpa lompatan dan tanpa pengulangan. Inilah fondasi semua flowchart.

```
╭──────────╮
│  START   │          ← TerminaL (OVAL)
╰────┬─────╯
     ▼
╱══════════════════╲
║    INPUT data     ║   ← I/O (JAJAR GENJANG)
╲══════════════════╱
     ▼
┌────────────────────┐
│  PROSES (hitungan) │   ← Proses (PERSEGI PANJANG)
└────┬───────────────┘
     ▼
╱════════════════════╲
║    OUTPUT (hasil)   ║   ← I/O (JAJAR GENJANG)
╲════════════════════╱
     ▼
╭──────────╮
│   END    │          ← TerminaL (OVAL)
╰──────────╯
```

**Pola umum: `START → INPUT → PROSES → OUTPUT → END`**

**Aturan membuat flowchart sequence:**
1. Mulai dengan Start dan akhiri End
2. Tiap langkah dalam satu simbol (satu simbol untuk satu aktivitas)
3. Gunakan panah untuk alur
4. Satu jalur masuk, satu jalur keluar (kecuali percabangan)

## 2.2 Input/Output (I/O)

- **Input** dan **Output** sama-sama memakai simbol **jajar genjang**.
- Contoh notasi: `INPUT nama`, `INPUT r`, `OUTPUT "Halo, " + nama`, `OUTPUT luas`.

> 💡 Tanpa input, program tidak punya data; tanpa output, hasil tidak sampai ke pengguna.

## 2.3 Pola-Pola Sequence yang Sering Dipakai

| Contoh | Alur |
|---|---|
| Sapa pengguna | Start → INPUT nama → OUTPUT "Halo, " + nama → End |
| Luas persegi panjang | Start → INPUT p → INPUT l → luas = p × l → OUTPUT luas → End |
| Konversi suhu C→F | Start → INPUT C → F = C × 9/5 + 32 → OUTPUT F → End |
| Rata-rata 3 nilai | Start → INPUT n1, n2, n3 → rata = (n1+n2+n3)/3 → OUTPUT rata → End |
| Rupiah → Dolar | Start → INPUT rupiah → dollar = rupiah / 15000 → OUTPUT dollar → End |

---

# BAGIAN 3 — PERCABANGAN (Pertemuan 7)

## 3.1 Konsep Percabangan

**Percabangan (branching)** memungkinkan algoritma mengambil keputusan berdasarkan suatu kondisi. Digambarkan dengan simbol **belah ketupat (decision)** yang memiliki **TWO jalur keluar: Ya dan Tidak**.

```
             │
             ▼
        ╱──────────╲
       ╱  usia >=   ╲
      │     17 ?     │
       ╲            ╱
        ╲──────────╱
     Ya │          │ Tidak
        ▼          ▼
╱════════════╲  ╱══════════════╲
║ OUTPUT     ║  ║ OUTPUT       ║
║ "Cukup     ║  ║ "Belum       ║
║  umur"     ║  ║ cukup umur"  ║
╲════════════╱  ╲══════════════╱
        │          │
        └────┬─────┘
             ▼
         ╭─────────╮
         │   END   │
         ╰─────────╯
```

## 3.2 Tiga Bentuk Percabangan

| Bentuk | Keterangan | Contoh |
|---|---|---|
| **IF sederhana** | Hanya 1 aksi bila benar, tanpa aksi bila salah | Jika hujan → bawa payung |
| **IF-THEN-ELSE** | 2 aksi berbeda (benar/salah) | Nilai ≥ 70 → "Lulus", selainnya → "Tidak Lulus" |
| **IF bertingkat (ELIF)** | Banyak kondisi diuji dari paling ketat ke paling longgar | Predikat A/B/C/D |

**Contoh IF-THEN-ELSE — Cek Genap/Ganjil:**

```
╭──────────────╮
│    START     │
╰──────┬───────╯
       ▼
╱════════════════════╲
║      INPUT angka    ║
╲════════════════════╱
       ▼
     ╱──────────────╲
    ╱  angka MOD 2   ╲
   │      == 0 ?      │
    ╲                 ╱
     ╲───────────────╱
    Ya│          │Tidak
      ▼          ▼
╱═══════════╲  ╱═══════════╲
║  "Genap"  ║  ║ "Ganjil"  ║
╲═══════════╱  ╲═══════════╱
      │          │
      └────┬─────┘
           ▼
        ╭──────────────╮
        │     END      │
        ╰──────────────╯
```

**Contoh IF bertingkat — Predikat Nilai** (pola "tangga": uji dari nilai tertinggi ke terendah):

```
╭──────────╮
│  START   │
╰────┬─────╯
     ▼
╱════════════════╲
║   INPUT nilai  ║
╲════════════════╱
     │
     ▼
  ╱──────────────╲
 ╱  nilai >= 85?  ╲──── Ya ──►  ╱════════╲ ──►  ╭─────────╮
 ╲                ╱            ║  "A"   ║       │  END    │
  ╲──────────────╱            ╲════════╱       ╰─────────╯
        │ Tidak
        ▼
  ╱──────────────╲
 ╱  nilai >= 70?  ╲──── Ya ──►  ╱════════╲ ──►  ╭─────────╮
 ╲                ╱            ║  "B"   ║       │  END    │
  ╲──────────────╱            ╲════════╱       ╰─────────╯
        │ Tidak
        ▼
  ╱──────────────╲
 ╱  nilai >= 55?  ╲──── Ya ──►  ╱════════╲ ──►  ╭─────────╮
 ╲                ╱            ║  "C"   ║       │  END    │
  ╲──────────────╱            ╲════════╱       ╰─────────╯
        │ Tidak
        ▼
  ╱──────────────╲
 ╱  selain itu    ╲ ──────────►  ╱════════╲ ──►  ╭─────────╮
 ╲                ╱            ║  "D"   ║       │  END    │
  ╲──────────────╱            ╲════════╱       ╰─────────╯
```

**Contoh kategori usia:** usia ≤ 5 → "Balita"; usia ≤ 12 → "Anak"; usia ≤ 17 → "Remaja"; selain itu → "Dewasa" (pola tangga yang sama).

## 3.3 Logika AND dan OR

| Operator | Arti | Syarat benar |
|---|---|---|
| **AND** | dan | **Semua** kondisi harus benar |
| **OR** | atau | **Salah satu** kondisi benar sudah cukup |

**Contoh AND — Cek Kelulusan Dobel:**
`nilai >= 70 AND absen >= 80` → benar hanya jika KEDUANYA terpenuhi. (nilai=75, absen=70 → **Tidak Lulus**)

**Contoh OR — Cek Hari Libur:**
`hari == "Sabtu" OR hari == "Minggu"` → benar jika salah SATU saja terpenuhi.

> 💡 Salah memakai AND/OR akan mengubah seluruh hasil keputusan!

## 3.4 Pola-Pola Percabangan yang Sering Dipakai

| Kasus | Kondisi |
|---|---|
| Kelulusan | `nilai >= 70` → Lulus / Tidak |
| Positif-negatif-nol | `angka > 0` → Positif; `angka < 0` → Negatif; selainnya Nol |
| Terbesar dari 3 angka | Bandingkan a>b, lalu a>c atau b>c (nested IF) |
| Tahun kabisat | `MOD 4 == 0` DAN (`MOD 100 != 0` ATAU `MOD 400 == 0`) |
| Suhu tubuh | > 37,5 Demam; ≥ 36,5 Normal; < 36,5 Hipotermia |

---

# BAGIAN 4 — PERULANGAN (Pertemuan 8)

## 4.1 Konsep Perulangan (Loop)

**Perulangan** menjalankan blok instruksi **berulang kali**. Dalam flowchart, ditandai dengan **panah kembali (back loop)** ke kondisi/ langkah sebelumnya.

| Jenis | Ciri | Kapan Digunakan | Contoh |
|---|---|---|---|
| **FOR** | Jumlah perulangan sudah diketahui sejak awal | Cetak 1–10 | 10 kali |
| **WHILE** | Berhenti berdasarkan kondisi | Ulangi sampai tebakan benar | tak tentu |
| **Repeat-Until** | Dijalankan minimal sekali | do...while | jarang dipakai di flowchart dasar |

> ⚠️ **Bahaya infinite loop:** jika kondisi tidak pernah berubah menjadi salah, perulangan tidak pernah berhenti. Selalu pastikan ada langkah yang **mengubah kondisi**.

## 4.2 Flowchart FOR Loop — Cetak 1–5

*Perhatikan panah kembali (back loop) dari `i = i + 1` ke kondisi `i <= 5?`. Tanpa `i = i + 1`, loop tidak pernah berhenti.*

```
╭──────────╮
│  START   │
╰────┬─────╯
     ▼
┌───────────┐
│    i = 1  │
└────┬──────┘
     ▼
   ╱──────────╲   ◀───────────────┐
  ╱   i <= 5?   ╲                 │  (kembali lagi)
  ╲             ╱                 │
   ╲──────────╱                   │
  Ya│        │Tidak               │
    ▼        ▼                    │
╱════════╲ ┌─────────┐            │
║ OUTPUT │ │   END   │            │
║   i    ║ └─────────┘            │
╲════════╱                        │
    │                              │
    ▼                              │
┌────────────┐                     │
│  i = i + 1 │─────────────────────┘
└────────────┘
```

**Contoh 2 — Cetak Bilangan Genap 2–10:** i mulai dari 2, tambah 2 setiap loop: 2, 4, 6, 8, 10.

## 4.3 Flowchart WHILE Loop — Hitung Mundur

*WHILE berhenti BEDASARKAN KONDISI. Update counter (`n = n - 1`) WAJIB ada di dalam loop.*

```
╭──────────╮
│  START   │
╰────┬─────╯
     ▼
╱════════════╲
║  INPUT n   ║
╲════════════╱
     ▼
   ╱──────────╲   ◀──────────────┐
  ╱    n > 0?   ╲                │  (kembali lagi)
  ╲             ╱                │
   ╲──────────╱                  │
  Ya│        │Tidak              │
    ▼        ▼                   │
╱═════════╲ ┌────────┐           │
║ OUTPUT n║ │ "Go!"  │           │
╲═════════╱ └────────┘           │
    │                             │
    ▼                             │
┌────────────┐                    │
│  n = n - 1 │────────────────────┘
└────────────┘
```

**Contoh 3 — Tebak Angka:** Start → komputer = random 1–10 → INPUT tebakan → `tebakan != komputer?` → **Ya** → INPUT tebakan lagi → kembali; **Tidak** → OUTPUT "Benar!" → End.

## 4.4 Akumulasi (Running Total)

**Akumulator** adalah variabel penampung jumlah kumulatif, contoh: `total = total + i`.

**Pola penting: inisialisasi `total = 0` diletakkan SEBELUM loop, bukan di dalam.**

| Contoh | Cara | Hasil |
|---|---|---|
| Jumlah 1–100 | total=0; i=1; ulang total=total+i | **5050** |
| Rata-rata N nilai | total=0; input nilai tiap iterasi; rata=total/n | – |
| Faktorial n! | fakt=1; ulang fakt=fakt×i | 5! = **120** |

## 4.5 Loop Bersarang (Nested Loop)

**Loop dalam selesai penuh untuk setiap iterasi loop luar.**
Contoh tabel perkalian 3×3: untuk tiap `baris` (3×), jalankan seluruh `kolom` (3×) → total iterasi = **3 × 3 = 9 kali**.

---

# BAGIAN 5 — APA ITU PSEUDOCODE? (Pertemuan 9)

## 5.1 Pengertian

**Pseudocode** adalah notasi algoritma yang **mirip bahasa manusia tetapi terstruktur seperti kode program**. Pseudocode **TIDAK bisa dijalankan langsung** di komputer — fungsinya merencanakan logika sebelum coding.

**Aturan menulis:**
1. Gunakan bahasa Indonesia/Inggris yang jelas
2. Gunakan indentasi (menjorok ke dalam) untuk menandai blok
3. Satu langkah per baris
4. Gunakan kata kunci baku: INPUT, OUTPUT, IF-THEN-ELSE, FOR, WHILE

## 5.2 Struktur Dasar & Kata Kunci

```
START
    INPUT variabel
    PROSES (rumus/logika)
    OUTPUT hasil
END
```

| Kata Kunci | Fungsi |
|---|---|
| **START / END** | Awal dan akhir algoritma |
| **INPUT** | Membaca data pengguna |
| **OUTPUT** | Menampilkan hasil |
| **IF ... THEN ... ELSE** | Percabangan |
| **FOR / WHILE** | Perulangan |
| **SET / =** | Assignment (pemberian nilai) |

## 5.3 Contoh Pseudocode Dasar

```
START
    INPUT panjang
    INPUT lebar
    luas = panjang * lebar
    OUTPUT luas
END
```

```
START
    INPUT celcius
    fahrenheit = celcius * 9/5 + 32
    OUTPUT fahrenheit
END
```

## 5.4 Pipeline Pembuatan Program

> **Flowchart → Pseudocode → Kode (Python/C++)**
> Flowchart memetakan alur, pseudocode merinci logika, kode yang mengeksekusi.

---

# BAGIAN 6 — PSEUDOCODE PERCABANGAN (Pertemuan 10)

## 6.1 IF Sederhana

```
INPUT usia
IF usia >= 17 THEN
    OUTPUT "Sudah cukup umur"
ENDIF
```

> Hanya menjalankan aksi bila kondisi benar; tanpa ELSE tidak ada aksi bila salah.

## 6.2 IF-THEN-ELSE

```
INPUT nilai
IF nilai >= 70 THEN
    OUTPUT "Lulus"
ELSE
    OUTPUT "Tidak Lulus"
ENDIF
```

## 6.3 IF-ELIF-ELSE (Bertingkat) — uji dari ketat ke longgar

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

## 6.4 Nested IF (IF di dalam IF)

```
INPUT usia
INPUT nilai
IF usia >= 17 THEN
    IF nilai >= 70 THEN
        OUTPUT "Lulus dan cukup umur"
    ELSE
        OUTPUT "Cukup umur tapi tidak lulus"
    ENDIF
ELSE
    IF nilai >= 70 THEN
        OUTPUT "Lulus tapi belum cukup umur"
    ELSE
        OUTPUT "Tidak lulus dan belum cukup umur"
    ENDIF
ENDIF
```

## 6.5 Pseudocode dengan AND / OR

```
INPUT nilai
INPUT absen
IF nilai >= 70 AND absen >= 80 THEN   // AND: dua-duanya harus benar
    OUTPUT "Lulus"
ELSE
    OUTPUT "Tidak Lulus"
ENDIF
```

```
INPUT usia
INPUT hari
IF usia < 12 OR hari == "Selasa" THEN  // OR: salah satu cukup
    OUTPUT "Dapat diskon"
ELSE
    OUTPUT "Tidak dapat diskon"
ENDIF
```

## 6.6 Translasi Pseudocode ↔ Flowchart

| Pseudocode | Flowchart |
|---|---|
| **IF** | Belah ketupat (decision) |
| **THEN** | Cabang **Ya** |
| **ELSE** | Cabang **Tidak** |
| **ENDIF** | Kembali ke alur utama |
| Jajar genjang (I/O) | **INPUT / OUTPUT** |
| Kotak proses | Assignment / rumus |

---

# BAGIAN 7 — PSEUDOCODE PERULANGAN (Pertemuan 11)

## 7.1 FOR — jumlah pasti, counter otomatis

```
FOR i = 1 TO 5
    OUTPUT i
ENDFOR
```
Output: 1 2 3 4 5

```
FOR i = 2 TO 10 STEP 2
    OUTPUT i
ENDFOR
```
Output: 2 4 6 8 10 (FOR mundur memakai `STEP -1`)

## 7.2 WHILE — berhenti berdasarkan kondisi, counter manual

```
i = 1
WHILE i <= 5
    OUTPUT i
    i = i + 1        // update counter WAJIB di dalam blok!
ENDWHILE
```

> ⚠️ Lupa `i = i + 1` di dalam blok WHILE = **infinite loop**.

## 7.3 FOR vs WHILE

| Aspek | FOR | WHILE |
|---|---|---|
| Jumlah iterasi | Diketahui sejak awal | Tergantung kondisi |
| Counter otomatis | Ya | Manual (i = i + 1) |
| Risiko infinite loop | Rendah | Tinggi (jika lupa update) |
| Contoh | Cetak 1–100 | Tebak angka sampai benar |

## 7.4 Contoh Pseudocode Perulangan

**Jumlah 1–5 (akumulasi):**
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
Tracing n=5 → 1×2×3×4×5 = **120**

**WHILE tebak angka:**
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

**Countdown sampai "Go!":**
```
INPUT n
WHILE n > 0
    OUTPUT n
    n = n - 1
ENDWHILE
OUTPUT "Go!"
```

---

# BAGIAN 8 — FLOWCHART vs PSEUDOCODE vs KODE

| Aspek | Flowchart | Pseudocode | Kode (Python) |
|---|---|---|---|
| Visual | ✅ | ❌ | ❌ |
| Mirip bahasa manusia | ❌ | ✅ | Sebagian |
| Siap di-coding langsung | ❌ | ✅ | ✅ |
| Butuh software khusus | Tidak | Tidak | Ya (interpreter) |

**Kunci:** Ketiganya menyampaikan **algoritma yang sama** — hanya beda bentuk. Flowchart paling visual, pseudocode paling ringkas untuk logika, kode yang paling siap dieksekusi.

---

# BAGIAN 9 — CONTOH SOAL GABUNGAN & PENYELESAIAN

**Soal 1 (mudah):** Tuliskan nama 4 simbol dasar flowchart beserta fungsinya.
**Jawaban:** Terminal (oval) = mulai/selesai; I/O (jajar genjang) = input/output; Proses (persegi panjang) = perhitungan; Decision (belah ketupat) = percabangan Ya/Tidak.

**Soal 2 (mudah):** Gambar alur flowchart menghitung luas persegi panjang.
**Jawaban:**
```
╭──────────╮
│  START   │
╰────┬─────╯
     ▼
╱════════════════════╲
║  INPUT panjang     ║
╲════════════════════╱
     ▼
╱═══════════════════╲
║  INPUT lebar      ║
╲═══════════════════╱
     ▼
┌────────────────────────┐
│  luas = panjang x lebar│
└────┬───────────────────┘
     ▼
╱═════════════════╲
║  OUTPUT luas    ║
╲═════════════════╱
     ▼
╭──────────╮
│   END    │
╰──────────╯
```

**Soal 3 (sedang):** Buat flowchart: input 2 angka, tampilkan bilangan yang lebih besar.
**Jawaban (alur):** Start (oval) → INPUT a (jajar genjang) → INPUT b (jajar genjang) → `a > b?` (belah ketupat) → **Ya** → OUTPUT a → End; **Tidak** → OUTPUT b → End.

**Soal 4 (sedang):** Buat pseudocode konversi suhu C→F, lalu tracing C = 25.
**Jawaban:**
```
START
    INPUT C
    F = C * 9/5 + 32
    OUTPUT F
END
```
Tracing: F = 25×9/5 + 32 = **77**.

**Soal 5 (sulit):** Tulis pseudocode WHILE: menerima angka, menjumlahkannya, berhenti saat input 0, lalu tampilkan totalnya.
**Jawaban:**
```
START
    total = 0
    INPUT x
    WHILE x != 0
        total = total + x
        INPUT x
    ENDWHILE
    OUTPUT total
END
```
Tracing: input 5, 3, 0 → total = **8**.

**Soal 6 (paling sulit):** Terjemahkan ke flowchart DAN pseudocode: cetak bilangan genap 2–10, lalu hitung jumlahnya.
**Jawaban (pseudocode):**
```
START
    jumlah = 0
    FOR i = 2 TO 10 STEP 2
        OUTPUT i
        jumlah = jumlah + i
    ENDFOR
    OUTPUT "Jumlah =", jumlah
END
```
Tracing: keluar 2,4,6,8,10; jumlah = **30**. (Flowchartnya: oval Start → `i = 2` (persegi) → belah ketupat `i <= 10?` → ya → OUTPUT i (jajar genjang) → `jumlah = jumlah + i` (persegi) → `i = i + 2` (persegi) → panah kembali ke belah ketupat → tidak → OUTPUT jumlah → oval End.)

---

# BAGIAN 10 — RANGKUMAN KUNCI

- **Flowchart** = rencana algoritma dalam bentuk simbol; **Pseudocode** = rencana dalam teks terstruktur.
- **5 simbol inti flowchart**: Terminal (oval), I/O (jajar genjang), Proses (persegi), Decision (belah ketupat), Garis alir (panah). Aturan: 1 simbol = 1 aktivitas; decision wajib 2 cabang.
- **Tiga struktur algoritma**: **Urutan** (sequence) → **Percabangan** (IF-THEN-ELSE) → **Perulangan** (FOR/WHILE).
- **Tracing** = menjalankan algoritma dengan nilai konkret untuk membuktikan kebenarannya.
- **AND** = semua syarat benar; **OR** = salah satu syarat cukup.
- **FOR** = jumlah pasti (counter otomatis, ENDFOR); **WHILE** = sampai kondisi (counter manual, ENDWHILE, hati-hati infinite loop).
- **Akumulator** (`total = total + i`) diinisialisasi **sebelum** loop.
- Pipeline: **Flowchart → Pseudocode → Kode**.

---

# BAGIAN 11 — GLOSARIUM

| Istilah | Arti |
|---|---|
| **Algoritma** | Urutan langkah untuk menyelesaikan masalah |
| **Flowchart** | Diagram alir berbasis simbol |
| **Terminal** | Simbol oval mulai/selesai |
| **Decision** | Simbol belah ketupat untuk percabangan |
| **Sequence** | Eksekusi langkah berurutan dari atas ke bawah |
| **Branching** | Percabangan alur berdasarkan kondisi |
| **Nested IF** | IF di dalam IF (bersarang) |
| **Loop** | Perulangan eksekusi blok instruksi |
| **FOR loop** | Perulangan jumlah iterasi pasti |
| **WHILE loop** | Perulangan berdasarkan kondisi |
| **Counter** | Variabel penghitung (i = i + 1) |
| **Akumulator** | Variabel penampung jumlah kumulatif |
| **Infinite loop** | Perulangan tak berujung |
| **Pseudocode** | Deskripsi algoritma bergaya bahasa manusia yang terstruktur |
| **Indentasi** | Menjorokkan baris untuk menandai blok |
| **Sintaks** | Aturan penulisan dalam bahasa pemrograman |
| **Tracing** | Menelusuri alur dengan nilai konkret |

---

# BAGIAN 12 — REFLEKSI (untuk siswa)

- Tiga struktur algoritma apa saja yang sudah kamu kuasai hari ini?
- Beda FOR dan WHILE — kapan masing-masing paling tepat dipakai?
- Beda AND dan OR — beri 1 contoh kehidupan sehari-hari untuk masing-masing.
- Bagian mana yang masih sulit dipahami?
- **Skala pemahaman diri:** ____/10

---

**MGMP Informatika SMAN 6 Cimahi — Fase F (Kelas XI) Semester 1**
*Materi gabungan Pertemuan 5–11: Notasi Algoritma, Flowchart, dan Pseudocode*