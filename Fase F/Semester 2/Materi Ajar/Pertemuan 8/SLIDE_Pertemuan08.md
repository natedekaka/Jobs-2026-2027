---
marp: true
theme: uncover
class: invert
---

# PERTEMUAN 8 — FASE F (S2)
## Cloud Computing ☁️
### Informatika – Fase F / Kelas XI
#### SMA Negeri 6 Cimahi

---

## Review — Pert 7

```
Topologi jaringan → bagaimana perangkat terhubung

Sekarang:
Bagaimana APLIKASI jalan di "AWAN"?
```

---

## Apersepsi

> Google Drive, Colab, Netflix, Spotify, Zoom

**Semua itu CLOUD COMPUTING!** ☁️

Data & aplikasi bukan di laptop kalian —
tapi di server Google / AWS!

---

## Tujuan Pembelajaran

1. ✅ Konsep cloud computing
2. ✅ IaaS vs PaaS vs SaaS
3. ✅ Kelebihan & risiko cloud
4. ✅ Praktik Google Colab

---

## Apa itu Cloud Computing?

> Komputasi via internet — bayar sesuai pemakaian

| Tradisional | Cloud |
|---|---|
| Beli server | Sewa server |
| Bayar di muka | Bayar per jam |
| Tim IT sendiri | Provider urus |

---

## Model Layanan — Diagram

```
IaaS:           PaaS:           SaaS:
┌──────┐       ┌──────┐       ┌──────┐
│ App  │──kelola│ App  │──kelola│ App  │──pakai
│ Data │       │ Data │       ├──────┤
├──────┤       ├──────┤       │ Data │
│ OS   │       │ OS   │       │ OS   │
│ Server│──     │ Server│──    │ Server│──
│ Jaringan│provider│ Jaringan│provider│ Jaringan│provider
└──────┘       └──────┘       └──────┘
```

---

## IaaS — Infrastructure as a Service

> Sewa server, storage, jaringan — kontrol tinggi

| Contoh | AWS EC2, Google Drive, DigitalOcean |
|---|---|
| Kelola | OS, middleware, aplikasi |
| Target | Admin IT |

---

## PaaS — Platform as a Service

> Platform untuk deploy aplikasi — fokus coding!

| Contoh | **Google Colab**, Heroku, Firebase, Vercel |
|---|---|
| Kelola | Aplikasi saja |
| Target | Developer |

---

## SaaS — Software as a Service

> Aplikasi jadi — tinggal pakai!

| Contoh | Gmail, Google Sheets, Netflix, Zoom, Canva |
|---|---|
| Kelola | Tidak ada |
| Target | Semua orang |

---

## Perbandingan

| Aspek | IaaS | PaaS | SaaS |
|---|---|---|---|
| Kontrol | ✅ Tinggi | ⚠️ Sedang | ❌ Rendah |
| Kelola | OS + middleware | Aplikasi | Tidak ada |
| Contoh | AWS EC2 | Google Colab | Gmail |

---

## Kelebihan Cloud

| ✅ Hemat | Bayar sesuai pakai |
|---|---|
| ✅ Skalabel | Tambah instant |
| ✅ Akses | Di mana saja |
| ✅ Aman | Provider jaga |

---

## Risiko Cloud

| ❌ Downtime | Internet mati → tidak bisa akses |
|---|---|
| ❌ Keamanan | Data di server orang lain |
| ❌ Vendor lock-in | Sulit pindah provider |
| ❌ Biaya | Lupa matikan server → tagihan! |

---

## Google Colab — PaaS Gratis!

```
Colab = Jupyter Notebook di cloud Google

Spesifikasi GRATIS:
🧠 CPU Intel Xeon 2 core
💾 RAM 12–25 GB
🎮 GPU NVIDIA Tesla (terbatas)
```

> Buka: colab.research.google.com

---

## Aktivitas 1 — Colab

### 25 menit — Individu

```
🐍 Cek spesifikasi server Google!
📊 Buat file CSV → download
💡 Refleksi: beda Colab vs lokal?
```

---

## Aktivitas 2 — Klasifikasi

### 20 menit — Berpasangan

8 layanan → IaaS / PaaS / SaaS?

```
AWS EC2, Google Sheets, Colab,
Netflix, Google Drive, Heroku,
Zoom, Firebase
```

---

## Aktivitas 3 — Studi Kasus

### 30 menit — Kelompok

| Tim | Kasus | Pilih Cloud? |
|---|---|---|
| A | Startup web — budget kecil | |
| B | Sekolah — email + dokumen | |
| C | Peneliti — GPU AI | |
| D | Bank — database sensitif | |

---

## Refleksi

- Aplikasi cloud favorit kalian?
- Risiko cloud paling penting?
- Skala 1–10?

---

## Tugas Rumah

> Buat 1 aplikasi Colab (kalkulator / konversi suhu / tebak angka)!

---

## Preview — Pert 9

### Troubleshooting Jaringan 🔧

> ping, traceroute, ipconfig — jadi admin jaringan!

---

# Terima Kasih

### MGMP Informatika SMAN 6 Cimahi

> "Cloud = komputasi yang bisa diakses dari mana saja, kapan saja!"
