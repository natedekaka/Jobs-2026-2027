# LEMBAR KERJA PESERTA DIDIK (LKPD)
## Pertemuan 8 (S2) – Cloud Computing

| TP | BK, LD — Konsep Sistem dan Keamanan Jaringan Komputer |
|---|---|
| Nama | ____________________ |
| Kelas | ____________________ |

---

### A. KONSEP CLOUD COMPUTING

**Soal 1:** Isi tabel perbandingan tradisional vs cloud!

| Aspek | Tradisional (On-Premise) | Cloud |
|---|---|---|
| Server | | |
| Biaya | | |
| Skalabilitas | | |
| Akses | | |

---

### B. KLASIFIKASI IaaS / PaaS / SaaS

**Soal 2:** Klasifikasikan 8 layanan berikut!

| No | Layanan | IaaS/PaaS/SaaS | Alasan |
|---|---|---|---|
| 1 | AWS EC2 | | |
| 2 | Google Sheets | | |
| 3 | Google Colab | | |
| 4 | Netflix | | |
| 5 | Google Drive | | |
| 6 | Heroku | | |
| 7 | Zoom | | |
| 8 | Firebase | | |

---

### C. PRAKTIK GOOGLE COLAB

**Soal 3:** Jalankan kode di Colab dan catat!

```python
import platform, psutil
from google.colab import files

print(f'Sistem: {platform.system()} {platform.release()}')
print(f'Prosesor: {platform.processor()}')
print(f'RAM: {psutil.virtual_memory().total / 1e9:.2f} GB')
print(f'CPU: {psutil.cpu_count()} core')
```

| Spesifikasi | Hasil |
|---|---|
| Sistem operasi | |
| Prosesor | |
| RAM | |
| CPU core | |

**Soal 4:** Buat file CSV lalu download!

```python
import csv

data = [
    ['Nama', 'Nilai'],
    ['Adi', 85],
    ['Budi', 70],
    ['Citra', 90]
]

with open('data.csv', 'w', newline='') as f:
    writer = csv.writer(f)
    writer.writerows(data)

files.download('data.csv')
```

✅ File terdownload?

**Soal 5:** Refleksi Colab

| Pertanyaan | Jawaban |
|---|---|
| Colab termasuk IaaS/PaaS/SaaS? | |
| Bedanya Colab vs Jupyter lokal? | |
| Kelebihan Colab untuk belajar Python? | |

---

### D. STUDI KASUS

**Soal 6:** Pilih layanan cloud untuk 4 skenario!

| Skenario | Pilihan (IaaS/PaaS/SaaS) + Provider | Alasan |
|---|---|---|
| A: Startup web — budget kecil | | |
| B: Sekolah — email + dokumen | | |
| C: Peneliti — GPU training AI | | |
| D: Bank — database sensitif | | |

---

### E. TUGAS RUMAH

Buat 1 aplikasi sederhana di Colab (kalkulator/konversi suhu/tebak angka)!

| Aspek | Status |
|---|---|
| Kode jalan di Colab | ✅ / ❌ |
| Screenshot | ✅ / ❌ |
| Link dibagikan | ✅ / ❌ |

**Link Colab:** ____________________

---

### F. REFLEKSI

| Pertanyaan | Jawaban |
|---|---|
| Aplikasi cloud favorit sehari-hari? | |
| Risiko cloud paling penting? | |
| Skala pemahaman (1–10) | / 10 |

---

**MGMP Informatika SMAN 6 Cimahi**
