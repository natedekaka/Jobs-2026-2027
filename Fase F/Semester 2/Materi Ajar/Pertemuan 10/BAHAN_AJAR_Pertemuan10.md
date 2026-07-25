# BAHAN AJAR – PERTEMUAN 10 (S2)
## Password Manager & 2FA

| TP | LD — Konsep Sistem dan Keamanan Jaringan Komputer |
|---|---|

---

### A. MASALAH PASSWORD

#### Statistik

| Fakta | Data |
|---|---|
| Rata-rata orang punya | **100+ akun online** |
| Password paling umum | "123456", "password", "admin" — masih digunakan 5% akun |
| Orang yang reuse password | **65%** pakai password yang sama untuk banyak akun |
| Kebocoran akun Indonesia 2024 | **10+ juta akun** |
| Waktu brute force "123456" | **< 1 detik** |

#### Akibat Password Lemah & Reuse

```
          +---------+
          | EMAIL   | ← password: "sman6cimahi"
          +----+----+
               │ (reuse)
     +---------+---------+
     │         │         │
     ▼         ▼         ▼
+--------+ +--------+ +--------+
| IG     | | GOJEK  | | TOKO   |
| pass:  | | pass:  | | pass:  |
| sman6..| | sman6..| | sman6..|
+--------+ +--------+ +--------+

🔓 EMAIL bocor → SEMUA akun terancam!
```

#### Password Kuat vs Lemah

| Password | Kekuatan | Waktu Brute Force |
|---|---|---|
| `123456` | ❌ Sangat lemah | < 1 detik |
| `sman6cimahi` | ❌ Lemah | 2 detik |
| `Sm4n6C1mah!` | ⚠️ Sedang | 3 jam |
| `G7$kL9#pQ2@mR5!` | ✅ Kuat | 5 abad |
| `I-lov3-1nf0rmat1ka-2027!` | ✅✅ Sangat kuat | 2 triliun tahun |

---

### B. PASSWORD MANAGER

#### Apa itu Password Manager?

> Aplikasi yang menyimpan semua password dalam vault terenkripsi — cukup ingat **1 master password**.

#### Cara Kerja

```
                    ┌─────────────────────────┐
                    │   MASTER PASSWORD        │
                    │   (hanya kamu yang tahu)  │
                    └────────┬────────────────┘
                             │
                             ▼
                ┌─────────────────────────┐
                │   VAULT TERENKRIPSI     │
                │   (AES-256)             │
                │                         │
                │   IG: password IG       │
                │   Email: password email │
                │   Google: password G    │
                │   ... (100+ akun)       │
                └─────────────────────────┘
                             │
                             ▼
              ┌─────────────────────────────┐
              │   AUTO-FILL di browser       │
              │   Generate password kuat     │
              │   Audit keamanan             │
              └─────────────────────────────┘
```

#### Bitwarden — Fitur Unggulan

| Fitur | Gratis | Premium ($10/th) |
|---|---|---|
| Vault tidak terbatas | ✅ | ✅ |
| Sync unlimited devices | ✅ | ✅ |
| Password generator | ✅ | ✅ |
| Browser extension | ✅ | ✅ |
| Vault health report | ✅ | ✅ |
| 2FA Authenticator | ✅ | ✅ |
| File attachments | ❌ | ✅ |
| Emergency access | ❌ | ✅ |

#### Cara Setup Bitwarden

| Langkah | Detail |
|---|---|
| 1. Buka | `bitwarden.com` |
| 2. Register | Email + **master password** (ingat! tidak bisa di-reset!) |
| 3. Install | Browser extension (Chrome/Edge/Firefox) |
| 4. Login | Login di extension dengan master password |
| 5. Tambah | Klik "+" → isi nama akun, username, password |
| 6. Generate | Klik ikon gear → pilih panjang (16+), simbol, angka |

---

### C. 2FA (Two-Factor Authentication)

#### Tiga Faktor Autentikasi

| Faktor | Contoh | Keamanan |
|---|---|---|
| **Something you know** | Password, PIN, jawaban security question | Rendah — bisa bocor, bisa ditebak |
| **Something you have** | HP, token, smart card, security key | Tinggi — butuh akses fisik |
| **Something you are** | Sidik jari, face ID, retina, suara | Sangat tinggi — unik |

> **2FA = Password + 1 faktor tambahan**

#### Metode 2FA

| Metode | Cara Kerja | Aman? | Risiko |
|---|---|---|---|
| **SMS/OTP** | Kode 6 digit dikirim via SMS | ❌ | SIM swap attack |
| **Authenticator App** | Kode 6 digit (TOTP) berganti 30 detik | ✅✅ | HP hilang (bisa recovery) |
| **Push Notification** | Notifikasi login ke HP — approve/reject | ✅ | Butuh koneksi internet |
| **Email OTP** | Kode dikirim ke email | ⚠️ | Email bisa diretas |
| **Security Key** | USB/NFC hardware — colok ke laptop | ✅✅✅ | Biaya (~$25) |

#### Cara Kerja TOTP (Time-based One-Time Password)

```
┌──────┐         ┌──────────────────┐
│ WAKTU│────────▶│ GOOGLE            │
│      │         │ AUTHENTICATOR     │
│ 30s  │         │ (HP)              │
│      │         │ Kode: 482915      │
└──────┘         └────────┬─────────┘
                          │
                          ▼
┌──────┐         ┌──────────────────┐
│ SITE │◀────────│ MASUKKAN KODE    │
│      │         │ 482915            │
│ Gmail│         │ ✅ Login sukses   │
└──────┘         └──────────────────┘
```

#### Aktivasi 2FA di Akun Google

| Langkah | Cara |
|---|---|
| 1. Buka | `myaccount.google.com` → Keamanan |
| 2. Verifikasi 2 langkah | Klik "Mulai" |
| 3. Choose method | "Authenticator app" |
| 4. Scan QR | Buka Google Authenticator → Scan QR |
| 5. Verifikasi | Masukkan kode dari HP |
| 6. Backup codes | Simpan kode cadangan (jika HP hilang) |

---

### D. AUDIT KEAMANAN

#### Vault Health Report (Bitwarden)

| Report | Arti | Tindakan |
|---|---|---|
| **Exposed passwords** | Password ditemukan di kebocoran data | Segera ganti! |
| **Reused passwords** | Password dipakai > 1 akun | Ganti — buat unik per akun |
| **Weak passwords** | < 12 karakter, tanpa simbol/angka | Generate ulang |
| **Missing 2FA** | Akun tidak punya 2FA | Aktivasi 2FA |

#### Checklist Keamanan

| Kebiasaan | ✅ |
|---|---|
| Password ≥ 16 karakter | |
| Setiap akun punya password unik | |
| Bitwarden ter-install | |
| 2FA aktif di akun utama (Google, Email) | |
| 2FA pakai authenticator app (bukan SMS) | |
| Backup codes disimpan | |
| Master password diingat (tidak dicatat) | |

---

### E. RANGKUMAN

| Konsep | Inti |
|---|---|
| **Password lemah** | Mudah ditebak — penyebab utama kebocoran |
| **Reuse password** | 1 bocor = semua bocor |
| **Password manager** | Bitwarden (gratis, open source) |
| **2FA** | Password + kode dari HP = aman |
| **TOTP** | Kode 6 digit berganti 30 detik |
| **Authenticator App** | Google Authenticator, Authy |

---

**MGMP Informatika SMAN 6 Cimahi**
