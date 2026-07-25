# MODUL AJAR INFORMATIKA – FASE F (KELAS XI)

| Komponen | Deskripsi |
|---|---|
| **Mata Pelajaran** | Informatika |
| **Fase / Kelas** | F / XI |
| **Semester** | 2 (Genap) |
| **Pertemuan ke-** | 9 |
| **Alokasi Waktu** | 5 JP × 45 menit (225 menit) |
| **Tahun Pelajaran** | 2026/2027 |
| **Satuan Pendidikan** | SMA Negeri 6 Cimahi |
| **Materi Esensial** | Konsep Sistem dan Keamanan Jaringan Komputer |

---

## Tujuan Pembelajaran

| TP | IKTP |
|---|---|
| **BK:** Melakukan troubleshooting jaringan dasar | 9.1 Menggunakan `ping` untuk uji koneksi |
| | 9.2 Menggunakan `traceroute` untuk lihat jalur data |
| | 9.3 Menggunakan `ipconfig`/`ifconfig` untuk cek konfigurasi IP |
| | 9.4 Mendiagnosis masalah jaringan sederhana |

---

## Langkah Pembelajaran

### Pembukaan (20 menit)

| Kegiatan | Waktu |
|---|---|
| 1. Salam, doa, cek kehadiran | 3 menit |
| 2. **Review**: "Pert 7: topologi. Pert 8: cloud. Sekarang: bagaimana cara **diagnosa** jaringan bermasalah?" | 7 menit |
| 3. **Apersepsi**: "Wi-Fi sekolah lemot. Web tidak bisa dibuka. Bagaimana cara cek — apakah internet mati, server down, atau DNS error?" | 10 menit |

### Inti (175 menit)

#### Memahami (50 menit)

**1. Pendekatan Troubleshooting (10 menit)**

| Langkah | Kegiatan |
|---|---|
| 1. Identifikasi | "Apa yang terjadi? Kapan mulai?" |
| 2. Isolasi | "Apakah hanya 1 komputer atau semua?" |
| 3. Test | Gunakan tool (ping, traceroute, dll.) |
| 4. Analisis | "Apa arti hasil test?" |
| 5. Solusi | Perbaiki masalah |
| 6. Verifikasi | Pastikan masalah selesai |

**2. Perintah Dasar Troubleshooting (30 menit)**

**a. `ping` — Uji Koneksi Dasar**

```bash
ping google.com           # ping terus-menerus
ping -c 4 google.com      # ping 4 kali (Linux/macOS)
ping -n 4 google.com      # ping 4 kali (Windows)
```

| Hasil | Arti |
|---|---|
| `Reply from ...` | Koneksi OK |
| `Request timed out` | Tidak ada respon — host mati / firewall blok |
| `Destination host unreachable` | Tidak ada rute ke tujuan |
| `TTL expired in transit` | Terlalu banyak hop — router loop |

**b. `traceroute` / `tracert` — Lihat Jalur Data**

```bash
traceroute google.com     # Linux/macOS
tracert google.com        # Windows
```

Menampilkan setiap router (hop) yang dilalui data dari komputer ke tujuan.

**c. `ipconfig` / `ifconfig` — Konfigurasi IP**

```bash
ipconfig                  # Windows — lihat IP, subnet mask, gateway, DNS
ipconfig /all             # Windows — detail lengkap
ifconfig                  # Linux/macOS
```

| Informasi | Arti |
|---|---|
| IPv4 Address | Alamat IP komputer |
| Subnet Mask | Batas jaringan lokal |
| Default Gateway | IP router untuk akses ke luar |
| DNS Server | Server penerjemah domain → IP |

**d. `netstat` — Koneksi Aktif**

```bash
netstat -an               # Semua koneksi aktif
netstat -an | grep 443    # Koneksi ke port 443 (HTTPS)
```

**e. `nslookup` — Cek DNS**

```bash
nslookup google.com       # Cari IP dari nama domain
nslookup 8.8.8.8          # Cari nama domain dari IP
```

**3. Skenario Masalah Jaringan (10 menit)**

| Masalah | Gejala | Kemungkinan | Test |
|---|---|---|---|
| **Kabel lepas** | "No internet" | Fisik | `ipconfig` — cek IP (169.254.x.x = APIPA) |
| **Wi-Fi lemah** | Lambat, putus | Sinyal | `ping` — latency tinggi, packet loss |
| **DNS error** | Web tidak bisa, WhatsApp bisa | DNS | `nslookup` — gagal? ganti DNS ke 8.8.8.8 |
| **Firewall blok** | Beberapa situs tidak bisa | Firewall | `ping` to IP vs to domain |
| **Router mati** | Semua tidak bisa | Router | `ping 192.168.1.1` (gateway) gagal |

#### Mengaplikasi — Praktik (95 menit)

**4. Demonstrasi Langsung (15 menit)**
- Buka terminal / command prompt
- Demo `ping google.com`
- Demo `tracert google.com` — lihat hop dari sekolah ke Google
- Demo `ipconfig` — lihat IP komputer
- Demo `nslookup google.com`

**5. Aktivitas 1 — Praktik Ping (20 menit) — Individu**

Buka terminal/CMD dan jalankan:

| Perintah | Hasil | Analisis |
|---|---|---|
| `ping -c 4 google.com` | | |
| `ping -c 4 8.8.8.8` (DNS Google) | | |
| `ping -c 4 sman6cimahi.sch.id` | | |
| `ping -c 4 192.168.1.1` (gateway) | | |

**Pertanyaan:**
- Apakah semua ping berhasil?
- Mana yang lebih cepat — google.com atau 8.8.8.8? Kenapa?
- Apa artinya jika ping ke 8.8.8.8 berhasil tapi ke google.com gagal?

**6. Aktivitas 2 — Traceroute (20 menit) — Berpasangan**

```bash
traceroute google.com      # atau tracert di Windows
```

| Hop | IP Address | Waktu | Lokasi (tebak) |
|---|---|---|---|
| 1 | | | |
| 2 | | | |
| 3 | | | |
| ... | | | |

**Pertanyaan:**
- Berapa hop dari sekolah ke Google?
- Hop mana yang paling lambat?
- Apa fungsi setiap hop?

**7. Aktivitas 3 — Diagnosa Kasus (30 menit) — Kelompok**

Setiap kelompok mendapat 1 skenario:

| Kelompok | Skenario |
|---|---|
| A | "Komputer tidak bisa akses internet sama sekali — LAN cable terhubung" |
| B | "Wi-Fi terhubung tapi web tidak bisa dibuka, WhatsApp masih jalan" |
| C | "Semua komputer di lab tidak bisa internet — tapi kemarin bisa" |
| D | "1 situs tertentu tidak bisa diakses — situs lain normal" |

**Tugas:** Tulis langkah diagnosa + perintah yang digunakan + kemungkinan penyebab

**8. Presentasi Diagnosa (10 menit) — 2 kelompok @5 menit**

#### Merefleksi (15 menit)

**9. Refleksi Jurnal (15 menit)**
- Perintah troubleshooting paling berguna?
- 1 masalah jaringan yang pernah dialami — bagaimana solusinya?
- Skala pemahaman 1–10

### Penutup (35 menit)

| Kegiatan | Waktu |
|---|---|
| 1. Rangkuman: ping (koneksi) → traceroute (jalur) → ipconfig (konfigurasi) → nslookup (DNS) | 10 menit |
| 2. Kuis lisan: "Apa bedanya ping timeout vs unreachable? Fungsi traceroute?" | 10 menit |
| 3. Preview: "Pert 10: Password Manager & 2FA — amankan akun kalian!" | 5 menit |
| 4. Tugas rumah: Cari tahu IP router rumah, cek ping ke google.com, screenshot hasil | 10 menit |

---

## Asesmen

| Kriteria | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| Ping (perintah + analisis) | Tidak jalan | Jalan | Jalan + analisis | Jalan + analisis + kesimpulan |
| Traceroute (hop + analisis) | Tidak jalan | Jalan | Jalan + catat hop | Jalan + analisis hop lambat |
| Diagnosa kasus | Tidak tepat | 1 langkah benar | 2–3 langkah benar | Langkah lengkap + solusi tepat |
| Presentasi | Tidak siap | Kurang jelas | Jelas | Jelas + demo langsung |

---

**MGMP Informatika SMAN 6 Cimahi**
