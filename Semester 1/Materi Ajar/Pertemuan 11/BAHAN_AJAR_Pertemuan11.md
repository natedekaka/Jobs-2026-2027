# BAHAN AJAR – PERTEMUAN 11
## Keamanan Dasar Jaringan

| TP | LD 2.5 |
|---|---|

---

### A. JENIS-JENIS JARINGAN

| Jenis | Jangkauan | Contoh Penggunaan | Risiko |
|---|---|---|---|
| **PAN** | Personal (1–10 m) | Bluetooth, hotspot HP | Penyadapan jarak dekat |
| **LAN** | Lokal (10–1000 m) | Lab komputer, kantor | ARP spoofing, penyadapan fisik |
| **WLAN (WiFi)** | Nirkabel (30–100 m) | WiFi rumah, sekolah | Snooping, password lemah |
| **MAN** | Kota (10–50 km) | Jaringan ISP | Skala besar → risiko besar |
| **WAN / Internet** | Global | Internet | Semua ancaman mungkin terjadi |

---

### B. ENKRIPSI WIFI — KUNCI KEAMANAN NIRKABEL

Enkripsi adalah proses mengacak data agar tidak bisa dibaca oleh pihak yang tidak berwenang.

#### Perbandingan Standar Enkripsi WiFi

| Standar | Metode | Tahun | Kecepatan | Keamanan | Rekomendasi |
|---|---|---|---|---|---|
| **WEP** | RC4 | 1997 | Lambat | 🔴 Bobol < 5 menit | ❌ Jangan dipakai |
| **WPA** | TKIP | 2003 | Cukup | 🟡 Bobol < 1 jam | ❌ Segera ganti |
| **WPA2** | AES-CCMP | 2004 | Cepat | 🟢 Standar minimal | ✅ Minimal wajib |
| **WPA3** | SAE | 2018 | Cepat | 🟢🟢 Tahan brute-force | ✅ Sangat direkomendasikan |

#### Cara Cek Enkripsi WiFi

| Perangkat | Langkah |
|---|---|
| **Windows 10/11** | Klik ikon WiFi di taskbar → Properties (pada SSID terhubung) → lihat Security type |
| **Android** | Settings → WiFi → gear icon di samping SSID → Security / Advanced |
| **iPhone / iPad** | Settings → WiFi → ikon (i) di samping SSID → Security |

---

### C. ANCAMAN KEAMANAN JARINGAN

#### 1. Snooping & Packet Sniffing

| Ancaman | Cara Kerja | Dampak |
|---|---|---|
| **Sniffing** | Menangkap data yang lewat di jaringan (paket data) | Password, email, chat bisa terbaca |
| **Snooping** | Mengamati aktivitas jaringan korban | Mengetahui situs yang dikunjungi |

**Pencegahan:** Gunakan HTTPS (gembok hijau di browser), hindari WiFi publik tanpa VPN.

#### 2. Man-in-the-Middle (MITM)

| Cara Kerja | Contoh |
|---|---|
| Penyerang menyusup di antara korban dan server | WiFi publik "gratis" yang mencatat semua aktivitas |
| Semua data melewati penyerang terlebih dahulu | Login Facebook di WiFi kafe → password dicuri |

**Pencegahan:** Jangan login ke akun penting di WiFi publik, gunakan VPN.

#### 3. Evil Twin / Rogue Access Point

| Cara Kerja | Ciri-ciri |
|---|---|
| Penyerang membuat SSID palsu mirip WiFi asli | SSID: "WiFi SMAN6" (asli) → "WiFi_SMAN6" (palsu) |
| Korban terhubung ke SSID palsu | Tidak pakai password / password mudah |

**Pencegahan:** Konfirmasi SSID asli ke pemilik, gunakan VPN.

#### 4. Password Lemah

| Password | Waktu Bobol |
|---|---|
| `12345678` | < 1 detik |
| `password` | < 1 detik |
| `sman6cimahi` | < 10 detik |
| `K3amananJ4ringan#2026` | > 100 tahun |

---

### D. FIREWALL — PINTU KEAMANAN KOMPUTER

Firewall menyaring lalu lintas jaringan — mana yang boleh masuk/keluar.

#### Cara Cek & Aktifkan Firewall

| OS | Langkah |
|---|---|
| **Windows** | Control Panel → Windows Defender Firewall → Turn on (aktifkan untuk Domain, Private, Public) |
| **Linux** | Terminal: `sudo ufw enable` (aktifkan), `sudo ufw status verbose` (cek status) |
| **macOS** | System Settings → Network → Firewall → Options → Turn on |

**Aturan dasar firewall:**
- Blokir semua koneksi masuk yang tidak diminta
- Izinkan aplikasi tepercaya (browser, game, Zoom)
- Nonaktifkan firewall hanya jika ada masalah (sementara)

---

### E. PRAKTIK KEAMANAN JARINGAN SEHARI-HARI

| Aktivitas | Praktik Aman |
|---|---|
| WiFi rumah | Ganti password default, gunakan WPA2/3, matikan SSID broadcasting (opsional) |
| WiFi publik | Jangan akses perbankan/email, gunakan VPN |
| Hotspot HP | Password ≥ 12 karakter, 5 GHz, matikan jika tidak dipakai |
| Bluetooth | Matikan jika tidak digunakan, nonaktifkan discoverable |
| Kabel LAN | Tidak ada risiko besar, tapi pastikan tidak ada orang asing mencolokkan kabel |

---

### F. Rangkuman

1. **Enkripsi WiFi**: WPA2 adalah minimum, WPA3 adalah terbaik
2. **Ancaman utama**: Sniffing, MITM, Evil Twin, password lemah
3. **Firewall**: Aktifkan selalu — di Windows/Linux/macOS
4. **Kebiasaan aman**: Password panjang, VPN di WiFi publik, matikan hotspot

---

**MGMP Informatika SMAN 6 Cimahi**
