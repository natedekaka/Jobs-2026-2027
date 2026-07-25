# ASESMEN – PERTEMUAN 5
## Pengujian (Testing) & Debugging

Informatika – Fase F / Kelas XI – SMA Negeri 6 Cimahi

---

## Rubrik Penilaian

### A. Jenis Testing (Bobot 20%)

| Kriteria Soal 1 | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| Mengisi tabel jenis testing | 0–1 benar | 2 benar | 3 benar | 4 benar + analogi |
| Soal 2 (black vs white) | Tidak diisi | 1 aspek benar | 2 aspek benar | 3+ aspek benar |

### B. Test Case (Bobot 30%)

| Kriteria | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| Jumlah test case | 0–1 | 2 | 3 | 4 (positif, negatif, boundary, edge) |
| Format (ID, skenario, input, expected) | Tidak sesuai | Sebagian | Hampir lengkap | Lengkap semua |

### C. Debugging HTML (Bobot 30%)

| Kriteria | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| Jumlah bug ditemukan | 0–1 | 2–3 | 4 | 5 |
| Perbaikan tepat | Tidak tepat | Sebagian tepat | Hampir tepat | Semua tepat |

### D. Studi Kasus Bug Nyata (Bobot 20%)

| Kriteria | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| Kelengkapan analisis | 0–1 item | 2–3 item | 4–5 item | 6 item lengkap |

---

## Kunci Jawaban

### Soal 1 — Jenis Testing

| No | Jenis Testing | Apa yang Diuji? | Analogi |
|---|---|---|---|
| 1 | Unit Test | Satu fungsi/komponen kecil | Cek satu bata |
| 2 | Integration Test | Kerja sama antar komponen | Cek apakah bata tersusun |
| 3 | System Test | Seluruh sistem | Cek seluruh rumah |
| 4 | UAT | Kesesuaian dengan kebutuhan user | Pemilik rumah periksa |

### Soal 2 — Black-box vs White-box

| Aspek | Black-box | White-box |
|---|---|---|
| Fokus | Input → output | Struktur internal kode |
| Melihat kode? | Tidak | Ya |

### Soal 3 — Test Case Login (contoh)

| ID | Skenario | Input NISN | Input Password | Expected Result |
|---|---|---|---|---|
| TC-01 | Login sukses | 12345 | abcde | Dashboard muncul |
| TC-02 | NISN salah | 99999 | abcde | "NISN tidak ditemukan" |
| TC-03 | Password salah | 12345 | xxxxx | "Password salah" |
| TC-04 | Input kosong | (kosong) | (kosong) | "Harap isi semua field" |

### Soal 4 — Debugging HTML (5 bug)

| No | Bug | Baris | Perbaikan |
|---|---|---|---|
| 1 | Tag `<title>` salah | 5 | `<title>` bukan `<titl>` |
| 2 | Tag `<h1>` tidak ditutup | 8 | Tambah `</h1>` |
| 3 | Tag `<label>` salah | 9 | `</label>` bukan `</lable>` |
| 4 | Tag `<input>` submit tidak ditutup | 12 | Tambah `>` setelah `"Daftar"` |
| 5 | Entitas HTML `&copy` kurang `;` | 13 | `&copy;` |

---

**MGMP Informatika SMAN 6 Cimahi**
