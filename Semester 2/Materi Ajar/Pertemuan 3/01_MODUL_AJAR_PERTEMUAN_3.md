# MODUL AJAR INFORMATIKA – FASE E (KELAS X)

## Informasi Umum

| Komponen | Deskripsi |
|---|---|
| **Mata Pelajaran** | Informatika |
| **Fase / Kelas** | E / X |
| **Semester** | 2 (Genap) |
| **Pertemuan ke-** | 3 |
| **Alokasi Waktu** | 2 JP × 45 menit (90 menit) |
| **Tahun Pelajaran** | 2026/2027 |
| **Satuan Pendidikan** | **SMA Negeri 6 Cimahi** |

---

## Tujuan Pembelajaran

| TP | Indikator Ketercapaian Tujuan Pembelajaran (IKTP) |
|---|---|
| **BK 1.1:** Memahami konsep struktur data dasar | 1.1.8 Menjelaskan konsep FIFO (First In First Out)<br>1.1.9 Mendemonstrasikan operasi enqueue dan dequeue<br>1.1.10 Membedakan stack (LIFO) dan queue (FIFO)<br>1.1.11 Mengidentifikasi penerapan queue dalam kehidupan sehari-hari |

---

## Langkah Pembelajaran

### Pembukaan (10 menit)

| Kegiatan | Waktu |
|---|---|
| 1. Salam, doa, cek kehadiran | 2 menit |
| 2. **Review**: "Apa beda stack dan array? LIFO artinya apa?" | 3 menit |
| 3. **Apersepsi**: "Siapa yang antre di kantin tadi pagi? Siapa dapat duluan? Yang datang pertama!" — queue. | 5 menit |

### Inti (65 menit)

#### Memahami (15 menit)

1. **Konsep Queue — FIFO (5 menit)**
   - **Queue (Antrian)**: data masuk di belakang, keluar dari depan
   - **FIFO**: First In First Out — yang pertama masuk, pertama keluar
   - **Operasi**:
     - `enqueue(data)`: menambah data ke belakang antrian
     - `dequeue()`: mengambil data dari depan antrian

2. **Perbandingan Stack vs Queue (5 menit)**
   | Aspek | Stack (LIFO) | Queue (FIFO) |
   |---|---|---|
   | Masuk/Keluar | Satu sisi (atas) | Depan (keluar), belakang (masuk) |
   | Operasi | push / pop | enqueue / dequeue |
   | Analogi | Tumpukan piring | Antrian kasir |
   | Contoh | Undo, Browser Back | Print queue, antrian bank |

3. **Contoh Queue (5 menit)**
   | Contoh | Enqueue | Dequeue |
   |---|---|---|
   | Antrian kasir | Pelanggan datang | Pelanggan dilayani |
   | Antrian printer | Dokumen dikirim | Dokumen dicetak |
   | Antrian bank | Ambil nomor antre | Dipanggil teller |
   | Sistem pesan (chat) | Pesan masuk | Pesan dibaca |

#### Mengaplikasi (40 menit)

4. **Aktivitas 1: Simulasi Antrian Kelas (10 menit)**
   - 6 siswa maju membentuk antrian
   - Masing-masing pegang kertas bernomor
   - Guru sebut "enqueue" → siswa baru di belakang
   - Guru sebut "dequeue" → siswa depan keluar
   - Catat urutan → buktikan FIFO

5. **Aktivitas 2: Queue dengan Kartu (15 menit) — Berpasangan**
   - Setiap pasangan punya 5 kartu + kertas "ANTRIAN"
   - **Percobaan 1**: Enqueue 5→3→8, Dequeue 2×, Enqueue 1→6, Dequeue 1×
   - **Percobaan 2**: Enqueue A→B→C, Dequeue 1×, Enqueue D→E, Dequeue 3×

6. **Aktivitas 3: Stack vs Queue (15 menit) — Kelompok**
   - **Tugas**: Isi tabel perbandingan lengkap dengan contoh
   - **Buat poster kecil** (kertas A4) perbandingan Stack vs Queue
   - Tempel di dinding — presentasi 2 kelompok

#### Merefleksi (10 menit)

7. **Kuis Cepat (5 menit)**
   - Push 1→2→3, Pop 1×, Push 4, Pop 2× → hasil?
   - Enqueue X→Y→Z, Dequeue 1×, Enqueue W, Dequeue 2× → hasil?

8. **Refleksi (5 menit)**

### Penutup (15 menit)

| Kegiatan | Waktu |
|---|---|
| 1. Rangkuman: "Queue FIFO, Stack LIFO. Keduanya struktur data dasar yang penting." | 3 menit |
| 2. **Kuis keluar (exit ticket)**: "Sebutkan 1 perbedaan stack dan queue!" | 5 menit |
| 3. Sampaikan: **Sekarang libur Ramadan + tugas mandiri.** Pertemuan 4: Sequential Search. | 4 menit |
| 4. **Tugas Ramadan**: Baca materi Searching & Sorting, kerjakan 5 soal, eksplorasi visualgo.net | 2 menit |
| 5. Doa & salam | 1 menit |

---

## Asesmen

| Kriteria | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| Simulasi FIFO | Tidak paham | Paham jika dibantu | Paham FIFO | Paham + bedakan dgn LIFO |
| Perbandingan | Tidak bisa | 1 perbedaan | 2 perbedaan | ≥ 3 perbedaan + contoh |
| Kuis | 0 benar | 1 benar | 2–3 benar | 4–5 benar |

---

**MGMP Informatika SMAN 6 Cimahi**
