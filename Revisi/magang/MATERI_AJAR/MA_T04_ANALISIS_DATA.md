# MATERI AJAR — TAHAP 4: ANALISIS DATA
## Excel Lanjut & Dashboard
*Untuk magang guru Informatika — pendekatan Memahami → Mengaplikasi → Merefleksi*

---

## 🧠 MEMAHAMI — Membangun Pemahaman Awal

### A. Mengapa Analisis Data Penting?
Dari administrasi sekolah hingga perusahaan multinasional, keputusan berbasis data. Guru perlu menguasai analisis untuk menyajikan data sekolah secara profesional sekaligus mengajar siswa Kelas XII.

### B. Konsep Data Utama
- **Tabel (Table):** kumpulan data terstruktur dengan header. Inisialisasi dgn **`Ctrl+T`** agar formula & pivot otomatis mengikuti range.
- **Range:** rentang sel, mis. `A1:A10`.
- **Formula:** ekspresi perhitungan yang diawali `=`.
- **Pivot Table:** ringkasan otomatis (kelompok, rata-rata, jumlah) dari data besar.

### C. Pantang Larang (Best Practice)
- **Jangan merge cell di area data** — gunakan *Center Across Selection* untuk judul.
- Gunakan `IFERROR` agar error tidak tampil mentah (#N/A).
- Selalu pakai **exact match** (`FALSE`) pada VLOOKUP/XLOOKUP.

---

## 🔧 MENGAPLIKASI — Praktik & Penerapan

### Praktik 1 — Fungsi Aritmatika Dasar
Buka `magang/DATA_DUMMY_NILAI_PTS.csv` di Excel.
| Fungsi | Rumus | Keterangan |
|---|---|---|
| Jumlah | `=SUM(C2:C16)` | menjumlahkan angka |
| Rata-rata | `=AVERAGE(C2:C16)` | rata-rata (cell kosong diabaikan, 0 dihitung) |
| Tertinggi | `=MAX(C2:C16)` | nilai terbesar |
| Terendah | `=MIN(C2:C16)` | nilai terkecil |
| Hitung angka | `=COUNT(C2:C16)` | banyak cell berisi angka |
| Hitung isi | `=COUNTA(C2:C16)` | banyak cell tidak kosong |

### Praktik 2 — Fungsi Logika IF & COUNTIF
```excel
=IF(C2>=70,"LULUS","TIDAK LULUS")      ' status
=COUNTIF(E2:E16,"LULUS")               ' jumlah lulus
=AVERAGEIF(A2:A16,"X-1",C2:C16)        ' rata-rata per kelas
```

### Praktik 3 — VLOOKUP & XLOOKUP
```excel
=VLOOKUP("Budi", A2:B16, 2, FALSE)     ' nilai_pencari, tabel, kolom, TEPAT
=XLOOKUP("Budi", A2:A16, B2:B16)       ' lebih fleksibel, Excel 2021+
```
- VLOOKUP: data yang dicari harus di **kolom pertama** tabel acuan.
- Bungkus dengan IFERROR:
  ```excel
  =IFERROR(VLOOKUP(A2, tabel_acuan, 2, FALSE),"Tidak ditemukan")
  ```

### Praktik 4 — Conditional Formatting
1. Sorot kolom nilai → **Home** → **Conditional Formatting**.
2. *Highlight Cells Rules* → Less Than `70` → merah.
3. *Greater Than `85`* → hijau.
4. Buat *New Rule → Use a formula* untuk highlight baris dengan status "TIDAK LULUS":
   ```
   =$E2="TIDAK LULUS"
   ```

### Praktik 5 — Pivot Table & Slicer
1. Klik data → **Insert** → **PivotTable**.
2. Seret field **Kelas** ke Rows, **Nilai** ke Values → pilih *Average*.
3. Tambahkan **Slicer** → filter kelas secara interaktif.

### Praktik 6 — Chart & Dashboard
1. Buat **bar chart** rata-rata per kelas, **pie chart** status, **line chart** tren.
2. Rapikan: title jelas, label axis, 1 pesan per chart, maksimal 1 pesan.
3. Susun semua chart + angka KPI di **1 sheet "DASHBOARD"** dengan slicer, tanpa tabel mentah.

### Praktik 7 — Analisis Data dengan Python (Colab)
```python
import pandas as pd
import matplotlib.pyplot as plt

df = pd.read_csv('data_nilai.csv')
print(df.groupby('Kelas')['Nilai'].mean())   # rata-rata per kelas
df.boxplot(column='Nilai', by='Kelas')
plt.show()
```
> Bandingkan workflow Excel vs Python: Excel cepat & interaktif; Python otomatis & mampu data besar.

---

## 🔍 MEREFLEKSI — Refleksi & Evaluasi

- Mengapa `Ctrl+T` (Table) menjadi langkah pertama yang baik sebelum formula/pivot?
- Kapan lebih cocok memakai Excel; kapan memakai Python?
- Bagaimana format yang rapi memengaruhi pembaca data?
- Skala pemahaman diri: ___/10

---

## Kunci & Latihan
1. Dengan `DATA_DUMMY_NILAI_PTS.csv`, buat tabel + formula dasar + status predikat.
2. Buat laporan otomatis 1 halaman (dengan conditional formatting).
3. Buat dashboard 1 halaman dengan pivot, chart, slicer.
4. Lakukan analisis yang sama di Python dan bandingkan hasilnya.

---

**MGMP Informatika SMAN 6 Cimahi — Program Magang Guru Informatika TP 2026/2027**