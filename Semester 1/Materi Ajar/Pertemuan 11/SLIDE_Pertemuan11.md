---
marp: true
theme: uncover
class: invert
---

# PERTEMUAN 11
## Keamanan Dasar Jaringan
### Informatika – Fase E / Kelas X
#### SMA Negeri 6 Cimahi

---

## Review — PTS

PTS sudah selesai.
Sekarang kita mulai **Bagian 4: Keamanan Digital**!

---

## Apersepsi

**Coba jawab jujur:**
- Siapa yang WiFi-nya **dipakai orang lain** tanpa izin?
- Siapa yang pernah HP-nya tiba-tiba ada notifikasi **perangkat baru terhubung**?
- Siapa yang masih pakai password WiFi **12345678**?

> Hari ini kita akan **mengamankan** jaringan kita!

---

# TUJUAN PEMBELAJARAN

1. ✅ Mengenal jenis jaringan & ancamannya
2. ✅ Membedakan enkripsi WiFi (WEP, WPA, WPA2, WPA3)
3. ✅ Mengonfigurasi hotspot dengan aman
4. ✅ Mengaktifkan & mengecek firewall

---

## Jenis Jaringan

| Jaringan | Jangkauan | Risiko |
|---|---|---|
| **PAN** | Personal (Bluetooth, hotspot) | Penyadapan jarak dekat |
| **LAN** | Lokal (lab, kantor) | Penyadapan fisik |
| **WiFi** | 30–100 m | Snooping, password lemah |
| **Internet** | Global | MITM, phishing |

---

## Enkripsi WiFi — Evolusi

| Standar | Keamanan | Status |
|---|---|---|
| **WEP** (1997) | 🔴 Bobol < 5 menit | ❌ |
| **WPA** (2003) | 🟡 Bobol < 1 jam | ❌ |
| **WPA2** (2004) | 🟢 Standar minimal | ✅ Wajib |
| **WPA3** (2018) | 🟢🟢 Paling aman | ✅ Rekomendasi |

> **Tips:** Cek enkripsi WiFi yang kamu pakai sekarang!

---

## Ancaman Jaringan

| Ancaman | Cara Kerja |
|---|---|
| **Sniffing** | Menangkap data yang lewat |
| **MITM** | Menyusup di tengah koneksi |
| **Evil Twin** | WiFi palsu mirip asli |
| **Password lemah** | Dibobol dalam detik |

---

## Aktivitas 1: Cek WiFi Sekitar

### Langkah (15 menit — Berpasangan):

1. Buka daftar **SSID** yang terdeteksi
2. Catat **Security type** masing-masing
3. Cari SSID mencurigakan (nama aneh, tanpa password?)

> ⚠️ **Etika:** Lihat saja, jangan coba masuk!

---

## Aktivitas 2: Konfigurasi Hotspot

### Atur hotspot HP-mu! (10 menit)

| Langkah | Target |
|---|---|
| SSID | Jangan pakai nama pribadi |
| Security | WPA2 / WPA3 **(bukan Open)** |
| Password | ≥ **12 karakter** + kombinasi |
| Band | **5 GHz** (lebih aman) |

> **Matikan hotspot** jika tidak dipakai!

---

## Aktivitas 3: Cek Firewall

### Cek firewall komputermu (15 menit)

| OS | Cara Cek |
|---|---|
| **Windows** | Control Panel → Windows Defender Firewall |
| **Linux** | Terminal: `sudo ufw status` |
| **macOS** | System Settings → Network → Firewall |

> **Pastikan ON** untuk semua jaringan!

---

## Diskusi

1. Apa yang paling mengejutkan?
2. Adakah SSID mencurigakan? Ciri-cirinya?
3. Kenapa WiFi publik berbahaya?

> "Jaringan yang tidak aman = rumah tanpa pintu"

---

## Rangkuman

| Kunci Keamanan | Praktik |
|---|---|
| **Enkripsi** | WPA2/WPA3 minimal |
| **Password** | ≥ 12 karakter |
| **Firewall** | Aktifkan selalu |
| **WiFi publik** | Hindari login penting |
| **Hotspot** | Matikan jika tidak dipakai |

---

## Tugas Rumah

### Cek keamanan WiFi rumahmu:
- SSID & enkripsi (WEP/WPA/WPA2/WPA3?)
- Password ≥ 12 karakter?
- Apakah perlu diperbaiki?

> Catat di LKPD!

---

## Pertemuan Berikutnya

### Manajemen Kata Sandi & Autentikasi 2 Langkah

> Password manager, 2FA, Face ID — amankan akunmu!

---

# Terima Kasih

### MGMP Informatika SMAN 6 Cimahi

> "Jaringan aman = data aman = kamu aman."
