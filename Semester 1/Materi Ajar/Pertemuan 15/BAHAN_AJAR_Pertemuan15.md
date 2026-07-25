# BAHAN AJAR – PERTEMUAN 15
## Validasi, Verifikasi & Data Cleansing

| TP | BK 1.2 |
|---|---|

---

### A. VALIDASI VS VERIFIKASI

| Aspek | Validasi | Verifikasi |
|---|---|---|
| **Fokus** | Aturan / format | Kebenaran / fakta |
| **Pertanyaan** | "Apakah formatnya benar?" | "Apakah isinya benar?" |
| **Otomatis?** | Ya — bisa dengan rules | Tidak — butuh sumber eksternal |
| **Contoh** | Nilai 0–100? Tanggal valid? | Nama siswa sesuai ijazah? |
| **Tools** | Data validation, IF, Conditional Format | Cross-check, dokumen asli |

---

### B. TEKNIK DATA CLEANSING

#### 1. Filter dan Sort

| Fungsi | Cara | Kegunaan |
|---|---|---|
| **Filter** | Data → Filter → centang kondisi | Lihat missing value, outlier, kategori tertentu |
| **Sort A–Z / Z–A** | Klik kanan kolom → Sort | Temukan duplikat berurutan, outlier |

**Contoh:**
- Filter kolom Nilai → (Blanks) → lihat semua siswa tanpa nilai
- Sort Tgl Lahir → lihat tanggal "01-01-1900" di awal/akhir

#### 2. Remove Duplicates

| Langkah | Keterangan |
|---|---|
| Pilih semua data | Ctrl+A |
| Data → Remove Duplicates | Pilih kolom yang dicek (biasanya semua) |
| OK | Hasil: duplikat terhapus |

**Catatan:** Sebelum hapus duplikat, pastikan baris mana yang asli dan mana duplikat!

#### 3. Find & Replace

| Langkah | Contoh |
|---|---|
| Ctrl+H | Find: "x-1" → Replace with: "X-1" |
| Options → Match entire cell contents | Agar tidak salah ganti |
| Replace All | |

**Kegunaan:** Standarisasi format kelas, perbaiki typo umum.

#### 4. Data Validation

| Langkah | Contoh Aturan |
|---|---|
| Pilih kolom → Data → Data Validation | Nilai: Decimal between 0–100 |
| Settings → Allow → pilih tipe | Tanggal: Date between 01-01-2008 to 31-12-2010 (logis) |
| Input Message (opsional) | Petunjuk untuk pengguna |

#### 5. Conditional Formatting

| Langkah | Contoh |
|---|---|
| Pilih kolom → Format → Conditional Formatting | Nilai > 100 → merah |
| Atur aturan | Nilai < 0 → merah |
| Atur format (fill color, font) | Kosong → kuning |

#### 6. Fungsi Teks untuk Standarisasi

| Fungsi | Kegunaan | Contoh |
|---|---|---|
| `=TRIM(A2)` | Hapus spasi berlebih | `"Cimahi "` → `"Cimahi"` |
| `=UPPER(A2)` | Ubah ke huruf BESAR | `"cimahi"` → `"CIMAHI"` |
| `=LOWER(A2)` | Ubah ke huruf kecil | `"CIMAHI"` → `"cimahi"` |
| `=PROPER(A2)` | Kapital setiap kata | `"cimahi"` → `"Cimahi"` |

---

### C. PROSES DATA CLEANSING — 4 LANGKAH

```
1. AUDIT
   ↓
   Temukan semua masalah (Pertemuan 14)
   
2. VALIDASI
   ↓
   Periksa aturan format, tipe, range
   
3. VERIFIKASI & CLEANSING
   ↓
   Perbaiki: hapus duplikat, koreksi format, isi missing, tandai outlier
   
4. FINAL
   ↓
   Dataset bersih siap olah
```

---

### D. CONTOH PRAKTIK CLEANSING

#### Dataset Kotor (RAW)

| Nama | Kelas | Tgl Lahir | No HP | Nilai | Alamat |
|---|---|---|---|---|---|
| Andi Pratama | X-1 | 15-03-2009 | 08123456789 | 85 | Cimahi |
| Budi Santoso | X-1 | 2009-05-20 | 08234567890 | | Cimahi |
| Cici Dewi Lestari | X-2 | 20/05/2009 | 08345678901 | 95 | |
| Andi Pratama | X-1 | 15-03-2009 | 08123456789 | 85 | Cimahi |
| Dedi Supriadi | X-3 | 01-01-1900 | 08456789 | 200 | Bandung |
| Euis | X-1 | 10-10-2009 | 08567ABCD | Tujuhpuluh | Cimahi |
| Fitri Handayani | X-22 | 30-02-2009 | 08678901234 | 80 | Cimahi |
| Gunawan | x-1 | 05-07-2009 | 08789012345 | 90 | Cimahi |

#### Dataset Bersih (CLEAN) — Setelah Cleansing

| Nama | Kelas | Tgl Lahir | No HP | Nilai | Alamat |
|---|---|---|---|---|---|
| Andi Pratama | X-1 | 15-03-2009 | 08123456789 | 85 | Cimahi |
| Budi Santoso | X-1 | 20-05-2009 | 08234567890 | | Cimahi |
| Cici Dewi Lestari | X-2 | 20-05-2009 | 08345678901 | 95 | |
| Dedi Supriadi | X-3 | 01-01-1900 | 08456789012 | | Bandung |
| Euis | X-1 | 10-10-2009 | 085671234567 | 70 | Cimahi |
| Fitri Handayani | X-2 | | 08678901234 | 80 | Cimahi |
| Gunawan | X-1 | 05-07-2009 | 08789012345 | 90 | Cimahi |

#### Log Perubahan (LOG)

| No | Masalah | Teknik | Baris | Hasil |
|---|---|---|---|---|
| 1 | Duplikat Andi | Remove Duplicates | 4 | Baris 4 dihapus |
| 2 | Format tanggal | Find & Replace | 2 | 2009-05-20 → 20-05-2009 |
| 3 | Format tanggal | Find & Replace | 3 | 20/05/2009 → 20-05-2009 |
| 4 | Kelas "X-22" | Koreksi manual | 7 | X-22 → X-2 |
| 5 | Kelas "x-1" | Find & Replace | 8 | x-1 → X-1 |
| 6 | No HP "08456789" | Tambah digit | 5 | 08456789 → 08456789012 |
| 7 | No HP "08567ABCD" | Hapus huruf | 6 | 08567ABCD → 085671234567 |
| 8 | Nilai "200" | Hapus (outlier) | 5 | Dikosongkan |
| 9 | Nilai "Tujuhpuluh" | Konversi | 6 | "Tujuhpuluh" → 70 |
| 10 | Tanggal 30-02-2009 | Invalid → hapus | 7 | Dikosongkan |

---

### E. RANGKUMAN

1. **Validasi**: cek format, tipe, range — bisa otomatis
2. **Verifikasi**: cek kebenaran — butuh sumber eksternal
3. **Data cleansing**: filter, sort, remove dupes, find & replace, data validation
4. **Hasil akhir**: dataset bersih + log perubahan

---

**MGMP Informatika SMAN 6 Cimahi**
