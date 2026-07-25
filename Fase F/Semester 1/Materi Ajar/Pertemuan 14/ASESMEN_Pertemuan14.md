# ASESMEN – PERTEMUAN 14
## Big Data & Data Mining

Informatika – Fase F / Kelas XI – SMA Negeri 6 Cimahi

---

## Rubrik Penilaian

### A. 5V Big Data (Bobot 20%)

| Kriteria | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| Soal 1 (5V) | 0–1 V benar | 2–3 V benar | 4 V benar | 5 V benar + arti |
| Soal 2 (V dominan) | 0–1 benar | 2–3 benar | 4 benar | 5 benar + alasan |

### B. Klasifikasi Big Data (Bobot 20%)

| Kriteria | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| Soal 3 | 0–1 benar | 2–3 benar | 4 benar | 5 benar + alasan |

### C. Asosiasi Market Basket (Bobot 30%)

| Kriteria | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| Support | 0 benar | 1 benar | 2–3 benar | 4 benar |
| Confidence | 0 benar | 1 benar | 2–3 benar | 4 benar |
| Interpretasi | Tidak ada | Sebagian | Cukup | Lengkap |

### D. Simulasi KDD (Bobop 20%)

| Kriteria | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| Proses KDD | Tidak ikut | 2 tahap | 4 tahap | 5 tahap + rekomendasi |
| Presentasi | Tidak | Kurang jelas | Jelas | Jelas + interaktif |

### E. Refleksi & Tugas (Bobot 10%)

| Kriteria | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| Refleksi | Tidak diisi | 1 jawaban | 2 jawaban | 3 jawaban |
| Tugas 5V | Tidak ada | 3V | 4V | 5V lengkap |

---

## Kunci Jawaban

### Soal 1 — 5V Big Data

| V | Kepanjangan | Arti |
|---|---|---|
| V | **Volume** | Jumlah data sangat besar |
| V | **Velocity** | Kecepatan data masuk |
| V | **Variety** | Keragaman jenis data |
| V | **Veracity** | Kebenaran/akurasi data |
| V | **Value** | Nilai/manfaat data |

### Soal 2 — V Dominan

| Sumber Data | V Paling Menonjol | Alasan |
|---|---|---|
| CCTV bandara 50 kamera 24 jam | Volume | Data video sangat besar |
| Twitter trending topic tiap detik | Velocity | Kecepatan data tinggi |
| Hoax berantai di WhatsApp | Veracity | Kebenaran data diragukan |
| Review produk di Shopee | Value | Nilai untuk rekomendasi |
| Data GPS gojek ribuan driver | Velocity + Volume | Data lokasi real-time |

### Soal 3 — Klasifikasi Big Data

| Data | Big Data? | Alasan |
|---|---|---|
| Nilai 1 kelas (36 siswa) | ❌ Tidak | Volume sangat kecil |
| Seluruh siswa SMA Indonesia (5 juta) | ✅ Ya | Volume besar |
| Foto liburan 1 orang (50 foto) | ❌ Tidak | Volume kecil |
| Video TikTok 1 jam terakhir (global) | ✅ Ya | Volume besar, velocity tinggi |
| Transaksi Indomaret seluruh Indonesia 1 tahun | ✅ Ya | Volume besar, value tinggi |

### Soal 4 — Market Basket

**Frekuensi:**
- Total transaksi: 10
- Kopi: 7 (1,2,3,4,6,7,9)
- Gula: 6 (1,2,4,6,8,9)
- Susu: 6 (3,4,7,8,9,10)
- Roti: 6 (1,5,6,7,9,10)
- Selai: 2 (5,10)

**Kopi + Gula:** transaksi 1,2,4,6,9 = 5
- Support: 5/10 = 50%
- Confidence: 5/7 = 71.4%

**Kopi + Susu:** transaksi 3,4,7,9 = 4
- Support: 4/10 = 40%
- Confidence: 4/7 = 57.1%

**Roti + Selai:** transaksi 5,10 = 2
- Support: 2/10 = 20%
- Confidence: 2/6 = 33.3%

**Kopi + Gula + Roti:** transaksi 1,6,9 = 3
- Support: 3/10 = 30%
- Confidence: 3/5 = 60%

---

**MGMP Informatika SMAN 6 Cimahi**
