# BAHAN AJAR – PERTEMUAN 9 (S2)
## Troubleshooting Jaringan

| TP | BK — Konsep Sistem dan Keamanan Jaringan Komputer |
|---|---|

---

### A. LANGKAH TROUBLESHOOTING

| Langkah | Kegiatan | Contoh |
|---|---|---|
| 1. Identifikasi | Tanya: apa yang terjadi? kapan? | "Web tidak bisa dibuka sejak tadi pagi" |
| 2. Isolasi | Apakah 1 komputer atau semua? | "Coba buka di komputer lain" |
| 3. Test | Gunakan tool diagnostik | `ping`, `traceroute`, `ipconfig` |
| 4. Analisis | Arti hasil test | "Ping timeout → kemungkinan firewall" |
| 5. Solusi | Lakukan perbaikan | "Restart router" |
| 6. Verifikasi | Pastikan masalah selesai | "Buka web lagi" |

---

### B. PERINTAH DASAR TROUBLESHOOTING

#### 1. `ping` — Uji Koneksi

**Fungsi:** Mengirim paket ICMP ke host tujuan dan mengukur waktu respon.

```bash
# Windows
ping google.com
ping -n 4 8.8.8.8

# Linux / macOS
ping -c 4 google.com
ping -c 4 192.168.1.1
```

**Output:**
```
PING google.com (142.250.1.1): 56 bytes
64 bytes from 142.250.1.1: icmp_seq=1 ttl=118 time=12.3 ms
64 bytes from 142.250.1.1: icmp_seq=2 ttl=118 time=11.8 ms

--- google.com ping statistics ---
4 packets transmitted, 4 received, 0% packet loss
time avg = 12.0 ms
```

**Interpretasi:**

| Hasil | Arti | Tindakan |
|---|---|---|
| `Reply` / `64 bytes` | Koneksi OK | ✅ |
| `Request timed out` | No response | Host mati / firewall blok / jaringan putus |
| `Destination host unreachable` | Tidak ada rute | Cek gateway |
| `TTL expired` | Too many hops | Ada routing loop |
| `Packet loss > 10%` | Koneksi tidak stabil | Cek Wi-Fi / kabel |

#### 2. `traceroute` / `tracert` — Lacak Jalur

**Fungsi:** Menampilkan setiap router (hop) yang dilalui data ke tujuan.

```bash
# Windows
tracert google.com

# Linux / macOS
traceroute google.com
```

**Output:**
```
 1  <1 ms  <1 ms  <1 ms  192.168.1.1          [Router rumah]
 2   2 ms   2 ms   2 ms  10.0.0.1             [ISP lokal]
 3   5 ms   5 ms   6 ms  172.16.1.2           [ISP regional]
 4  10 ms  12 ms  10 ms  74.125.244.1         [Google edge]
 5  11 ms  11 ms  12 ms  142.250.1.1          [Google server]
```

**Interpretasi:**

| Hop | Waktu | Arti |
|---|---|---|
| 1 | < 1 ms | Router rumah — sangat dekat |
| 2–3 | 2–10 ms | ISP — dalam kota |
| 4–5 | 10–50 ms | Server tujuan |
| **Tiba-tiba tinggi** | > 100 ms | Kemungkinan jaringan padat / jalur jauh |
| `* * *` (3 kali) | Timeout | Router tidak respon — konfigurasi security |

#### 3. `ipconfig` / `ifconfig` — Konfigurasi IP

**Fungsi:** Melihat alamat IP, subnet mask, gateway, DNS.

```bash
# Windows
ipconfig
ipconfig /all

# Linux
ifconfig
ip addr

# macOS
ifconfig
```

**Output `ipconfig`:**
```
Wireless LAN adapter Wi-Fi:
   IPv4 Address: 192.168.1.10
   Subnet Mask: 255.255.255.0
   Default Gateway: 192.168.1.1
   DNS Server: 192.168.1.1 / 8.8.8.8
```

**Interpretasi:**

| Informasi | Arti | Masalah Jika |
|---|---|---|
| `192.168.x.x` | IP pribadi (LAN) | — |
| `169.254.x.x` | APIPA — tidak dapat IP dari DHCP | Kabel/wireless tidak terhubung |
| `0.0.0.0` | Tidak ada IP | NIC mati / driver error |
| Gateway kosong | Tidak ada router | Tidak bisa internet |

#### 4. `netstat` — Koneksi Aktif

**Fungsi:** Menampilkan koneksi jaringan aktif, port terbuka.

```bash
netstat -an           # Semua koneksi + port
netstat -b            # (Windows) aplikasi yang pakai koneksi
netstat -an | findstr 443   # Cari koneksi HTTPS
```

**Output:**
```
Proto  Local Address     Foreign Address    State
TCP    192.168.1.10:54321 142.250.1.1:443    ESTABLISHED
TCP    192.168.1.10:54322 8.8.8.8:53         TIME_WAIT
```

| State | Arti |
|---|---|
| `ESTABLISHED` | Koneksi aktif |
| `LISTEN` | Port terbuka menunggu koneksi |
| `TIME_WAIT` | Koneksi ditutup |
| `CLOSE_WAIT` | Menunggu ditutup |

#### 5. `nslookup` — Cek DNS

**Fungsi:** Menerjemahkan domain ke IP atau sebaliknya.

```bash
nslookup google.com           # Cari IP google
nslookup 8.8.8.8              # Cari domain dari IP
nslookup google.com 8.8.8.8   # Pakai DNS tertentu
```

**Output:**
```
Server:  dns.google
Address:  8.8.8.8

Non-authoritative answer:
Name:    google.com
Addresses:  142.250.1.1
```

**Guna:**
- Apakah DNS bekerja? Jika `nslookup` gagal → DNS error
- Bandingkan DNS penyedia vs Google DNS (8.8.8.8)

---

### C. SKENARIO TROUBLESHOOTING

#### Skenario 1: "No Internet" — LAN terhubung

| Langkah | Perintah | Hasil | Analisis |
|---|---|---|---|
| 1 | `ipconfig` | IP 169.254.x.x | DHCP error — tidak dapat IP |
| 2 | `ipconfig /renew` | IP 192.168.1.10 | Dapat IP — selesai |

#### Skenario 2: "Web tidak bisa — WhatsApp jalan"

| Langkah | Perintah | Hasil | Analisis |
|---|---|---|---|
| 1 | `ping 8.8.8.8` | OK | Koneksi internet OK |
| 2 | `ping google.com` | Timeout | DNS bermasalah |
| 3 | `nslookup google.com` | Gagal | DNS server down |
| 4 | Ganti DNS ke 8.8.8.8 | ✅ Web bisa | DNS selesai |

#### Skenario 3: "Semua komputer mati"

| Langkah | Perintah | Hasil | Analisis |
|---|---|---|---|
| 1 | Cek 1 komputer | Tidak bisa | Bukan masalah per komputer |
| 2 | `ping 192.168.1.1` | Timeout | Router mati |
| 3 | Restart router | ✅ Semua bisa | Router selesai |

---

### D. RANGKUMAN

| Perintah | Fungsi | Contoh |
|---|---|---|
| `ping` | Uji koneksi ke host | `ping google.com` |
| `traceroute` | Lacak jalur data | `tracert google.com` |
| `ipconfig` | Lihat konfigurasi IP | `ipconfig /all` |
| `netstat` | Lihat koneksi aktif | `netstat -an` |
| `nslookup` | Cek DNS | `nslookup google.com` |

| Masalah | Test | Kemungkinan |
|---|---|---|
| Tidak bisa internet | `ping 8.8.8.8` | Kabel, router, DHCP |
| Web tidak bisa | `nslookup` | DNS |
| Lambat | `ping` latency | Wi-Fi lemah, bandwidth penuh |
| 1 situs tidak bisa | `traceroute` | Server down, firewall |

---

**MGMP Informatika SMAN 6 Cimahi**
