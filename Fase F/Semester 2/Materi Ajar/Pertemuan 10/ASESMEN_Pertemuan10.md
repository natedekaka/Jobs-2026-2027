# ASESMEN – PERTEMUAN 10 (S2)
## Password Manager & 2FA

Informatika – Fase F / Kelas XI – SMA Negeri 6 Cimahi

---

## Rubrik Penilaian

### A. Konsep Password (Bobot 15%)

| Kriteria | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| Identifikasi password kuat/lemah | 0–1 benar | 2–3 benar | 4 benar | 5 benar + alasan |

### B. Setup Bitwarden (Bobot 30%)

| Kriteria | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| Install | Tidak | Install | Install + login | Install + login + vault |
| Generate password | Tidak | Ada | Kuat (16+ char) | Kuat + simbol + angka |
| Tambah akun | 0 akun | 1 akun | 2 akun | 3+ akun |

### C. 2FA Activation (Bobot 25%)

| Kriteria | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| Authenticator install | Tidak | Install | Install + scan QR | Install + QR + backup codes |
| 2FA aktif di Google | Tidak | Sebagian | ✅ Aktif | ✅ + 1 akun lain |

### D. Audit Password (Bobot 20%)

| Kriteria | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| Laporan | Tidak | 1 laporan | 2 laporan | 3 laporan + rencana |
| Rencana perbaikan | Tidak | 1 prioritas | 2 prioritas | 3 prioritas + detail |

### E. Refleksi & Tugas (Bobot 10%)

| Kriteria | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| Refleksi | Tidak diisi | 1 jawaban | 2–3 jawaban | 3 jawaban + mendalam |
| Tugas 2FA | Tidak | 1 akun | 2 akun | 2 akun + screenshot |

---

## Kunci Jawaban

### Soal 1 — Kekuatan Password

| Password | Kuat/Lemah | Alasan |
|---|---|---|
| `123456` | ❌ Lemah | Paling umum — brute force < 1 detik |
| `sman6cimahi` | ❌ Lemah | Terkait identitas, mudah ditebak |
| `Budi2008` | ⚠️ Sedang | Ada kapital + angka, tapi usia mudah ditebak |
| `G7$kL9#pQ2@mR5!` | ✅ Kuat | 16 karakter, simbol, angka, kapital |
| Password IG | (disesuaikan) | Minimal 12 karakter + simbol + angka |

### Soal 3 — Generate Password (contoh)

| Password | Panjang | Simbol | Angka | Skor |
|---|---|---|---|---|
| `G7$kL9#pQ2@mR5!xY` | 16 | ✅ | ✅ | Kuat |
| `aB3#zK9$mN7@pQ2!wR5*yX` | 20 | ✅ | ✅ | Sangat kuat |
| `L8@xM3#pQ7` | 12 | ✅ | ✅ | Sedang-kuat |

### Soal 5 — Audit (contoh)

| Laporan | Jumlah | Tindakan |
|---|---|---|
| Weak passwords | 3 | Generate ulang dengan Bitwarden |
| Reused passwords | 5 | Buat unik per akun |
| Exposed passwords | 1 | Segera ganti + aktivasi 2FA |
| Total akun | 10 | Tambah semua akun ke Bitwarden |

---

**MGMP Informatika SMAN 6 Cimahi**
