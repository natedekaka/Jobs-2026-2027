# MODUL AJAR INFORMATIKA – FASE F (KELAS XI)

| Komponen | Deskripsi |
|---|---|
| **Mata Pelajaran** | Informatika |
| **Fase / Kelas** | F / XI |
| **Semester** | 1 (Ganjil) |
| **Pertemuan ke-** | 5 |
| **Alokasi Waktu** | 5 JP × 45 menit (225 menit) |
| **Tahun Pelajaran** | 2026/2027 |
| **Satuan Pendidikan** | SMA Negeri 6 Cimahi |

---

## Tujuan Pembelajaran

| TP | IKTP |
|---|---|
| **BK, AP:** Memahami tahap pengujian dan debugging | 5.1 Menjelaskan pentingnya pengujian dalam SDLC |
| | 5.2 Membedakan jenis pengujian (unit, integration, UAT) |
| | 5.3 Melakukan debugging sederhana pada kode |
| | 5.4 Membuat test case dari user story |

---

## Langkah Pembelajaran

### Pembukaan (15 menit)

| Kegiatan | Waktu |
|---|---|
| 1. Salam, doa, cek kehadiran | 2 menit |
| 2. **Review** & ice breaking: "Pert 4: Implementasi — HTML, Git. Pert 5: **Testing & Debugging** — pastikan kode tidak error." + tanya jawab singkat | 5 menit |
| 3. **Apersepsi** & motivasi: "Pernah beli aplikasi yang sering crash? Atau game yang tiba-tiba force close? Itu karena testing tidak maksimal." + tayangkan video dampak bug | 8 menit |

### Inti (175 menit)

#### Memahami (50 menit)

**1. Pentingnya Testing (10 menit)**
- **Bug**: Cacat/error dalam kode
- **Testing**: Proses mencari bug sebelum aplikasi dipakai
- **Kasus nyata:**
  - Mars Climate Orbiter 1999 — error satelit hancur ($327M)
  - Knight Capital 2012 — bug software rugi $440M dalam 45 menit
  - Therac-25 1985 — bug alat radio terapi menyebabkan kematian pasien
- **Diskusi**: "Pernahkah kalian menemukan bug di aplikasi yang kalian gunakan? Ceritakan!"

**2. Jenis-Jenis Testing (15 menit)**

| Jenis | Apa yang Diuji? | Analogi |
|---|---|---|
| **Unit Test** | Satu fungsi/komponen kecil | Cek satu bata |
| **Integration Test** | Antar komponen bekerja sama | Cek apakah bata tersusun rapi |
| **System Test** | Seluruh sistem secara utuh | Cek seluruh rumah |
| **UAT** (User Acceptance Test) | Apakah sesuai kebutuhan user? | Pemilik rumah periksa |
| **Black-box** | Input → Output (tanpa lihat kode) | Coba semua tombol |
| **White-box** | Struktur internal kode | Periksa kabel di dalam |

- Contoh konkret: Testing form login — unit test (cek fungsi validasi), integration test (form + database), UAT (siswa coba login)

**3. Debugging — Mencari Bug (10 menit)**

| Langkah Debugging | Contoh |
|---|---|
| 1. Identifikasi gejala | "Aplikasi crash saat klik login" |
| 2. Reproduksi | Coba lagi, catat langkah persis |
| 3. Cari penyebab | Cek kode login, mungkin typo |
| 4. Perbaiki | Edit kode |
| 5. Verifikasi | Uji lagi |

- Analogi debugging seperti detektif mencari petunjuk

**4. Demo Testing Tools (15 menit)**
- Demo **Browser DevTools** (F12): Console untuk lihat error, Elements untuk lihat HTML
- Demo **W3C Validator** (validator.w3.org): Cek validitas kode HTML
- Demo **Lighthouse**: Audit kualitas halaman
- Siswa mengikuti demo di laptop masing-masing

#### Mengaplikasi (95 menit)

**5. Aktivitas 1 — Debugging Kode HTML Sederhana (25 menit) — Individu**
   - Guru memberikan kode HTML yang sengaja rusak (typo tag, lupa tutup tag, salah atribut)
   - Siswa mencari dan memperbaiki error menggunakan browser DevTools
   - Lihat perbedaan sebelum vs sesudah di browser
   - Catat bug yang ditemukan dan cara memperbaikinya

**6. Aktivitas 2 — Peer Testing (25 menit) — Berpasangan**
   - Tukar halaman HTML hasil Pertemuan 4 dengan pasangan
   - Setiap siswa menjadi **tester** untuk kode temannya
   - Uji halaman HTML: apa saja yang error? apa yang tidak sesuai?
   - Buat laporan bug sederhana: deskripsi bug, langkah reproduksi, screenshot
   - Kembalikan laporan ke pemilik kode untuk diperbaiki

**7. Aktivitas 3 — Membuat Test Case (25 menit) — Berpasangan**
   - Dari user story Pert 2: "Sebagai siswa, saya ingin login agar bisa mengakses nilai"
   - Buat test case: input valid, input invalid (NISN salah), input kosong, password salah
   - Tulis di tabel: skenario, input, expected output, actual output
   - Tambahkan test case untuk edge case (karakter spesial, input terlalu panjang)

**8. Aktivitas 4 — Presentasi & Diskusi (20 menit)**
   - 2-3 pasangan presentasi hasil test case dan laporan bug
   - Kelompok lain menanggapi dan memberikan masukan
   - Guru memberikan penguatan

#### Merefleksi (15 menit)

**9. Refleksi — Jurnal Belajar 3-2-1 (15 menit)**
   - Siswa menulis jurnal belajar dengan format 3-2-1:
     - **3 hal** yang dipelajari hari ini
     - **2 hal** yang paling menarik
     - **1 pertanyaan** yang masih mengganjal
   - 2-3 siswa diminta membagikan tulisannya
   - Guru memberikan klarifikasi untuk pertanyaan yang muncul

### Penutup (35 menit)

| Kegiatan | Waktu |
|---|---|
| 1. Diskusi kelas — tanya jawab materi hari ini (siswa bertanya, guru menjawab) | 10 menit |
| 2. Kuis lisan — tebak istilah (guru menyebutkan definisi, siswa menebak istilah) | 10 menit |
| 3. Rangkuman & penguatan konsep oleh guru | 5 menit |
| 4. Preview: "Pert 6: Deployment & CI/CD — bagaimana kode sampai ke user?" | 5 menit |
| 5. Tugas rumah: Cari 1 bug terkenal di dunia IT dan tulis analisis singkat | 3 menit |
| 6. Doa & salam | 2 menit |

---

## Asesmen

| Kriteria | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| Membedakan jenis testing | Tidak bisa | 2 jenis | 4 jenis | 5+ jenis + contoh |
| Debugging kode HTML | Tidak menemukan | 1 bug | 2–3 bug | Semua bug + perbaikan |
| Membuat test case | Tidak jadi | 1 skenario | 2–3 skenario | 4 skenario + lengkap |

---

**MGMP Informatika SMAN 6 Cimahi**
