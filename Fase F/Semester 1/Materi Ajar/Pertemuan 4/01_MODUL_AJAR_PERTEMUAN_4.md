# MODUL AJAR INFORMATIKA – FASE F (KELAS XI)

| Komponen | Deskripsi |
|---|---|
| **Mata Pelajaran** | Informatika |
| **Fase / Kelas** | F / XI |
| **Semester** | 1 (Ganjil) |
| **Pertemuan ke-** | 4 |
| **Alokasi Waktu** | 5 JP × 45 menit (225 menit) |
| **Tahun Pelajaran** | 2026/2027 |
| **Satuan Pendidikan** | SMA Negeri 6 Cimahi |

---

## Tujuan Pembelajaran

| TP | IKTP |
|---|---|
| **BK, AP:** Memahami tahap implementasi/development | 4.1 Menjelaskan proses translasi desain ke kode |
| | 4.2 Menjelaskan konsep version control (Git) |
| | 4.3 Mengenal teknologi yang umum digunakan (frontend, backend, database) |
| | 4.4 Membuat halaman HTML/CSS sederhana dari wireframe |

---

## Langkah Pembelajaran

### Pembukaan (15 menit)

| Kegiatan | Waktu |
|---|---|
| 1. Salam, doa, cek kehadiran | 2 menit |
| 2. **Review** & ice breaking: "Pert 1: SDLC. Pert 2: Analisis Kebutuhan. Pert 3: Design (wireframe). Hari ini: tahap **Implementation** — kode!" + tanya jawab singkat | 5 menit |
| 3. **Apersepsi** & motivasi: "Wireframe yang kalian buat di pert 3 — bagaimana cara mengubahnya menjadi aplikasi nyata? Jawabannya: **coding!**" + tayangkan contoh hasil akhir aplikasi | 8 menit |

### Inti (175 menit)

#### Memahami (50 menit)

**1. Dari Wireframe ke Kode (10 menit)**

| Wireframe | → | Frontend (HTML/CSS/JS) | Contoh Kode |
|---|---|---|---|
| Kotak header | → | `<header>` | `<header><h1>Aplikasi Sekolah</h1></header>` |
| Tombol | → | `<button>` | `<button>Login</button>` |
| Form input | → | `<input>` | `<input type="text" placeholder="NISN">` |
| Warna & font | → | CSS (`color`, `font-family`) | `color: blue; font-family: Arial;` |

- Demo langsung: Guru menunjuk elemen wireframe, siswa menyebutkan padanan HTML-nya
- Contoh tambahan: navigasi (`<nav>`), footer (`<footer>`), gambar (`<img>`)

**2. Frontend, Backend, Database (10 menit)**

| Layer | Fungsi | Teknologi | Contoh Kasus |
|---|---|---|---|
| **Frontend** | Tampilan — apa yang dilihat user | HTML, CSS, JavaScript | Form login, dashboard nilai |
| **Backend** | Logika — proses data | Python, PHP, Node.js | Validasi login, hitung rata-rata nilai |
| **Database** | Penyimpanan — simpan data | MySQL, PostgreSQL | Tabel siswa, tabel nilai |

- Analogi restoran: Frontend = menu & meja, Backend = dapur, Database = kulkas penyimpanan
- Tanya siswa: "Apa contoh frontend/backend/database dari aplikasi yang kalian pakai sehari-hari?"

**3. Version Control — Git (15 menit)**
- **Masalah**: "Kode berantakan, timpak-timpakan file, tidak tahu siapa yang mengubah apa"
- **Solusi**: Git — melacak setiap perubahan kode
- **Konsep Git:**
  - **Repository (repo)**: folder proyek
  - **Commit**: "save point" — simpan snapshot kode
  - **Push**: upload ke server (GitHub)
  - **Pull**: download dari server
- **Demo live**: Guru buka terminal, jalankan `git init`, `git add`, `git commit`, `git log`
- Tampilkan visualisasi Git graph di layar

**4. Live Coding Demo (15 menit)**
- Guru membuka VS Code dan wireframe dari Pertemuan 3
- Demonstrasi langsung: wireframe → kode HTML/CSS
- Siswa mengamati dan mencatat langkah-langkahnya
- Fokus: bagaimana setiap elemen wireframe diterjemahkan ke tag HTML
- Hasil akhir: halaman login sederhana yang bisa dibuka di browser

#### Mengaplikasi (95 menit)

**5. Aktivitas 1 — Membuat Halaman HTML Sederhana (30 menit) — Individu**
   - Gunakan teks editor (VS Code / Notepad / Google Colab untuk HTML)
   - Buat halaman HTML sederhana dari wireframe login yang dibuat di Pert 3
   - Elemen: judul, form input (NISN, password), tombol submit
   - Tambahkan CSS sederhana (warna background, font, padding)
   - Guru berkeliling membantu siswa yang kesulitan

**6. Aktivitas 2 — Git Command Line (25 menit) — Berpasangan**
   - Buka terminal/command prompt
   - Praktikkan perintah Git dasar:
     - `git init` — buat repository lokal
     - `git add .` — staging file
     - `git commit -m "pesan"` — commit pertama
     - `git log --oneline` — lihat riwayat
   - Setiap pasangan membuat 3 commit dengan pesan berbeda
   - Catat perbedaan sebelum dan sesudah commit

**7. Aktivitas 3 — Eksplorasi GitHub (20 menit) — Berpasangan**
   - Buka github.com
   - Cari repository "informatika-sma" atau repositori populer
   - Identifikasi: siapa yang berkontribusi? apa saja file-nya?
   - Amati tab: Code, Issues, Pull Requests, Actions
   - Diskusikan: mengapa GitHub penting untuk kolaborasi?

**8. Aktivitas 4 — Git Simulation (20 menit) — Berkelompok (4-5 siswa)**
   - Simulasi Git tanpa komputer: "Kita akan edit dokumen bersama-sama"
   - 3-4 siswa jadi "developer", 1 siswa jadi "Git" yang mencatat versi
   - Setiap "developer" mengusulkan perubahan, "Git" mencatatnya sebagai commit
   - Giliran berganti agar semua siswa merasakan peran yang berbeda

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
| 4. Preview: "Pert 5: Pengujian (Testing) & Debugging — pastikan kode tidak error" | 5 menit |
| 5. Tugas rumah: Sempurnakan halaman HTML — tambah CSS sederhana (warna, font) | 3 menit |
| 6. Doa & salam | 2 menit |

---

## Asesmen

| Kriteria | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| Memahami frontend/backend/database | Tidak bisa | 1 layer | 2 layer | 3 layer + fungsi |
| Membuat HTML dari wireframe | Tidak jadi | Struktur salah | Struktur benar | Rapi + CSS |
| Memahami Git (simulasi) | Tidak ikut | Ikut pasif | Aktif | Aktif + jelaskan |

---

**MGMP Informatika SMAN 6 Cimahi**
