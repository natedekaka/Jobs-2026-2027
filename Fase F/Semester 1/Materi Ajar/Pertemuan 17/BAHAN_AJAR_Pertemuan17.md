# BAHAN AJAR – PERTEMUAN 17
## Konsep Sistem dan Keamanan Jaringan

| TP | BK, AP — Konsep Sistem dan Keamanan Jaringan |
|---|---|

---

### A. KONSEP SISTEM

#### Definisi

> **Sistem** = kumpulan elemen yang saling berinteraksi untuk mencapai tujuan.

#### Contoh Sistem

| Sistem | Input | Proses | Output | Feedback |
|---|---|---|---|---|
| **Pencernaan** | Makanan | Enzim, lambung | Nutrisi | Lapar/kenyang |
| **Transportasi** | Penumpang | Kendaraan, jalan | Sampai tujuan | Macet/tiba |
| **Komputer** | Data, perintah | CPU, OS | Hasil olah data | Error/berhasil |
| **Informasi** | Data mentah | Analisis, sorting | Laporan | Keputusan |

#### Sistem Komputer

```
┌─────────┐     ┌─────────┐     ┌─────────┐
│ INPUT   │────▶│ PROSES  │────▶│ OUTPUT  │
│ Keyboard│     │ CPU, OS │     │ Monitor │
│ Mouse   │     │ RAM     │     │ Printer │
│ Mikro   │     │         │     │ Speaker │
└─────────┘     └─────────┘     └─────────┘
                      │
                      ▼
               ┌──────────┐
               │ FEEDBACK │
               │ Error    │
               │ Notifikasi│
               └──────────┘
```

---

### B. JARINGAN KOMPUTER

#### Berdasarkan Jangkauan

| Jenis | Jangkauan | Contoh Penggunaan |
|---|---|---|
| **PAN** (Personal Area Network) | 1–10 m | Bluetooth HP ke smartwatch |
| **LAN** (Local Area Network) | 10 m – 1 km | Lab komputer, kantor |
| **MAN** (Metropolitan Area Network) | 1–100 km | Wi-Fi kota, CCTV kota |
| **WAN** (Wide Area Network) | > 100 km | Internet, antar pulau |

#### Model Arsitektur

| Model | Karakteristik | Contoh |
|---|---|---|
| **Client-Server** | Server pusat melayani banyak client | Web, email, database |
| **Peer-to-Peer** | Setiap node adalah client & server | BitTorrent, blockchain |

#### Protokol Jaringan

| Protokol | Fungsi | Port |
|---|---|---|
| **HTTP** | Web (tidak aman) | 80 |
| **HTTPS** | Web (aman, SSL/TLS) | 443 |
| **FTP** | Transfer file | 21 |
| **SSH** | Remote server (enkripsi) | 22 |
| **DNS** | Domain → IP | 53 |
| **SMTP** | Kirim email | 25 |
| **TCP/IP** | Dasar komunikasi internet | – |

---

### C. ANCAMAN KEAMANAN JARINGAN

#### 1. Malware

Kategori software berbahaya:

| Jenis | Cara Kerja | Dampak |
|---|---|---|
| **Virus** | Menempel di file, menyebar | Rusak data |
| **Worm** | Mereplikasi diri lewat jaringan | Habiskan bandwidth |
| **Trojan** | Menyamar sebagai software sah | Curi data |
| **Ransomware** | Enkripsi data → minta tebusan | Kehilangan data |
| **Spyware** | Memata-matai aktivitas | Kebocoran data |

#### 2. Phishing

> Tipuan digital untuk mencuri data pribadi.

**Ciri-ciri:**
- Email/SMS dari institusi resmi (tapi alamat aneh)
- Link mencurigakan (bit.ly, atau typo: go0gle.com)
- Ancaman: "Akun Anda akan ditutup!"
- Meminta password/OTP

**Contoh:**
```
Subject: Peringatan! Akun Anda diblokir
Dari: bank-bri-verify@gmail.com
Link: bit.ly/bri-perbaiki
Isi: Klik link untuk verifikasi!
```

#### 3. DoS / DDoS

| Serangan | Cara | Dampak |
|---|---|---|
| **DoS** | 1 sumber banjiri traffic | Server lambat |
| **DDoS** | Banyak sumber (botnet) | Server down total |

#### 4. Man-in-the-Middle (MITM)

```
💻 Korban        🌐 Hacker        🏦 Server bank
     ────► Wi-Fi palsu ────►
     ◄──        ◄──        ◄──
  Hacker menyadap semua komunikasi!
```

#### 5. SQL Injection

```
Form login yang rentan:
Username: ' OR 1=1 --
Password: [kosong]
→ Query: SELECT * FROM users WHERE username='' OR 1=1 --'
→ Login BERHASIL tanpa password!
```

#### 6. Social Engineering

> Manipulasi psikologis, bukan teknis.

| Taktik | Contoh |
|---|---|
| **Impersonasi** | "Saya dari IT, minta password" |
| **Baiting** | USB di parkir → "data gaji" → isinya virus |
| **Pretexting** | "Survey dari Kemendikbud" → data pribadi |

---

### D. TEKNIK KEAMANAN

#### 1. Enkripsi

| Simetris | Asimetris |
|---|---|
| 1 kunci untuk enkripsi & dekripsi | 2 kunci: publik + privat |
| Cepat | Lambat |
| Contoh: AES | Contoh: RSA, SSL/TLS |

**Caesar Cipher (Enkripsi Sederhana)**

```
Plainteks:   I N F O R M A T I K A
Geser +3:   L Q I R U P D W L N D

Dekripsi: geser -3
Cipherteks: L Q I R U P D W L N D
→ Plainteks: I N F O R M A T I K A
```

Kelemahan: hanya 25 kemungkinan kunci — mudah ditebak (brute force).

#### 2. Firewall

> Filter traffic berdasarkan aturan.

| Aturan | Traffic | Tindakan |
|---|---|---|
| IP source = 192.168.1.0/24 | Semua | Allow |
| Port = 80 (HTTP) | Incoming | Allow |
| Port = 22 (SSH) | Incoming dari luar | Deny |

#### 3. Autentikasi & Otorisasi

| Faktor | Contoh | Keamanan |
|---|---|---|
| **Something you know** | Password | Rendah (bisa bocor) |
| **Something you have** | HP, token | Sedang |
| **Something you are** | Sidik jari, wajah | Tinggi |

**2FA (Two-Factor Authentication)** = kombinasi 2 dari 3 faktor di atas.

#### 4. HTTPS & SSL/TLS

```
HTTP:   data tidak terenkripsi — siapa pun bisa lihat
HTTPS:  data terenkripsi — hanya server & client bisa baca

🔒 di browser = HTTPS aktif
```

---

### E. REGULASI KEAMANAN DATA

#### UU ITE (Undang-Undang Informasi dan Transaksi Elektronik)

| Pasal | Isi | Ancaman Pidana |
|---|---|---|
| **Pasal 27** | Akses ilegal ke sistem elektronik | 6 tahun / Rp 600 juta |
| **Pasal 28** | Penyebaran berita bohong | 6 tahun / Rp 1 miliar |
| **Pasal 30** | Intersepsi komunikasi ilegal | 10 tahun / Rp 800 juta |
| **Pasal 32** | Perusakan data elektronik | 8 tahun / Rp 2 miliar |
| **Pasal 35** | Phishing / penipuan online | 12 tahun / Rp 12 miliar |

#### UU Perlindungan Data Pribadi (UU PDP) — 2022

| Hak Individu | Kewajiban Pengelola Data |
|---|---|
| Tahu data apa yang dikumpulkan | Minta izin sebelum kumpulkan data |
| Minta hapus data | Lindungi data dari kebocoran |
| Tarik izin kapan saja | Lapor jika terjadi kebocoran |

---

### F. RANGKUMAN

| Konsep | Poin Penting |
|---|---|
| **Sistem** | Input → Proses → Output → Feedback |
| **Jaringan** | PAN/LAN/MAN/WAN, Client-Server, P2P |
| **Ancaman** | Malware, Phishing, DDoS, MITM, SQLi, Social Eng. |
| **Keamanan** | Enkripsi, Firewall, Autentikasi, HTTPS, VPN |
| **Regulasi** | UU ITE, UU PDP |

---

**MGMP Informatika SMAN 6 Cimahi**
