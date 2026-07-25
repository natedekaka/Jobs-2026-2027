# LEMBAR KERJA PESERTA DIDIK (LKPD)
## Pertemuan 9 (S2) – Troubleshooting Jaringan

| TP | BK — Konsep Sistem dan Keamanan Jaringan Komputer |
|---|---|
| Nama | ____________________ |
| Kelas | ____________________ |

---

### A. PING

**Soal 1:** Buka terminal/CMD. Jalankan ping!

| Perintah | Hasil (packet loss? time?) | Analisis |
|---|---|---|
| `ping -c 4 google.com` | | |
| `ping -c 4 8.8.8.8` | | |
| `ping -c 4 sman6cimahi.sch.id` | | |
| `ping -c 4 192.168.1.1` | | |

**Pertanyaan:**
1. Apakah google.com dan 8.8.8.8 memberikan hasil berbeda? Kenapa?
2. Jika ping ke 8.8.8.8 berhasil tapi ke google.com gagal, apa artinya?

---

### B. TRACEROUTE

**Soal 2:** Jalankan traceroute!

```bash
traceroute google.com    # atau tracert google.com (Windows)
```

| Hop | IP Address | Waktu (ms) | Tebakan lokasi |
|---|---|---|---|
| 1 | | | |
| 2 | | | |
| 3 | | | |
| 4 | | | |
| 5 | | | |
| 6 | | | |
| 7 | | | |

| Pertanyaan | Jawaban |
|---|---|
| Berapa hop total? | |
| Hop paling lambat? | |
| Fungsi router di setiap hop? | |

---

### C. IPCONFIG

**Soal 3:** Jalankan `ipconfig` / `ifconfig`!

| Informasi | Hasil |
|---|---|
| IPv4 Address | |
| Subnet Mask | |
| Default Gateway | |
| DNS Server | |

**Pertanyaan:**
- IP termasuk kelas apa? (A/B/C)?
- Jika IP 169.254.x.x, apa masalahnya?

---

### D. NSLOOKUP

**Soal 4:** Jalankan nslookup!

| Perintah | Hasil IP |
|---|---|
| `nslookup google.com` | |
| `nslookup sman6cimahi.sch.id` | |
| `nslookup 8.8.8.8` | |

---

### E. DIAGNOSA KASUS

**Soal 5:** Kelompok ____ — Skenario: ____________________

| Langkah | Perintah | Hasil | Analisis |
|---|---|---|---|
| 1 | | | |
| 2 | | | |
| 3 | | | |
| 4 | | | |

**Kesimpulan (kemungkinan penyebab + solusi):**
______________________________________________________

---

### F. TUGAS RUMAH

Cari IP router rumah + ping google.com!

| Aspek | Hasil |
|---|---|
| IP router rumah | |
| Ping google.com | |
| Screenshot | (tempel) |

---

### G. REFLEKSI

| Pertanyaan | Jawaban |
|---|---|
| Perintah paling berguna? | |
| Masalah jaringan pernah dialami? | |
| Skala pemahaman (1–10) | / 10 |

---

**MGMP Informatika SMAN 6 Cimahi**
