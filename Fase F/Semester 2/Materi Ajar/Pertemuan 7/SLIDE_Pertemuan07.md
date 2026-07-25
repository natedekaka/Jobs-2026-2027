---
marp: true
theme: uncover
class: invert
---

# PERTEMUAN 7 — FASE F (S2)
## Model Jaringan Komputer & Topologi
### Informatika – Fase F / Kelas XI
#### SMA Negeri 6 Cimahi

---

## Review — Pert 1–5

```
Pengolahan Data ✅
PTS ✅ (atau tidak)

Sekarang: materi baru!
MODEL JARINGAN & TOPOLOGI 🔌
```

---

## Apersepsi

30 komputer di lab — terhubung ke 1 switch.

> Kabel 1 komputer putus → yang lain masih nyala?

> Kabel switch putus → semua mati?

> **Itu TOPOLOGI!**

---

## Tujuan Pembelajaran

1. ✅ Klasifikasi jaringan (PAN–WAN)
2. ✅ 5 topologi jaringan
3. ✅ Analisis ± topologi
4. ✅ Pilih topologi tepat

---

## Review Jaringan

| Jenis | Jarak | Contoh |
|---|---|---|
| **PAN** | 1–10 m | Bluetooth |
| **LAN** | 10 m – 1 km | Lab sekolah |
| **MAN** | 1–100 km | Wi-Fi kota |
| **WAN** | > 100 km | Internet |

---

## Perangkat Jaringan

```
MODEM → ROUTER → SWITCH → PC
                  │
              ACCESS POINT (Wi-Fi)
```

---

## 5 Topologi Jaringan

```
1. BUS      — satu kabel backbone
2. STAR     — switch pusat
3. RING     — melingkar
4. MESH     — semua ke semua
5. TREE     — bercabang
```

---

## Bus — Hemat Kabel

```
💻──💻──💻──💻
          │
        🖨️

✅ Hemat kabel
❌ 1 putus = semua mati
```

---

## Star — Paling Populer

```
      💻
      │
💻──🔄SWITCH──💻
      │
      💻

✅ 1 putus → hanya 1 mati
❌ Switch mati → semua mati
```

---

## Ring — Token Passing

```
💻────💻
│      │
💻────💻

✅ Data teratur
❌ 1 putus = semua mati
```

---

## Mesh — Paling Andal

```
💻 ── 💻
│\  /│
│ \/ │
│ /\ │
│/  \│
💻 ── 💻

✅ Sangat andal
❌ Sangat mahal!
```

Rumus kabel: **n × (n-1) / 2**

---

## Tree — Gedung Bertingkat

```
     🔄 ROOT
    /      \
  🔄      🔄
 /  \    /  \
💻  💻  💻  💻

✅ Cocok per lantai
❌ Root mati → semua mati
```

---

## Perbandingan

| Topologi | Biaya | Andal | Troubleshoot |
|---|---|---|---|
| Bus | ✅ Hemat | ❌ Rendah | ❌ Sulit |
| Star | ⚠️ Sedang | ✅ Tinggi | ✅ Mudah |
| Ring | ✅ Hemat | ❌ Rendah | ❌ Sulit |
| Mesh | ❌ Mahal | ✅✅ Tinggi | ✅ Mudah |
| Tree | ⚠️ Sedang | ⚠️ Sedang | ⚠️ Sedang |

---

## Aktivitas 1 — Simulasi Tali

### 25 menit — Kelompok

Kelompok A–E, masing-masing 1 topologi

> Guru putuskan kabel → lihat dampak!

```
Bus:    kabel putus → semua mati?
Star:   kabel putus → hanya 1?
Mesh:   kabel putus → lewat jalur lain?
```

---

## Aktivitas 2 — Gambar & Analisis

### 20 menit — Individu

Gambar topologi + tulis:
```
✅ Nama
✅ Cara kerja
✅ 2 kelebihan
✅ 2 kekurangan
✅ Contoh nyata
```

---

## Aktivitas 3 — Studi Kasus Sekolah

### 20 menit — Berpasangan

```
5 LAB + Perpustakaan + Ruang Guru
115 komputer total
```

Pilih topologi → gambar → alasan

> Presentasi!

---

## Refleksi

- Topologi paling andal?
- Paling hemat?
- Untuk sekolah, pilih mana?
- Skala 1–10?

---

## Tugas Rumah

> Cari 1 jaringan di sekitar rumah/sekolah → identifikasi topologinya!

---

## Preview — Pert 8

### Cloud Computing ☁️

> IaaS, PaaS, SaaS — komputasi awan!

---

# Terima Kasih

### MGMP Informatika SMAN 6 Cimahi

> "Pilih topologi yang tepat — bukan yang termurah atau tercanggih, tapi yang sesuai kebutuhan!"
