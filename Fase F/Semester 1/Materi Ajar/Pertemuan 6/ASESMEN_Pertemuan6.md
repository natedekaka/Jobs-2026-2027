# ASESMEN – PERTEMUAN 6
## Deployment & CI/CD

Informatika – Fase F / Kelas XI – SMA Negeri 6 Cimahi

---

## Rubrik Penilaian

### A. Konsep Deployment (Bobot 20%)

| Kriteria | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| Soal 1 (lingkungan development/staging/production) | Tidak diisi | 1 benar | 2 benar | 3 benar |
| Soal 2 (jenis hosting) | 0–1 benar | 2 benar | 3 benar | 4 benar |

### B. CI/CD (Bobot 25%)

| Kriteria | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| Soal 3 (singkatan CI/CD) | Salah semua | CI benar | CD benar | Kedua benar |
| Soal 4 (urutan) | Salah | 1 benar | 2 benar | 3 benar |
| Soal 5 (keuntungan) | 0 | 1 | 2 | 2 + penjelasan |

### C. Deploy Netlify (Bobot 35%)

| Kriteria | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| Berhasil deploy | Tidak | Error, tidak selesai | Berhasil | Berhasil + URL dicatat |
| Halaman tampil | Error | Sebagian | Lengkap | Lengkap + rapi |
| Screenshot | Tidak ada | Ada, buram | Ada, jelas | Ada + URL jelas |

### D. CI/CD Pipeline Diagram (Bobot 20%)

| Kriteria | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| Diagram pipeline | Tidak ada | 2 tahap | 3 tahap | 4 tahap + label jelas |

---

## Kunci Jawaban

### Soal 1 — Lingkungan

| Lingkungan | Tujuan | Siapa yang Akses? |
|---|---|---|
| Development | Menulis & menguji kode | Developer |
| Staging | Uji coba mirip produksi | Tim internal |
| Production | Dipakai user sungguhan | Semua pengguna |

### Soal 2 — Jenis Hosting
1=D (Shared = 1 server banyak pengguna)
2=A (VPS = server virtual pribadi)
3=B (Cloud = bayar sesuai pemakaian)
4=C (Static = gratis untuk static site)

Jawaban: 1=D, 2=A, 3=B, 4=C

### Soal 3 — CI/CD
CI = Continuous Integration (setiap commit di-test otomatis)
CD = Continuous Deployment (setelah test lolos → auto deploy)

### Soal 4 — Urutan CI/CD
1. **B** (git push) → 2. **C** (test otomatis) → 3. **A** (deploy)

### Soal 5 — Keuntungan CI/CD
1. Proses deploy otomatis — tidak perlu manual
2. Setiap perubahan di-test dulu → lebih aman
3. Rilis fitur baru lebih cepat
4. Tidak ada versi yang ketinggalan

---

**MGMP Informatika SMAN 6 Cimahi**
