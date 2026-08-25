# BAHAN AJAR – PERTEMUAN 11 (S2)
## Jaringan Dasar — IP Address & DNS
*Mengacu pada Panduan Mapel 2025; INFORMATIKA Fase D-F — pendekatan Pembelajaran Mendalam (Memahami → Mengaplikasi → Merefleksi)*

| Informasi | Keterangan |
|---|---|
| **Fase / Kelas** | F / Kelas XI |
| **Alokasi Waktu** | 5 JP × 45 menit (225 menit) |
| **Elemen CP** | Jaringan Komputer dan Internet (JKI) & Dampak Sosial Informatika (DSI) |
| **Tujuan Pembelajaran** | Menjelaskan konsep jaringan komputer, mengidentifikasi perangkat jaringan, memahami jenis jaringan, dan menjelaskan cara kerja internet (IP, DNS, HTTP) |
| **Materi Prasyarat** | Pengetahuan dasar penggunaan internet sehari-hari |

---

## A. Kisah Pemantik 🎬

> **"Surat di Kota Tanpa Alamat"**
>
> Bayangkan sebuah kota besar tanpa nama jalan dan nomor rumah. Pak Pos ingin mengirim surat, tetapi tidak tahu ke mana surat itu harus diantar. Kacau! Untungnya setiap rumah punya **alamat unik** yang membuat surat sampai ke tujuan.
>
> Internet bekerja seperti itu. Setiap perangkat terhubung memiliki **IP Address** (alamat unik). Untuk memudahkan manusia, nama yang mudah diingat seperti *google.com* dipetakan ke alamat itu oleh **DNS** — seperti buku telepon yang menerjemahkan nama menjadi nomor.
>
> **Pertanyaan pemantik:** Apa yang terjadi jika dua perangkat memakai IP address yang sama di satu jaringan? Bagaimana kamu membayangkan alur surat dari kotamu sampai ke kota lain — mirip dengan apa dalam jaringan komputer?

---

## B. Apa Itu Jaringan Komputer? 🌐

**Jaringan komputer** adalah kumpulan dua atau lebih komputer yang saling terhubung untuk berbagi data, sumber daya (resource), dan berkomunikasi.

| Istilah | Arti | Analogi |
|---|---|---|
| **Jaringan** | Komputer yang saling terhubung | Kota yang saling terhubung jalan |
| **IP Address** | Alamat unik perangkat | Alamat rumah |
| **DNS** | Penerjemah nama domain ke IP | Buku telepon |
| **Router** | Menghubungkan jaringan berbeda | Pos perbatasan kota |
| **Gateway** | Pintu keluar ke jaringan lain | Pintu gerbang keluar kota |
| **Protocol** | Aturan komunikasi antar perangkat | Bahasa yang disepakati bersama |

**Manfaat jaringan komputer:**
1. Berbagi data dan file antar komputer.
2. Berbagi perangkat keras (printer, scanner, penyimpanan).
3. Komunikasi (email, chat, video call).
4. Akses internet bersama.
5. Remote access — mengakses komputer dari jarak jauh.

---

## C. Jenis Jaringan Berdasarkan Skala 📏

| Jenis | Cakupan | Contoh |
|---|---|---|
| **PAN** | 1–10 m | Bluetooth HP ↔ headset |
| **LAN** | 10 m – 1 km | Lab komputer, warnet, kantor |
| **MAN** | 1–100 km | Antar kecamatan dalam satu kota |
| **WAN** | 100+ km | Internet, antar negara |

**Topologi jaringan** — bentuk koneksi antar komputer:

| Topologi | Cara Kerja | Kelebihan | Kekurangan |
|---|---|---|---|
| **Bus** | Satu kabel utama | Hemat kabel | Jika kabel putus, semua mati |
| **Star** | Semua ke switch pusat | Stabil, mudah dikelola | Bergantung pada switch |
| **Ring** | Melingkar | Aliran data teratur | Jika satu putus, seluruh ring terganggu |
| **Mesh** | Semua terhubung semua | Sangat andal | Butuh banyak kabel |

> 💡 **Topologi Star** paling umum dipakai di sekolah dan kantor karena mudah dikelola dan satu komputer yang bermasalah tidak mengganggu komputer lain.

---

## D. Perangkat Jaringan 🛠️

| Perangkat | Fungsi | Analogi |
|---|---|---|
| **Modem** | Mengubah sinyal ISP menjadi data digital | Penerjemah bahasa |
| **Router** | Mengatur lalu lintas antar jaringan | Pos polisi lalu lintas |
| **Switch** | Menghubungkan perangkat dalam satu LAN | Pusat distribusi |
| **Access Point** | Memancarkan sinyal WiFi | Pemancar radio |
| **NIC / Kartu Jaringan** | Perangkat keras untuk koneksi | Mulut untuk berbicara |
| **Kabel UTP** | Media koneksi fisik standar | Jalan raya data |

**Router vs Switch:**
- **Switch** menghubungkan perangkat di dalam **jaringan yang sama** (LAN).
- **Router** menghubungkan **antar jaringan** yang berbeda dan menentukan jalur data menuju internet.

---

## E. Cara Kerja Internet: IP, DNS, HTTP 🌍

**1. IP Address** — alamat unik setiap perangkat di jaringan. Format: `xxx.xxx.xxx.xxx` dengan tiap bagian bernilai 0–255.

```text
Contoh: 192.168.1.1   (IP lokal router rumah)
        8.8.8.8       (server DNS Google)
```

- **IP publik** — dipakai di internet (misal alamat server sebuah website).
- **IP privat** — dipakai di jaringan lokal (misal 192.168.x.x di rumah/kantor).
- **IPv4** (4 blok angka) dan **IPv6** (format heksadesimal lebih panjang) untuk mengatasi keterbatasan alamat IPv4.

**2. DNS (Domain Name System)** — menerjemahkan nama domain menjadi IP address.

```text
google.com  →  142.250.190.78
```

| Analogi | Nama | Nomor |
|---|---|---|
| Buku telepon | Nama orang | Nomor telepon |
| DNS | Nama domain (google.com) | IP address (142.250...) |

> 💡 Tanpa DNS, kita harus menghafal deretan angka IP untuk mengunjungi setiap website. DNS memudahkan manusia mengingat *nama* bukan *nomor*.

**3. HTTP / HTTPS** — protokol transfer data untuk web.
- **HTTP** = HyperText Transfer Protocol (data dikirim tanpa enkripsi).
- **HTTPS** = versi aman dengan enkripsi (ikon gembok di browser).

**Alur mengunjungi website:**
1. Kamu mengetik `www.google.com`.
2. Browser bertanya ke **DNS**: "alamat IP google.com berapa?"
3. DNS menjawab dengan IP address.
4. Browser mengirim permintaan HTTP/HTTPS ke IP tersebut.
5. Server mengirim halaman web; browser menampilkannya.

---

## F. Contoh Soal & Penyelesaian 📝

**Contoh 1:** Jelaskan perbedaan LAN, MAN, dan WAN beserta contohnya.
**Jawaban:** LAN mencakup area kecil seperti lab komputer (10 m – 1 km). MAN mencakup area kota seperti antar kecamatan (1–100 km). WAN mencakup area sangat luas seperti antar negara (100+ km), contohnya internet.

**Contoh 2:** Apa fungsi router? Bedakan dengan switch!
**Jawaban:** Router menghubungkan **antar jaringan** yang berbeda dan mengarahkan data ke jalur yang tepat (termasuk ke internet). Switch hanya menghubungkan perangkat dalam **satu jaringan lokal** (LAN). Analoginya, router adalah pos polisi lalu lintas, switch adalah pusat distribusi.

**Contoh 3:** Mengapa DNS diperlukan padahal komputer sudah punya IP address?
**Jawaban:** Manusia sulit menghafal deretan angka IP, tetapi mudah mengingat nama seperti `google.com`. DNS bertindak seperti buku telepon yang menerjemahkan nama domain menjadi IP address, sehingga pengguna cukup mengetik nama.

**Contoh 4:** Apa itu IP address privat dan publik? Beri contoh!
**Jawaban:** IP privat dipakai di jaringan lokal dan tidak bisa diakses langsung dari internet, contohnya `192.168.1.10` di rumah. IP publik dipakai di internet untuk mengidentifikasi perangkat/server secara global, contohnya alamat IP server sebuah website.

**Contoh 5:** Jelaskan alur saat kamu membuka `www.google.com` dari browser.
**Jawaban:** Browser meminta DNS menerjemahkan `google.com` menjadi IP address. Setelah mendapat IP, browser mengirim permintaan HTTP/HTTPS ke server. Server membalas dengan halaman web yang kemudian ditampilkan browser. Proses ini melibatkan router dan perangkat jaringan lain untuk mengarahkan data.

---

## G. Miskonsepsi & Kesalahan Umum 🚫

| Miskonsepsi | Fakta yang Benar |
|---|---|
| "Router dan modem itu benda yang sama" | Modem mengubah sinyal ISP; router mengatur lalu lintas antar jaringan — keduanya berbeda |
| "DNS sama dengan IP address" | DNS menerjemahkan nama ke IP; keduanya berbeda peran |
| "WiFi dan internet itu sama" | WiFi adalah media koneksi lokal; internet adalah jaringan global yang diakses lewatnya |
| "Semakin jauh jaringan, semakin cepat" | Jarak tidak menjamin kecepatan; kecepatan dipengaruhi media, perangkat, dan kapasitas |
| "IP address bisa sama untuk semua perangkat" | IP address harus unik dalam jaringan; duplikasi menyebabkan konflik |

---

## H. Tantangan Praktik (Mengaplikasi) 🎯

**Tantangan 1 — Kenali Jaringanmu (Mudah):** Cek IP address perangkatmu (buka `ipconfig` di Windows atau `ip a` di Linux), catat IP privat dan subnetnya.

**Tantangan 2 — Gambar Topologi (Sedang):** Gambarlah topologi **Star** dengan 5 komputer + 1 switch, lalu beri label perangkatnya.

**Tantangan 3 — Lapor Praktikum (Sedang):** Jelaskan perbedaan LAN, MAN, WAN dengan contoh nyata di sekitarmu, lalu presentasikan singkat.

**Tantangan 4 — Debug Alur Internet (Sulit):** Uraikan alur lengkap dari mengetik `www.sekolah.com` hingga halaman tampil, sebutkan peran DNS, router, dan HTTP/HTTPS di setiap tahap.

---

## I. Rangkuman Kunci 🔑

- Jaringan komputer menghubungkan perangkat untuk berbagi data dan sumber daya.
- Jenis jaringan: **PAN → LAN → MAN → WAN** berdasarkan luas area.
- Topologi: bus, star, ring, mesh — **star** paling umum.
- Perangkat: modem, router, switch, access point, NIC, kabel UTP.
- **IP Address** = alamat unik perangkat; **DNS** = buku telepon nama→IP.
- **HTTP/HTTPS** = protokol transfer web; HTTPS terenkripsi.
- Router menghubungkan antar jaringan; switch menghubungkan dalam satu jaringan.

---

## J. Glosarium 📖

| Istilah | Arti |
|---|---|
| **Jaringan Komputer** | Kumpulan komputer yang saling terhubung |
| **IP Address** | Alamat unik perangkat dalam jaringan |
| **DNS** | Sistem penerjemah nama domain ke IP |
| **Router** | Perangkat penghubung antar jaringan |
| **Gateway** | Pintu keluar menuju jaringan lain |
| **Modem** | Pengubah sinyal ISP menjadi data digital |
| **Switch** | Penghubung perangkat dalam satu LAN |
| **LAN/MAN/WAN** | Jaringan area lokal/kota/luas |
| **Topologi** | Bentuk koneksi antar perangkat |

---

## K. Refleksi (Merefleksi) 🔍

- Bagaimana konsep IP address dan DNS membantu menjelaskan cara kerja internet yang selama ini kamu pakai?
- Materi mana yang paling menarik: perangkat jaringan atau cara kerja internet? Mengapa?
- Apa yang akan kamu lakukan jika terjadi konflik IP di jaringan sekolah?
- **Skala pemahaman diri:** ____/10
- Apa yang ingin kamu pelajari lebih dalam tentang jaringan di pertemuan berikutnya?

---

**MGMP Informatika SMAN 6 Cimahi — Fase F (Kelas XI) Semester 2**