# Panduan Belajar Detail — IBM SkillsBuild untuk Guru

> Dokumen pendamping study guide. Fokus: pemahaman mendalam (bukan sekadar hafalan) + cara cepat menyelesaikan LMS.
> Dibuat untuk: Bapak/Ibu guru peserta ToT IBM SkillsBuild Jawa Barat.

---

## DAFTAR ISI

1. [Cara Kerja LMS dari A-Z](#1-cara-kerja-lms-dari-a-z)
2. [Konsep Inti 1: AI — Apa Sebenarnya?](#2-konsep-inti-1-ai--apa-sebenarnya)
3. [Konsep Inti 2: Machine Learning — Cara AI Belajar](#3-konsep-inti-2-machine-learning--cara-ai-belajar)
4. [Konsep Inti 3: Deep Learning & Neural Network](#4-konsep-inti-3-deep-learning--neural-network)
5. [Konsep Inti 4: NLP & Computer Vision](#5-konsep-inti-4-nlp--computer-vision)
6. [Konsep Inti 5: Prompt Engineering](#6-konsep-inti-5-prompt-engineering)
7. [Konsep Inti 6: Etika AI](#7-konsep-inti-6-etika-ai)
8. [Hands-on: Watson Studio](#8-hands-on-watson-studio)
9. [Bank Soal Latihan + Pembahasan](#9-bank-soal-latihan--pembahasan)
10. [Checklist Pengerjaan LMS](#10-checklist-pengerjaan-lms)

---

## 1. Cara Kerja LMS dari A-Z

### 1.1 Struktur Satu Kursus (pahami ini dulu)

Setiap kursus di IBM SkillsBuild selalu berbentuk sama:

```
KURSUS
├── Modul 1
│   ├── Sub-topik 1.1   (video / teks / aktivitas)
│   ├── Sub-topik 1.2
│   ├── Sub-topik 1.3
│   └── Quiz Modul 1    ← hanya terbuka jika semua sub-topik sudah dicentang
├── Modul 2
│   └── ...
└── Assessment Akhir    ← untuk dapat badge
```

**Inti dari semuanya:** Progress bar di LMS tidak naik otomatis. Anda harus **centang "I have checked it out"** di setiap sub-topik setelah selesai membaca/menonton.

### 1.2 Langkah Lengkap Menyelesaikan Satu Kursus

| Tahap | Yang Anda Lakukan | Catatan |
|---|---|---|
| 1. Enroll | Cari kursus di Learning Catalog → klik **Enroll** | Kursus masuk ke "Your Learning" |
| 2. Buka | Klik judul kursus di dashboard → **Go to Activity** | Tunggu loading |
| 3. Baca | Baca materi / tonton video di sub-topik | Pahami, bukan hanya scroll |
| 4. Centang | Centang **"I have checked it out"** | Progress bar naik |
| 5. Ulangi | Lakukan untuk semua sub-topik | Panel kiri: topik selesai ditandai ✓ |
| 6. Quiz | Klik Quiz modul → Start Quiz → jawab → Submit | Bisa diulang jika belum lulus |
| 7. Assessment akhir | Kerjakan setelah semua modul selesai | Nilai ≥ batas minimum = lulus |
| 8. Badge | Badge otomatis masuk ke profil | Tunggu 24–48 jam, cek email |

### 1.3 Aturan Emas Menghindari Kesalahan Umum

1. **Jangan langsung klik Quiz** sebelum semua sub-topik dicentang — quiz tidak akan muncul.
2. **Video wajib ditonton** sampai habis (atau setidaknya sampai tombol centang aktif).
3. Jika progress tidak bertambah → penyebabnya 99% sub-topik belum dicentang.
4. Kerjakan quiz di browser **Chrome**, matikan ad blocker.
5. Simpan jawaban benar di catatan — soal sering diulang dengan kata-kata berbeda.

### 1.4 Ciri Jawaban Quiz AI (pola umum)

IBM menggunakan **satu jawaban paling tepat**, bukan semua yang benar. Trik membacanya:

- Soal bertanya "yang **PALING TEPAT**" → pilih jawaban paling lengkap/paling spesifik.
- Soal bertanya "yang **BUKAN** contoh X" → cari satu pilihan yang aneh/tidak relevan.
- Kata kunci soal sering memakai istilah resmi: *supervised*, *labeled*, *training data*, *inference*.
- Pilihan jawaban yang memakai kata "selalu", "tidak pernah", "pasti" → biasanya **salah** (AI itu probabilitas, bukan kepastian).

---

## 2. Konsep Inti 1: AI — Apa Sebenarnya?

### 2.1 Definisi yang Harus Anda Hafal (kata demi kata)

> **Artificial Intelligence (AI)** = kemampuan mesin/komputer untuk melakukan tugas yang **biasanya membutuhkan kecerdasan manusia**.

Contoh tugas yang "biasanya butuh kecerdasan manusia": mengenali wajah, memahami bahasa, membuat keputusan, mengenali gambar.

### 2.2 Analogi: AI seperti murid yang belajar

- **AI** = murid (sistem yang bisa belajar dan berpikir).
- **Data** = buku pelajaran (bahan yang dipelajari).
- **Model** = hasil pemahaman murid setelah belajar (representasi pola dari data).
- **Inference/prediksi** = murid menjawab soal baru menggunakan pemahamannya.
- **Training** = proses belajar itu sendiri.

### 2.3 Jenis-jenis AI (sering muncul di quiz)

| Jenis | Penjelasan | Contoh | Status |
|---|---|---|---|
| **Narrow AI** (AI Sempit) | Ahli di SATU tugas spesifik | Siri, Google Translate, Face ID | ✅ Nyata sekarang |
| **General AI** (AI Umum) | Bisa semua tugas seperti manusia | — | ⏳ Masih riset |
| **Super AI** | Lebih cerdas dari manusia | — | 🎬 Hanya fiksi ilmiah |

**Poin penting:** Semua AI yang Anda pakai sekarang adalah **Narrow AI**.

### 2.4 Tipe Data (muncul di Modul 1)

| Tipe | Arti | Contoh |
|---|---|---|
| **Structured** | Rapi, dalam tabel, punya kolom & baris | Spreadsheet, database |
| **Unstructured** | Tidak rapi, bebas | Foto, video, teks bebas, suara |
| **Semi-structured** | Campuran | Email (ada header + isi bebas), JSON |

---

## 3. Konsep Inti 2: Machine Learning — Cara AI Belajar

### 3.1 Definisi Hafalan

> **Machine Learning (ML)** = subset AI di mana mesin **belajar dari data tanpa diprogram secara eksplisit**.

Artinya: kita tidak menulis aturan "jika X maka Y". Kita memberi **contoh/contoh data**, dan mesin menemukan pola sendiri.

**Analogi: mengajar anak mengenali kucing**
- Cara lama (pemrograman biasa): Anda menulis 100 aturan "punya ekor = kucing, punya kumis = kucing..." — rumit dan gagal di kasus aneh.
- Cara ML: Anda tunjukkan 1000 foto yang sudah diberi label "kucing" dan "bukan kucing". Anak belajar sendiri polanya, dan bisa mengenali kucing baru yang belum pernah dilihat.

### 3.2 Tiga Jenis Machine Learning (WAJIB HAFAL — sering keluar di quiz & post-test)

#### A. Supervised Learning (Belajar dengan Bimbingan)
- Data **BERLABEL** (sudah tahu jawabannya).
- AI dilatih melihat (input → jawaban yang benar), lalu belajar.
- **Contoh:** foto hewan yang sudah ditandai "kucing"/"anjing" → AI belajar membedakan.
- **Tugas:** klasifikasi & prediksi (misal: prediksi harga rumah dari dataset rumah + harga).

#### B. Unsupervised Learning (Belajar Tanpa Bimbingan)
- Data **TANPA LABEL** (tidak diberi tahu jawabannya).
- AI mencari pola/kelompok sendiri.
- **Contoh:** data pelanggan tanpa keterangan → AI mengelompokkan pelanggan mirip secara otomatis (segmentasi pasar).
- **Tugas:** clustering (pengelompokan).

#### C. Reinforcement Learning (Belajar dari Trial & Error)
- AI beraksi, dapat **reward** (hadiah) untuk aksi baik dan **penalty** (hukuman) untuk aksi buruk.
- **Contoh:** AI bermain catur, robot belajar berjalan, AI bermain game.
- Belajar dari konsekuensi, seperti melatih hewan.

### 3.3 Cara Mengingat Cepat (mnemonik)

> **"SUR"** = Supervised pake label, Unsupervised nggak pake label, **R**einforcement coba-coba dapet hadiah.

| Jenis | Label? | Belajar dari? | Contoh soal quiz |
|---|---|---|---|
| Supervised | Ya | Jawaban yang benar | Dataset rumah + harga |
| Unsupervised | Tidak | Pola di data | Kelompokkan pelanggan |
| Reinforcement | — | Reward & penalty | AI bermain catur |

### 3.4 Istilah Penting (sering jadi pilihan jawaban quiz)

- **Label** = jawaban/jenis yang benar dari data (misal: "kucing").
- **Feature/fitur** = ciri-ciri data (misal: berat, tinggi, warna).
- **Training set** = data untuk belajar.
- **Test set** = data untuk menguji (tidak dipakai saat belajar).
- **Overfitting** = model terlalu hafal data latih sampai gagal di data baru (hafalan, bukan paham).
- **Accuracy** = persentase prediksi benar.

---

## 4. Konsep Inti 3: Deep Learning & Neural Network

### 4.1 Neural Network (Jaringan Saraf Tiruan)

> Sistem yang **meniru cara kerja otak manusia**: terdiri dari neuron (sel syaraf buatan) yang saling terhubung.

```
INPUT  →  HIDDEN LAYER(S)  →  OUTPUT
(Data)     (Proses/belajar)    (Hasil/prediksi)
```

- **Input layer**: data masuk.
- **Hidden layer(s)**: lapisan tersembunyi tempat proses belajar terjadi.
- **Output layer**: hasil (misal: "ini kucing").

**Analogi:** seperti banyak siswa saling berbisik. Siswa pertama terima gambar, tiap siswa mengolah sedikit informasi, sampai siswa terakhir menyimpulkan "kucing".

### 4.2 Deep Learning (Pembelajaran Mendalam)

> **Deep Learning** = neural network dengan **BANYAK hidden layer** (dalam).

- Makin banyak layer → makin mampu mengenali pola rumit.
- Butuh data sangat banyak & daya komputasi besar.
- **Contoh aplikasi:** Face ID, Google Translate, deteksi penyakit dari foto medis, mobil self-driving.

### 4.3 Hubungan AI → ML → DL (pasti keluar di quiz)

```
AI (paling luas)
 └── Machine Learning (bagian dari AI)
      └── Deep Learning (bagian dari ML, pakai neural network dalam)
```

**Contoh soal khas:** "Manakah urutan yang benar dari konsep paling luas ke paling sempit?"
→ **AI → Machine Learning → Deep Learning**

---

## 5. Konsep Inti 4: NLP & Computer Vision

### 5.1 NLP (Natural Language Processing)

> Cabang AI yang memungkinkan mesin **memahami, menginterpretasi, dan menghasilkan bahasa manusia**.

**Analogi:** seperti penerjemah yang mendengarkan bahasa Indonesia dan mengubahnya menjadi bahasa Inggris.

**Aplikasi nyata:**
- Chatbot customer service
- Voice assistant (Siri, Alexa, Google Assistant)
- Google Translate
- **Sentiment analysis** — menganalisis apakah ulasan berbau positif/negatif

**Kepanjangan hafalan:** NLP = **N**atural **L**anguage **P**rocessing (bukan New Learning Program, bukan Network Language Protocol).

### 5.2 Computer Vision

> Cabang AI yang memungkinkan mesin **"melihat" dan memahami gambar/video**.

**Analogi:** seperti dokter membaca hasil rontgen — mesin "melihat" gambar lalu menafsirkannya.

**Aplikasi nyata:**
- Face ID (pengenalan wajah)
- Object detection (deteksi objek)
- Mobil self-driving
- Medical imaging (membaca foto medis)

### 5.3 Tabel Perbedaan Cepat

| Cabang | Diproses | Contoh |
|---|---|---|
| NLP | Bahasa/teks/suara | Chatbot, translate |
| Computer Vision | Gambar/video | Face ID, self-driving |
| Generative AI | Membuat konten baru | ChatGPT (teks), DALL-E (gambar) |

---

## 6. Konsep Inti 5: Prompt Engineering

### 6.1 Definisi

> **Prompt** = instruksi/perintah yang Anda berikan ke AI.
> **Prompt Engineering** = seni menyusun instruksi agar AI memberi jawaban yang Anda inginkan.

**Analogi:** seperti memberi tugas ke asisten. Perintah "tolong buatkan materi" hasilnya umum dan berantakan. Perintah yang jelas, spesifik, dengan format & target → hasilnya langsung bagus.

### 6.2 Perbandingan Prompt Buruk vs Baik

| | Prompt Buruk | Prompt Baik |
|---|---|---|
| Teks | "Buatkan cerita" | "Buatkan cerita pendek tentang petualangan anak di hutan, gaya bahasa menarik untuk siswa SMP, sekitar 500 kata" |
| Masalah | Hasil umum, tidak sesuai target | Hasil sesuai target & bisa langsung dipakai |

### 6.3 Formula Prompt Efektif (ingat 5 W + H versi AI)

Prompt yang bagus mengandung informasi:

1. **Tugas** — apa yang diminta (buatkan/minta/jelaskan)
2. **Topik** — tentang apa
3. **Target audiens** — untuk siapa (siswa kelas X, guru, umum)
4. **Format** — bentuk hasil (tabel, paragraf, soal PG, RPP)
5. **Detail tambahan** — jumlah kata, tingkat kesulitan, gaya bahasa, batasan

### 6.4 Contoh Prompt Siap Pakai untuk Guru

**Buat RPP:**
> "Buatkan rencana pelajaran Informatika kelas X SMA tentang Pengenalan AI, durasi 2 x 45 menit, Kurikulum Merdeka, metode diskusi dan hands-on. Sertakan tujuan, materi, kegiatan, dan asesmen."

**Buat soal:**
> "Buatkan 10 soal pilihan ganda tentang Machine Learning untuk siswa kelas XI SMA/SMK, tingkat sedang, sertakan kunci jawaban dan pembahasan."

**Buat materi ajar:**
> "Buatkan materi ajar NLP untuk siswa kelas X SMA, bahasa sederhana, pakai analogi sehari-hari, lengkap dengan contoh aplikasi nyata."

### 6.5 Tips Jitu Berprompt

- Mulai dengan kata kerja jelas: *buatkan, ringkas, ubah, jelaskan, terjemahkan*.
- Beri batasan agar hasil tidak melebar: *"maksimal 500 kata", "dalam 5 poin", "untuk siswa SMA"*.
- Jika hasil kurang pas → **perbaiki prompt, jangan ganti topik**. Tambah detail.
- Prompt mengulang = instruksi lanjutan yang mempertajam hasil.

---

## 7. Konsep Inti 6: Etika AI

### 7.1 Mengapa Etika Penting?

AI memengaruhi kehidupan nyata. Tanpa etika, AI bisa memperbesar ketidakadilan, melanggar privasi, dan digunakan untuk hal merugikan.

### 7.2 Tiga Pilar Etika AI (WAJIB HAFAL)

| Pilar | Arti | Contoh masalah |
|---|---|---|
| **Fairness** (Keadilan) | AI adil untuk semua, tidak diskriminatif | AI pinjaman bank menolak kelompok tertentu |
| **Transparency** (Transparansi) | Cara kerja AI bisa dijelaskan; pengguna tahu sedang berinteraksi dengan AI | Chatbot harus bilang "saya bot", bukan pura-pura manusia |
| **Accountability** (Akuntabilitas) | Ada yang bertanggung jawab atas keputusan AI | Siapa bertanggung jawab jika mobil self-driving kecelakaan? |

### 7.3 Bias dalam AI (sering jadi kasus di quiz)

**Kasus terkenal:** AI rekrutmen Amazon tidak adil terhadap pelamar perempuan.
**Penyebab:** data training didominasi resume laki-laki → AI belajar pola dari data yang sudah bias.

**Kunci pemahaman:** **AI mewarisi bias dari data training.** AI tidak "jahat", tapi data yang mewakili sebagian kelompok membuat hasil tidak adil.

### 7.4 Cara Mencegah Bias (jawaban untuk soal essay)

1. Gunakan data training yang **representatif** (mewakili semua kelompok).
2. **Audit** model secara berkala.
3. Libatkan **tim beragam** dalam pengembangan.
4. **Transparan** soal keterbatasan AI.

### 7.5 Kasus Etika Lain

- **Deepfake** — video palsu untuk penipuan & misinformasi.
- **Privasi data** — AI butuh banyak data; data pribadi harus dilindungi, pengguna harus tahu datanya dipakai untuk apa.

---

## 8. Hands-on: Watson Studio

### 8.1 Apa Itu Watson Studio

Platform cloud IBM untuk membuat, melatih, dan mengevaluasi model ML tanpa perlu coding berat. Mirip "dapur" tempat Anda memasak model dari bahan (data).

### 8.2 Alur Kerja Standar (hafal urutannya)

```
1. SIAPKAN DATA  → upload dataset (misal: iris bunga)
2. PILIH MODEL    → pilih algoritma (Decision Tree, Random Forest)
3. TRAINING       → bagi data: training set & test set, lalu latih
4. EVALUASI       → uji dengan test set, lihat accuracy
5. DEPLOY         → gunakan model untuk prediksi data baru
```

### 8.3 Dataset Klasik untuk Praktik

| Dataset | Tugas |
|---|---|
| **Iris** | Klasifikasi 3 jenis bunga dari ukuran kelopak |
| **Titanic** | Prediksi penumpang selamat/tidak |
| **Housing** | Prediksi harga rumah |

### 8.4 Konsep yang Diuji di Quiz Watson Studio

- **Decision Tree** = model berbentuk percabangan keputusan (ya/tidak), mudah dipahami.
- **Random Forest** = kumpulan banyak decision tree, hasilnya dirata-rata → lebih akurat.
- **Training vs Test set** — training untuk belajar, test untuk menguji model yang belum pernah melihat data itu.
- Model kurang akurat → tambah data training, atau coba algoritma lain.
- Data harus format **CSV**, bersih (tidak ada karakter aneh).

---

## 9. Bank Soal Latihan + Pembahasan

### A. Pilihan Ganda — Coba jawab dulu, baru lihat pembahasannya

**1. Apa itu AI?**
- a) Software pengedit foto
- b) Kemampuan mesin meniru kecerdasan manusia ✅
- c) Bahasa pemrograman
- d) Sistem operasi

**Pembahasan:** Definisi baku. Yang lain adalah contoh alat, bukan definisi.

**2. Manakah yang BUKAN contoh penerapan AI?**
- a) Siri
- b) Google Translate
- c) Microsoft Word ✅
- d) Face ID

**Pembahasan:** Word adalah program pengolah kata biasa tanpa kecerdasan (AI-nya di versi baru bernama Copilot, tapi soal ini menguji Word lama sebagai "bukan AI").

**3. Jenis ML yang menggunakan data berlabel?**
- a) Unsupervised
- b) Reinforcement
- c) Supervised ✅
- d) Deep Learning

**Pembahasan:** Label = jawaban sudah diketahui. Itu ciri supervised.

**4. NLP singkatan dari...**
- a) Natural Language Processing ✅
- b) New Learning Program
- c) Network Language Protocol
- d) Neural Learning Process

**Pembahasan:** Hafalkan kepanjangan yang benar; opsi b–d adalah jebakan.

**5. "Bias" dalam AI artinya...**
- a) Kecepatan komputer
- b) Ketidakadilan dalam hasil AI ✅
- c) Ukuran model
- d) Jumlah data

**Pembahasan:** Bias = hasil tidak adil akibat data training yang tidak representatif.

**6. Urutan konsep dari paling luas ke paling sempit:**
- a) Deep Learning → ML → AI
- b) ML → AI → Deep Learning
- c) AI → ML → Deep Learning ✅
- d) AI → Deep Learning → ML

**Pembahasan:** AI wadah terbesar, ML di dalamnya, DL bagian dari ML.

**7. Siri, Alexa, Google Assistant termasuk jenis AI...**
- a) General AI
- b) Narrow AI ✅
- c) Super AI
- d) Semi AI

**Pembahasan:** Ahli satu tugas = Narrow AI.

**8. Dataset dengan kolom & baris rapi termasuk data...**
- a) Unstructured
- b) Semi-structured
- c) Structured ✅
- d) Raw

**Pembahasan:** Tabel/spreadsheet = structured.

**9. AI belajar dari reward & penalty termasuk ML jenis...**
- a) Supervised
- b) Unsupervised
- c) Reinforcement ✅
- d) Semi-supervised

**Pembahasan:** Reward/penalty = reinforcement.

**10. Tujuan utama evaluasi model dengan test set adalah...**
- a) Membuat data lebih banyak
- b) Menguji model pada data yang belum pernah dilihat ✅
- c) Menambah label
- d) Mempercepat training

**Pembahasan:** Test set = ujian pertama model pada data baru.

**11. Deep Learning berbeda dari ML biasa karena...**
- a) Tidak butuh data
- b) Memakai neural network dengan banyak layer ✅
- c) Tidak memakai komputer
- d) Hanya untuk gambar

**Pembahasan:** Ciri khas deep learning = banyak hidden layer.

**12. Jika hasil prediksi model tidak akurat, langkah pertama terbaik:**
- a) Hapus semua data
- b) Tambah data training / coba algoritma lain ✅
- c) Menyerah
- d) Memakai data yang sama

**Pembahasan:** Data lebih banyak & algoritma lain = perbaikan standar.

### B. Soal Essay — Kerangka Jawaban

**1. Jelaskan perbedaan AI, ML, dan Deep Learning!**
Kerangka: AI (umum, meniru kecerdasan) → ML (belajar dari data) → DL (ML dengan neural network berlapis banyak). Contoh nyata masing-masing.

**2. 3 contoh penerapan AI di pendidikan!**
Kerangka: (1) Chatbot bantu siswa, (2) AI membuat soal/RPP (prompt), (3) analisis hasil belajar siswa, (4) aplikasi belajar adaptif. Pilih 3 dan jelaskan singkat.

**3. Mengapa etika AI penting? Beri contoh!**
Kerangka: Dampak nyata ke manusia → jelaskan fairness/transparency/accountability → contoh kasus (bias rekrutmen Amazon, deepfake, privasi).

**4. Jelaskan cara kerja neural network dengan analogi!**
Kerangka: input (data) → hidden layer (proses) → output (hasil). Analogi siswa berbisik / menyortir surat di kantor pos.

**5. Rencanakan 1 proyek AI sederhana di sekolah!**
Kerangka: Nama proyek (contoh: klasifikasi bunga iris) → alat (Watson Studio/Teachable Machine) → target siswa → langkah → hasil belajar → bagaimana etikanya dibahas.

---

## 10. Checklist Pengerjaan LMS

### Sebelum Mulai
- [ ] Akun sudah aktif (email verifikasi sudah diklik)
- [ ] Login di browser Chrome
- [ ] Sudah jalankan AI Level Up Assessment

### Kursus 1: AI Fundamentals
- [ ] Enroll "AI Fundamentals"
- [ ] Modul 1 selesai + centang semua sub-topik + quiz ✅
- [ ] Modul 2 selesai + centang semua + quiz ✅
- [ ] Modul 3 selesai + centang semua + quiz ✅
- [ ] Modul 4 (Watson Studio) selesai + centang semua + quiz ✅
- [ ] Modul 5 (AI Ethics) selesai + centang semua + quiz ✅
- [ ] Modul 6 selesai + centang semua + quiz ✅
- [ ] Assessment akhir lulus
- [ ] Badge "AI Fundamentals" muncul di profil

### Kursus 2: Generative AI Roadmap
- [ ] Enroll
- [ ] Selesaikan semua modul dengan pola: baca → centang → quiz
- [ ] Assessment akhir lulus

### Kursus 3: Prompt Engineering (4 jam)
- [ ] Enroll
- [ ] Praktik setiap teknik langsung di ChatGPT / IBM Granite
- [ ] Assessment akhir lulus

### Setelah Selesai
- [ ] Badge di-share ke LinkedIn
- [ ] Screenshot sertifikat untuk arsip
- [ ] Rekap total jam belajar (untuk laporan ke sekolah)

### Pola Harian yang Disarankan (agar tidak kelelahan)
- 45–60 menit/hari, konsisten
- 1 modul per sesi → selesaikan quiz sebelum berhenti
- Catat istilah baru di buku catatan
- Jika gagal quiz → baca ulang materi modul itu, bukan mengulang quiz membabi buta

---

> Semangat, Bapak/Ibu. Kunci suksesnya: **pahami konsepnya (bukan hafalan), centang semua sub-topik, dan praktikkan prompt + Watson Studio.** Selamat belajar!