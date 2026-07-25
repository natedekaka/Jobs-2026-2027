---
marp: true
theme: uncover
class: invert
---

# PERTEMUAN 4 — FASE F
## Implementasi & Development
### Informatika – Fase F / Kelas XI
#### SMA Negeri 6 Cimahi

---

## Review — Pert 1-3

| Pert | Materi | Output |
|---|---|---|
| 1 | SDLC — 7 tahapan | Mind map |
| 2 | Analisis Kebutuhan | User story |
| 3 | Design — UI/UX | Wireframe |

> Hari ini: **Tahap 4 — Implementation!** Wireframe → Kode!

---

## Apersepsi

"Wireframe yang kalian buat — bagaimana cara mengubahnya jadi aplikasi nyata?"

> Jawabannya: **Coding!**

---

# TUJUAN PEMBELAJARAN

1. ✅ Translasi desain → kode
2. ✅ Frontend, Backend, Database
3. ✅ Version Control (Git)
4. ✅ HTML dari wireframe

---

## Dari Wireframe ke Kode

| Wireframe | → HTML/CSS |
|---|---|
| Kotak header | `<header>` |
| Tombol | `<button>` |
| Form input | `<input>` |
| Warna & font | CSS |

> Wireframe = Denah. HTML = Bangunannya.

---

## 3 Layer Aplikasi

```
┌──────────┐     ┌──────────┐     ┌──────────┐
│ FRONTEND │────▶│ BACKEND  │────▶│ DATABASE │
│ (Browser)│     │ (Server) │     │ (MySQL)  │
├──────────┤     ├──────────┤     ├──────────┤
│ Tampilan │     │ Proses   │     │ Simpan   │
│ HTML/CSS │     │ Python   │     │ Data     │
└──────────┘     └──────────┘     └──────────┘
```

---

## Frontend

Apa yang dilihat pengguna.

| Teknologi | Fungsi |
|---|---|
| **HTML** | Struktur halaman |
| **CSS** | Warna, font, layout |
| **JavaScript** | Interaktivitas |

---

## Backend

Logika di balik layar.

| Tugas | Contoh |
|---|---|
| Proses login | Cek NISN & password |
| Kirim notifikasi | Email/SMS |
| Simpan data | Ke database |

---

## Database

Tempat data disimpan.

| Database | Contoh |
|---|---|
| Relational | MySQL, PostgreSQL |
| Non-relational | MongoDB, Firebase |

---

## Version Control — Git

### Masalah tanpa Git:
❌ "File mana yang terbaru?"
❌ "Kode saya error, kemarin masih jalan"
❌ "Timpak-timpakan dengan teman"

### Git = Solusi!

---

## Konsep Git

| Konsep | Arti |
|---|---|
| **Repository** | Folder proyek |
| **Commit** | Save point — simpan snapshot |
| **Push** | Upload ke GitHub |
| **Pull** | Download dari GitHub |
| **Branch** | Cabang untuk fitur baru |

---

## Alur Git

```
git init         → Buat repo
git add .        → Pilih file
git commit -m "First" → Simpan
git push         → Upload ke GitHub
```

---

## Aktivitas 1: HTML dari Wireframe

### Individu — 20 menit

Dari wireframe Pert 3 → buat HTML!

**Checklist:**
- ✅ DOCTYPE, head, body
- ✅ Form input (min 2 field)
- ✅ Tombol submit
- ✅ CSS (warna, font)
- ✅ Link/ footer

---

## Kode Awal HTML

```html
<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8">
  <title>Login Aplikasi</title>
  <style>
    body { font-family: Arial; }
    .box { width: 300px; margin: auto; }
  </style>
</head>
<body>
  <div class="box">
    <h2>Login</h2>
    <input type="text" placeholder="NISN">
    <input type="password" placeholder="Password">
    <button>MASUK</button>
  </div>
</body>
</html>
```

---

## Aktivitas 2: Eksplorasi GitHub

### Berpasangan — 10 menit

1. Buka `github.com`
2. Cari repository "aplikasi-sekolah"
3. Identifikasi: pemilik, commit, bahasa, README

---

## Aktivitas 3: Simulasi Git

### 5 menit

3 "developer" edit dokumen bersama
1 "Git" mencatat versi

> Lihat bagaimana Git mencegah chaos!

---

## Rangkuman

| Konsep | Inti |
|---|---|
| **Frontend** | Tampilan — HTML/CSS/JS |
| **Backend** | Logika — Python/PHP |
| **Database** | Penyimpanan — MySQL |
| **Git** | Version control |
| **Commit** | Save point |

---

## Tugas Rumah

Sempurnakan HTML + tambah CSS (warna, font, padding)!

> Kirim file `.html` ke guru!

---

## Pertemuan Depan

### Pengujian (Testing) & Debugging
> Cari bug sebelum aplikasi dipakai!

---

# Terima Kasih

### MGMP Informatika SMAN 6 Cimahi

> "Kode yang baik lahir dari proses yang terstruktur."
