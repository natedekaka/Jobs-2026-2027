# BAHAN AJAR – PERTEMUAN 8 (S2)
## Cloud Computing

| TP | BK, LD — Konsep Sistem dan Keamanan Jaringan Komputer |
|---|---|

---

### A. APA ITU CLOUD COMPUTING?

#### Definisi

> **Cloud Computing** = penyediaan sumber daya komputasi (server, storage, database, software, analitik, AI) melalui internet — bayar sesuai pemakaian (pay-as-you-go).

#### Analogi Tradisional vs Cloud

| Aspek | Tradisional (On-Premise) | Cloud |
|---|---|---|
| Server | Beli & rawat sendiri | Sewa dari provider |
| Biaya | Kapital besar di awal | Operasional bulanan |
| Skalabilitas | Beli server baru (lama) | Tambah kapasitas instant |
| Maintenance | Tim IT sendiri | Provider |
| Akses | Dalam kantor | Dari mana saja |

#### Karakteristik Cloud (NIST Definition)

| Karakteristik | Penjelasan |
|---|---|
| **On-demand self-service** | Pengguna bisa provisioning resource tanpa interaksi manusia |
| **Broad network access** | Akses via internet dari berbagai perangkat |
| **Resource pooling** | Resource multi-tenant — dibagi banyak pengguna |
| **Rapid elasticity** | Skala naik/turun cepat — otomatis |
| **Measured service** | Bayar sesuai pemakaian (metered) |

---

### B. MODEL LAYANAN CLOUD

#### 1. IaaS (Infrastructure as a Service)

```
┌──────────────────────────────┐
│        APLIKASI              │ ← kelola pengguna
│        DATA                  │
│        RUNTIME               │
│        MIDDLEWARE            │
│        OS (Linux/Windows)    │
├──────────────────────────────┤
│        VIRTUALISASI          │ ← kelola penyedia
│        SERVER                │
│        STORAGE               │
│        JARINGAN              │
└──────────────────────────────┘
```

**Contoh:**
- AWS EC2 — virtual server
- Google Compute Engine — VM di Google Cloud
- DigitalOcean Droplets — server sederhana
- Google Drive / Dropbox — cloud storage

**Cocok untuk:**
- Admin IT yang ingin kontrol penuh
- Migrasi server tradisional ke cloud
- Hosting database, aplikasi kustom

#### 2. PaaS (Platform as a Service)

```
┌──────────────────────────────┐
│        APLIKASI              │ ← kelola pengguna
│        DATA                  │
├──────────────────────────────┤
│        RUNTIME               │ ← kelola penyedia
│        MIDDLEWARE            │
│        OS                    │
│        SERVER                │
│        STORAGE               │
│        JARINGAN              │
└──────────────────────────────┘
```

**Contoh:**
- Google App Engine — deploy aplikasi web
- **Google Colab** — Jupyter Notebook di cloud
- Heroku — hosting app
- Firebase — backend mobile
- Vercel / Netlify — hosting statis

**Cocok untuk:**
- Developer yang ingin fokus coding, bukan管理 server
- Deploy aplikasi cepat
- Prototyping dan MVP

#### 3. SaaS (Software as a Service)

```
┌──────────────────────────────┐
│        APLIKASI              │ ← kelola pengguna
├──────────────────────────────┤
│        DATA                  │ ← kelola penyedia
│        RUNTIME               │
│        MIDDLEWARE            │
│        OS                    │
│        SERVER                │
│        STORAGE               │
│        JARINGAN              │
└──────────────────────────────┘
```

**Contoh:**
- Google Workspace (Gmail, Google Docs, Sheets, Drive)
- Microsoft 365 (Word, Excel, Teams)
- Canva — design online
- Spotify — streaming musik
- Netflix — streaming video
- Zoom — video conference
- Figma — design kolaborasi

**Cocok untuk:**
- Pengguna umum — tinggal pakai
- Kolaborasi tim
- Tidak perlu instalasi

#### Perbandingan

| Karakteristik | IaaS | PaaS | SaaS |
|---|---|---|---|
| Kontrol | ✅ Tinggi | ⚠️ Sedang | ❌ Rendah |
| Kelola sendiri | OS, middleware | Aplikasi | Tidak ada |
| Contoh | AWS EC2 | Google Colab | Gmail |
| Pengguna target | Admin IT | Developer | End user |
| Biaya | Per jam/GB | Per penggunaan | Per user/bulan |
| Kecepatian deploy | Lambat | Sedang | Instant |

---

### C. MODEL DEPLOYMENT CLOUD

| Model | Deskripsi | Contoh |
|---|---|---|
| **Public Cloud** | Resource dibagi banyak pengguna via internet | AWS, Google Cloud, Azure |
| **Private Cloud** | Resource khusus 1 organisasi (on-premise atau hosted) | Cloud internal bank |
| **Hybrid Cloud** | Gabungan public + private | Public untuk web, private untuk database |
| **Multi-Cloud** | Pakai > 1 public cloud | AWS + Google Cloud |

---

### D. KELEBIHAN & RISIKO CLOUD

#### Kelebihan

| Kelebihan | Penjelasan |
|---|---|
| **Hemat biaya** | Tidak beli server, bayar sesuai pakai |
| **Skalabilitas** | Tambah kapasitas instant — otomatis |
| **Reliabilitas** | Data tersebar di banyak server → tidak mudah hilang |
| **Keamanan** | Provider investasi besar untuk keamanan |
| **Akses global** | Dari mana saja, perangkat apa saja |
| **Update otomatis** | Provider管理 maintenance |

#### Risiko

| Risiko | Penjelasan | Mitigasi |
|---|---|---|
| **Downtime** | Internet mati → tidak bisa akses | Backup lokal, SLA |
| **Keamanan data** | Data di server orang lain | Enkripsi, compliance |
| **Vendor lock-in** | Susah pindah provider | Gunakan standar terbuka |
| **Biaya tak terduga** | Lupa matikan server → tagihan besar | Budget alert |
| **Privasi** | Data sensitive di cloud publik | Private cloud untuk data sensitif |

---

### E. GOOGLE COLAB — PRAKTIK CLOUD

**Google Colab** adalah PaaS — Jupyter Notebook gratis di cloud Google.

#### Kelebihan Colab

| Fitur | Spesifikasi |
|---|---|
| CPU | Intel Xeon 2 core (gratis) |
| RAM | 12–25 GB (gratis) |
| GPU | NVIDIA Tesla T4/K80 (gratis, terbatas) |
| Disk | 100 GB (gratis) |
| Storage | Terhubung Google Drive |
| Biaya | **Gratis!** |

#### Cara Penggunaan

| Langkah | Cara |
|---|---|
| 1. Buka | `colab.research.google.com` |
| 2. Login | Akun Google |
| 3. Notebook | File → New notebook |
| 4. Kode | Tulis Python → Shift+Enter untuk jalan |
| 5. GPU | Runtime → Change runtime type → GPU |
| 6. Simpan | Otomatis ke Google Drive |

---

### F. CLOUD DI INDONESIA

| Provider | Region Jakarta | Layanan |
|---|---|---|
| **Google Cloud** | ✅ (asia-southeast2) | Compute, Storage, AI, Colab |
| **AWS** | ✅ (ap-southeast-3) | EC2, S3, Lambda, RDS |
| **Azure** | ✅ (Southeast Asia) | VM, SQL, AI |
| **BTI Cloud** | ✅ | IaaS lokal |
| **Biznet Gio** | ✅ | Cloud & data center |
| **IDCloudHost** | ✅ | Hosting & cloud |

---

### G. RANGKUMAN

| Konsep | Inti |
|---|---|
| **Cloud Computing** | Komputasi via internet — bayar sesuai pakai |
| **IaaS** | Sewa infra (server, storage) — kontrol tinggi |
| **PaaS** | Platform untuk deploy aplikasi — fokus coding |
| **SaaS** | Aplikasi jadi — tinggal pakai |
| **Colab** | PaaS gratis dari Google — Python di cloud |
| **Risiko** | Downtime, keamanan, vendor lock-in |

---

**MGMP Informatika SMAN 6 Cimahi**
