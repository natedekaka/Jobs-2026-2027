Saya sengaja mengosongkan kolom **Nilai Huruf** dan **Keterangan** agar siswa berlatih mengisi rumus.

Saya gunakan kriteria latihan sebagai berikut:

- **Nilai Huruf**
  - 85 – 100 = **A**
  - 70 – 84 = **B**
  - 55 – 69 = **C**
  - 0 – 54 = **D**
- **Keterangan**
  - **LULUS** jika **Nilai Ujian ≥ 75** dan **Kehadiran ≥ 80%**
  - Selain itu **GAGAL**

> Jika kriteria kelulusan yang Anda gunakan berbeda, tinggal ubah angka `75` dan `80%` pada rumus.

---

## A. Tabel Latihan Siswa

Salin tabel ini ke Excel, mulai dari sel **A1**.

|   No | Nama           | Nilai Ujian | Kode Kelas | Kehadiran (%) | Nilai Huruf | Keterangan |
| ---: | -------------- | ----------: | :--------: | ------------: | :---------: | :--------: |
|    1 | Aditya Nugraha |          84 |    11A     |           80% |             |            |
|    2 | Bela Puspita   |          85 |    11B     |           79% |             |            |
|    3 | Cahyo Wibowo   |          55 |    11C     |           85% |             |            |
|    4 | Dewi Anggraini |          75 |    11A     |           80% |             |            |
|    5 | Eko Prasetyo   |          74 |    11B     |           90% |             |            |
|    6 | Fira Ramadhani |          70 |    11C     |           95% |             |            |
|    7 | Galih Saputra  |          69 |    11A     |           88% |             |            |
|    8 | Hana Nurhaliza |          54 |    11B     |           80% |             |            |
|    9 | Indra Maulana  |          95 |    11C     |          100% |             |            |
|   10 | Joko Susilo    |          60 |    11A     |           79% |             |            |
|   11 | Kartika Sari   |          88 |    11B     |           88% |             |            |
|   12 | Laksmana Putra |          78 |    11C     |           81% |             |            |
|   13 | Maya Rahma     |          50 |    11A     |           70% |             |            |
|   14 | Nugroho Adi    |          82 |    11B     |           75% |             |            |
|   15 | Oka Mahendra   |          76 |    11C     |           84% |             |            |
|   16 | Putri Ayunda   |          65 |    11A     |           92% |             |            |
|   17 | Qori Ananda    |          90 |    11B     |           83% |             |            |
|   18 | Rina Amelia    |          72 |    11C     |           80% |             |            |
|   19 | Surya Pratama  |          81 |    11A     |           78% |             |            |
|   20 | Tania Lestari  |          99 |    11B     |           96% |             |            |

---

## B. Tabel Mapping Kode Kelas

Tabel ini bisa dipakai jika Anda ingin menambah latihan **VLOOKUP** untuk menampilkan Nama Kelas.

| Kode Kelas | Nama Kelas |
| :--------: | ---------- |
|    11A     | XI IPA 1   |
|    11B     | XI IPS 1   |
|    11C     | XI BAHASA  |

---

## C. Rekap yang Harus Diisi Siswa

| Rekap               | Hasil / Rumus |
| ------------------- | ------------- |
| RATA-RATA           |               |
| NILAI TERTINGGI     |               |
| NILAI TERENDAH      |               |
| SELISIH NILAI       |               |
| JUMLAH SISWA        |               |
| JUMLAH YANG LULUS   |               |
| RATA-RATA KELAS 11A |               |
| RATA-RATA KELAS 11B |               |
| RATA-RATA KELAS 11C |               |

---

## D. Contoh Rumus Excel

Catatan:  
Rumus di bawah menggunakan tanda **titik koma** `;` sebagai pemisah. Jika Excel Anda menggunakan tanda **koma** `,`, silakan ganti semua `;` menjadi `,`.

### 1. Rumus Nilai Huruf pada Kolom F

Ketikan di sel **F2**:

```excel
=IF(C2>=85;"A";IF(C2>=70;"B";IF(C2>=55;"C";"D")))
```

Lalu salin/drag ke bawah sampai **F21**.

---

### 2. Rumus Keterangan pada Kolom G

Ketikan di sel **G2**:

```excel
=IF(AND(C2>=75;E2>=80%);"LULUS";"GAGAL")
```

Lalu salin/drag ke bawah sampai **G21**.

Jika kolom Kehadiran tidak menggunakan format persen, tetapi angka biasa 0–100, gunakan rumus:

```excel
=IF(AND(C2>=75;E2>=80);"LULUS";"GAGAL")
```

---

### 3. Rumus Rekap

| Rekap               | Rumus                             |
| ------------------- | --------------------------------- |
| RATA-RATA           | `=AVERAGE(C2:C21)`                |
| NILAI TERTINGGI     | `=MAX(C2:C21)`                    |
| NILAI TERENDAH      | `=MIN(C2:C21)`                    |
| SELISIH NILAI       | `=MAX(C2:C21)-MIN(C2:C21)`        |
| JUMLAH SISWA        | `=COUNTA(B2:B21)`                 |
| JUMLAH YANG LULUS   | `=COUNTIF(G2:G21;"LULUS")`        |
| RATA-RATA KELAS 11A | `=AVERAGEIF(D2:D21;"11A";C2:C21)` |
| RATA-RATA KELAS 11B | `=AVERAGEIF(D2:D21;"11B";C2:C21)` |
| RATA-RATA KELAS 11C | `=AVERAGEIF(D2:D21;"11C";C2:C21)` |

---

### 4. Rumus Tambahan: Mencari Nama Kelas dengan VLOOKUP

Jika Anda ingin menambah kolom **Nama Kelas**, misalnya di kolom **H**, gunakan rumus seperti ini:

```excel
=VLOOKUP(D2;$J$2:$K$4;2;FALSE)
```

Sesuaikan range `$J$2:$K$4` dengan lokasi tabel mapping Kode Kelas di file Excel Anda.

---

## E. Kunci Jawaban untuk Guru

Berikut kunci jawaban kolom **Nilai Huruf** dan **Keterangan** berdasarkan kriteria di atas.

|   No | Nilai Huruf | Keterangan |
| ---: | :---------: | :--------: |
|    1 |      B      |   LULUS    |
|    2 |      A      |   GAGAL    |
|    3 |      C      |   GAGAL    |
|    4 |      B      |   LULUS    |
|    5 |      B      |   GAGAL    |
|    6 |      B      |   GAGAL    |
|    7 |      C      |   GAGAL    |
|    8 |      D      |   GAGAL    |
|    9 |      A      |   LULUS    |
|   10 |      C      |   GAGAL    |
|   11 |      A      |   LULUS    |
|   12 |      B      |   LULUS    |
|   13 |      D      |   GAGAL    |
|   14 |      B      |   GAGAL    |
|   15 |      B      |   LULUS    |
|   16 |      C      |   GAGAL    |
|   17 |      A      |   LULUS    |
|   18 |      B      |   GAGAL    |
|   19 |      B      |   GAGAL    |
|   20 |      A      |   LULUS    |

---

## F. Kunci Jawaban Rekap

Jika semua rumus dikerjakan sesuai data di atas, hasil rekapnya adalah sebagai berikut.

| Rekap               | Jawaban |
| ------------------- | ------: |
| RATA-RATA           |   75,10 |
| NILAI TERTINGGI     |      99 |
| NILAI TERENDAH      |      50 |
| SELISIH NILAI       |      49 |
| JUMLAH SISWA        |      20 |
| JUMLAH YANG LULUS   |       8 |
| RATA-RATA KELAS 11A |   69,14 |
| RATA-RATA KELAS 11B |   81,71 |
| RATA-RATA KELAS 11C |   74,33 |

> Angka desimal bisa berbeda tampilannya tergantung pembulatan dan pengaturan regional Excel.