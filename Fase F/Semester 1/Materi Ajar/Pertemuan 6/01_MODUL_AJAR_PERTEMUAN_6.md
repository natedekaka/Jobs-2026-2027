# MODUL AJAR INFORMATIKA – FASE F (KELAS XI)

| Komponen | Deskripsi |
|---|---|
| **Mata Pelajaran** | Informatika |
| **Fase / Kelas** | F / XI |
| **Semester** | 1 (Ganjil) |
| **Pertemuan ke-** | 6 |
| **Alokasi Waktu** | 5 JP × 45 menit (225 menit) |
| **Tahun Pelajaran** | 2026/2027 |
| **Satuan Pendidikan** | SMA Negeri 6 Cimahi |

---

## Tujuan Pembelajaran

| TP | IKTP |
|---|---|
| **BK, AP:** Memahami tahap deployment dan CI/CD | 6.1 Menjelaskan konsep deployment |
| | 6.2 Membedakan hosting (shared, VPS, cloud) |
| | 6.3 Menjelaskan CI/CD sederhana |
| | 6.4 Melakukan deploy halaman HTML ke platform hosting gratis |

---

## Langkah Pembelajaran

### Pembukaan (15 menit)

| Kegiatan | Waktu |
|---|---|
| 1. Salam, doa, cek kehadiran | 2 menit |
| 2. **Review** & ice breaking: "Pert 5: Testing — temukan bug sebelum rilis. Hari ini: **Deployment** — bagaimana kode kita bisa diakses semua orang!" + tanya jawab singkat | 5 menit |
| 3. **Apersepsi** & motivasi: "Kode HTML yang kalian buat di Pert 4 — sejauh ini hanya bisa dibuka di komputer kalian sendiri. Bagaimana cara orang lain mengaksesnya?" + tayangkan contoh website live | 8 menit |

### Inti (175 menit)

#### Memahami (50 menit)

**1. Apa itu Deployment? (10 menit)**
- **Deployment**: Proses memindahkan aplikasi dari komputer developer ke server agar bisa diakses publik
- **Analogi**: "Kalian masak nasi goreng di dapur → ditaruh di piring → disajikan ke tamu" — deployment itu penyajiannya!
- **Server**: Komputer yang menyala 24/7 dan terhubung ke internet
- **Perbedaan**: Localhost (komputer sendiri) vs Production (server publik)
- **Tanya siswa**: "Website apa saja yang kalian akses hari ini? Di mana mereka di-host?"

**2. Jenis Hosting (15 menit)**

| Jenis | Analogi | Kelebihan | Kekurangan | Contoh |
|---|---|---|---|---|
| **Shared Hosting** | Kos-kosan (1 rumah dibagi) | Murah | Sumber daya terbatas | Hostinger, Niagahoster |
| **VPS** | Rumah sendiri | Bisa atur sendiri | Butuh pengetahuan teknis | DigitalOcean, Linode |
| **Cloud** | Hotel berbintang | Skalabel, andal | Bisa mahal | AWS, Google Cloud, Azure |
| **Static Hosting** | Pameran lukisan | Gratis untuk static site | Hanya untuk frontend | Netlify, Vercel, GitHub Pages |

- Bedah studi kasus: Website sekolah — hosting apa yang cocok? Mengapa?

**3. CI/CD — Continuous Integration / Continuous Deployment (10 menit)**

- **Masalah**: Manual deploy setiap ada perubahan → repot, rawan error
- **CI/CD**: Otomatisasi — setiap kali kode di-commit ke GitHub, otomatis di-test dan di-deploy

| Konsep | Arti | Analogi |
|---|---|---|
| **CI** | Setiap commit di-test otomatis | Cek kualitas di setiap gerbang |
| **CD** | Setelah lolos test → auto-deploy | Barang lolos QC langsung dikirim |

- Contoh nyata: Netlify auto-deploy dari GitHub

**4. Demo Bedah Website Live (15 menit)**
- Guru membuka 3-4 website nyata di browser
- Bedah bersama: perhatikan URL, https, kecepatan load, teknologi yang digunakan
- Gunakan **WhoIs** / **BuiltWith** untuk tebak teknologi hosting
- Gunakan **Network tab** di DevTools untuk lihat aset website
- Siswa menebak: hosting apa yang digunakan? Static atau dynamic?

#### Mengaplikasi (95 menit)

**5. Aktivitas 1 — Deploy HTML ke Netlify (25 menit) — Individu**
   - Buka netlify.com
   - Drag & drop folder HTML hasil Pert 4
   - Lihat website langsung online!
   - Catat URL yang diberikan Netlify
   - Ganti nama site (setting → site details → change site name)

**6. Aktivitas 2 — Setup GitHub Pages (25 menit) — Individu**
   - Buat repository baru di GitHub (jika belum punya akun, daftar dulu)
   - Upload file HTML dan CSS ke repository
   - Aktifkan GitHub Pages di Settings → Pages
   - Akses halaman live di `username.github.io/nama-repo`
   - Bandingkan: Netlify vs GitHub Pages — mana yang lebih mudah?

**7. Aktivitas 3 — Membuat Pipeline Sederhana (25 menit) — Berpasangan**
   - Buat diagram CI/CD di kertas A4/karton
   - Flow: `git push → auto-test → auto-build → auto-deploy → live`
   - Tambahkan keterangan teknologi yang digunakan di setiap tahap
   - Hias diagram agar menarik dan mudah dipahami

**8. Aktivitas 4 — Deploy Timeline & Presentasi (20 menit) — Berkelompok**
   - Siswa simulasi timeline deployment aplikasi sekolah:
     `Commit → CI test → Build → Deploy → User bisa akses`
   - Setiap kelompok mempresentasikan diagram CI/CD + hasil deploy
   - Guru memberikan umpan balik

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
| 4. Preview: "Pert 7: **PTS** — review pert 1–6" | 5 menit |
| 5. Tugas rumah: screenshot halaman yang sudah di-deploy + URL | 3 menit |
| 6. Doa & salam | 2 menit |

---

## Asesmen

| Kriteria | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| Memahami konsep deployment | Tidak bisa | Shared hosting | 3 jenis hosting | 4 jenis + perbandingan |
| Memahami CI/CD | Tidak bisa | CI saja | CI/CD | CI/CD + pipeline diagram |
| Deploy HTML ke Netlify | Tidak berhasil | Error | Berhasil | Berhasil + URL cantumkan |

---

**MGMP Informatika SMAN 6 Cimahi**
