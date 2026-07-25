# LKPD Pert 11 (S2) – Jaringan Dasar
*Mengacu pada Panduan Mapel 2025; INFORMATIKA Fase D-F — pendekatan Pembelajaran Mendalam (Memahami → Mengaplikasi → Merefleksi)*
| Nama | ____________________ |
|---|---|
| Kelas | ____________________ |





### 🧠 Memahami — Membangun Pemahaman Awal

### Aktivitas 1 — Kuis Jaringan (Individu, 15 menit)
Jawab pertanyaan:
a) Kepanjangan LAN: ____________________
b) Perangkat untuk koneksi internet: ____________________
c) Alamat unik perangkat di jaringan: ____________________
d) Contoh jaringan WAN: ____________________

### Aktivitas 2 — Gambar Topologi (Berpasangan, 25 menit)
Gambar topologi STAR dengan 5 komputer + 1 switch + 1 printer.
Beri label semua perangkat dan jenis kabel.

### Aktivitas 3 — Cek IP (Praktik, 20 menit)
Buka CMD/Terminal. Ketik: ipconfig (Windows) atau ip a (Linux).
Catat: a) IPv4 Address: _____ b) Subnet Mask: _____ c) Default Gateway: _____





### 🔧 Mengaplikasi — Praktik & Penerapan

### Aktivitas 4 — Diskusi (Kelompok, 20 menit)
Diskusikan: bagaimana internet sampai ke Hp/laptopmu di rumah? Gambar alurnya!
ISP -> Modem -> Router -> _____ -> _____ -> Hp/laptop


Catat: Alamat MAC: _____ Berapa digit? _____ (format heksadesimal)
```
ip link      # Linux/Mac
getmac       # Windows
```bash
Cek alamat MAC laptop:
d) Bedakan IP private dan public! Private: _____ Public: _____
c) IP 172.16.0.1 termasuk kelas? _____
b) IP 10.0.0.1 termasuk kelas? _____
a) IP 192.168.1.1 termasuk kelas? _____
d) Apakah ada server lokal? _____
b) Ada berapa switch? _____ c) Koneksi internet dari ISP mana? _____
a) Bagaimana jaringan di lab komputer sekolah?
Diskusikan dan gambar:
Catat: IP google.com: _____ IP sman6cimahi.sch.id: _____
```
nslookup sman6cimahi.sch.id
nslookup google.com
```bash
Skala: ___/10. Jaringan: _________________
### Aktivitas 5 — Tantangan (Individu, 10 menit)
Cek IP website: buka CMD -> ping google.com -> catat waktu respon: ____ ms

Skala: ___/10. Jaringan: _________________

### Aktivitas 6 — Cek DNS (Individu, 10 menit)
```bash
nslookup google.com
nslookup sman6cimahi.sch.id
```
Catat: IP google.com: _____ IP sman6cimahi.sch.id: _____

### Aktivitas 7 — Analisis Jaringan Sekolah (Kelompok, 10 menit)
Diskusikan dan gambar:
a) Bagaimana jaringan di lab komputer sekolah?
b) Ada berapa switch? _____ c) Koneksi internet dari ISP mana? _____
d) Apakah ada server lokal? _____

### Aktivitas 8 — Mengenal IP Address (Individu, 10 menit)
a) IP 192.168.1.1 termasuk kelas? _____
b) IP 10.0.0.1 termasuk kelas? _____
c) IP 172.16.0.1 termasuk kelas? _____
d) Bedakan IP private dan public! Private: _____ Public: _____

### Aktivitas 9 — Alamat MAC (Individu, 10 menit)
Cek alamat MAC laptop:
```bash
getmac       # Windows
ip link      # Linux/Mac
```
Catat: Alamat MAC: _____ Berapa digit? _____ (format heksadesimal)


- Apa konsep paling penting yang kamu pelajari hari ini?
- Bagian mana yang masih sulit dipahami?
- Skala pemahaman diri: ___/10


### 🔍 Merefleksi — Refleksi & Evaluasi

- Apa konsep paling penting yang kamu pelajari hari ini?
- Bagian mana yang masih sulit dipahami?
- Skala pemahaman diri: ___/10

---
**MGMP Informatika SMAN 6 Cimahi — Fase F (Kelas XI) Semester 2**
