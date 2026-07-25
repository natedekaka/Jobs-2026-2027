---
marp: true
theme: uncover
class: invert
---

# PERTEMUAN 10 — FASE F (S2)
## Password Manager & 2FA 🔐
### Informatika – Fase F / Kelas XI
#### SMA Negeri 6 Cimahi

---

## Review — Pert 9

```
Troubleshooting → diagnosa jaringan

Sekarang:
Amankan AKUN kalian! 🔒
```

---

## Apersepsi

> Berapa akun online kalian? IG? TikTok? Email? Gojek?

> Berapa yang pakai **password sama**?

> 🔓 **1 akun bocor → SEMUA AKUN TERANCAM!**

---

## Masalah Password

| Fakta | Data |
|---|---|
| Rata-rata akun per orang | 100+ |
| Reuse password | 65% orang |
| Password "123456" | < 1 detik di-brute-force |
| Akun Indonesia bocor 2024 | 10+ juta |

---

## Password Lemah vs Kuat

| Password | Waktu Brute Force |
|---|---|
| `123456` | < 1 detik ❌ |
| `sman6cimahi` | 2 detik ❌ |
| `Sm4n6C1mah!` | 3 jam ⚠️ |
| `G7$kL9#pQ2@mR5!` | 5 abad ✅ |

---

## Solusi: Password Manager 🔐

> **Bitwarden** — gratis, open source, aman!

| Cukup ingat | 1 master password |
|---|---|
| Simpan | 100+ password di vault |
| Generate | Password 16+ karakter |

---

## Cara Kerja Bitwarden

```
Master Password ↓
         │
   ┌─────┴─────┐
   │  VAULT     │
   │ (AES-256)  │
   │ IG: pass.. │
   │ Email: ... │
   └─────┬─────┘
         │
         ▼
   🔄 Auto-fill di browser
   🎲 Generate password kuat
   📊 Audit keamanan
```

---

## Aktivitas 1 — Setup Bitwarden

### 25 menit — Individu

```
1. bitwarden.com → Register
2. Install browser extension
3. Tambah 2 akun
4. Generate password kuat untuk IG
```

⚠️ **Master password: INGAT! Tidak bisa di-reset!**

---

## 2FA — Lapisan Keamanan Kedua

> Password + Kode dari HP = **2FA**

| Metode | Aman? |
|---|---|
| SMS/OTP | ❌ SIM swap |
| **Authenticator App** | ✅✅ |
| Security Key | ✅✅✅ |

---

## Aktivitas 2 — Setup 2FA

### 25 menit — Berpasangan

1. Install **Google Authenticator** di HP
2. Buka `myaccount.google.com`
3. Verifikasi 2 langkah
4. Scan QR → kode 6 digit
5. ✅ Aktif!

---

## Aktivitas 3 — Audit Password

### 25 menit — Individu

Di Bitwarden → Reports:

| Check | Temuan |
|---|---|
| Weak passwords | ... |
| Reused passwords | ... |
| Exposed passwords | ... |

Buat rencana perbaikan!

---

## Refleksi

- Fitur Bitwarden paling berguna?
- 1 akun yang akan di-2FA?
- Skala 1–10?

---

## Tugas Rumah

> 2FA di minimal 2 akun + screenshot!

---

## Preview — Pert 11

### UU ITE & UU PDP

> Regulasi keamanan data di Indonesia!

---

# Terima Kasih

### MGMP Informatika SMAN 6 Cimahi

> "Password kuat + 2FA = aman 99% dari peretasan!"
