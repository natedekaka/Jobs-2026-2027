# BAHAN AJAR – PERTEMUAN 3
## Simulasi Dinamika Input-Proses-Output (IPO)

| Mata Pelajaran | Informatika |
|---|---|
| Fase / Kelas | E / X |
| TP | BK 1.6 |
| Semester | 1 (Ganjil) |

---

### A. Konsep Alamat Memori

Memori komputer (RAM) dapat dibayangkan seperti **deretan loker** atau **rumah di suatu kompleks**. Setiap loker/rumah memiliki **nomor unik** yang disebut **alamat memori**.

```
Memori sebagai deretan loker:

┌─────┬─────┬─────┬─────┬─────┬─────┬─────┬─────┐
│  7  │  3  │  0  │  5  │  2  │  9  │  4  │  6  │ ← Isi Data
├─────┼─────┼─────┼─────┼─────┼─────┼─────┼─────┤
│  0  │  1  │  2  │  3  │  4  │  5  │  6  │  7  │ ← Alamat
└─────┴─────┴─────┴─────┴─────┴─────┴─────┴─────┘
```

| Analogi | Sistem Komputer |
|---|---|
| Kompleks perumahan | Memori (RAM) |
| Nomor rumah | Alamat memori (0, 1, 2, ...) |
| Orang yang tinggal | Data (angka, huruf, instruksi) |
| Kurir | CPU (melalui Bus) |
| Kurir mengambil orang dari rumah | READ (Load) — data disalin, tidak hilang |
| Kurir menaruh orang di rumah | WRITE (Store) — data lama terganti |

**Dua Operasi Dasar CPU terhadap Memori:**

1. **READ (Load)** — CPU membaca data dari alamat memori tertentu. Data di memori **tetap ada** (disalin, bukan dipindahkan).
2. **WRITE (Store)** — CPU menulis data ke alamat memori tertentu. Data **lama di alamat itu akan terganti**.

---

### B. Siklus Fetch-Decode-Execute (Siklus Mesin)

CPU menjalankan instruksi dalam siklus berulang yang disebut **siklus mesin (machine cycle)**:

```
          ┌─────────────────────────────────────┐
          │           SIKLUS MESIN              │
          │                                     │
          │  1. FETCH — Ambil instruksi         │
          │     dari memori berdasarkan PC      │
          │                                     │
          │  2. DECODE — Terjemahkan instruksi  │
          │     (apa yang harus dilakukan?)      │
          │                                     │
          │  3. EXECUTE — Jalankan instruksi    │
          │     (ALU menghitung, atau           │
          │      pindahkan data, dll.)          │
          │                                     │
          │  4. STORE — Simpan hasil            │
          │     (kembali ke memori/register)    │
          │                                     │
          └─────────────────────────────────────┘
```

**Program Counter (PC):** Sebuah register khusus di CPU yang menyimpan alamat instruksi yang akan dijalankan **berikutnya**. Setelah satu instruksi selesai, PC bertambah 1 (atau sesuai kebutuhan) untuk menunjuk ke instruksi berikutnya.

---

### C. Eksekusi Program: Contoh Langkah demi Langkah

**Program:** Hitung `(5 + 3) × 2`

**Kondisi awal memori:**

| Alamat | Isi | Arti |
|---|---|---|
| 0 | LOAD 5 | Ambil data dari alamat 5 → Register A |
| 1 | LOAD 6 | Ambil data dari alamat 6 → Register B |
| 2 | ADD | A = A + B |
| 3 | LOAD 8 | Ambil data dari alamat 8 → Register B |
| 4 | MUL | A = A × B |
| 5 | STORE 7 | Simpan A ke alamat 7 |
| 6 | HALT | Hentikan program |
| 7 | — | (hasil) |
| 8 | 5 | Data |
| 9 | 3 | Data |
| 10 | 2 | Data |

**Eksekusi langkah demi langkah:**

| Langkah | PC | Instruksi | Yang Terjadi | Register A | Register B | Alamat 7 |
|---|---|---|---|---|---|---|
| 0 | — | — | (keadaan awal) | ? | ? | — |
| 1 | 0 | LOAD 5 | A ← data[5] = 5 | **5** | ? | — |
| 2 | 1 | LOAD 6 | B ← data[6] = 3 | 5 | **3** | — |
| 3 | 2 | ADD | A = A + B = 5 + 3 = 8 | **8** | 3 | — |
| 4 | 3 | LOAD 8 | B ← data[8] = 2 | 8 | **2** | — |
| 5 | 4 | MUL | A = A × B = 8 × 2 = 16 | **16** | 2 | — |
| 6 | 5 | STORE 7 | memori[7] ← A = 16 | 16 | 2 | **16** |
| 7 | 6 | HALT | Program berhenti | 16 | 2 | 16 |

**Hasil:** (5 + 3) × 2 = **16** ✅

---

### D. Clock Speed dan Kinerja CPU

CPU bekerja berdasarkan **detak clock (clock cycle)** — seperti detak jantung atau irama drum.

| Istilah | Penjelasan | Analogi |
|---|---|---|
| **Clock Cycle** | Satu detak — satu langkah kerja CPU | Satu pukulan drum |
| **Clock Speed** | Jumlah detak per detik (dalam GHz) | Tempo drum (cepat/lambat) |
| **1 GHz** | 1 miliar siklus per detik | — |

**Contoh:** Jika CPU 3 GHz, artinya dalam 1 detik CPU bisa melakukan 3 miliar siklus. Satu instruksi biasanya membutuhkan 1–4 siklus clock.

> **Clock speed bukan satu-satunya penentu kecepatan.** Arsitektur CPU (jumlah core, pipeline, cache) juga sangat berpengaruh.

---

### E. Studi Kasus IPO dalam Aplikasi Sehari-hari

#### Studi Kasus 1: Memutar Lagu di Aplikasi Musik

| Tahap | Proses |
|---|---|
| **Input** | User mengetuk judul lagu di layar |
| **Proses** | CPU membaca file lagu dari memori internal → decoder mengubah sinyal digital ke analog |
| **Output** | Suara lagu keluar dari speaker/headphone |
| **Storage** | File lagu tetap tersimpan di memori internal; data yang sedang diputar disimpan sementara di RAM |

#### Studi Kasus 2: Mengirim Pesan WhatsApp

| Tahap | Proses |
|---|---|
| **Input** | User mengetik pesan dan menekan kirim |
| **Proses** | CPU memproses teks → enkripsi → dikirim ke antena WiFi/seluler |
| **Output** | Teks terkirim (tampil centang di layar) |
| **Storage** | Pesan disimpan di database WhatsApp (HP dan cloud) |

#### Studi Kasus 3: Memotret dengan HP

| Tahap | Proses |
|---|---|
| **Input** | Sensor kamera menangkap cahaya → diubah ke sinyal digital |
| **Proses** | CPU/ISP (Image Signal Processor) memproses gambar → noise reduction, color correction |
| **Output** | Gambar tampil di layar HP |
| **Storage** | File foto disimpan di memori internal HP |

---

### F. Rangkuman

1. **Alamat memori** adalah nomor unik setiap lokasi penyimpanan di RAM — CPU mengakses data berdasarkan alamat.
2. **READ (Load)**: CPU menyalin data dari memori (data sumber tidak hilang).
3. **WRITE (Store)**: CPU menulis data ke memori (data lama terganti).
4. **Siklus mesin**: Fetch → Decode → Execute → Store — diulang miliaran kali per detik.
5. **Program Counter (PC)**: menunjuk ke instruksi yang akan dijalankan berikutnya.
6. **Clock speed** menentukan seberapa cepat CPU menjalankan siklus.
7. Setiap aktivitas digital (musik, WA, foto) melibatkan alur IPO yang melibatkan CPU, memori, dan bus.

---

### G. Glosarium

| Istilah | Arti |
|---|---|
| **Alamat Memori** | Nomor unik setiap lokasi di memori |
| **READ (Load)** | Operasi membaca data dari memori ke CPU |
| **WRITE (Store)** | Operasi menulis data dari CPU ke memori |
| **PC (Program Counter)** | Register yang menyimpan alamat instruksi berikutnya |
| **Siklus Mesin** | Satu putaran Fetch-Decode-Execute-Store |
| **Clock Cycle** | Satu detak clock pada CPU |
| **Register** | Memori kecil berkecepatan tinggi di dalam CPU |
| **Bus** | Jalur komunikasi antar komponen komputer |

---

**MGMP Informatika SMAN 6 Cimahi**
