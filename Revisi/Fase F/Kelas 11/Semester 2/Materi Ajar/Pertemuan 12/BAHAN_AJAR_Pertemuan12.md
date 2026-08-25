# BAHAN AJAR – PERTEMUAN 12 (S2)
## Jaringan di Sekitar Kita
*Mengacu pada Panduan Mapel 2025; INFORMATIKA Fase D-F — pendekatan Pembelajaran Mendalam (Memahami → Mengaplikasi → Merefleksi)*

| Informasi | Keterangan |
|---|---|
| **Fase / Kelas** | F / Kelas XI |
| **Alokasi Waktu** | 5 JP × 45 menit (225 menit) |
| **Elemen CP** | Jaringan Komputer dan Internet (JKI) & Dampak Sosial Informatika (DSI) |
| **Tujuan Pembelajaran** | Mengidentifikasi jaringan di lingkungan sekitar, memahami cara kerja WiFi, melakukan pengecekan koneksi, dan melakukan troubleshooting dasar |
| **Materi Prasyarat** | Jaringan Dasar — IP Address & DNS (Pertemuan 11) |

---

## A. Kisah Pemantik 🎬

> **"Pencarian Sinyal di Perpustakaan"**
>
> Setiap kali masuk perpustakaan sekolah, Rina selalu menemukan titik mati di pojok ruangan — WiFi sering putus di sana. Ia mulai mengamati: di dekat jendela cepat, di balik lemari besi lambat. Rina sadar bahwa **jaringan ada di mana-mana** dan dipengaruhi banyak hal: posisi router, halangan dinding, hingga jumlah pengguna.
>
> Sekarang giliranmu menjadi "detektif jaringan": mengamati jaringan di sekolah, rumah, dan kota, lalu belajar memeriksa dan memperbaiki koneksi.
>
> **Pertanyaan pemantik:** Mengapa sinyal WiFi bisa kuat di satu tempat dan lemah di tempat lain? Faktor apa saja yang menurutmu memengaruhi kecepatan internet di sekolahmu?

---

## B. Jaringan di Sekitar Kita 🏫🏠🏙️

**Di Sekolah:**
- Lab komputer memakai LAN kabel UTP.
- WiFi dipancarkan access point di tiap lantai.
- Server menyimpan data guru, siswa, dan nilai.
- Koneksi internet dari ISP melalui fiber optik.

**Di Rumah:**
- Alur: Modem ISP → Router WiFi → perangkat (HP, laptop, TV).
- Jenis koneksi: fiber optik, ADSL, atau seluler (4G/5G).

**Di Kota:**
- Menara BTS untuk sinyal HP.
- Fiber optik bawah tanah menghubungkan antar wilayah.
- Hotspot publik di taman, kafe, dan pusat kota.

| Lokasi | Perangkat Utama | Media Koneksi |
|---|---|---|
| Sekolah | Server, switch, access point | Kabel UTP, fiber optik, WiFi |
| Rumah | Modem, router WiFi | Fiber optik, ADSL, 4G |
| Kota | Menara BTS, backbone fiber | Gelombang radio, fiber optik |

---

## C. Cara Kerja WiFi 📡

**WiFi** (Wireless Fidelity) adalah teknologi koneksi nirkabel memakai gelombang radio.

| Frekuensi | Kelebihan | Kekurangan |
|---|---|---|
| **2.4 GHz** | Jangkauan jauh, tembus dinding | Lebih lambat, rawan gangguan |
| **5 GHz** | Lebih cepat, sedikit gangguan | Jangkauan pendek, mudah terhalang |

| Istilah WiFi | Arti |
|---|---|
| **SSID** | Nama jaringan WiFi yang tampil di daftar |
| **Password** | Kunci untuk masuk ke jaringan |
| **Enkripsi** | Pengaman data, standar: **WPA2 / WPA3** |
| **WPS** | Fitur koneksi cepat — sebaiknya dinonaktifkan |

> 💡 Jika dekat router, pakai **5 GHz** untuk kecepatan tinggi; jika jauh, pakai **2.4 GHz** agar koneksi tetap stabil.

---

## D. Praktik Pengecekan Koneksi 🖥️

Perintah di terminal/command prompt untuk memeriksa jaringan:

```bash
ipconfig            # Windows — lihat IP, gateway, DNS
ip a                # Linux — lihat IP
ping google.com     # tes koneksi internet (waktu respon ms)
tracert google.com  # Windows — lihat jalur (hop) ke server
nslookup google.com # cek IP address sebuah domain
```

| Perintah | Fungsi | Contoh Hasil |
|---|---|---|
| `ping` | Menguji apakah host dapat dijangkau | `Reply from ... time=12ms` |
| `tracert` | Melihat rute/hop menuju tujuan | Daftar IP per hop |
| `nslookup` | Mencari IP dari nama domain | `google.com → 142.250.x.x` |
| `ipconfig` | Menampilkan konfigurasi jaringan lokal | IP, subnet, gateway |

---

## E. Troubleshooting Jaringan Dasar 🔧

| Masalah | Kemungkinan Penyebab | Solusi |
|---|---|---|
| Tidak ada internet | Kabel lepas, modem mati | Cek kabel, restart modem |
| WiFi lambat | Banyak pengguna, jarak jauh | Pindah ke 5 GHz, dekatkan router |
| WiFi tidak connect | Password salah | Lupakan jaringan, hubungkan ulang |
| Ping timeout | Server mati / firewall memblokir | Coba ping IP lain |
| DNS error | Server DNS bermasalah | Ganti DNS ke `8.8.8.8` |

**Langkah restart modem:**
1. Matikan modem, tunggu 30 detik.
2. Nyalakan kembali.
3. Tunggu 2 menit sampai lampu indikator stabil.

**Urutan periksa (troubleshooting):**
1. Apakah WiFi terhubung? → 2. Apakah IP didapat? → 3. Apakah gateway bisa di-ping? → 4. Apakah internet bisa di-ping?

---

## F. Keamanan WiFi 🔒

1. Ganti password default router.
2. Gunakan enkripsi **WPA2/WPA3**, hindari WEP.
3. Ganti SSID — jangan pakai nama atau data pribadi.
4. Nonaktifkan fitur **WPS**.
5. Cek daftar perangkat yang terhubung secara rutin.
6. Matikan jaringan WiFi saat tidak dipakai lama.

> 💡 Jaringan WiFi terbuka (tanpa password) memungkinkan orang lain menyadap data. Selalu gunakan jaringan yang aman.

---

## G. Contoh Soal & Penyelesaian 📝

**Contoh 1:** Jelaskan alur koneksi internet di rumah dari ISP hingga perangkatmu.
**Jawaban:** Sinyal dari ISP masuk melalui kabel fiber optik ke **modem** yang mengubahnya menjadi data digital. Data diteruskan ke **router WiFi** yang menyebarkannya secara nirkabel. Perangkat (HP/laptop) menangkap sinyal lewat kartu jaringan (NIC) dan terhubung ke jaringan lokal, lalu mengakses internet.

**Contoh 2:** Mengapa WiFi di dekat dapur rumahmu lebih lambat daripada di ruang tamu?
**Jawaban:** Sinyal WiFi melemah saat menembus penghalang seperti dinding tebal, lemari, atau peralatan elektronik (gelombang mikro). Jarak yang lebih jauh juga memperlemah sinyal. Solusinya mendekatkan perangkat ke router atau memindahkan router ke posisi lebih terbuka.

**Contoh 3:** Perintah apa yang kamu gunakan jika ingin mengetahui IP address komputer di Windows? Jelaskan!
**Jawaban:** Perintah `ipconfig` di Command Prompt menampilkan konfigurasi jaringan, termasuk IP address, subnet mask, dan gateway default. Dari sini kita tahu alamat perangkat di jaringan lokal.

**Contoh 4:** Internet di rumahmu sering putus. Sebutkan 3 langkah troubleshooting!
**Jawaban:** (1) Cek apakah kabel dan modem menyala; (2) restart modem (matikan 30 detik lalu nyalakan kembali, tunggu stabil); (3) cek dengan `ping google.com` — jika timeout, periksa gateway dengan `ping` ke IP gateway untuk memastikan masalah di jaringan lokal atau di ISP.

**Contoh 5:** Apa beda memakai WiFi 2.4 GHz dan 5 GHz? Kapan memakai masing-masing?
**Jawaban:** 2.4 GHz menjangkau lebih jauh dan tembus dinding tetapi lebih lambat dan rawan gangguan; cocok untuk jarak jauh. 5 GHz lebih cepat dan sedikit gangguan tetapi jangkauan pendek; cocok saat dekat dengan router dan butuh kecepatan tinggi (streaming, game).

---

## H. Miskonsepsi & Kesalahan Umum 🚫

| Miskonsepsi | Fakta yang Benar |
|---|---|
| "Semakin mahal router, pasti WiFi pasti cepat" | Kecepatan juga dipengaruhi ISP, jumlah pengguna, dan penghalang |
| "WiFi 5 GHz selalu lebih baik" | 5 GHz cepat tapi jangkauan pendek; pilih sesuai situasi |
| "Restart modem tidak perlu" | Restart adalah langkah pertama yang efektif untuk banyak gangguan |
| "Ping timeout berarti internet mati total" | Bisa juga karena firewall memblokir atau server tujuan mati |
| "SSID boleh memakai nama pribadi" | Hindari data pribadi di SSID demi keamanan |

---

## I. Tantangan Praktik (Mengaplikasi) 🎯

**Tantangan 1 — Deteksi Jaringan (Mudah):** Cek IP address komputer/laptopmu dan catat gateway serta DNS-nya.

**Tantangan 2 — Uji Koneksi (Sedang):** Jalankan `ping google.com`, catat waktu respon (ms). Ulangi di lokasi berbeda dan bandingkan hasilnya.

**Tantangan 3 — Telusuri Jalur (Sedang):** Jalankan `tracert google.com` dan catat berapa hop yang dilalui menuju server.

**Tantangan 4 — Audit WiFi (Sulit):** Catat daftar WiFi yang tersedia di sekitar kelas, klasifikasikan kekuatan sinyalnya, dan analisis faktor yang memengaruhinya.

**Tantangan 5 — Identifikasi Perangkat (Sulit):** Amati lab komputer sekolah, identifikasi modem, router, switch, dan access point-nya, lalu buat skema koneksinya.

---

## J. Rangkuman Kunci 🔑

- Jaringan ada di sekolah (LAN, WiFi), rumah (modem→router→perangkat), dan kota (BTS, fiber).
- **WiFi** memakai gelombang radio; **2.4 GHz** jangkauan jauh, **5 GHz** cepat.
- Perintah cek koneksi: `ipconfig`, `ping`, `tracert`, `nslookup`.
- **Troubleshooting**: cek kabel → restart modem → uji ping → periksa gateway.
- Keamanan WiFi: ganti password, WPA2/WPA3, nonaktifkan WPS, cek perangkat terhubung.

---

## K. Glosarium 📖

| Istilah | Arti |
|---|---|
| **WiFi** | Teknologi jaringan nirkabel berbasis gelombang radio |
| **SSID** | Nama jaringan WiFi |
| **BTS** | Menara pemancar sinyal seluler |
| **Backbone** | Jaringan tulang punggung internet berkapasitas besar |
| **Ping** | Perintah untuk menguji keterjangkauan host |
| **Hop** | Setiap titik perantara dalam rute pengiriman data |
| **Troubleshooting** | Proses menemukan dan memperbaiki masalah |
| **ISP** | Penyedia layanan internet |
| **WPA2/WPA3** | Standar enkripsi keamanan WiFi |

---

## L. Refleksi (Merefleksi) 🔍

- Faktor apa yang paling berpengaruh terhadap kualitas jaringan di sekitarmu?
- Setelah praktik `ping` dan `tracert`, bagaimana pemahamanmu tentang perjalanan data di internet?
- Apakah kamu pernah mengalami masalah jaringan? Bagaimana kamu akan menanganinya sekarang?
- **Skala pemahaman diri:** ____/10
- Apa yang ingin kamu teliti lebih lanjut tentang jaringan di kotamu?

---

**MGMP Informatika SMAN 6 Cimahi — Fase F (Kelas XI) Semester 2**