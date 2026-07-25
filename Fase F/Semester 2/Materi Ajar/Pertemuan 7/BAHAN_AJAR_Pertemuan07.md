# BAHAN AJAR – PERTEMUAN 7 (S2)
## Model Jaringan Komputer & Topologi

| TP | BK — Konsep Sistem dan Keamanan Jaringan Komputer |
|---|---|

---

### A. KLASIFIKASI JARINGAN KOMPUTER

#### Berdasarkan Jangkauan

| Jenis | Jangkauan | Contoh | Kecepatan Khas |
|---|---|---|---|
| **PAN** | 1–10 m | Bluetooth HP ke laptop | 1–24 Mbps |
| **LAN** | 10 m – 1 km | Lab komputer, warnet | 100–1000 Mbps |
| **MAN** | 1–100 km | Wi-Fi kota, CCTV kota | 10–100 Mbps |
| **WAN** | > 100 km | Internet, VPN antar kota | 1–100 Mbps |

#### Berdasarkan Model Koneksi

| Model | Cara Kerja | Contoh |
|---|---|---|
| **Client-Server** | Server pusat → banyak client | Web, email, database |
| **Peer-to-Peer** | Setiap node setara | Torrent, LAN sharing |

#### Perangkat Jaringan

```
┌─────────┐    ┌──────────┐    ┌──────────┐    ┌──────────┐
│ MODEM   │────│ ROUTER   │────│ SWITCH   │────│ KOMPUTER │
│ (ISP)   │    │ (antar   │    │ (dalam   │    │          │
│         │    │  jaringan)│    │  LAN)    │    │          │
└─────────┘    └──────────┘    └──────────┘    └──────────┘
                                       │
                                  ┌────┴────┐
                                  │ ACCESS  │
                                  │ POINT   │
                                  │ (Wi-Fi) │
                                  └─────────┘
```

---

### B. TOPOLOGI JARINGAN

#### 1. Topologi Bus

**Gambar:**
```
┌────┐  ┌────┐  ┌────┐  ┌────┐  ┌────┐
│ PC1│──│ PC2│──│ PC3│──│ PC4│──│ PC5│
└────┘  └────┘  └────┘  └────┘  └────┘
                  │
              ┌───┴───┐
              │ PRINTER│
              └───────┘
```

**Cara Kerja:**
- Semua perangkat terhubung ke 1 kabel backbone
- Data dikirim ke semua perangkat → hanya tujuan yang memproses
- Terminator di ujung kabel untuk menyerap sinyal

| ✅ Kelebihan | ❌ Kekurangan |
|---|---|
| Hemat kabel | Jika kabel backbone putus → semua mati |
| Sederhana | Sulit deteksi masalah |
| Biaya rendah | Kinerja turun jika banyak perangkat |

#### 2. Topologi Star

**Gambar:**
```
                ┌────┐
                │ PC1│
                └─┬──┘
                  │
┌────┐     ┌──────┴──────┐     ┌────┐
│ PC2│─────│   SWITCH    │─────│ PC3│
└────┘     └──────┬──────┘     └────┘
                  │
                ┌─┴──┐
                │ PC4│
                └────┘
```

**Cara Kerja:**
- Semua perangkat terhubung ke switch/hub pusat
- Data dikirim ke switch → switch meneruskan ke tujuan

| ✅ Kelebihan | ❌ Kekurangan |
|---|---|
| Jika 1 kabel putus → hanya 1 komputer mati | Butuh switch (biaya tambahan) |
| Mudah troubleshoot | Jika switch mati → semua mati |
| Kinerja stabil | Kabel lebih panjang |

#### 3. Topologi Ring

**Gambar:**
```
    ┌────┐
┌───│ PC1│───┐
│   └────┘   │
│            │
┌┴──┐      ┌─┴──┐
│ PC4│      │ PC2│
└─┬──┘      └─┬──┘
  │           │
  │  ┌────┐   │
  └──│ PC3│───┘
     └────┘
```

**Cara Kerja:**
- Setiap perangkat terhubung ke 2 tetangga
- Token (data izin) berputar satu arah
- Hanya pemilik token yang bisa kirim data

| ✅ Kelebihan | ❌ Kekurangan |
|---|---|
| Data teratur (tidak tabrakan) | Jika 1 putus → semua mati |
| Kinerja stabil untuk beban berat | Sulit tambah/kurang perangkat |
| Mudah implementasi | Lebih lambat dari star |

#### 4. Topologi Mesh

**Gambar:**
```
    ┌────┐
   /│ PC1│\
  / └────┘ \
 /  /    \  \
│  /      \  │
┌┴──┐    ┌─┴──┐
│ PC2│────│ PC3│
└────┘    └────┘
```

**Cara Kerja:**
- Setiap perangkat terhubung ke semua perangkat lain
- Jika 1 jalur putus → data lewat jalur lain

| ✅ Kelebihan | ❌ Kekurangan |
|---|---|
| Sangat andal (banyak jalur) | Sangat mahal |
| Tidak ada single point of failure | n×(n-1)/2 kabel untuk n perangkat |
| Keamanan tinggi | Konfigurasi kompleks |

**Rumus:** Jumlah kabel = n × (n-1) / 2
- 4 perangkat: 6 kabel
- 5 perangkat: 10 kabel
- 10 perangkat: 45 kabel

#### 5. Topologi Tree

**Gambar:**
```
        ┌──────┐
        │ ROOT │ (Switch Pusat)
        └──┬───┘
           │
     ┌─────┴─────┐
     │           │
  ┌──┴──┐     ┌──┴──┐
  │SW 1 │     │SW 2 │ (Switch Lantai)
  └──┬──┘     └──┬──┘
   │  │  │     │  │  │
  PC1 PC2 PC3  PC4 PC5 PC6
```

| ✅ Kelebihan | ❌ Kekurangan |
|---|---|
| Mudah管理 per cabang | Jika root mati → semua mati |
| Cocok gedung bertingkat | Butuh banyak kabel |
| Mudah dikembangkan | Konfigurasi lebih kompleks |

---

### C. PERBANDINGAN TOPOLOGI

| Topologi | Biaya | Keandalan | Troubleshoot | Tambah Device | Cocok untuk |
|---|---|---|---|---|---|
| **Bus** | Rendah | Rendah | Sulit | Mudah | Jaringan kecil temporer |
| **Star** | Sedang | Tinggi | Mudah | Mudah | Lab, kantor |
| **Ring** | Rendah | Rendah | Sulit | Sulit | Jaringan token-based |
| **Mesh** | Tinggi | Sangat Tinggi | Mudah | Sulit | Server penting, militer |
| **Tree** | Sedang | Sedang | Sedang | Mudah | Gedung bertingkat |

---

### D. MEMILIH TOPOLOGI

| Pertanyaan | Jawaban | Rekomendasi |
|---|---|---|
| Berapa banyak perangkat? | < 10 | Bus atau Star |
| | 10–50 | Star |
| | > 50 | Tree |
| Apakah keandalan kritis? | Ya | Mesh |
| | Tidak | Star |
| Berapa budget? | Rendah | Bus |
| | Sedang | Star |
| | Tinggi | Tree / Mesh |

---

### E. RANGKUMAN

| Topologi | Kelebihan Utama | Kekurangan Utama |
|---|---|---|
| **Bus** | Hemat kabel | 1 putus = semua mati |
| **Star** | Mudah troubleshoot | Butuh switch |
| **Ring** | Data teratur | 1 putus = semua mati |
| **Mesh** | Sangat andal | Sangat mahal |
| **Tree** | Cocok gedung | Root = single point |

---

**MGMP Informatika SMAN 6 Cimahi**
