---
marp: true
theme: uncover
class: invert
---

# PERTEMUAN 3 — FASE F
## Perancangan (Design) & UI/UX
### Informatika – Fase F / Kelas XI
#### SMA Negeri 6 Cimahi

---

## Review — Pert 1 & 2

| Pert | Materi | Output |
|---|---|---|
| 1 | SDLC — 7 tahapan | Mind map SDLC |
| 2 | Analisis Kebutuhan | User story, F/NF |

> Hari ini: **Tahap 3 — Design!** Dari daftar kebutuhan → tampilan visual!

---

## Apersepsi

"Buka aplikasi favorit kalian — perhatikan tata letak, warna, tombol."

> Itu semua adalah hasil **design**!

---

# TUJUAN PEMBELAJARAN

1. ✅ Output tahap design (wireframe, mockup, prototype)
2. ✅ UI vs UX
3. ✅ Prinsip desain yang baik
4. ✅ Membuat wireframe

---

## Output Tahap Design

| Output | Deskripsi |
|---|---|
| **Wireframe** | Sketsa kerangka — hitam putih |
| **Mockup** | Desain visual — warna, font |
| **Prototype** | Mockup interaktif — bisa diklik |
| **ERD** | Struktur database |
| **User Flow** | Alur pengguna |

---

## Wireframe → Mockup → Prototype

```
Wireframe       Mockup          Prototype
┌──────┐       ┌──────┐        ┌──────┐
│ Logo │       │ 🔵   │        │ klik→│
│      │  →    │ Warna│   →    │berpi│
│ [   ]│       │ Font │        │ndah!│
└──────┘       └──────┘        └──────┘
Sketsa         Visual          Interaktif
```

---

## UI vs UX

| UI | UX |
|---|---|
| Tampilan | Pengalaman |
| Warna, font, tombol | Mudah, cepat, nyaman |
| "Bagaimana tampilannya?" | "Bagaimana rasanya?" |
| **Antarmuka** | **Pengalaman** |

> UI yang baik + UX yang baik = Produk sukses!

---

## UI vs UX — Analogi Restoran

| UI | UX |
|---|---|
| Desain menu — font, gambar, warna | Kemudahan memilih menu |
| Dekorasi restoran | Kecepatan pelayanan |
| Seragam pelayan | Keramahan pelayan |

> Restoran cantik tapi pelayanan lambat = **UI baik, UX buruk**

---

## Prinsip 1: Konsisten

Elemen yang sama harus terlihat sama di seluruh halaman.

| ❌ | ✅ |
|---|---|
| Tombol simpan berubah posisi | Tombol selalu di kanan atas |
| Warna menu berbeda tiap halaman | Warna konsisten |

---

## Prinsip 2: Sederhana

Jangan membebani pengguna.

| ❌ Terlalu Ramai | ✅ Sederhana |
|---|---|
| 15 menu di homepage | 3–5 menu utama |
| 10 warna berbeda | 2–3 warna utama |
| Paragraf panjang | Poin singkat |

---

## Prinsip 3: Umpan Balik

Pengguna harus tahu aksinya diproses.

| Aksi | Feedback |
|---|---|
| Klik tombol | Tombol berubah warna |
| Loading | Animasi / progress bar |
| Error | Pesan jelas (bukan "Error 500") |
| Berhasil | Notifikasi hijau ✅ |

---

## Prinsip 4: Toleransi Error

Pengguna boleh salah — bisa diperbaiki.

| ❌ | ✅ |
|---|---|
| Hapus langsung hilang | "Yakin hapus?" + undo |
| Tidak bisa kembali | Tombol "Kembali" |
| Form hilang jika error | Data tetap terisi |

---

## Aktivitas 1: Analisis UI/UX

### Individu — 10 menit

Buka 1 aplikasi favorit.

| | Analisis |
|---|---|
| **UI** | Warna, font, tata letak |
| **UX** | Mudah? Feedback? Nyaman? |

> Catat 1 hal baik + 1 hal yang bisa diperbaiki!

---

## Aktivitas 2: Wireframe

### Berpasangan — 15 menit

Dari hasil analisis kebutuhan (Pert 2):
- Pilih **1 fitur utama**
- Buat wireframe di kertas

**Yang harus ada:**
✅ Header (logo, judul)
✅ Konten utama
✅ Navigasi
✅ Label elemen

---

## Contoh Wireframe — Login

```
┌────────────────────────┐
│ [LOGO]                 │
│   Masuk ke Akun        │
│                        │
│ ┌──────────────────┐   │
│ │ NISN              │   │
│ └──────────────────┘   │
│ ┌──────────────────┐   │
│ │ Password          │   │
│ └──────────────────┘   │
│ ┌──────────────────┐   │
│ │     MASUK        │   │
│ └──────────────────┘   │
│ Lupa password?         │
│ Belum daftar?           │
└────────────────────────┘
```

---

## Aktivitas 3: Peer Review

### 10 menit

Tukar wireframe dengan kelompok lain!

Berikan masukan:
- Apa yang kurang?
- Apa yang membingungkan?
- Saran perbaikan

---

## Rangkuman

| Konsep | Inti |
|---|---|
| **Wireframe** | Sketsa kerangka |
| **UI** | Tampilan (warna, font) |
| **UX** | Pengalaman (mudah, nyaman) |
| **Prinsip** | Konsisten, sederhana, feedback, toleransi |

---

## Tugas Rumah

Sempurnakan wireframe berdasarkan review!

---

## Pertemuan Depan

### Implementasi & Development
> Desain → Kode! Wireframe jadi aplikasi nyata!

---

# Terima Kasih

### MGMP Informatika SMAN 6 Cimahi

> "Desain yang baik adalah desain yang tidak terasa — karena semuanya sudah sesuai harapan."
