# BAHAN AJAR – PERTEMUAN 15 (S2)
## Review PAS & Refleksi Semester 2

---

### A. PETA KONSEP SEMESTER 2 — 14 PERTEMUAN

```
                    FASE F — SEMESTER 2
                           │
        ┌──────────────────┴──────────────────┐
        │                                     │
  PENGOLAHAN DATA                    KEAMANAN & ETIKA
  (Pert 1–5)                         (Pert 7–13)
        │                                     │
  ┌─────┼──────┐                    ┌─────────┼─────────┐
  │     │      │                    │         │         │
  1     2     3                   7,8,9    10,11,12    13
Big   Clean  Visu                   Jaringan  Keamanan  Etika
Data  & Label                        & Cloud   Digital  Digital
  │                              
  4     5     6
JSON  Pipeline  PTS
Python
        │
        14
     Proyek Akhir
     (Python)
```

---

### B. RINGKASAN PER PERTEMUAN

#### Pert 1 — Big Data & Sumber Data Terbuka

| Konsep | Definisi |
|---|---|
| **Big Data 5V** | **V**olume (besar), **V**elocity (cepat), **V**ariety (beragam), **V**eracity (kebenaran), **V**alue (nilai) |
| **Sumber data terbuka** | data.go.id, data.jakarta.go.id, BPS, WHO, World Bank |
| **Structured vs Unstructured** | Structured (CSV/Excel) vs Unstructured (gambar/video/teks) |

#### Pert 2 — Data Cleansing & Labeling

| Teknik | Fungsi |
|---|---|
| **Hapus duplikat** | `drop_duplicates()` |
| **Isi missing value** | Mean imputation (rata-rata), median, modus, forward fill |
| **Deteksi outlier** | IQR (Q1–1.5×IQR, Q3+1.5×IQR), Z-score |
| **Normalisasi** | Min-max scaling → 0–1 |
| **Labeling** | Memberi label/kategori pada data |

#### Pert 3 — Visualisasi Data & Dashboard

| Grafik | Cocok untuk |
|---|---|
| **Bar chart** | Perbandingan kategori |
| **Pie chart** | Proporsi / persentase |
| **Line chart** | Tren waktu |
| **Scatter plot** | Korelasi 2 variabel |
| **Histogram** | Distribusi data |

**Dashboard tools:** Google Looker Studio (gratis), Tableau, Power BI

#### Pert 4 — JSON/CSV & Python

```python
import pandas as pd
df = pd.read_csv('file.csv')
df = pd.read_json('file.json')

df.head()      # 5 baris pertama
df.info()      # info dataset
df.describe()  # statistik
df['kolom']    # akses kolom
df.loc[baris]  # akses baris by label
df.iloc[baris] # akses baris by index
df.sort_values('kolom', ascending=False)
df[df['kolom'] > 80]  # filter
```

#### Pert 5 — Studi Kasus Pipeline

Pipeline analisis data penjualan:
- Load → Clean → Transform → Analyze → Visualize
- Metrik: total revenue, top product, tren regional

#### Pert 6 — PTS

20 PG + 4 Esai — materi Pengolahan Data (Pert 1–5)

#### Pert 7 — Topologi Jaringan

| Topologi | Kelebihan | Kekurangan |
|---|---|---|
| **Bus** | Hemat kabel | Jika kabel putus → semua mati |
| **Star** | Mudah dikelola | Switch = single point of failure |
| **Ring** | Kinerja stabil | Sulit troubleshoot |
| **Mesh** | Sangat andal | Mahal, banyak kabel |
| **Tree** | Skalabel | Konfigurasi kompleks |
| **Hybrid** | Fleksibel | Manajemen sulit |

#### Pert 8 — Cloud Computing

| Model | Contoh | Pengguna |
|---|---|---|
| **IaaS** | AWS EC2, GCP Compute Engine | Admin IT |
| **PaaS** | Google App Engine, Heroku | Developer |
| **SaaS** | Google Drive, Canva, Zoom | End user |

**Karakteristik:** On-demand self-service, broad network access, resource pooling, rapid elasticity, measured service

#### Pert 9 — Troubleshooting Jaringan

| Perintah | Fungsi | OS |
|---|---|---|
| `ping` | Cek koneksi ke host | Windows/Linux/Mac |
| `tracert` / `traceroute` | Lacak rute paket | Windows / Linux-Mac |
| `ipconfig` / `ifconfig` | Lihat konfigurasi IP | Windows / Linux-Mac |
| `nslookup` | Cari IP dari domain | Semua |

**Langkah troubleshooting:** Identifikasi → Isolasi → Uji → Analisis → Perbaiki → Verifikasi

#### Pert 10 — Password Manager & 2FA

| Konsep | Penjelasan |
|---|---|
| **Password manager** | Bitwarden, 1Password, Google Password Manager |
| **2FA** | Dua lapis: password + OTP/TOTP/biometrik |
| **TOTP** | Kode 6 digit, berubah tiap 30 detik (Google Authenticator) |
| **Passkey** | Passwordless — fingerprint/face ID |
| **Backup codes** | Kode cadangan jika HP hilang |

#### Pert 11 — UU ITE & UU PDP

**10 Pasal Kunci UU ITE:**

| Pasal | Pelanggaran | Hukuman |
|---|---|---|
| 27(1) | Konten asusila | 6 th / Rp 1 M |
| 27(3) | Pencemaran nama baik | 4 th / Rp 750 jt |
| 28(1) | Hoaks menyesatkan | 6 th / Rp 1 M |
| 30 | Akses ilegal | 6 th / Rp 600 jt |
| 32 | Intersepsi ilegal | 10 th / Rp 800 jt |
| 35 | Phishing / manipulasi | 12 th / Rp 12 M |

**7 Hak Subjek Data (UU PDP):**
1. Tahu data digunakan untuk apa
2. Akses data pribadi
3. Koreksi data
4. Hapus data
5. Batasi pemrosesan
6. Portabilitas data
7. Tidak diprofilkan untuk keputusan penting

#### Pert 12 — Platform Digital

| Platform | Fitur Keamanan |
|---|---|
| **Marketplace** | Escrow, rating, garansi, 2FA |
| **M-Banking** | OTP, m-Token, device binding, limit transaksi |
| **Dompet Digital** | PIN, 2FA, QRIS, notifikasi |

**Tips aman:**
- Bayar lewat escrow — jangan transfer langsung
- Jangan share OTP ke siapa pun
- Aktivasi 2FA di semua akun
- Waspada phishing — jangan klik link dari SMS/WA

#### Pert 13 — Etika Digital & Demokrasi Digital

| Konsep | Definisi |
|---|---|
| **Netiket** | 10 aturan etika di internet (Virginia Shea) |
| **Misinformasi** | Salah → tanpa niat |
| **Disinformasi** | Salah → sengaja menipu |
| **Malinformasi** | Benar → sengaja merugikan |
| **Filter bubble** | Algoritma hanya menampilkan konten sesuai minat |
| **Echo chamber** | Hanya berinteraksi dengan orang sepaham |
| **Demokrasi digital** | Partisipasi demokrasi via internet |

#### Pert 14 — Proyek Akhir Python

**Pipeline 7 tahap:**

```
LOAD (read_csv) → EXPLORE (head, info) → CLEAN (dropna, drop_duplicates, fillna)
    → TRANSFORM (kolom baru, groupby) → ANALYZE (mean, sort)
    → VISUALIZE (bar, pie, scatter) → EXPORT (to_csv)
```

---

### C. SIMULASI PAS — KUNCI JAWABAN

#### PG (20 Soal)

| 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9 | 10 |
|---|---|---|---|---|---|---|---|---|---|
| a | b | c | b | b | c | b | b | a | b |
| 11 | 12 | 13 | 14 | 15 | 16 | 17 | 18 | 19 | 20 |
| b | b | b | b | c | b | b | b | b | b |

#### Esai (Kunci)

**Esai 1 — Pipeline Python (min 5 tahap):**
1. Load: `pd.read_csv()`
2. Explore: `df.head()`, `df.info()`, `df.describe()`
3. Clean: `df.drop_duplicates()`, `df.fillna()`
4. Transform: kolom baru, `df['Rata'] = df.mean(axis=1)`, `df.groupby()`
5. Analyze: `df.sort_values()`, `df['kolom'].mean()`
6. Visualize: `plt.bar()`, `plt.pie()`, `plt.scatter()`
7. Export: `df.to_csv()`

**Esai 2 — Topologi (4 dari 6):**
- Bus: semua di 1 kabel — hemat, jika putus semua mati
- Star: semua ke switch — mudah kelola, switch=SPoF
- Ring: melingkar — stabil, sulit troubleshoot
- Mesh: semua ke semua — andal, mahal
- Tree: hierarkis — skalabel, kompleks
- Hybrid: kombinasi — fleksibel, sulit manage

**Esai 3 — IaaS/PaaS/SaaS:**
- IaaS: server virtual (AWS EC2, GCP Compute Engine)
- PaaS: platform (Google App Engine, Heroku)
- SaaS: aplikasi (Google Drive, Canva, Zoom)

**Esai 4 — Analisis phishing:**
- Jenis: Phishing — social engineering via SMS
- Kesalahan: panik, klik link, kasih password
- Langkah benar: cek langsung di app Shopee
- Pasal UU ITE: Pasal 35 (manipulasi/penipuan) — 12 th / Rp 12 M
- Lapor: ke platform + patrolisiber.id + polisi

**Esai 5 — Filter bubble & echo chamber:**
- Filter bubble: algoritma hanya tampilkan konten sesuai minat
- Echo chamber: hanya diskusi dengan sepaham
- Dampak demokrasi: polarisasi, ekstremisasi, diskusi sehat hilang
- Cara hindari: ikuti akun beda pandangan, verifikasi silang, cek inkognito, diskusi terbuka

---

### D. RENCANA PEMBELAJARAN KELAS XII

| Semester | Materi |
|---|---|
| 1 (XII) | Machine Learning dasar, Neural Network, AI Ethics, Proyek Klasifikasi |
| 2 (XII) | Cybersecurity (penetration testing, firewall), Big Data lanjutan, Proyek Capstone |

---

**MGMP Informatika SMAN 6 Cimahi**
