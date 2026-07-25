# MODUL AJAR INFORMATIKA – FASE F (KELAS XI)

| Komponen | Deskripsi |
|---|---|
| **Mata Pelajaran** | Informatika |
| **Fase / Kelas** | F / XI |
| **Semester** | 1 (Ganjil) |
| **Pertemuan ke-** | 17 |
| **Alokasi Waktu** | 5 JP × 45 menit (225 menit) |
| **Tahun Pelajaran** | 2026/2027 |
| **Satuan Pendidikan** | SMA Negeri 6 Cimahi |
| **Materi Esensial** | Konsep Sistem dan Keamanan Jaringan |

---

## Tujuan Pembelajaran

| TP | IKTP |
|---|---|
| **BK, AP:** Memahami konsep sistem komputer dan keamanan jaringan | 17.1 Menjelaskan konsep sistem dan contohnya |
| | 17.2 Menjelaskan arsitektur jaringan (LAN, WAN, client-server) |
| | 17.3 Mengidentifikasi jenis ancaman keamanan jaringan |
| | 17.4 Menjelaskan teknik keamanan (enkripsi, firewall, HTTPS) |
| | 17.5 Menjelaskan regulasi terkait keamanan data (UU ITE) |

---

## Langkah Pembelajaran

### Pembukaan (20 menit)

| Kegiatan | Waktu |
|---|---|
| 1. Salam, doa, cek kehadiran | 3 menit |
| 2. **Review**: "Pert 14–16: Big Data → Olah Data → Visualisasi. Sekarang: bagaimana data dikirim & diamankan?" | 5 menit |
| 3. **Apersepsi**: "Kalian kirim chat WA, buka e-commerce, transfer uang — data kalian lewat mana? Apakah aman?" | 7 menit |
| 4. **Trigger**: "Tahun ini ada berita kebocoran data? Siapa yang kena?" | 5 menit |

### Inti (170 menit)

#### Memahami (65 menit)

**1. Konsep Sistem (15 menit)**

| Definisi | Contoh |
|---|---|
| Sistem = kumpulan elemen yang saling berinteraksi untuk mencapai tujuan | Sistem pencernaan, sistem transportasi, sistem komputer |
| **Sistem Komputer**: Input → Proses → Output → Feedback | CPU, RAM, storage, OS |
| **Sistem Informasi**: Data → Informasi → Pengetahuan → Keputusan | SIAKAD, e-commerce |

**2. Jaringan Komputer (20 menit)**

| Jenis | Jangkauan | Contoh |
|---|---|---|
| **PAN** | Personal (1–10 m) | Bluetooth HP ke laptop |
| **LAN** | Lokal (gedung/kampus) | Lab komputer sekolah |
| **MAN** | Kota | Wi-Fi kota |
| **WAN** | Negara/dunia | Internet |

**Model Arsitektur:**
- **Client-Server**: Server pusat, client terhubung (web, email)
- **Peer-to-Peer**: Setiap node setara (torrent, blockchain)

**Protokol:**
- **TCP/IP**: Dasar internet — pecah data jadi paket, kirim, rakit ulang
- **HTTP/HTTPS**: Web — HTTPS = aman (SSL/TLS)
- **DNS**: Terjemahkan domain (google.com) → IP

**3. Ancaman Keamanan Jaringan (15 menit)**

| Ancaman | Cara Kerja | Contoh |
|---|---|---|
| **Malware** | Virus, worm, trojan, ransomware | WannaCry (2017) — enkripsi data, tebus $300 |
| **Phishing** | Tipuan email/SMS minta data | Email "Akun Anda diblokir" → link palsu |
| **DoS/DDoS** | Banjiri server dengan traffic | Serangan ke situs bank/ pemerintah |
| **Man-in-the-Middle** | Sadap komunikasi 2 pihak | Wi-Fi publik palsu |
| **SQL Injection** | Inject kueri SQL ke form login | Ambil database pengguna |
| **Social Engineering** | Manipulasi psikologis | Telepon "Saya dari IT, minta password" |

**4. Teknik Keamanan (15 menit)**

| Teknik | Cara Kerja | Contoh |
|---|---|---|
| **Enkripsi** | Ubah data jadi ciphertext, butuh kunci dekripsi | AES, RSA, SSL/TLS |
| **Firewall** | Filter traffic berdasarkan aturan | Windows Firewall, router ACL |
| **Autentikasi** | Verifikasi identitas | Password, biometric, 2FA |
| **OTP** | One-Time Password — kode sekali pakai | SMS/email kode login |
| **HTTPS** | HTTP + SSL/TLS — data terenkripsi | 🔒 di browser |
| **VPN** | Tunnel terenkripsi ke jaringan lain | Bypass blokir, kerja remote |

#### Mengaplikasi (75 menit)

**5. Diskusi Kasus (20 menit) — Kelompok**

Setiap kelompok mendapat 1 studi kasus:

| Kelompok | Kasus |
|---|---|
| A | Kebocoran data Tokopedia (2020) — 91 juta akun bocor |
| B | Ransomware WannaCry (2017) — 200.000 korban di 150 negara |
| C | Phishing BRI (2023) — link palsu undian berhadiah |
| D | Serangan DDoS ke situs KPU (2024) — pemilu terganggu |

**Tugas**: Analisis — (1) jenis ancaman, (2) bagaimana terjadi, (3) dampak, (4) bagaimana mencegah?

**6. Aktivitas 1 — Simulasi Enkripsi Sederhana (20 menit) — Berpasangan**

**Metode Caesar Cipher** — enkripsi paling sederhana.

| Plaintext | Geser 3 → | Ciphertext |
|---|---|---|
| A | | D |
| B | | E |
| INFORMATIKA | | LQIRUPDWLND |

**Langkah:**
- Satu siswa tulis pesan → enkripsi Caesar shift 3 → beri ke pasangan
- Pasangan dekripsi (geser mundur 3)
- Diskusi: "Apa kelemahan Caesar Cipher?"

**7. Aktivitas 2 — Praktik Cek Keamanan Website (20 menit) — Individu**

Buka 5 website — isi tabel:

| Website | HTTPS? (🔒) | Sertifikat berlaku? | Domain asli? | Aman? |
|---|---|---|---|---|
| `gmail.com` | | | | |
| `sman6cimahi.sch.id` | | | | |
| `belajar.kemdikbud.go.id` | | | | |
| `tokopedia.com` | | | | |
| (pilih sendiri) | | | | |

**Cara**: Klik 🔒 di address bar → Certificate → lihat masa berlaku.

**8. Aktivitas 3 — Poster Keamanan Jaringan (15 menit) — Kelompok**

Buat poster digital (Canva) berisi:
- 1 jenis ancaman + cara kerja + pencegahan
- Selesai → presentasi kilat (30 detik/kelompok)

#### Merefleksi (15 menit)

**9. Refleksi Jurnal (15 menit)**
- Ancaman paling berbahaya menurut kalian? Mengapa?
- 1 kebiasaan baru yang akan kalian lakukan untuk keamanan data
- Skala pemahaman 1–10

### Penutup (35 menit)

| Kegiatan | Waktu |
|---|---|
| 1. Rangkuman: Sistem → Jaringan → Ancaman → Keamanan → Regulasi | 10 menit |
| 2. Kuis lisan: "Apa itu enkripsi? Bedanya HTTP vs HTTPS? Contoh phishing?" | 10 menit |
| 3. Preview: "Pert 18: PAS — 90 menit soal mencakup semua materi S1!" | 5 menit |
| 4. Tugas rumah: Baca UU ITE pasal 27–35 — catat 3 poin penting | 10 menit |

---

## Asesmen

| Kriteria | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| Konsep sistem & jaringan | Tidak paham | Sebagian | Paham semua | Paham + bisa contoh sendiri |
| Ancaman keamanan | 0–1 disebut | 2–3 disebut | 4–5 disebut | 6 disebut + cara kerja |
| Teknik keamanan | 0–1 teknik | 2–3 teknik | 4 teknik | 5 teknik + kapan digunakan |
| Simulasi enkripsi | Tidak selesai | Enkripsi | Enkripsi + dekripsi | Enkripsi + dekripsi + kelemahan |
| Poster | Tidak buat | Ada, kurang jelas | Jelas, benar | Menarik + benar + dipresentasikan |

---

**MGMP Informatika SMAN 6 Cimahi**
