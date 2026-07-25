# MODUL AJAR INFORMATIKA – FASE E (KELAS X)

## Informasi Umum

| Komponen | Deskripsi |
|---|---|
| **Mata Pelajaran** | Informatika |
| **Fase / Kelas** | E / X |
| **Semester** | 1 (Ganjil) |
| **Pertemuan ke-** | 12 |
| **Alokasi Waktu** | 2 JP × 45 menit (90 menit) |
| **Tahun Pelajaran** | 2026/2027 |
| **Satuan Pendidikan** | **SMA Negeri 6 Cimahi** |

---

## Profil Pelajar Pancasila

| Dimensi | Indikator |
|---|---|
| Mandiri | Mengelola kata sandi akun secara bertanggung jawab |
| Bernalar Kritis | Menganalisis kekuatan dan kelemahan berbagai metode autentikasi |
| Berkebinekaan Global | Melindungi data diri di platform digital global |

---

## Sarana & Prasarana

| Sarana | Keterangan |
|---|---|
| Lab komputer / laptop | 1 unit per siswa |
| Smartphone (milik siswa) | Untuk praktik 2FA & authenticator app |
| Koneksi internet | Untuk aktivasi 2FA |
| Proyektor / LCD | Untuk demo |
| Akun Google/ Microsoft | Masing-masing siswa (untuk praktik 2FA) |

---

## Tujuan Pembelajaran

| TP | Indikator Ketercapaian Tujuan Pembelajaran (IKTP) |
|---|---|
| **LD 2.11:** Memahami cara mengelola kata sandi yang aman | 2.11.1 Membedakan kata sandi kuat dan lemah<br>2.11.2 Menggunakan password manager untuk menyimpan dan menghasilkan kata sandi<br>2.11.3 Menerapkan kebiasaan manajemen kata sandi yang baik |
| **LD 2.12:** Memahami autentikasi dua langkah (2FA) dan cara mengaktifkannya | 2.12.1 Menjelaskan konsep 2FA dan jenis-jenisnya<br>2.12.2 Mengaktifkan 2FA pada akun Google/Microsoft pribadi<br>2.12.3 Membandingkan keamanan SMS 2FA vs authenticator app vs hardware key |

---

## Peta Kompetensi

```
Pertemuan 12 — Manajemen Kata Sandi & 2FA
│
├── Pendahuluan (10 menit)
│   ├── Tugas rumah: siapa yang WiFi-nya WEP?
│   └── Apersepsi: demo bobol password "12345678"
│
├── Inti (65 menit)
│   ├── Memahami (15 menit)
│   │   ├── Kata sandi: statistik, cara bobol, ciri kuat
│   │   └── 2FA: something you know + have / are
│   │
│   ├── Mengaplikasi (40 menit)
│   │   ├── [10'] Demo password manager (Bitwarden / Google PM)
│   │   ├── [15'] Praktik: generate password + simpan
│   │   └── [15'] Praktik: aktivasi 2FA Google
│   │
│   └── Merefleksi (10 menit)
│       └── Analisis keamanan akun sendiri
│
└── Penutup (15 menit)
```

---

## Langkah Pembelajaran

### Pembukaan (10 menit)

| Kegiatan | Waktu |
|---|---|
| 1. Salam, doa, cek kehadiran | 2 menit |
| 2. **Review tugas**: 2–3 siswa lapor hasil cek WiFi rumah — ada yang masih WEP? | 4 menit |
| 3. **Apersepsi**: Guru demo situs **howsecureismypassword.net** — ketik "12345678" → "0 seconds to crack". Ketik "Sman6Cimahi#2026" → "200 years". Bandingkan reaksi siswa. "Berapa lama password kalian bisa bertahan?" | 2 menit |
| 4. Sampaikan tujuan: hari ini kita amankan semua akun dengan password kuat + 2FA | 2 menit |

### Inti (65 menit)

#### Memahami (berkesadaran, menggembirakan) — 15 menit

1. **Kata Sandi: Lemah vs Kuat (5 menit)**

   | Password Lemah | Waktu Bobol | Password Kuat | Waktu Bobol |
   |---|---|---|---|
   | `123456` | < 1 detik | `Cimahi#2026!Ku4t` | 2 abad |
   | `password` | < 1 detik | `SayaD1giTaL#2026` | 50 tahun |
   | `sman6cimahi` | 10 detik | `k3AM4n4N_D1gT4L!` | 500 tahun |
   | `nama+panggilan` | < 1 menit | frasa acak 4+ kata | > 1000 tahun |

   **Ciri password kuat:**
   - ✅ ≥ 12 karakter (minimal)
   - ✅ Kombinasi: huruf besar + kecil + angka + simbol
   - ✅ Bukan kata di kamus / data pribadi (tanggal lahir, nama, NIK)
   - ✅ Unik — jangan pakai password yang sama untuk semua akun

2. **Autentikasi Dua Langkah / 2FA (5 menit)**

   ```
   Password (something you KNOW)  
        +  
   2FA (something you HAVE / ARE)
        =  
   Aman!
   ```

   | Faktor | Contoh | Keterangan |
   |---|---|---|
   | **Pengetahuan** | Password, PIN | Sesuatu yang kamu tahu |
   | **Kepemilikan** | SMS, Authenticator app, hardware key | Sesuatu yang kamu punya |
   | **Biometrik** | Sidik jari, Face ID | Sesuatu yang kamu adalah |

   **Mengapa 2FA penting?** Jika password bocor, akun tetap aman karena penyerang butuh faktor kedua.

3. **Password Manager (5 menit)**
   - Masalah: manusia tidak bisa mengingat 50+ password unik
   - Solusi: **password manager** — menyimpan semua password terenkripsi
   - Contoh: Bitwarden (gratis), Google Password Manager, Apple iCloud Keychain
   - Cukup ingat **1 master password** saja

#### Mengaplikasi (bermakna, menggembirakan) — 40 menit

4. **Demo Password Manager (10 menit)**

   **Google Password Manager (built-in Chrome):**
   - Buka Chrome → Settings → Autofill → Password Manager
   - Lihat daftar password yang tersimpan
   - **Cek keamanan**: Password Checkup → lihat password yang bocor/lemah/dipakai ulang

   **Bitwarden (jika ingin alternatif gratis):**
   - Buka bitwarden.com → Register
   - Buat 1 master password yang sangat kuat
   - Tambahkan beberapa akun contoh
   - Gunakan **Password Generator** bawaan (16 karakter, semua jenis)

5. **Aktivitas 1: Generate & Simpan Password (15 menit)**

   | Langkah | Target |
   |---|---|
   | 1. Buka password generator (Chrome built-in / bitwarden) | |
   | 2. Generate 3 password berbeda (masing-masing 16 karakter) | |
   | 3. Simpan ke password manager | |
   | 4. Cek: apakah password lama sudah lemah? | |

   > **Kalau tidak punya banyak akun**: buat password untuk akun fiktif (latihan).

   **Catat di LKPD:**
   - Password sebelum vs setelah (hanya panjang & jenis karakter, jangan tulis password asli!)
   - Jumlah password yang sama dipakai di banyak akun

6. **Aktivitas 2: Aktivasi 2FA Google (15 menit)**

   | Langkah | Keterangan |
   |---|---|
   | 1. Buka **myaccount.google.com** | |
   | 2. Klik **Security** → **2-Step Verification** | |
   | 3. Klik **Get Started** → masuk password | |
   | 4. Pilih metode: **Authenticator app** (Google Authenticator) | **Jangan pilih SMS jika bisa app** |
   | 5. Scan QR code dengan HP | |
   | 6. Masukkan kode 6 digit dari app | |
   | 7. Selesai — 2FA aktif! | |

   **Alternatif (jika tidak bisa Google Authenticator):**
   - Gunakan **Microsoft Authenticator**
   - Atau terima **SMS** (kurang aman tapi lebih baik dari tanpa 2FA)

   **Demo juga:**
   - Cara **backup code** (download/cetak kode cadangan)
   - Cara **logout** dari perangkat yang tidak dikenal

#### Merefleksi (berkesadaran, bermakna) — 10 menit

7. **Analisis Keamanan Akun Sendiri (5 menit)**
   - Buka **Password Checkup** (Google) → lihat skor keamanan
   - Berapa banyak password yang **bocor**? **Lemah**? **Dipakai ulang**?
   - Buat **rencana perbaikan** — password mana yang harus segera diganti

8. **Refleksi Individu (5 menit)**
   - Apakah 2FA sudah aktif? Jika belum, rencana kapan?
   - Satu kebiasaan baru yang akan diterapkan setelah hari ini
   - Skala pemahaman: ___ / 10

### Penutup (15 menit)

| Kegiatan | Waktu |
|---|---|
| 1. Rangkuman: "Password kuat + unik + password manager + 2FA = akun aman" | 3 menit |
| 2. Tanya jawab | 5 menit |
| 3. **Tugas**: Aktifkan 2FA di MINIMAL 1 akun (Google/Apple/Microsoft/IG/WA) + screenshot | 3 menit |
| 4. Sampaikan pertemuan depan: Privasi, Filter Konten & Keamanan Akun | 2 menit |
| 5. Doa & salam | 2 menit |

---

## Asesmen

### Rubrik Formatif — LKPD

| Kriteria | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| **Password manager** | Tidak mencoba | Mencoba generate | Generate + simpan | Generate + simpan + analisis keamanan |
| **2FA aktivasi** | Tidak aktif | Aktif SMS | Aktif authenticator app | App + backup code disimpan |
| **Refleksi & analisis** | Tidak mengisi | Analisis minimal | Analisis cukup | Analisis mendalam + rencana perbaikan |

---

**MGMP Informatika SMAN 6 Cimahi**
