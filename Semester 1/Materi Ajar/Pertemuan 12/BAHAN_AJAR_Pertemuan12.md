# BAHAN AJAR – PERTEMUAN 12
## Manajemen Kata Sandi & Autentikasi 2 Langkah

| TP | LD 2.11, 2.12 |
|---|---|

---

### A. MENGAPA KATA SANDI PENTING?

**Statistik:**
- 81% pelanggaran data disebabkan password lemah atau bocor
- 65% orang menggunakan password yang sama di banyak akun
- Password paling umum di Indonesia: `123456`, `password`, `bismillah`

---

### B. CIRI KATA SANDI KUAT

| Aspek | Lemah | Kuat |
|---|---|---|
| Panjang | < 8 karakter | ≥ 12 karakter |
| Variasi | Huruf kecil saja | Huruf Besar + kecil + angka + simbol |
| Data pribadi | Tanggal lahir, nama, NIK | Bukan data pribadi |
| Keunikan | Sama untuk semua akun | Berbeda setiap akun |
| Pola | `qwerty123`, `abc123` | Acak, tidak berpola |

**Cara mengecek kekuatan password:**
- Buka **passwordmonster.com** atau **howsecureismypassword.net**
- Masukkan password contoh (jangan password asli!)

---

### C. PASSWORD MANAGER — SOLUSI INGAT BANYAK PASSWORD

#### Cara Kerja
1. Semua password disimpan dalam **brankas digital** (terenkripsi AES-256)
2. Brankas dikunci dengan **1 master password** (yang harus kamu ingat)
3. Password manager bisa auto-fill saat login

| Password Manager | Gratis? | Platform | Fitur Unggulan |
|---|---|---|---|
| **Google Password Manager** | ✅ | Chrome, Android | Built-in, password checkup |
| **Bitwarden** | ✅ | Semua platform | Open source, murah premium |
| **Apple iCloud Keychain** | ✅ | Apple ecosystem | Terintegrasi dengan Face ID/Touch ID |
| **KeePassXC** | ✅ | Desktop | Offline, open source |

#### Fitur Password Generator
Password manager bisa **membuatkan** password acak:
- Panjang: 16–20 karakter
- Sertakan: huruf besar, huruf kecil, angka, simbol
- Hindari karakter ambigu (Il1O0)

---

### D. AUTENTIKASI DUA LANGKAH (2FA)

#### Konsep
2FA menambahkan **lapisan kedua** setelah password.

```
Password dicuri? Masih butuh kode 2FA!
```

#### Jenis-jenis 2FA

| Metode | Cara Kerja | Tingkat Keamanan | Kelemahan |
|---|---|---|---|
| **SMS / Telepon** | Kode dikirim via SMS | 🟡 Cukup | SIM swap, penyadapan SMS |
| **Authenticator App** | Kode 6 digit berubah tiap 30 detik | 🟢 Aman | HP hilang (backup code penting!) |
| **Push Notification** | Notifikasi "Login?" → Tap Ya/Tidak | 🟢 Aman | Butuh koneksi internet |
| **Hardware Key** | USB/NFC key (YubiKey, Titan) | 🟢🟢 Paling aman | Biaya, bisa hilang |
| **Biometrik** | Sidik jari, Face ID | 🟢 Aman | Bisa ditiru (jarang) |

#### Cara Aktivasi 2FA di Google

1. Buka **myaccount.google.com**
2. Pilih **Security** → **2-Step Verification**
3. Masukkan password
4. Pilih metode:
   - **Authenticator app** (paling disarankan)
   - **SMS** (jika tidak bisa app)
5. Scan QR code → masukkan kode 6 digit
6. **Backup code**: download / cetak kode cadangan
7. Selesai!

#### Backup Code
- 10 kode cadangan (sekali pakai)
- Simpan di tempat aman (brankas, dompet, password manager)
- Gunakan jika HP hilang → tetap bisa login

---

### E. PRAKTIK BAIK MANAJEMEN PASSWORD

| Ya | Tidak |
|---|---|
| ✅ Gunakan password manager | ❌ Simpan password di notes HP |
| ✅ Aktifkan 2FA di semua akun penting | ❌ Pakai password yang sama untuk akun bank & IG |
| ✅ Ganti password jika ada notifikasi bocor | ❌ Bagikan password ke teman/keluarga |
| ✅ Backup code disimpan aman | ❌ Screenshot backup code di galeri HP |
| ✅ Cek keamanan password berkala | ❌ Pakai tanggal lahir sebagai password |

---

### F. Rangkuman

1. **Password kuat**: ≥ 12 karakter, campur jenis, unik, bukan data pribadi
2. **Password manager**: Simpan & generate password dengan aman
3. **2FA**: Lapisan ke-2 setelah password — wajib diaktifkan!
4. **Authenticator app** > **SMS** > **Tidak ada 2FA**

---

**MGMP Informatika SMAN 6 Cimahi**
