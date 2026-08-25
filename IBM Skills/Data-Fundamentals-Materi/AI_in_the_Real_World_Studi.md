# AI in the Real World — Materi Belajar Offline

> Disusun dari materi IBM SkillsBuild (AI Fundamentals & study guide program JA SkillsBuild Jawa Barat). Dipakai sebagai bekal sambil menunggu platform kembali normal.

---

## 1. Apa itu AI?

> **Artificial Intelligence (AI)** = kemampuan mesin/komputer untuk melakukan tugas yang **biasanya membutuhkan kecerdasan manusia**.

Contoh tugas yang biasanya butuh kecerdasan manusia: mengenali wajah, memahami bahasa, membuat keputusan, mengenali gambar, dan belajar dari pengalaman.

**Kata kunci penting:** AI adalah mesin yang **belajar dari data**, bukan diprogram aturan satu per satu.

### 1.1 Jenis-Jenis AI (sering muncul di quiz)

| Jenis | Penjelasan | Contoh | Status |
|---|---|---|---|
| **Narrow AI** (AI Sempit) | Ahli di SATU tugas spesifik | Siri, Google Translate, Face ID, rekomendasi Netflix | ✅ Nyata sekarang |
| **General AI** (AI Umum) | Bisa semua tugas seperti manusia | — | ⏳ Masih riset |
| **Super AI** | Lebih cerdas dari manusia | — | 🎬 Hanya fiksi ilmiah |

**Poin penting:** Semua AI yang kita pakai sekarang adalah **Narrow AI**.

---

## 2. AI di Kehidupan Sehari-Hari

### 2.1 Di Rumah
- **Voice assistant** (Siri, Alexa, Google Assistant) — memahami perintah suara (NLP)
- **Rekomendasi video/musik** (YouTube, Spotify, Netflix) — machine learning menganalisis kebiasaan menonton
- **Smart TV / smart home** — mengenali perintah dan pola kebiasaan

### 2.2 Di Smartphone
- **Face ID / pengenalan wajah** (computer vision)
- **Keyboard prediktif** — memprediksi kata berikutnya yang akan kamu ketik
- **Google Lens** — mengenali objek dari foto
- **Fitur kamera AI** — mengenali pemandangan untuk menyetel kamera

### 2.3 Di Transportasi
- **Google Maps / Waze** — prediksi rute dan kemacetan dari data jutaan pengguna
- **Gojek/Grab** — AI untuk prediksi rute, estimasi tarif, dan pencocokan driver
- **Mobil self-driving** — menggabungkan computer vision (melihat) + ML (mengambil keputusan)
- **Deteksi kecelakaan** di beberapa mobil modern

### 2.4 Di Media Sosial & E-commerce
- **Feed algoritma** (Instagram, TikTok, Facebook) — memilih konten yang paling relevan
- **Chatbot customer service** — menjawab pertanyaan pelanggan otomatis
- **Rekomendasi produk** (Shopee, Tokopedia, Amazon) — "produk yang mungkin kamu suka"
- **Deteksi spam & konten berbahaya** — menyaring postingan otomatis

---

## 3. AI di Berbagai Industri

### 3.1 Kesehatan (Healthcare)
- **Diagnosis dari citra medis** — AI membaca foto rontgen/MRI untuk mendeteksi penyakit (mis. tumor)
- **Drug discovery** — mempercepat penemuan obat baru
- **Chatbot kesehatan** — menjawab pertanyaan gejala awal
- **AI membantu dokter** — menganalisis rekam medis, bukan menggantikan dokter

### 3.2 Pendidikan (Education)
- **Tutor AI** — pembelajaran adaptif sesuai kemampuan siswa
- **Grading otomatis** — menilai jawaban/esai
- **Chatbot untuk menjawab pertanyaan siswa**
- **Rencana pelajaran berbantuan AI** (mis. membantu guru membuat materi)

### 3.3 Keuangan & Perbankan (Finance)
- **Deteksi penipuan (fraud detection)** — menganalisis transaksi mencurigakan secara real-time
- **Penilaian kredit** — memprediksi risiko pinjaman
- **Chatbot perbankan** — layanan nasabah 24 jam
- **Trading algoritmik** — menganalisis pasar saham

### 3.4 Ritel & E-commerce
- **Rekomendasi produk** — personalisasi belanja
- **Manajemen stok/inventaris** — prediksi permintaan barang
- **Optimasi harga** — menyesuaikan harga secara dinamis
- **Analisis ulasan pelanggan** — sentiment analysis

### 3.5 Manufaktur & Industri
- **Predictive maintenance** — memprediksi mesin akan rusak sebelum rusak
- **Quality control** — computer vision memeriksa cacat produk di jalur produksi
- **Robotika** — robot yang belajar menyelesaikan tugas
- **Optimasi rantai pasok (supply chain)**

### 3.6 Pemerintahan & Publik
- **Analisis data untuk kebijakan publik**
- **Pengenalan wajah** untuk keamanan (dengan pertimbangan etika)
- **Chatbot layanan publik** (mis. layanan informasi)

---

## 4. Bagaimana AI Bekerja di Dunia Nyata

### 4.1 Alur Umum Sistem AI
```
Data (kumpulan contoh)  →  Model (belajar pola)  →  Inference (prediksi baru)
```

- **Data** = buku pelajaran AI
- **Model** = hasil pemahaman AI setelah belajar dari data
- **Inference** = AI menjawab pertanyaan baru menggunakan pemahamannya

### 4.2 Tiga Cara AI Belajar (wajib hafal)
1. **Supervised Learning** — belajar dari data **berlabel** (sudah ada jawabannya). Contoh: prediksi harga rumah.
2. **Unsupervised Learning** — belajar dari data **tanpa label**, mencari pola sendiri. Contoh: segmentasi pelanggan.
3. **Reinforcement Learning** — belajar dari **trial & error** dengan reward/penalty. Contoh: AI bermain catur.

### 4.3 Cabang Utama AI di Dunia Nyata

| Cabang | Memproses | Contoh Nyata |
|---|---|---|
| **NLP** (Natural Language Processing) | Bahasa/teks/suara | Chatbot, Siri, Google Translate, sentiment analysis |
| **Computer Vision** | Gambar/video | Face ID, self-driving, medical imaging |
| **Generative AI** | Membuat konten baru | ChatGPT (teks), DALL-E (gambar), IBM Granite |

---

## 5. Contoh Kasus Nyata IBM & Dunia

- **Scuderia Ferrari F1** — AI menganalisis data balapan untuk performa mobil & pengalaman penonton.
- **Gojek/Grab** — prediksi rute & estimasi waktu kedatangan dengan ML.
- **ChatGPT / IBM Granite** — generative AI untuk membuat teks.
- **AI di bank** — mendeteksi transaksi palsu dalam hitungan detik.
- **AI di sekolah** — rekomendasi materi sesuai kemampuan tiap siswa.

---

## 6. Etika AI di Dunia Nyata

### 6.1 Bias (prasangka)
- AI bisa **bias** jika data latihan tidak representatif
- Contoh: sistem rekrutmen yang lebih memilih satu kelompok karena data historis
- Solusi: pastikan data latihan beragam dan adil

### 6.2 Prinsip AI yang Bertanggung Jawab
- **Fairness** (keadilan) — tidak diskriminatif
- **Transparency** (transparansi) — bagaimana AI mengambil keputusan bisa dijelaskan
- **Accountability** (akuntabilitas) — ada yang bertanggung jawab atas dampak AI
- **Privacy** (privasi) — melindungi data pribadi pengguna

### 6.3 Yang Perlu Diingat
- AI adalah **alat bantu manusia**, bukan pengganti keputusan manusia
- Keputusan penting tetap butuh penilaian manusia
- Pengembang dan pengguna AI punya tanggung jawab atas dampaknya

---

## 7. Dampak AI terhadap Dunia Kerja

### 7.1 Peluang Karir di Bidang AI
- **AI Engineer** — membangun sistem AI
- **Data Scientist** — menganalisis data untuk wawasan bisnis
- **Machine Learning Engineer** — membangun & melatih model ML
- **AI Product Manager** — mengelola produk berbasis AI
- **AI Ethics Officer** — memastikan AI dipakai secara bertanggung jawab

### 7.2 Dampak Pekerjaan
- Beberapa tugas rutin akan **terotomasi** (diambil alih AI)
- Muncul **pekerjaan baru** yang belum ada sebelumnya
- 85% pekerjaan di 2030 mungkin belum ada sekarang
- Skill AI = skill yang dibutuhkan semua perusahaan

---

## 8. Cara Menggunakan AI Secara Bijak (untuk Guru & Siswa)

1. **Gunakan sebagai asisten, bukan pengganti berpikir** — AI membantu, manusia yang menilai.
2. **Periksa hasil AI** — AI bisa salah/halusinasi, cek ulang fakta.
3. **Jaga privasi** — jangan masukkan data pribadi siswa ke AI publik.
4. **Beri prompt yang jelas** — hasil AI bagus tergantung instruksi yang spesifik.
5. **Gunakan etis di kelas** — ajarkan siswa kapan dan bagaimana AI boleh dipakai.

---

## 9. Ringkasan Cepat (untuk dipelajari sebelum quiz)

- **AI** = mesin yang meniru kecerdasan manusia, belajar dari data.
- Semua AI sekarang = **Narrow AI** (spesialis satu tugas).
- AI dipakai di: rumah, HP, transportasi, medsos, kesehatan, pendidikan, keuangan, industri, pemerintahan.
- **NLP** = memahami bahasa; **Computer Vision** = melihat gambar; **Generative AI** = membuat konten baru.
- AI belajar 3 cara: **Supervised** (berlabel), **Unsupervised** (tanpa label), **Reinforcement** (coba-coba + hadiah).
- AI bisa **bias** jika datanya tidak adil → butuh etika: fairness, transparency, accountability.
- AI menciptakan **karir baru** dan mengubah cara kerja semua industri.

**Trik jawaban quiz IBM:**
- Soal "yang PALING TEPAT" → pilih jawaban paling lengkap/spesifik.
- Pilihan yang memakai kata "selalu/pasti/tidak pernah" → biasanya salah (AI itu probabilitas).
- Soal "BUKAN contoh X" → cari satu pilihan yang aneh/tidak relevan.