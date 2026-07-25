---
marp: true
theme: uncover
class: invert
---

# PERTEMUAN 6 — FASE F
## Deployment & CI/CD
### Informatika – Fase F / Kelas XI
#### SMA Negeri 6 Cimahi

---

## Review — SDLC Journey

| Pert | Tahap SDLC | Output |
|---|---|---|
| 1 | Perencanaan | Mind map SDLC |
| 2 | Analisis Kebutuhan | User story |
| 3 | Design | Wireframe |
| 4 | Implementasi | HTML |
| 5 | Testing | Test case |

> Hari ini: **Deployment** — aplikasi siap dipakai!

---

## Apersepsi

"Kode HTML kalian — sejauh ini cuma bisa dibuka di komputer sendiri. Bagaimana cara orang lain mengaksesnya?"

> Jawaban: **Deployment!**

---

# TUJUAN PEMBELAJARAN

1. ✅ Konsep deployment
2. ✅ Jenis hosting
3. ✅ CI/CD — otomatisasi deploy
4. ✅ Deploy HTML ke Netlify

---

## Deployment?

**Proses memindahkan aplikasi dari komputer developer ke server agar bisa diakses publik.**

### Analogi: Restoran

| Restoran | Aplikasi |
|---|---|
| Masak | Coding |
| Uji rasa | Testing |
| **Sajikan** | **Deployment** |

---

## 3 Lingkungan Aplikasi

```
Development ──► Staging ──► Production
  (coding)      (uji coba)     (live!)
```

| Lingkungan | Pengguna |
|---|---|
| Development | Developer saja |
| Staging | Tim internal |
| Production | Semua user! |

---

## Jenis Hosting

| Jenis | Analogi | Biaya |
|---|---|---|
| **Shared** | Kos-kosan | ~Rp50rb/bln |
| **VPS** | Rumah sendiri | ~Rp200rb/bln |
| **Cloud** | Hotel bintang 5 | Bayar pemakaian |
| **Static** | Pameran lukisan | **Gratis!** |

> Static Hosting (Netlify, Vercel) = **Gratis** untuk HTML/CSS/JS!

---

## Domain & DNS

```
Domain: sman6cimahi.sch.id
            │
            ▼
    DNS → IP 103.x.x.x
            │
            ▼
    Browser ambil data dari server
```

| Istilah | Arti |
|---|---|
| Domain | Nama website |
| DNS | Buku alamat internet |

---

## CI/CD — Otomatisasi!

### Tanpa CI/CD:
```
Edit → Commit → "Tolong deploy" → FTP manual → Lupa → ❌
```

### Dengan CI/CD:
```
git push → Test otomatis → Deploy otomatis → ✅ Live!
```

---

## CI/CD Pipeline

```
┌─────────┐   ┌─────────┐   ┌─────────┐   ┌─────────┐
│ git push│──▶│  CI     │──▶│  CD     │──▶│  LIVE!  │
│         │   │ Test    │   │ Deploy  │   │  🚀     │
└─────────┘   └─────────┘   └─────────┘   └─────────┘
```

| CI | CD |
|---|---|
| Test otomatis | Deploy otomatis |
| Cek kualitas | Upload ke server |

---

## Aktivitas 1: Deploy ke Netlify

### Individu — 20 menit

1. Buka **netlify.com**
2. Login dengan Google/GitHub
3. **Drag & drop** folder HTML Pert 4
4. Tunggu 10–30 detik
5. **Catat URL** yang muncul!

> Website kalian sekarang LIVE di internet! 🎉

---

## Aktivitas 2: Pipeline Diagram

### Berpasangan — 10 menit

Gambar pipeline CI/CD di kertas:
```
git push → ? → ? → ?
```

---

## Aktivitas 3: Timeline Deploy

### 5 menit

Simulasi timeline deploy aplikasi sekolah:

```
Commit → CI test → Build → Deploy → User bisa akses!
```

---

## Rangkuman

| Konsep | Inti |
|---|---|
| **Deployment** | Kode → Server → Publik |
| **Shared / VPS / Cloud** | Jenis hosting |
| **Netlify / Vercel** | Static hosting gratis |
| **CI/CD** | Otomatis test + deploy |

---

## Tugas Rumah

Screenshot halaman yang sudah di-deploy + catat URL!

> Kirim ke guru!

---

## Pertemuan Depan

### PTS — Review Pert 1-6

> Persiapkan materi dari SDLC sampai Deployment!

---

# Terima Kasih

### MGMP Informatika SMAN 6 Cimahi

> "Kode yang hebat tidak berguna jika tidak bisa diakses siapa pun."
