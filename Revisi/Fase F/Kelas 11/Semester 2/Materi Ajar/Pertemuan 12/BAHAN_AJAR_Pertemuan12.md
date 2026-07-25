# BAHAN AJAR – PERTEMUAN 12 (S2)
## Jaringan di Sekitar Kita
*Mengacu pada Panduan Mapel 2025; INFORMATIKA Fase D-F — pendekatan Pembelajaran Mendalam (Memahami → Mengaplikasi → Merefleksi)*



### 🧠 Memahami — Membangun Pemahaman Awal

## A. Tujuan Pembelajaran
Setelah mempelajari materi ini, siswa mampu:
1. Mengidentifikasi jaringan di lingkungan sekitar (sekolah, rumah, kota)
2. Memahami komponen jaringan WiFi dan cara kerjanya
3. Melakukan pengecekan koneksi jaringan sederhana
4. Troubleshooting jaringan dasar

## B. Jaringan di Sekitar Kita
**Di Sekolah:**
- Lab komputer: LAN kabel UTP
- WiFi: Access Point tiap lantai
- Server: data guru, siswa, nilai
- Internet: fiber optik dari ISP

**Di Rumah:**
- Modem ISP -> Router WiFi -> perangkat
- Koneksi: fiber optik/ADSL/4G

**Di Kota:**
- Tower BTS untuk sinyal HP
- Fiber optik bawah tanah
- Hotspot publik

## C. Cara Kerja WiFi
WiFi = Wireless Fidelity — koneksi tanpa kabel via gelombang radio.

| Frekuensi | Kelebihan | Kekurangan |
|-----------|-----------|------------|
| 2.4 GHz | Jarak jauh, tembus tembok | Lambat, banyak gangguan |
| 5 GHz | Cepat, sedikit gangguan | Jarak pendek, mudah terhalang |

**SSID:** nama jaringan WiFi
**Enkripsi:** WPA2/WPA3 (standar keamanan)

## D. Praktik Cek Koneksi
```bash
ipconfig         # Windows — lihat IP
ip a             # Linux
ping google.com  # tes koneksi internet
tracert google.com   # Windows — lihat hop
nslookup google.com  # cek IP domain
```

## E. Troubleshooting Jaringan
| Masalah | Penyebab | Solusi |
|---------|----------|--------|
| Tidak Internet | Kabel lepas, modem mati | Cek kabel, restart modem |
| WiFi lambat | Banyak user, jarak jauh | Pindah 5 GHz, dekatkan router |
| WiFi tidak connect | Password salah | Lupa jaringan -> hubungkan ulang |
| Ping timeout | Server mati, firewall | Coba ping IP lain |
| DNS error | DNS bermasalah | Ganti DNS ke 8.8.8.8 |

**Restart urutan:** Matikan modem 30 detik -> Nyalakan -> Tunggu 2 menit.

## F. Keamanan WiFi
1. Ganti password default router
2. Gunakan WPA2/WPA3, jangan WEP
3. Ganti SSID — jangan pakai nama pribadi
4. Nonaktifkan WPS
5. Cek daftar perangkat terhubung


### 🔧 Mengaplikasi — Praktik & Penerapan

## G. Latihan
1. Cek IP address komputer/laptop masing-masing
2. Ping google.com — catat waktu respon (ms)
3. Tracert google.com — ada berapa hop?
4. Catat daftar WiFi yang tersedia di sekitar kelas
5. Identifikasi perangkat jaringan di lab komputer


### 🔍 Merefleksi — Refleksi & Evaluasi

- Apa konsep paling penting yang kamu pelajari hari ini?
- Bagaimana konsep ini terkait dengan materi sebelumnya?
- Skala pemahaman diri: ___/10
- Apa yang ingin kamu pelajari lebih lanjut?

---
**MGMP Informatika SMAN 6 Cimahi — Fase F (Kelas XI) S2 Pert 12**
