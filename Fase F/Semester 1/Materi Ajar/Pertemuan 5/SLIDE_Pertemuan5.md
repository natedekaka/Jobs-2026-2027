---
marp: true
theme: uncover
class: invert
---

# PERTEMUAN 5 — FASE F
## Pengujian (Testing) & Debugging
### Informatika – Fase F / Kelas XI
#### SMA Negeri 6 Cimahi

---

## Review — Pert 1-4

| Pert | Materi | Output |
|---|---|---|
| 1 | SDLC — 7 tahapan | Mind map |
| 2 | Analisis Kebutuhan | User story |
| 3 | Design — UI/UX | Wireframe |
| 4 | Implementasi & Development | HTML |

> Hari ini: **Testing & Debugging!** Pastikan kode tidak error!

---

## Apersepsi

"Pernah main game yang tiba-tiba force close? Atau aplikasi crash pas lagi dipakai?"

> Itu karena **bug** — dan testing yang kurang!

---

# TUJUAN PEMBELAJARAN

1. ✅ Pentingnya testing
2 ✅ Jenis-jenis testing
3. ✅ Debugging sederhana
4. ✅ Test case

---

## Dampak Bug — Kasus Nyata

| Kasus | Dampak |
|---|---|
| Mars Climate Orbiter 1999 | Satelit hancur — $327M |
| Knight Capital 2012 | Rugi $440M — 45 menit! |
| Boeing 737 MAX 2018 | 346 orang meninggal |
| CrowdStrike 2024 | BSOD jutaan komputer |

> Testing itu **nyawa aplikasi!**

---

## Piramida Testing

```
        ╱╲
       ╱UAT╲
      ╱─────╲
     ╱System╲
    ╱─────────╲
   ╱Integration╲
  ╱───────────────╲
 ╱   Unit Test     ╲
╱─────────────────────╲
```

---

## Jenis Testing

| Jenis | Analogi |
|---|---|
| **Unit Test** | Cek satu bata |
| **Integration** | Cek susunan bata |
| **System Test** | Cek seluruh rumah |
| **UAT** | Pemilik periksa rumah |

---

## Black-box vs White-box

| | Black-box | White-box |
|---|---|---|
| Fokus | Input→Output | Struktur kode |
| Lihat kode? | ❌ Tidak | ✅ Ya |

---

## Apa itu Test Case?

**Test Case** = Skenario uji fitur

| ID | Skenario | Input | Expected |
|---|---|---|---|
| TC-01 | Login sukses | NISN: 12345, PW: abcde | Dashboard muncul |
| TC-02 | NISN salah | NISN: 99999 | "NISN tidak ditemukan" |
| TC-03 | Password salah | PW: xxxxx | "Password salah" |
| TC-04 | Input kosong | (kosong) | "Harap isi" |

---

## Aktivitas 1: Debugging HTML

### Individu — 15 menit

5 bug dalam kode HTML — temukan & perbaiki!

```
<body>
  <h1>Judul<h1>      ← tag tidak ditutup
  <p>Paragraf</p       ← lupa >
</body>
```

---

## Aktivitas 2: Buat Test Case

### Berpasangan — 15 menit

Dari user story login:
> "Sebagai siswa, saya ingin login agar bisa mengakses nilai"

Buat 4 test case:
1. ✅ Positif (sukses)
2. ❌ Negatif (gagal)
3. ⚠️ Boundary (batas)
4. 🚫 Edge case (ekstrem)

---

## Aktivitas 3: Presentasi

### 5 menit

1-2 pasangan presentasi test case-nya!

---

## Langkah Debugging

```
Identifikasi → Reproduksi → Cari penyebab → Perbaiki → Verifikasi
```

> "Bicara dengan bebek karet" — teknik debugging terkenal!

---

## Rangkuman

| Konsep | Inti |
|---|---|
| **Testing** | Cari bug sebelum rilis |
| **Test Case** | Skenario uji |
| **Debugging** | 5 langkah perbaiki bug |
| **Unit / Integration / System / UAT** | Jenis testing |

---

## Tugas Rumah

Cari 1 bug terkenal di dunia IT — tulis analisis!

> Nama sistem, tahun, dampak, penyebab, pelajaran

---

## Pertemuan Depan

### Deployment & CI/CD
> Bagaimana kode sampai ke user?

---

# Terima Kasih

### MGMP Informatika SMAN 6 Cimahi

> "Kode tanpa testing ibarat jembatan tanpa uji beban."
