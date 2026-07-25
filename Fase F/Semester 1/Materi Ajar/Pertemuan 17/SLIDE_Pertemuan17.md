---
marp: true
theme: uncover
class: invert
---

# PERTEMUAN 17 — FASE F
## Konsep Sistem & Keamanan Jaringan
### Informatika – Fase F / Kelas XI
#### SMA Negeri 6 Cimahi

---

## Review — Pert 14–16

```
Big Data → Olah Data → Visualisasi ↘
                                    ↘
                    Data dikirim lewat mana?
                           ⬇
                  KEAMANAN JARINGAN!
```

---

## Apersepsi

> Chat WA, e-commerce, transfer uang, login Instagram...

**Data kalian lewat mana? Aman atau tidak?**

---

## Tujuan Pembelajaran

1. ✅ Konsep sistem
2. ✅ Jenis jaringan
3. ✅ Ancaman keamanan
4. ✅ Teknik keamanan
5. ✅ Regulasi

---

# BAGIAN 1
## Konsep Sistem

---

## Apa itu Sistem?

> Kumpulan elemen yang saling berinteraksi untuk mencapai tujuan.

### Komponen Sistem:

```
INPUT → PROSES → OUTPUT
            ↑
        FEEDBACK
```

---

## Contoh Sistem

| Sistem | Input | Proses | Output |
|---|---|---|---|
| AC | Suhu ruang | Kompresor | Udara dingin |
| Komputer | Data, perintah | CPU + OS | Hasil olah |
| Gojek | Pesanan | Algoritma | Driver datang |

---

# BAGIAN 2
## Jaringan Komputer

---

## Jaringan Berdasarkan Jangkauan

```
PAN  🔵 1–10 m      → Bluetooth
LAN  🏢 10–1000 m   → Lab sekolah
MAN  🏙️ 1–100 km    → Wi-Fi kota
WAN  🌍 >100 km     → Internet
```

---

## Arsitektur Jaringan

| Client-Server | vs | Peer-to-Peer |
|---|---|---|
| Server pusat | | Semua setara |
| Web, email, DB | | Torrent, blockchain |
| Terpusat | | Tersebar |

---

## Protokol Internet

| Protokol | Guna |
|---|---|
| **TCP/IP** | Dasar komunikasi |
| **HTTP/HTTPS** | Web browsing |
| **DNS** | Domain → IP |
| **SMTP** | Email |

---

# BAGIAN 3
## Ancaman Keamanan

---

## 1. Malware

```
🦠 Virus    → Menempel di file
🪱 Worm     → Mereplikasi lewat jaringan
🐴 Trojan   → Menyamar sebagai software sah
💰 Ransomware → Enkripsi → tebus
```

> **WannaCry (2017)**: 200.000 korban, 150 negara

---

## 2. Phishing

> Tipuan digital — pura-pura jadi institusi resmi

```
✉️ "Akun Anda diblokir! Klik link!"
   dari: bank-bri-verify@gmail.com
   link: bit.ly/bri-perbaiki

❌ JANGAN KLIK!
```

---

## 3. Man-in-the-Middle

```
💻 Kamu          🕵️ Hacker          🏦 Server
  ──── Wi-Fi palsu ────
  ◄──           ◄──              ◄──

Semua data login dicuri! 😱
```

---

## 4. SQL Injection

> Form login, ketik: `' OR 1=1 --`

```
Query jadi:
SELECT * FROM users WHERE username='' OR 1=1 --'

✅ Login BERHASIL tanpa password!
```

---

## 5. DDoS

```
💻💻💻💻💻 BOTNET 💻💻💻💻💻
             │
      ──▶ 🎯 SERVER ◀──
          
Server kewalahan → DOWN!
```

---

## 6. Social Engineering

> Manusia adalah celah keamanan terlemah!

```
📞 "Saya dari IT — minta password Anda"
📧 "Klik link ini untuk hadiah"
💿 "USB berisi data gaji" → isinya VIRUS
```

---

# BAGIAN 4
## Teknik Keamanan

---

## Enkripsi

### Caesar Cipher — geser 3

```
INFORMATIKA → LQIRUPDWLND
    geser +3           geser -3
```

❌ Kelemahan: hanya 25 kemungkinan kunci!

---

## HTTPS & SSL/TLS

```
HTTP  →  🔓 Data terbuka
HTTPS →  🔒 Data terenkripsi

Ciri: 🔒 di address bar browser
```

---

## Firewall

> Filter traffic berdasarkan aturan

```
🌐 Internet ──► FIREWALL ──► 🏢 Server Internal
                    │
            Allow/Deny traffic
```

---

## Autentikasi 2FA

| Faktor | Contoh | Aman |
|---|---|---|
| Sesuatu yang diketahui | Password | ❌ |
| Sesuatu yang dimiliki | HP/Token | ✅ |
| Ciri fisik | Sidik jari/wajah | ✅✅ |

> **2FA = pakai 2 dari 3!**

---

# BAGIAN 5
## Regulasi

---

## UU ITE & UU PDP

| Pelanggaran | Pasal | Ancaman |
|---|---|---|
| Akses ilegal | 27 | 6 thn / Rp 600 jt |
| Berita bohong | 28 | 6 thn / Rp 1 M |
| Phishing | 35 | 12 thn / Rp 12 M |

> **UU PDP (2022)**: Lindungi data pribadi Anda!

---

## Aktivitas

| Aktivitas | Waktu | Cara |
|---|---|---|
| Kasus keamanan | 20 mnt | Kelompok, 4 kasus |
| Caesar Cipher | 20 mnt | Berpasangan |
| Cek HTTPS | 20 mnt | Individu |
| Poster | 15 mnt | Canva |

---

## Refleksi

- Ancaman paling berbahaya?
- 1 kebiasaan baru untuk keamanan data?
- Skala 1–10?

---

## Preview — PAS

> **Pert 18: Penilaian Akhir Semester**

90 menit — semua materi S1 (Pert 1–17)

---

# Terima Kasih

### MGMP Informatika SMAN 6 Cimahi

> "Keamanan bukan fitur tambahan — itu kebutuhan dasar!"
