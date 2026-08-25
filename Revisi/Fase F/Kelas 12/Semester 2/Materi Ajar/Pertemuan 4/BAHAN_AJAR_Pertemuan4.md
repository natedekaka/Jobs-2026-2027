# BAHAN AJAR – PERTEMUAN 4 (S2)
## Workshop — Analisis Data
*Mengacu pada Panduan Mapel 2025; INFORMATIKA Fase D-F — pendekatan Pembelajaran Mendalam (Memahami → Mengaplikasi → Merefleksi)*

| Informasi | Keterangan |
|---|---|
| **Fase / Kelas** | F / Kelas XII |
| **Alokasi Waktu** | 5 JP × 45 menit (225 menit) |
| **Elemen CP** | PLB (Praktik Lintas Bidang) |
| **Tujuan Pembelajaran** | Menggunakan Pivot Table untuk meringkas data, membuat visualisasi (bar, pie, line chart), menginterpretasikan hasil, dan menarik kesimpulan berbasis data |
| **Materi Prasyarat** | Data bersih siap analisis (Pertemuan 3); dasar Pivot Table (S1) |

---

## A. Kisah Pemantik 🎬

> **"Grafik yang Berbicara"**
>
> Kelompok Nadia punya 40 baris data minat baca. Saat presentasi bimbingan, guru bertanya, *"Apa temuan kalian?"* Nadia kebingungan karena mereka hanya menunjukkan tabel mentah. Gurunya memberi tantangan: *"Buat ringkasan dalam satu tabel dan satu grafik yang bisa menjawab pertanyaan orang dalam 10 detik."*
>
> Dengan Pivot Table dan chart, mereka menemukan: kelas XI-A membaca 3,5 buku/bulan — tertinggi; genre fiksi paling populer (45%); dan sebagian besar siswa membaca kurang dari 1 jam per hari. Sekarang grafik mereka "berbicara", dan setiap temuan didukung angka yang jelas.
>
> **Pertanyaan pemantik:**
> 1. Mengapa tabel data mentah dengan 40 baris sulit dibaca orang lain?
> 2. Pertanyaan analisis apa yang ingin kamu jawab dari data proyekmu?
> 3. Grafik jenis apa yang paling cocok untuk menunjukkan proporsi?

---

## B. Konsep Inti: Dari Data Mentah Menjadi Wawasan

Analisis data mengubah data mentah menjadi **informasi** dan **wawasan (insight)** melalui tiga langkah: **ringkas → visualisasikan → interpretasikan**.

| Istilah | Arti | Contoh |
|---|---|---|
| **Pivot Table** | Fitur Excel untuk meringkas data | Rata-rata buku per kelas |
| **Rows** | Area Pivot untuk kategori baris | Kelas, Genre |
| **Values** | Area Pivot untuk nilai yang dihitung | Count, Average, Sum |
| **PivotChart** | Grafik yang dibuat dari Pivot Table | Column, Pie, Line |
| **Interpretasi** | Penjelasan makna dari angka/grafik | "Kelas XI-A paling aktif membaca" |

> 💡 **Ingat:** Pivot Table tidak mengubah data asli — ia membuat ringkasan yang diperbarui otomatis jika data sumber berubah.

---

## C. Workshop 2: Analisis Data dengan Pivot Table

### C.1 Langkah Membuat Pivot Table
1. Blok seluruh data bersih (atau klik dalam tabel berformat Ctrl+T).
2. **Insert → PivotTable → New Worksheet**.
3. Drag field ke area sesuai kebutuhan analisis.

### C.2 Analisis Wajib untuk Proyek

| Analisis | Pivot Rows | Pivot Values | Grafik |
|---|---|---|---|
| Perbandingan per kelas | Kelas | Count / Average | Bar / Column |
| Kategori favorit | Genre / Kategori | Count | Pie |
| Rata-rata numerik | Kelas | Average | Column |
| Tren / frekuensi | Kategori | Count | Bar / Line |

### C.3 Contoh Analisis Survei Minat Baca

1. **Rata-rata buku/bulan per kelas** — Rows: Kelas, Values: Average of Buku/bulan.
   *Interpretasi:* "Kelas XI-A rata-rata 3,5 buku/bulan, tertinggi dibanding kelas lain."
2. **Genre favorit** — Rows: Genre, Values: Count, lalu Pie chart.
   *Interpretasi:* "Fiksi adalah genre paling populer (45% dari responden)."
3. **Hubungan kelas dan waktu baca** — Rows: Kelas, Columns: Waktu_baca, Values: Count.
   *Interpretasi:* "Kelas XII lebih banyak membaca >2 jam/hari dibanding kelas XI."

---

## D. Membuat Grafik dari Pivot Table

1. Klik di dalam Pivot Table.
2. Menu **PivotTable Analyze → PivotChart**.
3. Pilih jenis grafik sesuai pesan:

| Jenis Grafik | Kegunaan | Kapan Dipakai |
|---|---|---|
| Column / Bar | Membandingkan kategori | Nilai per kelas, jumlah per genre |
| Pie | Menunjukkan proporsi bagian | Porsi 1 genre dari total |
| Line | Menunjukkan tren waktu | Perubahan selama beberapa periode |

> 💡 **Tips:** Grafik yang benar memudahkan pembaca menangkap pesan dalam sekejap. Pie cocok untuk maksimal 4–5 kategori; jika lebih, gunakan column.

---

## E. Interpretasi Data — Menulis Makna, Bukan Sekadar Angka

### E.1 Template Interpretasi
> "Berdasarkan grafik **[judul grafik]**, dapat dilihat bahwa **[temuan utama]**. **[Kategori A]** memiliki **[nilai]** lebih **[tinggi/rendah]** dibanding **[kategori B]**. Hal ini menunjukkan bahwa **[kesimpulan]**. Kemungkinan penyebab: **[alasan]**. Rekomendasi: **[saran]**."

### E.2 Contoh Interpretasi
"Berdasarkan grafik *Rata-rata Buku per Kelas*, dapat dilihat bahwa kelas XI-A memiliki rata-rata 3,5 buku/bulan, lebih tinggi dari kelas XI-B (2,1 buku/bulan). Hal ini menunjukkan minat baca kelas XI-A lebih baik. Kemungkinan penyebab: kelas XI-A memiliki pojok baca yang aktif. Rekomendasi: kelas XI-B perlu program literasi tambahan."

### E.3 Perbedaan Deskripsi vs Interpretasi

| Deskripsi (belum cukup) | Interpretasi (bermakna) |
|---|---|
| "Pie chart menunjukkan 45% menyukai fiksi" | "Fiksi mendominasi karena siswa menganggapnya lebih menghibur; rekomendasi: sediakan lebih banyak koleksi fiksi di pojok baca." |
| "Rata-rata 2,5 jam membaca" | "Rata-rata masih rendah dibanding target; perlu kampanye gerakan literasi." |

---

## F. Contoh Soal & Penyelesaian 📝

**Soal 1:** Data proyek memiliki kolom: Kelas, Genre, Buku/bulan. Untuk menjawab "genre apa yang paling disukai siswa?", jelaskan pengaturan Pivot Table-nya.
**Pembahasan:** Rows: Genre (kategori sebagai baris), Values: Count of Genre (menghitung jumlah tiap genre). Hasilnya berupa jumlah responden per genre; nilai terbesar = genre terfavorit. Untuk menampilkan proporsi, gunakan Pie chart.

**Soal 2:** Jelaskan perbedaan antara deskripsi dan interpretasi data dengan contoh.
**Pembahasan:** Deskripsi hanya menyebut angka ("45% suka fiksi"), sedangkan interpretasi menjelaskan makna, kemungkinan penyebab, dan rekomendasi ("Fiksi mendominasi karena menghibur; tambahkan koleksi fiksi di pojok baca"). Interpretasi menjawab pertanyaan "jadi apa?" dari data.

**Soal 3:** Mengapa Pie chart kurang cocok jika ada 8 kategori genre?
**Pembahasan:** Pie chart dengan banyak kategori sulit dibaca karena potongan-potongan kecil hampir sama dan labelnya menumpuk. Untuk banyak kategori, lebih baik menggunakan column/bar chart yang memudahkan perbandingan.

---

## G. Kesalahan Umum dalam Analisis Data 🚫

| Kesalahan | Akibat | Solusi |
|---|---|---|
| Menganalisis data yang belum bersih | Hasil salah/menyesatkan | Pastikan cleaning selesai dulu |
| Hanya membuat grafik tanpa interpretasi | Pembaca tidak paham maknanya | Tulis interpretasi di bawah tiap grafik |
| Memilih grafik yang salah (pie untuk banyak kategori) | Pesan tidak terbaca | Gunakan bar/column untuk banyak kategori |
| Mengedit data di dalam Pivot Table | Angka jadi salah | Edit data sumber, lalu Refresh |
| Menyimpulkan hanya dari satu responden | Kesimpulan bias | Pastikan ≥30 responden |

---

## H. Tantangan Praktik (Mengaplikasi) 🎯

**Milestone Minggu 4 (Analisis Data):**
- [ ] **Tingkat 1 (Dasar):** Buat 3 Pivot Table (perbandingan kelas, kategori favorit, rata-rata numerik).
- [ ] **Tingkat 2 (Menengah):** Buat 3 chart dari Pivot (column, pie, column/line) sesuai jenis data.
- [ ] **Tingkat 3 (Mahir):** Tulis interpretasi 3–4 kalimat untuk tiap chart dan simpan sebagai "Analisis_Proyek_NamaKelompok.xlsx" di Google Drive.

---

## I. Rangkuman Kunci 🔑

1. Alur analisis: **ringkas (Pivot) → visualisasi (chart) → interpretasi**.
2. Pivot Table meringkas data; atur Rows, Columns, dan Values sesuai pertanyaan.
3. Column untuk perbandingan, Pie untuk proporsi, Line untuk tren.
4. Interpretasi menjelaskan temuan, penyebab, dan rekomendasi — bukan sekadar angka.
5. 3 analisis wajib: perbandingan per kelas, kategori favorit, rata-rata numerik.
6. Pivot Table harus di-*refresh* jika data sumber diubah.

---

## J. Glosarium 📖

| Istilah | Arti |
|---|---|
| **Pivot Table** | Tabel ringkasan interaktif di Excel |
| **Rows / Columns / Values** | Area pengaturan dalam Pivot Table |
| **PivotChart** | Grafik yang terhubung dengan Pivot Table |
| **Interpretasi** | Penjelasan makna dari data/grafik |
| **Insight** | Wawasan/penemuan penting dari analisis |
| **Count / Average / Sum** | Operasi perhitungan dalam Values |

---

## K. Refleksi (Merefleksi) 🔍

- Temuan apa yang paling mengejutkan dari data proyek kelompokmu?
- Apakah interpretasimu sudah menjawab "jadi apa?" — bukan sekadar menyebut angka?
- Grafik mana yang paling sulit dibuat dan bagaimana kamu mengatasinya?
- **Skala pemahaman diri:** ____/10
- Apa yang akan kamu lakukan jika temuanmu berbeda dari dugaan awal?

---

**MGMP Informatika SMAN 6 Cimahi — Fase F (Kelas XII) Semester 2**