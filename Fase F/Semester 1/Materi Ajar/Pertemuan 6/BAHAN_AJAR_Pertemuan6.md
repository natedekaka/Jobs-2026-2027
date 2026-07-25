# BAHAN AJAR – PERTEMUAN 6
## Deployment & CI/CD

| TP | BK, AP — Proses Rekayasa |
|---|---|

---

### A. APA ITU DEPLOYMENT?

**Deployment** adalah proses memindahkan aplikasi dari lingkungan pengembangan (lokal) ke lingkungan produksi (server) sehingga dapat diakses oleh pengguna.

#### Analogi: Restoran

| Restoran | Aplikasi |
|---|---|
| Resep masakan | **Kode** yang sudah ditulis (Pert 4) |
| Uji rasa dulu | **Testing** (Pert 5) |
| **Sajikan ke pelanggan** | **Deployment** (Pert 6) |
| Meja, piring, restoran | **Server / Hosting** |

#### Perbedaan Lingkungan

| Lingkungan | Tujuan | Siapa yang Akses? |
|---|---|---|
| **Development** (lokal) | Menulis & menguji kode | Developer sendiri |
| **Staging** | Uji coba mirip produksi | Tim internal, tester |
| **Production** | Dipakai user sungguhan | Semua pengguna |

---

### B. JENIS HOSTING

**Hosting** adalah layanan penyewaan ruang server untuk menyimpan dan menjalankan aplikasi.

#### 1. Shared Hosting

Satu server fisik dipakai bersama banyak pengguna.

```
┌─────────────────────────────────────┐
│          1 SERVER FISIK             │
├──────────┬──────────┬───────────────┤
│ Website  │ Website  │   Website     │
│  User A  │  User B  │   User C      │
│ WordPress│ Laravel  │   HTML saja   │
└──────────┴──────────┴───────────────┘
```

**Cocok untuk**: Website sederhana, blog, landing page
**Biaya**: ~Rp50.000–200.000/bulan
**Contoh**: Niagahoster, Rumahweb

#### 2. VPS (Virtual Private Server)

Satu server fisik dibagi secara virtual — tiap pengguna punya "komputer virtual" sendiri.

| Kelebihan | Full akses root, bebas install apapun |
|---|---|
| Kekurangan | Harus atur server sendiri |
| Biaya | ~Rp100.000–500.000/bulan |
| Contoh | DigitalOcean, Vultr, Linode |

#### 3. Cloud Hosting

Infrastruktur raksasa (AWS, Google Cloud, Azure) — bayar sesuai pemakaian.

| Kelebihan | Skalabel otomatis, andal, global |
|---|---|
| Kekurangan | Bisa mahal jika tidak diatur |
| Contoh | AWS EC2, Google Cloud Run, Azure App Service |

#### 4. Static Hosting (Gratis!)

Untuk website frontend (HTML, CSS, JS) tanpa backend.

| Platform | Domain | Fitur |
|---|---|---|
| **Netlify** | `namamu.netlify.app` | Drag & drop deploy, CI/CD otomatis |
| **Vercel** | `namamu.vercel.app` | Integrasi GitHub auto-deploy |
| **GitHub Pages** | `username.github.io` | Gratis dari repositori GitHub |

---

### C. DOMAIN & DNS

| Istilah | Arti | Analogi |
|---|---|---|
| **Domain** | Nama website | Alamat rumah |
| **IP Address** | Angka unik server | Koordinat GPS |
| **DNS** | Penerjemah domain → IP | Buku alamat |
| **TLD** | .com, .id, .net, .sch.id | Jenis jalan (perumahan, sekolah) |

#### Cara Kerja DNS

```
User ketik: sman6cimahi.sch.id
           │
           ▼
    DNS Server ─── "IP 103.x.x.x"
           │
           ▼
    Browser ambil data dari server IP tersebut
```

---

### D. CI/CD — CONTINUOUS INTEGRATION & CONTINUOUS DEPLOYMENT

#### Masalah Tanpa CI/CD

```
Developer           Server Produksi
    │                     │
    ├─── edit kode        │
    ├─── commit git       │
    ├─── "Tolong di-deploy" → ── manual FTP
    ├─── edit kode lagi   │
    ├─── commit git       │
    ├─── "Deploy lagi ya" → ── manual SSH
    │                     │   ❌ Lupa? Aplikasi usang!
```

#### Dengan CI/CD

```
Developer commit ──► CI (test otomatis) ──► CD (deploy otomatis) ──► User
   ke GitHub          ├── Lint code            ├── Build
                      ├── Unit test            ├── Upload ke server
                      ├── Integration test     ├── Restart server
                      └── ✅ lolos             └── ✅ Selesai!
```

#### CI/CD Pipeline — Visual

```
┌─────────┐   ┌─────────┐   ┌─────────┐   ┌─────────┐
│ git push│──▶│  CI     │──▶│  CD     │──▶│  LIVE!  │
│         │   │ Test    │   │ Deploy  │   │  🚀     │
└─────────┘   └─────────┘   └─────────┘   └─────────┘
```

#### Alur CI/CD Sederhana (Netlify)

```
1. Buat repositori GitHub berisi HTML
2. Hubungkan ke Netlify
3. Setiap kali git push ke GitHub:
   └── Netlify otomatis build & deploy
       └── URL langsung update!
```

#### Keuntungan CI/CD

| Keuntungan | Penjelasan |
|---|---|
| **Otomatis** | Tidak perlu deploy manual |
| **Cepat** | Rilis fitur baru dalam hitungan menit |
| **Aman** | Setiap perubahan di-test dulu |
| **Tidak ada "error karena lupa deploy"** | Selalu versi terbaru |

---

### E. LANGKAH DEPLOY KE NETLIFY

#### 1. Siapkan File
- Pastikan file utama bernama `index.html`
- Semua file dalam 1 folder

#### 2. Deploy ke Netlify
- Buka `netlify.com`
- Login dengan Google/GitHub
- Klik **"Sites" → "Drag and drop your site folder here"**
- Drag folder HTML yang sudah siap
- Tunggu beberapa detik → website online!
- URL contoh: `https://random-name-123456.netlify.app`

#### 3. Custom Domain (Opsional)
- Bisa pakai domain sendiri
- Atau biarkan domain `.netlify.app` gratis

---

### F. RANGKUMAN

| Konsep | Inti |
|---|---|
| **Deployment** | Memindahkan kode → server → publik |
| **Hosting** | Tempat menyewa server |
| **Shared / VPS / Cloud** | Jenis hosting (murah → mahal) |
| **Static Hosting** | Netlify, Vercel — gratis untuk frontend |
| **CI/CD** | Otomatis test + deploy setiap commit |
| **Domain** | Nama website |
| **DNS** | Penerjemah domain → IP |

---

**MGMP Informatika SMAN 6 Cimahi**
