# MODUL AJAR INFORMATIKA – FASE F (KELAS XI)

| Komponen | Deskripsi |
|---|---|
| **Mata Pelajaran** | Informatika |
| **Fase / Kelas** | F / XI |
| **Semester** | 2 (Genap) |
| **Pertemuan ke-** | 10 |
| **Alokasi Waktu** | 5 JP × 45 menit (225 menit) |
| **Tahun Pelajaran** | 2026/2027 |
| **Satuan Pendidikan** | SMA Negeri 6 Cimahi |
| **Materi Esensial** | Konsep Sistem dan Keamanan Jaringan Komputer |

---

## Tujuan Pembelajaran

| TP | IKTP |
|---|---|
| **LD:** Mengelola kata sandi dengan manajer kata sandi dan autentikasi dua langkah | 10.1 Menjelaskan risiko penggunaan password lemah & reuse |
| | 10.2 Menggunakan password manager (Bitwarden) |
| | 10.3 Mengaktifkan 2FA dengan authenticator app |
| | 10.4 Membuat kebiasaan keamanan digital yang baik |

---

## Langkah Pembelajaran

### Pembukaan (20 menit)

| Kegiatan | Waktu |
|---|---|
| 1. Salam, doa, cek kehadiran | 3 menit |
| 2. **Review**: "Pert 9: troubleshooting jaringan — tool untuk diagnosa. Sekarang: amankan akun kalian dari peretasan!" | 5 menit |
| 3. **Apersepsi**: "Berapa banyak akun yang kalian punya? Email, IG, TikTok, WA, Google Classroom. Berapa yang pakai password sama? Berapa yang mudah ditebak?" | 7 menit |
| 4. **Trigger**: "Tahun 2024: 10 juta akun bocor di Indonesia — mayoritas karena password lemah + tidak ada 2FA" | 5 menit |

### Inti (170 menit)

#### Memahami (50 menit)

**1. Masalah Password (15 menit)**

| Masalah | Dampak | Contoh |
|---|---|---|
| **Password lemah** | Mudah ditebak / brute force | "123456", "password", "admin", nama sendiri |
| **Reuse password** | 1 akun bocor → semua akun terancam | Pakai password yang sama untuk IG, email, dan Gojek |
| **Tidak pernah ganti** | Risiko tinggi jika terjadi kebocoran | Password 5 tahun tidak diganti |
| **Catat di sembarang tempat** | Bisa dilihat orang lain | Sticky note di monitor, catatan HP tanpa proteksi |
| **Phishing** | Korban memberikan password sendiri | Email/SMS palsu dari "bank" |

**Data Kebocoran Password (2024):**
- 10 juta+ akun Indonesia bocor
- Password paling umum: "123456" (digunakan 5% akun)
- Rata-rata orang punya 100+ akun

**2. Password Manager (20 menit)**

| Konsep | Penjelasan |
|---|---|
| **Apa itu?** | Aplikasi yang menyimpan semua password dalam satu vault terenkripsi — cukup ingat 1 **master password** |
| **Cara kerja** | Password dienkripsi (AES-256) — hanya bisa dibuka dengan master password |
| **Fitur** | Generate password kuat, autofill, sync antar devices, audit keamanan |

**Perbandingan Password Manager:**

| Aplikasi | Harga | Open Source | Fitur |
|---|---|---|---|
| **Bitwarden** | Gratis (premium $10/th) | ✅ Ya | Semua fitur dasar, sync unlimited |
| Google Password Manager | Gratis | ❌ | Terbatas di ekosistem Google |
| Apple iCloud Keychain | Gratis | ❌ | Terbatas di Apple |
| 1Password | Berbayar ($36/th) | ❌ | UI bagus, travel mode |
| LastPass | Freemium | ❌ | Pernah kena breach |

**Mengapa Bitwarden?**
- **Gratis** — tidak ada limitasi fitur penting
- **Open source** — kode bisa diaudit siapa pun
- **Multi-platform** — Windows, Mac, Linux, Android, iOS, browser extension
- **Audit keamanan** — cek password lemah, reuse, kebocoran

**3. 2FA (Two-Factor Authentication) (15 menit)**

> 2FA = autentikasi dengan 2 faktor dari 3 kategori:

| Faktor | Contoh | Aman |
|---|---|---|
| **Something you know** | Password, PIN | ❌ Bisa bocor |
| **Something you have** | HP, token, security key | ✅ Sulit dicuri |
| **Something you are** | Sidik jari, wajah, retina | ✅ Sangat aman |

**Jenis 2FA:**

| Metode | Cara | Aman |
|---|---|---|
| **SMS/OTP** | Kode via SMS | ❌ Rentan SIM swap |
| **Authenticator App** | TOTP (kode 6 digit berganti 30 detik) | ✅✅ |
| **Push Notification** | Approve login dari HP | ✅ |
| **Security Key** | USB/NFC hardware key | ✅✅✅ |

#### Mengaplikasi — Praktik (90 menit)

**4. Demonstrasi Bitwarden (15 menit)**
- Buka `bitwarden.com` → Create Account
- Install browser extension (Chrome/Firefox/Edge)
- Tambah 1 password: login Google
- Generate password kuat (16 karakter, simbol + angka)
- Cek fitur: generator, vault, autofill

**5. Aktivitas 1 — Setup Bitwarden (25 menit) — Individu**

| Langkah | Status |
|---|---|
| 1. Buka bitwarden.com → Register (email + master password) | ✅ / ❌ |
| 2. Download/install browser extension | ✅ / ❌ |
| 3. Login ke extension dengan master password | ✅ / ❌ |
| 4. Tambah 2 akun (IG + Email sekolah) | ✅ / ❌ |
| 5. Generate password kuat untuk akun IG | ✅ / ❌ |
| 6. Cek "Vault Health" → apa yang merah? | ✅ / ❌ |

**Peringatan:** Jangan pakai master password yang sama dengan password akun lain! **Master password harus diingat — tidak bisa di-reset!**

**6. Aktivitas 2 — Setup 2FA (25 menit) — Berpasangan**

**a. Install Google Authenticator (HP)**

| Platform | Cara |
|---|---|
| Android | Play Store → Google Authenticator |
| iOS | App Store → Google Authenticator |

**b. Aktivasi 2FA di Akun Google:**
1. Buka `myaccount.google.com`
2. Keamanan → Verifikasi 2 langkah
3. Pilih "Authenticator app"
4. Scan QR code dengan Google Authenticator
5. Masukkan kode 6 digit dari HP

**Tugas:** Aktivasi 2FA untuk Akun Google atau akun lain yang mendukung

**7. Aktivitas 3 — Audit Password (25 menit) — Individu**

Gunakan fitur **Vault Health** / **Reports** di Bitwarden:

| Laporan | Temuan |
|---|---|
| Password lemah (weak) | ... akun |
| Password reuse | ... akun |
| Password bocor (exposed) | ... akun |
| Total akun | ... |

Tulis rencana perbaikan:
1. Password mana yang harus segera diganti?
2. Akun mana yang perlu 2FA?

**8. Diskusi Refleksi (15 menit) — Pleno**
- "Apakah kalian akan terus pakai Bitwarden?"
- "Apa tantangan terbesar menggunakan password manager?"
- "2FA akun apa saja yang sudah kalian aktifkan?"

#### Merefleksi (15 menit)

**9. Refleksi Jurnal (15 menit)**
- Fitur Bitwarden paling berguna?
- 1 akun yang akan di-2FA setelah pertemuan ini
- Skala pemahaman 1–10

### Penutup (35 menit)

| Kegiatan | Waktu |
|---|---|
| 1. Rangkuman: Password Manager (Bitwarden) → 2FA (Authenticator) → Audit → Kebiasaan baik | 10 menit |
| 2. Kuis lisan: "Bedanya password manager vs catatan biasa? Apa itu TOTP? Kenapa SMS 2FA kurang aman?" | 10 menit |
| 3. Preview: "Pert 11: UU ITE & UU PDP — regulasi keamanan data di Indonesia" | 5 menit |
| 4. Tugas rumah: Aktivasi 2FA di minimal 2 akun + screenshot | 10 menit |

---

## Asesmen

| Kriteria | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| Setup Bitwarden | Tidak | Install | Install + vault | Install + vault + generator |
| Password kuat | Tidak | Generate | Generate + 16 karakter | Generate + audit |
| 2FA aktivasi | Tidak | 1 akun | 1 akun + authenticator | 2 akun + authenticator |
| Audit password | Tidak | 1 laporan | 2 laporan | 3 laporan + rencana |

---

**MGMP Informatika SMAN 6 Cimahi**
