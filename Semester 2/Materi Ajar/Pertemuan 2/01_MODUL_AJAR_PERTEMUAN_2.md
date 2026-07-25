# MODUL AJAR INFORMATIKA – FASE E (KELAS X)

## Informasi Umum

| Komponen | Deskripsi |
|---|---|
| **Mata Pelajaran** | Informatika |
| **Fase / Kelas** | E / X |
| **Semester** | 2 (Genap) |
| **Pertemuan ke-** | 2 |
| **Alokasi Waktu** | 2 JP × 45 menit (90 menit) |
| **Tahun Pelajaran** | 2026/2027 |
| **Satuan Pendidikan** | **SMA Negeri 6 Cimahi** |

---

## Profil Pelajar Pancasila

| Dimensi | Indikator |
|---|---|
| Bernalar Kritis | Menganalisis penerapan LIFO dalam berbagai konteks |
| Kreatif | Menemukan contoh stack di luar materi |
| Mandiri | Melakukan simulasi stack secara mandiri |

---

## Tujuan Pembelajaran

| TP | Indikator Ketercapaian Tujuan Pembelajaran (IKTP) |
|---|---|
| **BK 1.1:** Memahami konsep struktur data dasar | 1.1.5 Menjelaskan konsep LIFO (Last In First Out)<br>1.1.6 Mendemonstrasikan operasi push dan pop<br>1.1.7 Mengidentifikasi penerapan stack dalam kehidupan sehari-hari dan teknologi |

---

## Langkah Pembelajaran

### Pembukaan (10 menit)

| Kegiatan | Waktu |
|---|---|
| 1. Salam, doa, cek kehadiran | 2 menit |
| 2. **Review tugas**: 2–3 siswa sebutkan contoh array yang ditemukan di rumah | 5 menit |
| 3. **Apersepsi**: Guru menumpuk buku di meja — "Buku mana yang bisa diambil pertama? Buku paling atas. Itulah **stack**!" | 3 menit |

### Inti (65 menit)

#### Memahami (15 menit)

1. **Konsep Stack — LIFO (5 menit)**
   - **Stack (Tumpukan)**: Data masuk dan keluar di satu tempat (atas)
   - **Prinsip LIFO**: Last In First Out — yang terakhir masuk, pertama keluar
   - **Dua operasi dasar**:
     - `push(item)`: menambah data ke atas tumpukan
     - `pop()`: mengambil data dari atas tumpukan

2. **Contoh Stack (5 menit)**
   | Contoh | Push | Pop |
   |---|---|---|
   | Tumpukan piring | Menaruh piring baru di atas | Mengambil piring paling atas |
   | Fitur Undo (Ctrl+Z) | Menyimpan aksi ke stack | Membatalkan aksi terakhir |
   | Riwayat browser (Back) | Halaman baru masuk stack | Kembali ke halaman sebelumnya |
   | Tumpukan buku | Menaruh buku di atas | Mengambil buku paling atas |

3. **Stack dalam Python (5 menit) — Preview**
   - Gunakan list Python sebagai stack:
   ```python
   stack = []        # stack kosong
   stack.push(5)     # [5] (sebenarnya append)
   stack.push(3)     # [5, 3]
   stack.pop()       # 3 → stack = [5]
   ```
   - Siswa cukup melihat demo, belum coding detail

#### Mengaplikasi (40 menit)

4. **Aktivitas 1: Simulasi Stack dengan Buku (15 menit) — Klasikal**
   - 5 siswa maju, masing-masing pegang buku
   - Guru sebut nama → siswa menumpuk buku (push)
   - Guru minta "ambil buku" → siswa ambil dari atas (pop)
   - Catat urutan masuk dan keluar → buktikan LIFO

5. **Aktivitas 2: Stack dengan Kartu (15 menit) — Berpasangan**
   - Setiap pasangan punya 5 kartu bernomor
   - **Percobaan 1**: Push 5→3→8→1→6, lalu Pop 3× → catat hasilnya
   - **Percobaan 2**: Push 2→4, Pop 1×, Push 7→9, Pop 2× → catat hasilnya
   - **Percobaan 3**: Buat urutan sendiri, tukar dengan pasangan lain

6. **Aktivitas 3: Teka-teki Stack (10 menit)**
   - Soal: "Jika kita push urutan A→B→C→D, lalu pop 2×, lalu push E→F, lalu pop 3×. Urutan pop?"
   - Jawab: D, C, F, E (Buktikan dengan simulasi kartu!)

#### Merefleksi (10 menit)

7. **Diskusi (5 menit)**
   - "Apa beda stack dengan array biasa?"
   - "Mengapa browser menggunakan stack untuk tombol Back?"
   - "Apa kelemahan stack?"

8. **Refleksi Individu (5 menit)**
   - Satu analogi stack favorit
   - Bedakan push dan pop dengan kata sendiri

### Penutup (15 menit)

| Kegiatan | Waktu |
|---|---|
| 1. Rangkuman | 3 menit |
| 2. Tanya jawab | 5 menit |
| 3. **Tugas**: Temukan 2 contoh stack di rumah/sekolah selain dari materi | 3 menit |
| 4. Sampaikan pertemuan depan: Queue (Antrian) — FIFO | 2 menit |
| 5. Doa & salam | 2 menit |

---

## Asesmen

| Kriteria | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| Simulasi LIFO | Tidak paham | Paham jika dibantu | Paham LIFO | Paham + bisa prediksi pop |
| Teka-teki stack | Tidak bisa | 1–2 benar | 3–4 benar | 5 benar |
| Contoh stack | Tidak ada | 1 contoh | 2 contoh | 2 contoh + analisis |

---

**MGMP Informatika SMAN 6 Cimahi**
