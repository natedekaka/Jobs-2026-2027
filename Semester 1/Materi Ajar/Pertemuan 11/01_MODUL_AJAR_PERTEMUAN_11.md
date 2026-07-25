# MODUL AJAR INFORMATIKA – FASE E (KELAS X)

## Informasi Umum

| Komponen | Deskripsi |
|---|---|
| **Mata Pelajaran** | Informatika |
| **Fase / Kelas** | E / X |
| **Semester** | 1 (Ganjil) |
| **Pertemuan ke-** | 11 |
| **Alokasi Waktu** | 2 JP × 45 menit (90 menit) |
| **Tahun Pelajaran** | 2026/2027 |
| **Satuan Pendidikan** | **SMA Negeri 6 Cimahi** |

---

## Profil Pelajar Pancasila

| Dimensi | Indikator |
|---|---|
| Bernalar Kritis | Menganalisis risiko keamanan pada berbagai jenis jaringan |
| Mandiri | Mengonfigurasi pengaturan keamanan jaringan secara mandiri |
| Gotong Royong | Berdiskusi dan berbagi temuan praktik keamanan |

---

## Sarana & Prasarana

| Sarana | Keterangan |
|---|---|
| Lab komputer / laptop | 1 unit per siswa (OS Windows/Linux/macOS) |
| Koneksi WiFi | Untuk praktik keamanan nirkabel |
| Smartphone (milik siswa) | Untuk praktik hotspot & WiFi analysis |
| Proyektor / LCD | Untuk demo |
| Aplikasi (opsional) | Wireshark (demo saja), atau Network Settings bawaan OS |
| Hotspot seluler guru | Untuk demo captive portal / keamanan WiFi publik |

---

## Tujuan Pembelajaran (TP 2.5)

| TP | Indikator Ketercapaian Tujuan Pembelajaran (IKTP) |
|---|---|
| **LD 2.5:** Memahami konsep keamanan jaringan (kabel dan nirkabel) serta melakukan konfigurasi keamanan sederhana | 2.5.1 Mengidentifikasi jenis-jenis jaringan dan ancaman keamanannya<br>2.5.2 Membedakan enkripsi WiFi (WEP, WPA, WPA2, WPA3)<br>2.5.3 Mengonfigurasi pengaturan keamanan WiFi / hotspot<br>2.5.4 Mengaktifkan dan mengatur firewall dasar pada sistem operasi |

---

## Peta Kompetensi

```
Pertemuan 11 — Keamanan Dasar Jaringan
│
├── Pendahuluan (10 menit)
│   ├── Review PTS / hasil PTS
│   ├── Apersepsi: "Pernah WiFi kalian dipakai orang lain?"
│   └── Tujuan: Kenali risiko jaringan & cara amankannya
│
├── Inti (65 menit)
│   ├── Memahami (15 menit)
│   │   ├── Jenis jaringan: LAN, WAN, WiFi, Internet
│   │   ├── Ancaman: snooping, MITM, rogue AP, packet sniffing
│   │   └── Enkripsi WiFi: WEP (🔴), WPA (🟡), WPA2 (🟢), WPA3 (🟢)
│   │
│   ├── Mengaplikasi (40 menit)
│   │   ├── [15'] Cek keamanan WiFi kampus/sekolah
│   │   ├── [10'] Konfigurasi hotspot HP + password
│   │   └── [15'] Firewall: cek & aktifkan
│   │
│   └── Merefleksi (10 menit)
│       └── Diskusi & refleksi
│
└── Penutup (15 menit)
```

---

## Langkah Pembelajaran

### Pembukaan (10 menit)

| Kegiatan | Waktu |
|---|---|
| 1. Salam, doa, cek kehadiran | 2 menit |
| 2. **Review singkat**: "Bagaimana PTS kemarin? Ada soal yang paling sulit?" | 4 menit |
| 3. **Apersepsi**: Guru bertanya: "Siapa yang pernah WiFi-nya dipakai orang lain tanpa izin? Siapa yang pernah HP-nya tiba-tiba muncul notifikasi 'ada perangkat baru terhubung'?" | 2 menit |
| 4. Sampaikan tujuan: hari ini belajar **mengamankan jaringan** — dari WiFi rumah sampai firewall laptop | 2 menit |

### Inti (65 menit)

#### Memahami (berkesadaran, menggembirakan) — 15 menit

1. **Jenis Jaringan & Risikonya (5 menit)**
   | Jaringan | Contoh | Risiko Utama |
   |---|---|---|
   | **LAN (kabel)** | Kantor, lab komputer | Penyadapan fisik, ARP spoofing |
   | **WiFi (nirkabel)** | Rumah, sekolah, kafe | Snooping, rogue AP, password lemah |
   | **Internet** | Semua jaringan publik | MITM, phishing, DNS hijacking |

2. **Enkripsi WiFi — Generasi (5 menit)**
   | Standar | Tahun | Keamanan | Status |
   |---|---|---|---|
   | **WEP** | 1997 | 🔴 Sangat lemah — bisa dibobol < 5 menit | Jangan gunakan |
   | **WPA** | 2003 | 🟡 Cukup — masih bisa diretas | Hindari jika ada alternatif |
   | **WPA2** | 2004 | 🟢 Aman — standar minimal saat ini | Wajib jika WPA3 belum ada |
   | **WPA3** | 2018 | 🟢🟢 Paling aman (SAE handshake) | Recommended |

   **Demo cepat:** Guru menunjukkan cara cek jenis enkripsi WiFi sekolah:
   - Windows: Klik ikon WiFi → Properties → Security type
   - Android: Settings → WiFi → gear icon → Security
   - iPhone: Settings → WiFi → (i) → Security

3. **Firewall Dasar (5 menit)**
   - **Firewall** = pintu keamanan — menyaring lalu lintas masuk/keluar
   - Windows: Windows Defender Firewall
   - Linux: `ufw` atau `iptables`
   - macOS: System Settings → Network → Firewall

#### Mengaplikasi (bermakna, menggembirakan) — 40 menit

4. **Aktivitas 1: Cek Keamanan WiFi (15 menit) — Berpasangan**
   - **Tugas**: Cek dan catat pengaturan WiFi yang tersedia di sekitar
   | Langkah | Kegiatan | Catatan |
   |---|---|---|
   | 1. Buka daftar WiFi (SSID) yang terdeteksi | Catat semua SSID yang muncul | |
   | 2. Klik Properties pada WiFi sekolah | Catat Security type & password | |
   | 3. Cek enkripsi WiFi tetangga (yang terlihat) | Apakah ada WEP? WPA2? | |
   | 4. Identifikasi risiko | Adakah SSID mencurigakan? (nama aneh, tanpa password) | |
   | 5. Catat di LKPD | | |

   > ⚠️ **Catatan etika**: Siswa hanya mengamati SSID yang terlihat, TIDAK boleh mencoba masuk ke jaringan orang lain.

   - **Diskusi**: Kenapa WiFi publik (kafe, mal) berbahaya? Apa itu **evil twin**?

5. **Aktivitas 2: Konfigurasi Keamanan Hotspot (10 menit) — Individu**
   - **Tugas**: Atur hotspot HP dengan keamanan maksimal
   | Langkah | Keterangan |
   |---|---|
   | 1. Buka Settings → Hotspot & Tethering | |
   | 2. Set AP Band: 5 GHz (lebih aman dari 2,4 GHz) | |
   | 3. Security: WPA2 / WPA3 (jangan Open/None) | |
   | 4. Password: minimal 12 karakter (kombinasi) | |
   | 5. Nama SSID: jangan gunakan nama pribadi | |
   | 6. Matikan hotspot jika tidak dipakai | |

6. **Aktivitas 3: Firewall — Cek & Aktifkan (15 menit)**
   - **Windows**:
     - Buka **Control Panel → Windows Defender Firewall**
     - Pastikan status: **On** untuk Domain, Private, Public
     - Klik **Allow an app through firewall** → lihat aplikasi mana yang diizinkan
   - **Linux** (jika ada):
     - Terminal: `sudo ufw status` → `sudo ufw enable`
     - Cek port terbuka: `sudo ss -tuln`
   - **Catat di LKPD**: Status firewall, jumlah aplikasi yang diizinkan

#### Merefleksi (berkesadaran, bermakna) — 10 menit

7. **Diskusi Kelas (5 menit)**
   - "Apa yang paling mengejutkan dari aktivitas tadi?"
   - "Apakah ada SSID mencurigakan? Apa cirinya?"
   - "Kenapa kita tidak boleh pakai WiFi publik tanpa VPN?"

8. **Refleksi Individu (5 menit)**
   - Satu ancaman jaringan yang baru kamu ketahui hari ini
   - Satu hal yang akan kamu ubah pada pengaturan jaringan di rumah
   - Skala pemahaman: ___ / 10

### Penutup (15 menit)

| Kegiatan | Waktu |
|---|---|
| 1. Rangkuman: "WiFi aman = WPA2/3 + password kuat + firewall aktif" | 3 menit |
| 2. Tanya jawab | 5 menit |
| 3. **Tugas rumah**: Cek keamanan WiFi rumah — catat SSID, enkripsi, password ≥ 12 char? | 3 menit |
| 4. Sampaikan pertemuan depan: Manajemen Kata Sandi & Autentikasi 2 Langkah | 2 menit |
| 5. Doa & salam | 2 menit |

---

## Asesmen

### Rubrik Formatif — LKPD

| Kriteria | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| **Identifikasi jaringan** | Tidak mengisi | Mencatat < 3 SSID | Mencatat ≥ 5 SSID + enkripsi | Lengkap + analisis risiko |
| **Konfigurasi hotspot** | Tidak mencoba | Setting dasar | WPA2 + password ≥ 8 | WPA2/3 + password ≥ 12 + 5 GHz |
| **Firewall** | Tidak cek | Cek status | Cek + catat status | Cek + catat + analisis aturan |

---

**MGMP Informatika SMAN 6 Cimahi**
