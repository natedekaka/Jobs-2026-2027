# ASESMEN – PERTEMUAN 17
## Konsep Sistem dan Keamanan Jaringan

Informatika – Fase F / Kelas XI – SMA Negeri 6 Cimahi

---

## Rubrik Penilaian

### A. Pemahaman Konsep Sistem & Jaringan (Bobot 20%)

| Kriteria | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| Sistem (input-proses-output) | Tidak paham | 1–2 contoh | 3–4 contoh | 4 contoh + benar |
| Jaringan (jenis + arsitektur) | 0–1 benar | 2 benar | 3–4 benar | 4 benar + penjelasan |

### B. Identifikasi Ancaman (Bobot 20%)

| Kriteria | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| Jenis ancaman | 0–2 benar | 3–4 benar | 5–6 benar | 6 benar + penjelasan |
| Pencegahan | 0–1 tepat | 2 tepat | 3 tepat | 3 tepat + 2 cara per ancaman |

### C. Simulasi Caesar Cipher (Bobot 15%)

| Kriteria | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| Enkripsi | 0–2 benar | 3–4 benar | 5–6 benar | 6 benar |
| Dekripsi | 0–1 benar | 2 benar | 3 benar | 3 benar |
| Kelemahan | Tidak tahu | Sebagian | Tepat | Tepat + contoh serangan |

### D. Praktik Cek Website (Bobot 15%)

| Kriteria | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| Website diperiksa | 0–1 | 2–3 | 4 | 5 |
| Analisis benar | Tidak | 1–2 tepat | 3–4 tepat | 5 tepat |

### E. Studi Kasus & Poster (Bobot 20%)

| Kriteria | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| Analisis kasus | Tidak selesai | 2 pertanyaan | 3 pertanyaan | 4 pertanyaan + mendalam |
| Poster | Tidak buat | Ada, kurang jelas | Jelas + benar | Menarik + benar + presentasi |

### F. Refleksi & Tugas (Bobot 10%)

| Kriteria | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| Refleksi | Tidak diisi | 1 jawaban | 2 jawaban | 2 jawaban + mendalam |
| UU ITE | Tidak baca | 1 poin | 2 poin | 3 poin + nomor pasal |

---

## Kunci Jawaban

### Soal 2 — Jaringan

| Skenario | Jenis | Arsitektur |
|---|---|---|
| 30 komputer lab | LAN | Client-Server |
| Bluetooth HP ke laptop | PAN | Peer-to-Peer |
| Akses website | WAN | Client-Server |
| BitTorrent | WAN | Peer-to-Peer |

### Soal 3 — Ancaman

| Skenario | Ancaman |
|---|---|
| Email bank minta link | Phishing |
| File berubah `.encrypted` | Ransomware |
| Wi-Fi palsu | Man-in-the-Middle |
| Server lambat — 10.000 bot | DDoS |
| `' OR 1=1 --` login sukses | SQL Injection |
| Telepon minta OTP | Social Engineering |

### Soal 5 — Caesar Enkripsi

| Plainteks | Cipherteks |
|---|---|
| A | D |
| B | E |
| C | F |
| KOMPUTER | NRPSXWHU |
| JARINGAN | MDULQJDQ |
| AMAN | DPDA |

### Soal 6 — Caesar Dekripsi

| Cipherteks | Plainteks |
|---|---|
| D | A |
| V | S |
| LQIRUPDWLND | INFORMATIKA |
| HWLND | ETIKA |

### Soal 7 — Kelemahan Caesar Cipher

Hanya 25 kemungkinan geseran — bisa di-brute-force dalam hitungan detik. Pola huruf juga mudah dikenali dengan frekuensi analisis.

### Soal 9 — Studi Kasus (contoh untuk Kasus A: Tokopedia 2020)

| Pertanyaan | Jawaban |
|---|---|
| Jenis ancaman | SQL Injection pada database |
| Bagaimana terjadi? | Celah keamanan di database → 91 juta akun bocor (email, password ter-hash) |
| Dampak | Akun diretas, data pribadi dijual di dark web, phishing massal |
| Mencegah | Patch database, input validation, enkripsi password dengan bcrypt, penetration testing |

### Kunci — UU ITE (Pasal 27–35)

| Pasal | Isi |
|---|---|
| 27 (1) | Akses ilegal ke sistem elektronik — 6 tahun / Rp 600 juta |
| 28 (1) | Berita bohong yang merugikan — 6 tahun / Rp 1 miliar |
| 30 | Intersepsi ilegal — 10 tahun / Rp 800 juta |
| 32 | Rusak data elektronik — 8 tahun / Rp 2 miliar |
| 35 | Phishing/penipuan online — 12 tahun / Rp 12 miliar |

---

**MGMP Informatika SMAN 6 Cimahi**
