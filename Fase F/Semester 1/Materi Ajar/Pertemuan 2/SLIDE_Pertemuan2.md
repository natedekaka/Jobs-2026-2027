---
marp: true
theme: uncover
class: invert
---

# PERTEMUAN 2 — FASE F
## Analisis Kebutuhan & Spesifikasi
### Informatika – Fase F / Kelas XI
#### SMA Negeri 6 Cimahi

---

## Review — Pert 1

7 tahapan SDLC:
```
Planning → Analysis → Design → Implementation
    ↑                                  |
    +────────── Maintenance ←─── Deployment
```

> Hari ini: **Tahap 2 — Analysis!**

---

## Apersepsi

"Bayangin kalian disuruh buat aplikasi tanpa bilang mau fitur apa."

Hasilnya pasti **tidak sesuai**.

> Makanya **analisis kebutuhan** itu penting!

---

## Masalah #1 di Dunia Software

### ❌ Bukan "salah coding"
### ✅ Tapi "**salah kebutuhan**"

Banyak proyek gagal karena:
- Fitur tidak sesuai
- Salah memahami pengguna
- Tidak jelas apa yang harus dibuat

---

# TUJUAN PEMBELAJARAN

1. ✅ Tujuan & teknik analisis kebutuhan
2. ✅ Fungsional vs Non-Fungsional
3. ✅ Menulis user story
4. ✅ Wawancara simulasi

---

## Apa Itu Analisis Kebutuhan?

**Analisis Kebutuhan** = proses menggali, memahami & mendokumentasikan apa yang dibutuhkan pengguna

**Output:** SRS (Software Requirements Specification)

> Dokumen yang menjawab: **"Aplikasi ini harus bisa apa?"**

---

## Kebutuhan Fungsional

### "Apa yang sistem lakukan?"

Berkaitan dengan **fitur**:
| Aplikasi Perpustakaan | |
|---|---|
| Login siswa | ✅ |
| Cari buku | ✅ |
| Pinjam buku | ✅ |
| Kembalikan buku | ✅ |
| Cetak laporan | ✅ |

---

## Kebutuhan Non-Fungsional

### "Seberapa baik sistem melakukannya?"

Berkaitan dengan **kualitas**:
| Jenis | Contoh |
|---|---|
| Performance | Cari buku < 2 detik |
| Security | Hanya petugas bisa hapus data |
| Usability | Bisa dipakai tanpa pelatihan |
| Reliability | 99.9% uptime |

---

## Fungsional vs Non-Fungsional

| | Fungsional | Non-Fungsional |
|---|---|---|
| **Pertanyaan** | Apa yang dilakukan? | Seberapa baik? |
| **Contoh** | Login | Login < 2 detik |
| **Diukur?** | Ada/tidak | Skala (detik, %) |

---

## User Story

Format sederhana menulis kebutuhan dari sudut pandang **pengguna**.

```
Sebagai [PERAN],
saya ingin [FITUR],
sehingga [MANFAAT].
```

### Contoh:
> Sebagai **guru**, saya ingin **scan QR siswa** sehingga **presensi cepat**.

---

## Teknik Penggalian Kebutuhan

| Teknik | Cara | Cocok |
|---|---|---|
| 🗣️ **Wawancara** | Tanya langsung | Detail mendalam |
| 👀 **Observasi** | Lihat kegiatan | Konteks nyata |
| 📋 **Kuesioner** | Angket | Banyak responden |
| 📄 **Studi dokumen** | Sistem lama | Data historis |

---

## Aktivitas 1: Klasifikasi

### Individu — 10 menit

10 pernyataan → klasifikasikan F/NF

Contoh:
- "Login dengan NISN" = **F**
- "Login < 3 detik" = **NF**

---

## Aktivitas 2: Wawancara Simulasi

### Berpasangan — 15 menit

**Skenario:**
- Kamu = **developer**
- Pasangan = **klien**

**Tema:** Aplikasi untuk sekolah
(Presensi / Perpus / Kantin / dll.)

> Wawancarai! Cari minimal 5 fungsional + 3 non-fungsional!

---

## Panduan Wawancara

1. "Ceritakan proses saat ini?"
2. "Masalah utama?"
3. "Fitur paling penting?"
4. "Siapa penggunanya?"

> Gunakan pertanyaan **terbuka** (bukan ya/tidak)!

---

## Aktivitas 3: User Story

### Berpasangan — 10 menit

Dari hasil wawancara, tulis 3 user story:

```
Sebagai __________,
saya ingin __________,
sehingga __________.
```

---

## Contoh Hasil Wawancara

**Aplikasi Presensi Sekolah**

Pengguna: Guru, Wali Kelas, Orang Tua, Admin BK

| Fungsional | Non-Fungsional |
|---|---|
| Scan QR siswa | Scan < 2 detik |
| Rekap bulanan | Data aman |
| Notifikasi ortu | Notif < 1 menit |
| Ekspor Excel | 500 user bersamaan |

---

## Rangkuman

| Konsep | Inti |
|---|---|
| Fungsional | Fitur yang harus ada |
| Non-Fungsional | Kualitas sistem |
| User Story | Sebagai... ingin... sehingga... |
| Teknik | Wawancara, observasi, kuesioner |

---

## Tugas Rumah

Sempurnakan daftar kebutuhan dari wawancara hari ini!

> Minimal 5 fungsional + 3 non-fungsional

---

## Pertemuan Depan

### Perancangan (Design) & UI/UX
> Kita buat **wireframe** aplikasi!

---

# Terima Kasih

### MGMP Informatika SMAN 6 Cimahi

> "Kegagalan terbesar bukan salah coding, tapi salah kebutuhan."
