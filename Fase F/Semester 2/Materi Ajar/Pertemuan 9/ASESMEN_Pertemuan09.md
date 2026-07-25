# ASESMEN – PERTEMUAN 9 (S2)
## Troubleshooting Jaringan

Informatika – Fase F / Kelas XI – SMA Negeri 6 Cimahi

---

## Rubrik Penilaian

### A. Ping (Bobot 20%)

| Kriteria | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| Perintah benar | 0–1 | 2 | 3 | 4 |
| Analisis | Tidak | 1 analisis | 2–3 analisis | 4 analisis + kesimpulan |

### B. Traceroute (Bobot 20%)

| Kriteria | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| Hop tercatat | 0–2 | 3–4 | 5–6 | 7+ |
| Analisis | Tidak | Jumlah hop | Jumlah + terlambat | Lengkap + tebak lokasi |

### C. ipconfig & nslookup (Bobot 20%)

| Kriteria | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| ipconfig | Tidak | Sebagian | Lengkap | Lengkap + analisis IP kelas |
| nslookup | 0 | 1 | 2 | 3 |

### D. Diagnosa Kasus (Bobot 30%)

| Kriteria | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| Langkah | Tidak logis | 1 langkah | 2–3 langkah | 4+ langkah logis |
| Perintah tepat | Tidak | 1 tepat | 2 tepat | 3+ tepat |
| Solusi | Tidak ada | Kurang tepat | Tepat | Tepat + alasan |

### E. Refleksi & Tugas (Bobot 10%)

| Kriteria | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| Refleksi | Tidak diisi | 1 jawaban | 2 jawaban | 2 jawaban + mendalam |
| Tugas rumah | Tidak | Ada | Ada + screenshot | Ada + screenshot + analisis |

---

## Kunci Jawaban

### Soal 1 — Ping Analisis

| Hasil | Analisis |
|---|---|
| google.com vs 8.8.8.8 berbeda | 8.8.8.8 lebih cepat karena tidak perlu DNS lookup. Jika google.com gagal tapi 8.8.8.8 OK → DNS error |
| Ping 192.168.1.1 gagal | Router/gateway tidak merespon → cek kabel, restart router |

### Soal 2 — Traceroute (contoh)

| Hop | IP | Waktu | Lokasi |
|---|---|---|---|
| 1 | 192.168.1.1 | < 1 ms | Router sekolah/rumah |
| 2 | 10.0.0.1 | 2 ms | ISP lokal |
| 3 | 172.16.x.x | 5 ms | ISP regional |
| 4 | 74.125.x.x | 10 ms | Google edge |
| 5 | 142.250.x.x | 12 ms | Google server |

### Soal 3 — ipconfig

| IP Kelas | 192.168.x.x = Kelas C (192.0.0.0 – 223.255.255.255) |
|---|---|
| 169.254.x.x | APIPA — DHCP tidak merespon → kabel/wireless tidak terhubung |

### Soal 5 — Skenario Diagnosa (contoh untuk skenario A)

| Langkah | Perintah | Hasil | Analisis |
|---|---|---|---|
| 1 | `ipconfig` | IP 169.254.x.x | Tidak dapat IP dari DHCP |
| 2 | Cek kabel LAN | Lampu LED mati | Kabel putus |
| 3 | Ganti kabel | IP 192.168.x.x | ✅ Normal |

### Skenario B — Web tidak bisa, WhatsApp jalan

| Langkah | Perintah | Hasil | Analisis |
|---|---|---|---|
| 1 | `ping 8.8.8.8` | OK | Internet OK |
| 2 | `nslookup google.com` | Gagal | DNS error |
| 3 | Ganti DNS ke 8.8.8.8 | ✅ Web bisa | DNS server ISP bermasalah |

### Skenario C — Semua lab mati

| Langkah | Perintah | Hasil | Analisis |
|---|---|---|---|
| 1 | Cek 1 komputer | Tidak bisa | Bukan per komputer |
| 2 | `ping 192.168.1.1` | Timeout | Router/modem mati |
| 3 | Restart router | ✅ Semua normal | Router hang |

---

**MGMP Informatika SMAN 6 Cimahi**
