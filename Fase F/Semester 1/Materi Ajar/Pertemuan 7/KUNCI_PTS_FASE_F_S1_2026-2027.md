# KUNCI JAWABAN & RUBRIK PTS
## Informatika Fase F – Semester 1 TP 2026/2027

---

## A. Pilihan Ganda

| No | Jawaban | Pembahasan |
|---|---|---|
| 1 | C | SDLC memiliki 7 tahapan: Planning, Analysis, Design, Implementation, Testing, Deployment, Maintenance |
| 2 | B | Wireframe & mockup dibuat di tahap Design/Perancangan |
| 3 | C | Perencanaan adalah tahap paling awal sebelum coding |
| 4 | B | Kebutuhan non-fungsional mengukur kualitas (kecepatan, keamanan) |
| 5 | B | Format: Sebagai [peran], saya ingin [fitur], agar [manfaat] |
| 6 | A | Wireframe sketsa hitam-putih, mockup sudah detail & warna |
| 7 | A | Konsistensi: elemen seragam di seluruh halaman |
| 8 | C | HTML/CSS/JS adalah teknologi frontend |
| 9 | B | `git commit` menyimpan snapshot kode |
| 10 | B | GitHub paling populer untuk hosting repositori Git |
| 11 | C | Unit Test menguji satu unit/komponen terkecil |
| 12 | B | Test negatif menguji input tidak valid |
| 13 | B | Debugging = proses mencari & memperbaiki bug |
| 14 | C | Production = lingkungan untuk user sungguhan |
| 15 | B | Continuous Integration / Continuous Deployment |
| 16 | C | Deployment = rilis ke produksi |
| 17 | B | Wawancara = tanya jawab langsung, detail mendalam |
| 18 | A | Mockup sudah warna & detail visual |
| 19 | D | MySQL adalah database, bukan frontend |
| 20 | C | git pull = unduh perubahan terbaru |
| 21 | B | Identifikasi → Reproduksi → Cari penyebab → Perbaiki → Verifikasi |
| 22 | C | System Test = menguji seluruh sistem end-to-end |
| 23 | A | Shared Hosting = satu server untuk banyak pengguna |
| 24 | D | Maintenance = perbaikan & update setelah rilis |
| 25 | C | Non-fungsional = kualitas (kecepatan, keamanan, dll) |

## B. Esai — Jawaban Contoh

### 16. 7 Tahapan SDLC
1. **Planning**: Tujuan, anggaran, jadwal
2. **Analysis**: Kebutuhan user dikumpulkan
3. **Design**: Wireframe, mockup, arsitektur
4. **Implementation**: Coding / development
5. **Testing**: Cari bug
6. **Deployment**: Rilis ke produksi
7. **Maintenance**: Perbaikan & update

### 17. User Story Aplikasi Perpustakaan
- "Sebagai **siswa**, saya ingin **mencari buku berdasarkan judul** agar **bisa menemukan buku yang saya butuhkan**"
- "Sebagai **petugas perpustakaan**, saya ingin **mencatat peminjaman buku** agar **data peminjaman tercatat dengan rapi**"

### 18. Prinsip Desain UI/UX
1. **Consistency**: Tampilan seragam
2. **Hierarchy**: Urutan informasi penting
3. **Feedback**: Respons saat user berinteraksi
4. **Affordance**: Bentuk menunjukkan fungsi
5. **Accessibility**: Dapat diakses semua orang
6. **Simplicity**: Sederhana, tidak membingungkan

### 19. 3 Layer Aplikasi
- **Frontend**: HTML, CSS, JavaScript (tampilan)
- **Backend**: Python, PHP, Node.js (logika)
- **Database**: MySQL, MongoDB (penyimpanan)

### 20. Test Case — Mencari Buku
| ID | Skenario | Input | Expected Result |
|---|---|---|---|
| TC-01 | Cari buku yang ada | "Laskar Pelangi" | Buku ditemukan, detail muncul |
| TC-02 | Cari buku tidak ada | "Buku XYZ" | "Buku tidak ditemukan" |
| TC-03 | Input kosong | (kosong) | "Masukkan kata kunci" |

### 21. Jenis Hosting

| Hosting | Kelebihan | Kekurangan |
|---|---|---|
| **Shared** | Murah | Sumber daya terbatas |
| **VPS** | Bisa atur sendiri | Butuh pengetahuan teknis |
| **Cloud** | Skalabel, andal | Bisa mahal |
| **Static** (Netlify/Vercel) | Gratis untuk frontend | Hanya untuk static site |

### 22. SDLC — Aplikasi Kantin Sekolah Online

| Tahap | Contoh |
|---|---|
| **Planning** | Tujuan: memesan makanan tanpa antre. Target: siswa & penjaga kantin |
| **Analysis** | Wawancara siswa: mau lihat menu + harga. Wawancara penjaga: mau catat pesanan otomatis |
| **Design** | Wireframe halaman menu, mockup tampilan pesan, user flow: pilih → bayar → ambil |
| **Implementation** | Coding frontend (HTML/CSS/JS) dan backend (Python) untuk proses pesanan |
| **Testing** | Unit test fungsi tambah menu, integration test: pilih menu → masuk keranjang |
| **Deployment** | Rilis di server sekolah, URL dibagikan ke siswa |
| **Maintenance** | Tambah fitur pembayaran QR, perbaiki bug jika ada error |

---

## Rubrik Penilaian (Revisi)

| No | Skor 4 (100%) | Skor 3 (75%) | Skor 2 (50%) | Skor 1 (25%) |
|---|---|---|---|---|
| 16 | 7 tahapan lengkap + penjelasan jelas | 5–6 tahapan benar | 3–4 tahapan | < 3 tahapan |
| 17 | 2 user story format benar + relevan | 2 user story format benar | 1 user story format benar | Tidak sesuai format |
| 18 | 4 prinsip + penjelasan | 3 prinsip + penjelasan | 2 prinsip | 1 prinsip |
| 19 | 3 layer + contoh teknologi | 3 layer, kurang contoh | 2 layer | 1 layer |
| 20 | 3 test case lengkap (ID, skenario, input, expected) | 3 test case kurang lengkap | 2 test case | 1 test case |
| 21 | 4 jenis hosting + kelebihan & kekurangan | 3 jenis hosting | 2 jenis | 1 jenis |
| 22 | 7 tahapan + contoh konkret semua tahap | 5-6 tahap + contoh | 3-4 tahap | < 3 tahap |

### Pedoman Nilai

| Komponen | Soal | Maks Skor |
|---|---|---|
| Pilihan Ganda | 1–25 | 60 (2,4 per soal) |
| Esai | 16 | 5 |
| Esai | 17 | 5 |
| Esai | 18 | 5 |
| Esai | 19 | 5 |
| Esai | 20 | 5 |
| Esai | 21 | 5 |
| Esai | 22 | 10 |
| **Total** | | **100** |

---

**MGMP Informatika SMAN 6 Cimahi**
