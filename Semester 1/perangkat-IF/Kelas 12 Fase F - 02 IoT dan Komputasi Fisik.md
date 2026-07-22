# Rancangan Pembelajaran Terdiferensiasi — Fase F Kelas 12
## Materi: IoT dan Komputasi Fisik

---

### 1. Tujuan Pembelajaran

1.1 Memahami konsep IoT (*Internet of Things*) dan arsitekturnya (sensor, aktuator, konektivitas, *cloud*).  
1.2 Mengidentifikasi komponen komputasi fisik (mikrokontroler, sensor, aktuator).  
1.3 Merancang sistem IoT sederhana untuk menyelesaikan masalah nyata.  
1.4 Memprogram mikrokontroler (Arduino/MicroPython) untuk membaca sensor dan mengendalikan aktuator.  
1.5 Mengirim data antar perangkat dalam jaringan dan ke *platform cloud* IoT.  
1.6 Memahami aspek keamanan dan privasi dalam sistem IoT.

---

### 2. Kompetensi Prasyarat

| No | Kompetensi Prasyarat | Keterkaitan |
|----|----------------------|-------------|
| 1 | Peserta didik mampu membuat program dengan *library* eksternal (Fase 11) | Prasyarat pemrograman mikrokontroler |
| 2 | Peserta didik memahami jaringan komputer dasar | Prasyarat konektivitas IoT |
| 3 | Peserta didik memahami konsep input-proses-output (Fase E) | Dasar interaksi sensor-aktuator |
| 4 | Peserta didik mampu merancang solusi berbasis kebutuhan | Prasyarat desain sistem IoT |

---

### 3. Asesmen Awal

#### 3.1 Instrumen Asesmen Awal

**Bentuk:** Kuis pengetahuan IoT + studi kasus desain + observasi.

**Kuis Pengetahuan IoT:**
- [ ] Saya tahu apa itu IoT
- [ ] Saya pernah mendengar Arduino/Raspberry Pi
- [ ] Saya tahu perbedaan sensor dan aktuator
- [ ] Saya pernah melihat proyek IoT (lampu otomatis, sensor suhu, dll)
- [ ] Saya paham bahwa perangkat IoT bisa diretas

**Studi Kasus Desain:**
> "Kebun sekolah perlu disiram otomatis ketika tanah kering. Buatlah sketsa sistem yang terdiri dari: (1) komponen yang dibutuhkan, (2) cara kerja, (3) bagaimana data dikirim dan diproses!"

**Observasi:**
> Berikan peserta didik sebuah LED dan baterai. Minta mereka menyalakan LED. Amati: apakah mereka bisa merangkai secara mandiri? Apakah mereka memahami konsep rangkaian sederhana?

#### 3.2 Kriteria Kesiapan Belajar

| Kondisi | Kategori | Tindak Lanjut |
|---------|----------|---------------|
| Mencentang ≤ 1, sketsa tidak sistematis, belum bisa merangkai LED | **Kurang Siap** | Pengenalan konsep IoT dengan video dan analogi; simulasi *unplugged* |
| Mencentang 2-3, sketsa cukup sistematis, bisa merangkai dengan panduan | **Cukup Siap** | Tutorial terbangun menggunakan simulator (Wokwi/Tinkercad) + komponen fisik |
| Mencentang ≥ 4, sketsa sistematis dan detail, merangkai mandiri | **Sudah Siap** | Proyek IoT nyata dengan sensor, aktuator, dan konektivitas *cloud* |

---

### 4. Rancangan Diferensiasi

#### 4.1 Diferensiasi Konten

| Kelompok | Sumber Belajar | Kompleksitas |
|----------|---------------|--------------|
| **Kurang Siap** | Video "Apa itu IoT?" + infografis komponen IoT + kartu sensor & aktuator + diagram arsitektur IoT | Visual, istilah minimal, analogi |
| **Cukup Siap** | Modul tutorial Arduino/simulator + panduan sensor suhu/LDR/LED + *template* kode + contoh proyek | Semi-teknis, bertahap, contoh kode |
| **Sudah Siap** | Dokumentasi teknis ESP32/NodeMCU + tutorial MQTT/HTTP + *platform* IoT *cloud* (ThingSpeak/Blynk) | Teknis, protokol, *cloud* |

#### 4.2 Diferensiasi Proses

| Kelompok | Aktivitas Pembelajaran | Pendampingan |
|----------|------------------------|--------------|
| **Kurang Siap** | Simulasi "tubuh sebagai IoT": satu peserta jadi sensor (mata), satu sebagai prosesor (otak), satu sebagai aktuator (tangan) — mengirim "data" secara manual | Didampingi, analogi fisik, bergerak |
| **Cukup Siap** | Menggunakan simulator (Tinkercad/Wokwi): merangkai LED + sensor suhu LDR → membaca nilai → menyalakan LED berdasarkan kondisi | *Scaffolding* dengan diagram rangkaian dan *template* kode |
| **Sudah Siap** | Proyek IoT nyata (ESP32/Arduino): sensor suhu/kelembaban → kirim data ke *cloud* → visualisasi *dashboard* → *alert* otomatis | Mandiri, pendidik sebagai konsultan teknis |

#### 4.3 Diferensiasi Produk

| Kelompok | Bentuk Produk | Kriteria |
|----------|--------------|----------|
| **Kurang Siap** | Poster "Cara Kerja IoT" — diagram alir dari sensor → proses → aktuator dengan gambar dan keterangan | Menunjukkan 3 komponen + alur data |
| **Cukup Siap** | Simulasi IoT berjalan (Tinkercad): sensor membaca nilai → LED/buzzer merespons → ditampilkan di serial monitor | Rangkaian benar, kode berjalan, output sesuai |
| **Sudah Siap** | Sistem IoT nyata: sensor → mikrokontroler → koneksi WiFi → *cloud dashboard* → *alert* otomatis (email/telegram) | Sistem end-to-end, *real-time*, dokumentasi |

---

### 5. Pengelompokan Fleksibel

- Kelompok proyek IoT berdasarkan minat aplikasi (rumah pintar, kebun otomatis, monitoring kelas, dll).
- Rotasi peran: *hardware designer*, *programmer*, *network engineer*, *documenter*.
- Peserta didik yang sudah siap dapat merancang tantangan tambahan (tambah sensor, integrasi API).

---

### 6. Asesmen Sumatif (Akhir Materi)

| Indikator | Perlu Perbaikan | Cukup | Baik | Sangat Baik |
|-----------|----------------|-------|------|-------------|
| Konsep IoT | Tidak paham | Menjelaskan definisi | Menjelaskan arsitektur + komponen | Menjelaskan arsitektur + protokol + keamanan |
| Perakitan/perangkaian | Tidak bisa | Rangkaian dengan panduan | Rangkaian mandiri | Rangkaian + *troubleshooting* |
| Pemrograman | Tidak bisa | Kode *template* dimodifikasi | Kode mandiri (baca sensor + aktuator) | Kode + konektivitas *cloud* + fitur lanjut |
| Sistem end-to-end | Tidak terintegrasi | Sebagian terintegrasi | Sistem berfungsi penuh | Sistem + *dashboard* + *alert* + dokumentasi |
