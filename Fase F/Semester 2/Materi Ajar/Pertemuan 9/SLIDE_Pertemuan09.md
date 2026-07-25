---
marp: true
theme: uncover
class: invert
---

# PERTEMUAN 9 — FASE F (S2)
## Troubleshooting Jaringan 🔧
### Informatika – Fase F / Kelas XI
#### SMA Negeri 6 Cimahi

---

## Review — Pert 8

```
Cloud Computing → aplikasi di awan

Tapi bagaimana kalau:
"Internet lemot?"
"Web tidak bisa dibuka?"
```

> **Troubleshooting!** Jadi admin jaringan!

---

## Apersepsi

> Wi-Fi sekolah lemot. Web error. Bagaimana cara cek?

> Apakah internet mati? Server down? DNS error? Kabel putus?

> **Gunakan TOOL!** 🛠️

---

## Tujuan Pembelajaran

1. ✅ `ping` — uji koneksi
2. ✅ `traceroute` — lacak jalur
3. ✅ `ipconfig` — cek IP
4. ✅ `nslookup` — cek DNS
5. ✅ Diagnosa masalah

---

## Langkah Troubleshooting

```
1. Identifikasi — apa yang terjadi?
2. Isolasi — 1 komputer atau semua?
3. Test — gunakan tool
4. Analisis — arti hasil
5. Solusi — perbaiki
6. Verifikasi — pastikan selesai
```

---

## ping — Uji Koneksi

```bash
ping google.com
ping -c 4 8.8.8.8
```

| Hasil | Arti |
|---|---|
| ✅ Reply | Koneksi OK |
| ❌ Timeout | Host mati / firewall |
| ❌ Unreachable | Tidak ada rute |
| ⚠️ Packet loss | Koneksi tidak stabil |

---

## Demo: Ping

> Buka terminal → `ping google.com`

Hasil:
```
64 bytes from 142.250.1.1: time=12ms
→ ✅ Koneksi OK! Latensi 12 ms
```

---

## traceroute — Lacak Jalur

```bash
tracert google.com    # Windows
traceroute google.com # Linux/Mac
```

```
Hop 1:  192.168.1.1    [Router rumah]     <1 ms
Hop 2:  10.0.0.1       [ISP]              2 ms
Hop 3:  172.16.1.2     [ISP regional]     5 ms
...
Hop 10: 142.250.1.1    [Google server]    12 ms
```

> Lihat jalur data dari sekolah ke Google! 🌐

---

## ipconfig — Cek IP

```bash
ipconfig        # Windows
ifconfig        # Linux/Mac
```

```
IPv4 Address: 192.168.1.10    ✅ Normal
Subnet Mask: 255.255.255.0
Default Gateway: 192.168.1.1
DNS Server: 8.8.8.8
```

⚠️ Jika IP `169.254.x.x` → kabel lepas / DHCP error!

---

## nslookup — Cek DNS

```bash
nslookup google.com
```

```
Server:  dns.google (8.8.8.8)
Name:    google.com
Address: 142.250.1.1
```

> Web error → cek DNS dulu!

---

## Aktivitas 1 — Ping

### 20 menit — Individu

Ping 4 host:
```
1. google.com
2. 8.8.8.8
3. sman6cimahi.sch.id
4. 192.168.1.1 (gateway)
```

> Catat hasil + analisis!

---

## Aktivitas 2 — Traceroute

### 20 menit — Berpasangan

```
tracert google.com
```

Catat semua hop:
| Hop | IP | Waktu | Lokasi |
|---|---|---|---|

> Berapa hop ke Google? Yang paling lambat?

---

## Aktivitas 3 — Diagnosa

### 30 menit — Kelompok

| Kelompok | Masalah |
|---|---|
| A | LAN terhubung — no internet |
| B | Wi-Fi nyala — web error, WA jalan |
| C | Semua lab mati total |
| D | 1 situs tidak bisa |

> Tulis langkah + perintah + solusi!

---

## Refleksi

- Perintah troubleshooting paling berguna?
- Masalah jaringan pernah dialami?
- Skala 1–10?

---

## Tugas Rumah

> Cari IP router rumah → `ping google.com` → screenshot!

---

## Preview — Pert 10

### Password Manager & 2FA 🔐

> Amankan akun kalian!

---

# Terima Kasih

### MGMP Informatika SMAN 6 Cimahi

> "Troubleshooting = detective work — cari petunjuk, analisis, perbaiki!"
