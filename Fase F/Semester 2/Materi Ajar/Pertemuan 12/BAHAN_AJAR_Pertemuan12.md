# BAHAN AJAR – PERTEMUAN 12 (S2)
## Platform Digital

| TP | LD — Konsep Sistem dan Keamanan Jaringan Komputer |
|---|---|

---

### A. LOKAPASAR / MARKETPLACE

#### Definisi

> Platform digital yang mempertemukan penjual dan pembeli, menyediakan fitur transaksi, pembayaran, dan pengiriman.

#### Marketplace di Indonesia

| Platform | Tahun | Pengguna (2025) | Pembayaran |
|---|---|---|---|
| **Shopee** | 2015 | 150+ juta | ShopeePay, COD, transfer |
| **Tokopedia** | 2009 | 100+ juta | GoPay, transfer, kartu |
| **Lazada** | 2012 | 50+ juta | Lazada Wallet, kartu |
| **Bukalapak** | 2010 | 30+ juta | BukaDompet, mitra |
| **Blibli** | 2011 | 20+ juta | Blibli Pay, cicilan |

#### Fitur Keamanan Marketplace

| Fitur | Penjelasan |
|---|---|
| **Escrow** | Dana pembeli ditahan platform sampai barang diterima |
| **Rating & Review** | Lihat reputasi penjual sebelum beli |
| **Diskusi** | Tanya barang langsung ke penjual |
| **Garansi** | Pengembalian barang jika tidak sesuai |
| **Asuransi** | Perlindungan kerusakan saat pengiriman |

#### Tips Aman Belanja Online

| ✅ Lakukan | ❌ Jangan |
|---|---|
| Cek rating & review toko | Transfer langsung ke rekening penjual |
| Baca deskripsi barang teliti | Klik link dari SMS/WA "diskon besar" |
| Bayar lewat escrow platform | Beri password/OTP ke siapa pun |
| Simpan bukti transaksi | Beli dari toko tanpa rating |
| Aktivasi 2FA di akun marketplace | Gunakan Wi-Fi publik untuk transaksi |

---

### B. PERBANKAN DIGITAL

#### Jenis Perbankan Digital

| Jenis | Contoh | Akses | Cocok untuk |
|---|---|---|---|
| **Mobile Banking** | BCA Mobile, Mandiri Livin' | HP (app) | Transaksi harian |
| **Internet Banking** | KlikBCA, Mandiri Online | Browser | Transaksi besar |
| **Digital Bank** | Jenius, SeaBank, Digibank | HP 100% | Anak muda, tanpa cabang |

#### Fitur Keamanan M-Banking

| Fitur | Cara Kerja | Aman dari |
|---|---|---|
| **User ID + Password** | Login | Akses tanpa izin |
| **OTP (One-Time Password)** | Kode SMS/notifikasi | Transaksi tanpa persetujuan |
| **m-Token** | Generate kode di app | Transaksi besar |
| **Device Binding** | Hanya 1 HP terdaftar | Login dari HP lain |
| **Transaksi Limit** | Maks transfer per hari | Kerugian besar |
| **Notifikasi** | SMS/notifikasi setiap transaksi | Transaksi mencurigakan |
| **Biometrik** | Sidik jari / wajah | Akses fisik |

#### Tips Aman M-Banking

| Tips | Kenapa |
|---|---|
| Jangan root/jailbreak HP | Root = keamanan turun |
| Install app dari store resmi | App palsu bisa curi data |
| Jangan simpan PIN di catatan HP | Jika HP hilang, PIN terbaca |
| Logout setelah selesai | Akses dari perangkat bersama |
| Aktivasi notifikasi transaksi | Tahu jika ada transaksi mencurigakan |
| Laporkan segera jika HP hilang | Blokir akses m-banking |

---

### C. DOMPET DIGITAL / E-WALLET

#### Dompet Digital di Indonesia

| Dompet | Rating | Fitur Unggulan |
|---|---|---|
| **GoPay** | ✅✅✅✅ | Integrasi Gojek, QRIS |
| **OVO** | ✅✅✅✅ | Points, tarik tunai di ATM |
| **DANA** | ✅✅✅✅✅ | QRIS, transfer, bayar PBB |
| **ShopeePay** | ✅✅✅✅ | Bayar Shopee, merchant |
| **LinkAja** | ✅✅✅ | Transportasi umum, PBB |

#### QRIS — Standar Pembayaran Nasional

> **QRIS** = Quick Response Code Indonesian Standard — satu QR code untuk semua dompet digital.

**Cara Kerja:**
```
Merchant punya 1 QR code
Pembeli scan pakai GoPay / OVO / DANA / ShopeePay / M-Banking
Semua bisa — satu QR untuk semua!
```

**Kelebihan QRIS:**
- Satu QR untuk semua dompet
- Merchant tidak perlu banyak stiker
- Transaksi tercatat
- Aman (terverifikasi BI)

#### Risiko Dompet Digital

| Risiko | Contoh | Mitigasi |
|---|---|---|
| **HP hilang** | Saldo GoPay bisa dipakai | PIN 6 digit + device lock |
| **Phishing QRIS** | QR palsu di tempel | Cek merchant, tanya staff |
| **Top-up salah** | Salah input nomor | Verifikasi nama sebelum konfirmasi |
| **Saldo menganggur** | Uang di dompet tidak berbunga | Top-up secukupnya |
| **Aplikasi palsu** | Download dari sumber tidak resmi | Install dari Play Store/App Store |

---

### D. STUDI KASUS PENIPUAN

#### Kasus 1: Phishing Marketplace

**Skenario:** SMS dari "Shopee" → link unblock akun → minta email + password → saldo ShopeePay raib

**Analisis:**
| Jenis | Phishing — social engineering |
|---|---|
| Kesalahan | Panik → klik link → kasih password |
| Seharusnya | Cek di app resmi, jangan klik link SMS |
| Pelaporan | Lapor ke platform + Kominfo (patrolisiber.id) |

#### Kasus 2: Penjual Fiktif

**Skenario:** Pembeli transfer langsung ke rekening penjual → barang tidak dikirim

**Analisis:**
| Jenis | Penipuan klasik |
|---|---|
| Kesalahan | Transfer di luar escrow |
| Seharusnya | Bayar lewat platform (escrow) |
| Pelaporan | Lapor ke platform + polisi |

#### Kasus 3: OTP Bocor

**Skenario:** "Saya dari Bank — verifikasi data Anda. Mohon sebutkan OTP yang baru dikirim"

**Analisis:**
| Jenis | Social engineering — OTP phishing |
|---|---|
| Kesalahan | Memberitahu OTP ke orang lain |
| Seharusnya | OTP = rahasia! Tidak boleh diberi ke siapa pun |
| Pelaporan | Hubungi bank segera + blokir rekening |

---

### E. TIPS KEAMANAN RINGKASAN

| Platform | Tips Utama |
|---|---|
| **Marketplace** | Bayar lewat escrow, cek rating, jangan transfer langsung |
| **M-Banking** | Jangan share OTP, aktivasi notifikasi, limit transaksi |
| **Dompet Digital** | PIN kuat, top-up secukupnya, scan QR dari merchant tepercaya |
| **Umum** | 2FA di semua akun, password unik per platform, waspada phishing |

> **Ingat: OTP adalah RAHASIA. Tidak ada bank/marketplace yang minta OTP!**

---

**MGMP Informatika SMAN 6 Cimahi**
