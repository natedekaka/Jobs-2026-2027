# KUNCI JAWABAN – ASESMEN AWAL PERTEMUAN 1 (S1)
## Review Excel (Teori & Praktik)

| No | Tipe | Kunci | Pembahasan Singkat |
|----|------|-------|--------------------|
| 1 | Mudah | **C** | `=SUM(A1:A10)` menjumlahkan seluruh angka dalam range A1:A10. |
| 2 | Mudah | **B** | `AVERAGE` menghitung rata-rata = jumlah nilai ÷ banyak cell berisi angka. |
| 3 | Mudah | **C** | `MAX` mengembalikan angka terbesar pada range. |
| 4 | Mudah | **B** | Cell kosong TIDAK dihitung oleh AVERAGE, sedangkan cell berisi 0 TETAP dihitung. |
| 5 | Mudah | **B** | `COUNT` hanya menghitung cell berisi angka → hanya A1 (75) yang dihitung, jadi hasil 1. |
| 6 | Mudah | **C** | `COUNTA` menghitung semua cell yang tidak kosong (angka maupun teks). |
| 7 | Mudah | **A** | 85 ≥ 70 (KKM), sehingga hasil IF adalah "LULUS". |
| 8 | Sedang | **C** | Rata-rata = (80+75+90+65+90) ÷ 5 = 400 ÷ 5 = **80**. |
| 9 | Sedang | **A** | 92 ≥ 85, sehingga IF bertingkat mengembalikan "A". |
| 10 | Sedang | **B** | `COUNTIF` menghitung jumlah cell yang memenuhi kriteria, yaitu yang berisi "LULUS". |
| 11 | Sedang | **D** | Freeze Top Row membuat baris header tetap terlihat saat scroll. |
| 12 | Sedang | **B** | Ctrl+T (Insert→Table) otomatis membuat header tebal, dropdown filter, dan baris selang-seling. |
| 13 | Sedang | **B** | Format **Currency** (Rp) menampilkan angka dengan simbol Rp dan pemisah ribuan. |
| 14 | Sedang | **B** | Wrap Text menampilkan teks panjang agar tetap terbaca dalam cell sempit. |
| 15 | Sedang | **D** | `COUNTA` menghitung semua cell terisi (nama siswa) → jumlah siswa yang terdata. (`COUNT` akan gagal karena nama berupa teks.) |
| 16 | Sulit | **B** | `=MAX(range)-MIN(range)` menghitung selisih nilai tertinggi dan terendah (98 − 45 = 53). |
| 17 | Sulit | **B** | `AVERAGEIF` menghitung rata-rata dengan syarat/kriteria: kelas = "XI-A". |
| 18 | Sulit | **C** | Jika data tidak ditemukan, VLOOKUP mengembalikan error `#N/A` — bisa diatasi dengan `IFERROR`. |
| 19 | Sulit | **B** | Argumen FALSE = exact match (pencarian persis); TRUE = approximate match. |
| 20 | Sulit | **C** | Cell kosong tidak dihitung (12 − 2 = 10), cell berisi 0 tetap dihitung. Rata-rata = 630 ÷ 10 = **63 ribu rupiah**. |

**Catatan KKM & Konversi (acu bahan ajar):**
- KKM = 70 → `=IF(nilai>=70,"LULUS","TIDAK LULUS")`
- Huruf Mutu: 85–100 = A, 70–84 = B, 55–69 = C, 0–54 = D

---
**MGMP Informatika SMAN 6 Cimahi — Fase F (Kelas XII) S1 Pert 1**