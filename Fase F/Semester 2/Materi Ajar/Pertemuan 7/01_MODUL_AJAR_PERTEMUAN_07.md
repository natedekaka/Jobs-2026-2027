# MODUL AJAR INFORMATIKA – FASE F (KELAS XI)

| Komponen | Deskripsi |
|---|---|
| **Mata Pelajaran** | Informatika |
| **Fase / Kelas** | F / XI |
| **Semester** | 2 (Genap) |
| **Pertemuan ke-** | 7 |
| **Alokasi Waktu** | 5 JP × 45 menit (225 menit) |
| **Tahun Pelajaran** | 2026/2027 |
| **Satuan Pendidikan** | SMA Negeri 6 Cimahi |
| **Materi Esensial** | Konsep Sistem dan Keamanan Jaringan Komputer |

---

## Tujuan Pembelajaran

| TP | IKTP |
|---|---|
| **BK:** Memahami model jaringan komputer dan topologi | 7.1 Menjelaskan klasifikasi jaringan (LAN, MAN, WAN) |
| | 7.2 Menggambar dan menjelaskan 5 topologi jaringan |
| | 7.3 Menganalisis kelebihan & kekurangan setiap topologi |
| | 7.4 Memilih topologi yang tepat berdasarkan kebutuhan |

---

## Langkah Pembelajaran

### Pembukaan (20 menit)

| Kegiatan | Waktu |
|---|---|
| 1. Salam, doa, cek kehadiran | 3 menit |
| 2. **Review**: "S1 kita sempat bahas jaringan — LAN, WAN, protokol. Sekarang kita **dalamkan**: bagaimana perangkat terhubung secara fisik?" | 7 menit |
| 3. **Apersepsi**: "Lab komputer sekolah — 30 komputer terhubung ke 1 switch. Itu topologi apa? Kalau kabel putus, semua mati atau hanya 1 komputer?" | 10 menit |

### Inti (170 menit)

#### Memahami (60 menit)

**1. Review Jaringan Komputer (15 menit)**

| Jenis | Jangkauan | Contoh |
|---|---|---|
| **PAN** | 1–10 m | Bluetooth HP ke laptop |
| **LAN** | 10 m – 1 km | Lab komputer, kantor |
| **MAN** | 1–100 km | Wi-Fi kota |
| **WAN** | > 100 km | Internet |

**Perangkat Jaringan:**
| Perangkat | Fungsi |
|---|---|
| **Switch** | Menghubungkan perangkat dalam LAN |
| **Router** | Menghubungkan jaringan berbeda (LAN ke WAN) |
| **Access Point** | Mengubah sinyal kabel ke Wi-Fi |
| **Modem** | Mengubah sinyal ISP ke sinyal digital |

**2. Topologi Jaringan (30 menit)**

**a. Topologi Bus**

```
💻──💻──💻──💻──💻
    │
    └──🖨️
```

| Kelebihan | Kekurangan |
|---|---|
| Hemat kabel | Jika kabel utama putus → semua mati |
| Sederhana | Sulit troubleshooting |

**b. Topologi Star**

```
        💻
        │
💻────🔄SWITCH────💻
        │
        💻
```

| Kelebihan | Kekurangan |
|---|---|
| Jika 1 kabel putus → hanya 1 komputer mati | Butuh switch/hub (biaya tambahan) |
| Mudah troubleshooting | Jika switch mati → semua mati |

**c. Topologi Ring**

```
💻────💻
│      │
💻────💻
```

| Kelebihan | Kekurangan |
|---|---|
| Data teratur (token passing) | Jika 1 putus → semua mati |
| Kinerja stabil | Sulit tambah perangkat |

**d. Topologi Mesh**

```
💻 ── 💻
│\  /│
│ \/ │
│ /\ │
│/  \│
💻 ── 💻
```

| Kelebihan | Kekurangan |
|---|---|
| Sangat andal (banyak jalur alternatif) | Sangat mahal (kabel sebanyak n×(n-1)/2) |
| Tidak ada single point of failure | Konfigurasi kompleks |

**e. Topologi Tree**

```
        🔄ROOT
        /    \
      🔄     🔄
     /  \   /  \
    💻  💻 💻  💻
```

| Kelebihan | Kekurangan |
|---|---|
| Mudah dikelola per cabang | Jika root mati → semua mati |
| Cocok untuk gedung bertingkat | Butuh banyak kabel |

**3. Memilih Topologi (15 menit)**

| Kebutuhan | Topologi Rekomendasi | Alasan |
|---|---|---|
| Lab sekolah (20–30 komp) | **Star** | Mudah管理, jika 1 rusak tidak ganggu yg lain |
| Kantor kecil (5–10 komp) | **Star / Bus** | Hemat biaya |
| Server penting (bank, militer) | **Mesh** | Keandalan tinggi |
| Gedung bertingkat | **Tree** | Per cabang per lantai |
| Jaringan temporer | **Ring** | Sederhana |

#### Mengaplikasi — Praktik (80 menit)

**4. Demonstrasi Cisco Packet Tracer (15 menit)**
- Buka Cisco Packet Tracer (atau alat simulasi web)
- Buat topologi Star: 1 switch + 4 PC
- Konfigurasi IP: 192.168.1.x
- Uji koneksi: `ping 192.168.1.2`
- Putuskan 1 kabel → lihat dampak

**5. Aktivitas 1 — Simulasi Fisik dengan Tali (25 menit) — Kelompok**

Setiap kelompok mendapat 1 topologi untuk disimulasikan:

| Kelompok | Topologi | Alat |
|---|---|---|
| A | Bus | Tali 5 m, 5 kartu "komputer" |
| B | Star | Tali 5 m, 5 kartu, 1 kartu "switch" |
| C | Ring | Tali 5 m, 5 kartu |
| D | Mesh | Tali 10 m, 4 kartu |
| E | Tree | Tali 10 m, 6 kartu, 2 kartu "switch" |

**Cara:** Rentangkan tali sesuai topologi. Guru "putuskan" kabel → siswa lihat dampak ke komputer mana saja.

**6. Aktivitas 2 — Gambar & Analisis (20 menit) — Individu**

Gambar topologi yang ditugaskan + tulis:
- Nama topologi
- Cara kerja (jelaskan aliran data)
- 2 kelebihan
- 2 kekurangan
- 1 contoh kasus penggunaan nyata

**7. Aktivitas 3 — Studi Kasus (20 menit) — Berpasangan**

| Skenario | Tugas |
|---|---|
| "Sekolah ingin membangun jaringan 5 lab + 1 perpustakaan + 1 ruang guru" | Pilih topologi terbaik + gambar + alasan |

**Presentasi 2 kelompok, @5 menit**

#### Merefleksi (15 menit)

**8. Refleksi Jurnal (15 menit)**
- Topologi paling andal?
- Topologi paling hemat?
- Jika diminta pilih 1 untuk sekolah — mana? Mengapa?
- Skala pemahaman 1–10

### Penutup (35 menit)

| Kegiatan | Waktu |
|---|---|
| 1. Rangkuman: Bus → Star → Ring → Mesh → Tree — setiap topologi punya trade-off | 10 menit |
| 2. Kuis lisan: "Topologi paling andal? Paling hemat? Star cocok untuk?" | 10 menit |
| 3. Preview: "Pert 8: Cloud Computing — komputasi awan, IaaS/PaaS/SaaS, Google Cloud" | 5 menit |
| 4. Tugas rumah: Cari 1 jaringan di sekitar (rumah/sekolah) → identifikasi topologinya | 10 menit |

---

## Asesmen

| Kriteria | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| Topologi (gambar + nama) | 1–2 | 3 | 4 | 5 + benar |
| Kelebihan & kekurangan | Tidak tepat | Sebagian tepat | Tepat | Tepat + contoh |
| Simulasi tali (partisipasi) | Tidak ikut | Ikut pasif | Ikut aktif | Aktif + analisis |
| Studi kasus | Tidak selesai | Pilih topologi | Pilih + alasan | Pilih + gambar + alasan + alternatif |

---

**MGMP Informatika SMAN 6 Cimahi**
