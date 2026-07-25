# MODUL AJAR INFORMATIKA – FASE F (KELAS XI)

| Komponen | Deskripsi |
|---|---|
| **Mata Pelajaran** | Informatika |
| **Fase / Kelas** | F / XI |
| **Semester** | 2 (Genap) |
| **Pertemuan ke-** | 8 |
| **Alokasi Waktu** | 5 JP × 45 menit (225 menit) |
| **Tahun Pelajaran** | 2026/2027 |
| **Satuan Pendidikan** | SMA Negeri 6 Cimahi |
| **Materi Esensial** | Konsep Sistem dan Keamanan Jaringan Komputer |

---

## Tujuan Pembelajaran

| TP | IKTP |
|---|---|
| **BK, LD:** Memahami konsep cloud computing dan layanannya | 8.1 Menjelaskan definisi cloud computing |
| | 8.2 Membedakan IaaS, PaaS, SaaS dengan contoh |
| | 8.3 Mengidentifikasi kelebihan & risiko cloud |
| | 8.4 Menggunakan Google Colab sebagai cloud service |

---

## Langkah Pembelajaran

### Pembukaan (20 menit)

| Kegiatan | Waktu |
|---|---|
| 1. Salam, doa, cek kehadiran | 3 menit |
| 2. **Review**: "Pert 7: topologi jaringan. Sekarang: bagaimana aplikasi berjalan di **awan** — bukan di komputer kita?" | 7 menit |
| 3. **Apersepsi**: "Google Drive, Google Colab, Netflix, Spotify — pernah pakai? Itu semua **Cloud Computing**! Data dan aplikasi tidak di komputer kalian, tapi di server Google/AWS." | 10 menit |

### Inti (175 menit)

#### Memahami (55 menit)

**1. Apa itu Cloud Computing? (15 menit)**

> **Cloud Computing** = penyediaan sumber daya komputasi (server, storage, database, software) melalui internet — bayar sesuai pemakaian.

| Analogi | Cloud Computing |
|---|---|
| Dulu: beli generator listrik sendiri | Sekarang: listrik dari PLN — bayar sesuai pemakaian |
| Dulu: beli server, install sendiri | Sekarang: sewa server dari AWS/Google — bayar per jam |

**Sejarah:**
- 2006: Amazon luncurkan AWS (Amazon Web Services)
- 2008: Google luncurkan App Engine
- 2010: Microsoft Azure
- 2020+: Cloud jadi standar industri

**2. Model Layanan Cloud (20 menit)**

**a. IaaS (Infrastructure as a Service)**

```
Pengguna kelola: aplikasi, data, runtime, middleware, OS
Penyedia kelola: server, storage, jaringan, virtualisasi
```

| Contoh | Kegunaan |
|---|---|
| AWS EC2, Google Compute Engine | Hosting server, database |
| DigitalOcean, Linode | Server aplikasi |
| Google Drive, Dropbox | Storage file |

**b. PaaS (Platform as a Service)**

```
Pengguna kelola: aplikasi dan data
Penyedia kelola: runtime, middleware, OS, server, storage, jaringan
```

| Contoh | Kegunaan |
|---|---|
| Google App Engine | Deploy aplikasi tanpa管理 server |
| Google Colab | Jupyter Notebook di cloud |
| Heroku, Railway | Hosting aplikasi web |
| Firebase | Backend untuk mobile app |

**c. SaaS (Software as a Service)**

```
Pengguna tinggal pakai — penyedia kelola semua
```

| Contoh | Kegunaan |
|---|---|
| Google Workspace (Gmail, Docs, Sheets) | Email, dokumen |
| Microsoft 365 | Office online |
| Zoom, Google Meet | Video conference |
| Canva, Figma | Design online |
| Spotify, Netflix | Streaming |

**Perbandingan:**

| Aspek | IaaS | PaaS | SaaS |
|---|---|---|---|
| Kontrol | Tinggi | Sedang | Rendah |
| Kelola sendiri | OS, middleware | Aplikasi | Tidak ada |
| Contoh | AWS EC2 | Google Colab | Gmail |
| Cocok untuk | Admin IT | Developer | Pengguna umum |

**3. Kelebihan & Risiko Cloud (10 menit)**

| Kelebihan | Risiko |
|---|---|
| Hemat biaya (bayar sesuai pakai) | Ketergantungan internet |
| Skalabilitas (mudah naik/turun) | Keamanan data |
| Akses di mana saja | Privasi (data di server orang lain) |
| Backup & recovery otomatis | Vendor lock-in |
| Update otomatis | Biaya bisa membengkak |

**4. Cloud di Indonesia (10 menit)**

| Layanan | Provider |
|---|---|
| Google Cloud | google cloud (Jakarta region sejak 2020) |
| AWS | aws (Jakarta region) |
| Azure | Microsoft (Asia Tenggara) |
| Lokal | BTI, IDCloudHost, Biznet Gio |

#### Mengaplikasi — Praktik (90 menit)

**5. Demonstrasi Google Colab (15 menit)**
- Buka `colab.research.google.com`
- Buat notebook baru
- Tunjukkan: Runtime → Change runtime type → GPU (gratis!)
- Tulis kode Python sederhana
- Simpan di Google Drive
- Tunjukkan bahwa kode jalan di server Google, bukan laptop

**6. Aktivitas 1 — Colab Python (25 menit) — Individu**

```python
# Cek spesifikasi server cloud Google!
import platform
print(f'Sistem: {platform.system()} {platform.release()}')
print(f'Prosesor: {platform.processor()}')

import psutil
print(f'RAM: {psutil.virtual_memory().total / 1e9:.2f} GB')
print(f'CPU: {psutil.cpu_count()} core')

# Buat file dan simpan
teks = "File ini dibuat di Google Colab — Cloud Computing!"
with open('contoh.txt', 'w') as f:
    f.write(teks)

# Download file
from google.colab import files
files.download('contoh.txt')
```

Tugas:
1. Jalankan kode — catat spesifikasi server Google
2. Buat file CSV dengan Python → download
3. Tulis refleksi: "Apa bedanya Colab vs Jupyter lokal?"

**7. Aktivitas 2 — Klasifikasi Layanan Cloud (20 menit) — Berpasangan**

| No | Layanan | IaaS / PaaS / SaaS | Alasan |
|---|---|---|---|
| 1 | AWS EC2 (virtual server) | | |
| 2 | Google Sheets | | |
| 3 | Google Colab | | |
| 4 | Netflix | | |
| 5 | Google Drive | | |
| 6 | Heroku | | |
| 7 | Zoom | | |
| 8 | Firebase | | |

**8. Aktivitas 3 — Studi Kasus: Pilih Cloud (30 menit) — Kelompok**

| Skenario | Pilih cloud | Alasan |
|---|---|---|
| A: Startup mau hosting web aplikasi — budget kecil, dev 2 orang | | |
| B: Sekolah ingin email + dokumen online untuk 100 guru | | |
| C: Peneliti butuh GPU untuk training AI — 1 bulan | | |
| D: Bank butuh server database — keamanan tinggi | | |

**Presentasi 2 kelompok, @5 menit**

#### Merefleksi (15 menit)

**9. Refleksi Jurnal (15 menit)**
- Aplikasi cloud favorit yang kalian pakai sehari-hari?
- Risiko cloud paling penting menurut kalian?
- Skala pemahaman 1–10

### Penutup (35 menit)

| Kegiatan | Waktu |
|---|---|
| 1. Rangkuman: Cloud = komputasi via internet. IaaS (infra) → PaaS (platform) → SaaS (aplikasi) | 10 menit |
| 2. Kuis lisan: "Bedanya IaaS, PaaS, SaaS? Contoh masing-masing?" | 10 menit |
| 3. Preview: "Pert 9: Troubleshooting Jaringan — ping, traceroute, ipconfig — jadi admin jaringan!" | 5 menit |
| 4. Tugas rumah: Bikin 1 aplikasi sederhana di Colab (kalkulator / konversi suhu) + screenshot | 10 menit |

---

## Asesmen

| Kriteria | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| Konsep cloud | Tidak paham | Sebagian | Paham | Paham + analogi |
| IaaS/PaaS/SaaS | 0–2 benar | 3–4 benar | 5–6 benar | 7–8 benar + alasan |
| Praktik Colab | Tidak jalan | Jalan | Jalan + download | Jalan + analisis spesifikasi |
| Studi kasus | Tidak tepat | 1 tepat | 2–3 tepat | 4 tepat + alasan |

---

**MGMP Informatika SMAN 6 Cimahi**
