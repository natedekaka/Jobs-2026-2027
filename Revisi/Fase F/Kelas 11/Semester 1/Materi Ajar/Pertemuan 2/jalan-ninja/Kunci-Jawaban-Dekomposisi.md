# KUNCI JAWABAN – LKPD DEKOMPOSISI

**Informatika Kelas XI (Fase F)** – SMAN 6 Cimahi
*Pegangan guru / MGMP — jangan dibagikan ke siswa sebelum dikerjakan.*

---

## Bagian 1 – Pemahaman

> Dekomposisi adalah **memecah** masalah besar menjadi **bagian-bagian kecil** yang lebih mudah diselesaikan.

Urutan yang benar: Identifikasi masalah → **Dekomposisi** → **Algoritma**

- Dekomposisi dilakukan **SEBELUM** menyusun algoritma. *(lingkari: SEBELUM)*

---

## Bagian 2 – Class Meeting

6 sub-masalah (contoh alternatif):

1. Menentukan jenis lomba
2. Membagi panitia per lomba
3. Menyiapkan peralatan
4. Menentukan jadwal
5. Mengelola anggaran
6. Dokumentasi & publikasi

> *Terima jawaban lain yang masuk akal, asalkan masalah dipecah menjadi bagian yang lebih kecil.*

---

## Bagian 3 – Startup Edukasi Online (kerja tim)

| No | Sub-Masalah | Tim yang Bertanggung Jawab |
|----|-------------|----------------------------|
| 1  | Analisis kebutuhan pengguna | Tim riset |
| 2  | Penyusunan kurikulum | Tim konten/pengajar |
| 3  | Pembangunan platform (aplikasi) | Developer backend/frontend |
| 4  | Pembayaran digital | Developer payment gateway |
| 5  | Registrasi & autentikasi pengguna | Developer autentikasi |
| 6  | Pemasaran | Tim marketing |

**Mengapa dibagi per tim lebih efektif?**
Karena tiap anggota punya **tanggung jawab jelas**, pekerjaan bisa **dikerjakan bersamaan (paralel)**, dan jika ada kendala mudah diketahui **bagian mana yang perlu diperbaiki**.

---

## Bagian 4 – Mengurutkan `9 8 2 7 5 6`

### Cara A – Bubble Sort

| Langkah | Bandingkan & tukar | Hasil sementara |
|---------|--------------------|-----------------|
| 1 | 9 dan 8 → tukar | `8 9 2 7 5 6` |
| 2 | 9 dan 2 → tukar | `8 2 9 7 5 6` |
| 3 | 9 dan 7 → tukar | `8 2 7 9 5 6` |
| 4 | 9 dan 5 → tukar | `8 2 7 5 9 6` |
| 5 | 9 dan 6 → tukar | `8 2 7 5 6 9` |
| dst. | ulangi sampai urut | `2 5 6 7 8 9` |

Total tukar (bubble): para putaran 1 = 5 tukar, putaran berikutnya hingga urut → **total ± 15 tukar** (hitung ulang sesuai langkah siswa).

### Cara B – Selection Sort

| Putaran | Cari terkecil dari sisa | Hasil |
|---------|-------------------------|-------|
| 1 | dari `9 8 2 7 5 6`, terkecil = 2 | `2 8 9 7 5 6` |
| 2 | dari `8 9 7 5 6`, terkecil = 5 | `2 5 9 7 8 6` |
| 3 | dari `9 7 8 6`, terkecil = 6 | `2 5 6 9 8 7` |
| dst. | lanjutkan sampai urut | `2 5 6 7 8 9` |

### Strategi Efektif
- Pilihan metode: **A atau B** (bebas, sesuai kenyamanan siswa).
- **Selection sort** biasanya lebih efektif untuk data kecil seperti ini (langkah lebih sedikit & mudah dilacak).
- Alasan siswa boleh berbeda — nilai pelajaran utamanya: **mampu memilih & membenarkan strategi**, bukan kebenaran mutlak satu metode.

---

## Bagian 5 – Masalah Nyata (ala SAP-K11-04-U)

Tugas: A=3, B=1, C=2, D=1,5, E=2,5 jam. Waktu tersedia **6 jam**.

1. Urutkan dari durasi terkecil: **B, D, C, E, A**
2. Ambil urutan terkecil sampai total tidak lewat 6 jam:
   - B (1) → 1
   - D (1,5) → 2,5
   - C (2) → 4,5
   - E (2,5) → 7 (tidak muat) ✗
   - A (3) → 7,5 (tidak muat) ✗
3. Tugas terpilih: **B, D, C** → total **4,5 jam**
4. **Maksimal 3 tugas**

> *Catatan: soal versi asli buku (SAP-K11-04-U) memakai 10 PR dan 8 jam; versi LKPD ini disederhanakan agar bisa dikerjakan di kelas.*

---

## Bagian 6 – Refleksi (tidak ada kunci)

Jawaban bersifat pribadi siswa (konsep, manfaat, skala pemahaman, dan keinginan belajar lanjut).

---

## Ringkasan Kunci 3 Detik (penguat materi)

> **BESAR → KECIL → SELESAIKAN SATU PER SATU**
> Dekomposisi = memecah masalah besar jadi bagian kecil; dilakukan **sebelum** menyusun algoritma; memungkinkan **kerja tim** dan **eksekusi paralel**.