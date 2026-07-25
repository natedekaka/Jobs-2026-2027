# MODUL AJAR INFORMATIKA – FASE F (KELAS XI)

| Komponen | Deskripsi |
|---|---|
| **Mata Pelajaran** | Informatika |
| **Fase / Kelas** | F / XI |
| **Semester** | 2 (Genap) |
| **Pertemuan ke-** | 12 |
| **Alokasi Waktu** | 5 JP × 45 menit (225 menit) |
| **Tahun Pelajaran** | 2026/2027 |
| **Satuan Pendidikan** | SMA Negeri 6 Cimahi |
| **Materi Esensial** | Konsep Sistem dan Keamanan Jaringan Komputer |

---

## Tujuan Pembelajaran

| TP | IKTP |
|---|---|
| **LD:** Memahami platform digital & aspek keamanan transaksi | 12.1 Menjelaskan mekanisme lokapasar (marketplace) |
| | 12.2 Menjelaskan cara kerja perbankan digital & dompet digital |
| | 12.3 Mengidentifikasi risiko keamanan transaksi digital |
| | 12.4 Menerapkan praktik aman bertransaksi online |

---

## Langkah Pembelajaran

### Pembukaan (20 menit)

| Kegiatan | Waktu |
|---|---|
| 1. Salam, doa, cek kehadiran | 3 menit |
| 2. **Review**: "Pert 11: UU ITE & PDP — aturan digital. Sekarang: platform digital yang kita pakai sehari-hari — bagaimana cara kerjanya & amankah?" | 5 menit |
| 3. **Apersepsi**: "Siapa yang pernah belanja di Shopee/Tokopedia? Transfer pakai M-Banking? Top-up GoPay? Kalian sudah pakai — tapi paham cara kerja & risikonya?" | 7 menit |
| 4. **Trigger**: "2023: 10.000+ kasus penipuan online di Indonesia. Kerugian Rp 100+ miliar. Kebanyakan karena pembeli kurang waspada." | 5 menit |

### Inti (170 menit)

#### Memahami (55 menit)

**1. Lokapasar / Marketplace (20 menit)**

| Definisi | Platform yang mempertemukan penjual & pembeli secara online |
|---|---|

**Marketplace di Indonesia:**

| Platform | Model | Pembayaran | Fitur Khas |
|---|---|---|---|
| **Tokopedia** | Marketplace + toko resmi | Transfer, kartu, dompet | GoPay, gratis ongkir |
| **Shopee** | Marketplace | ShopeePay, COD | Live streaming, flash sale |
| **Lazada** | Marketplace | Kartu, transfer, COD | Lazada Wallet |
| **Bukalapak** | Marketplace + mitra | BukaDompet | Mitra (agen BRILink) |
| **Blibli** | Marketplace | Kartu, transfer, cicilan | Blibli Pay |

**Mekanisme Transaksi:**

```
PEMBELI → Pilih barang → Bayar → DANA DITAHAN (escrow)
                                        │
                        ┌───────────────┴───────────────┐
                        │                               │
                   PENJUAL kirim barang           PEMBELI terima
                        │                               │
                        └───────────────┬───────────────┘
                                        ▼
                                  DANA DILEPAS ke penjual
```

**Fitur Escrow:** Uang pembeli ditahan platform sampai barang diterima → aman

**2. Perbankan Digital (15 menit)**

| Jenis | Contoh | Fungsi |
|---|---|---|
| **Mobile Banking** | BCA Mobile, Mandiri Livin', BNI Mobile | Transfer, bayar, cek saldo via HP |
| **Internet Banking** | KlikBCA, Mandiri Online | Transaksi via browser |
| **Digital Bank** | Jenius, Digibank by DBS, SeaBank | 100% online — tanpa kantor cabang |

**Keamanan M-Banking:**

| Fitur | Fungsi |
|---|---|
| **PIN/Password** | Akses login |
| **2FA / OTP** | Verifikasi transaksi |
| **m-Token / SecureApp** | Generate kode untuk transaksi besar |
| **Device Binding** | Hanya bisa akses dari HP terdaftar |
| **Limit Transaksi** | Batas nominal per hari |

**3. Dompet Digital / E-Wallet (20 menit)**

| Dompet | Pengembang | Fitur |
|---|---|---|
| **GoPay** | Gojek | Bayar Gojek, top-up, transfer |
| **OVO** | Grab | Bayar Grab, merchant, tarik tunai |
| **DANA** | DANA Indonesia | Transfer, bayar, QRIS |
| **ShopeePay** | Shopee | Bayar di Shopee, merchant |
| **LinkAja** | BUMN | Bayar transportasi, PBB |
| **QRIS** | Standar BI | Satu QR untuk semua dompet — bayar di mana saja |

**Cara Kerja Dompet Digital:**

```
TOP UP:  Rekening → Dompet Digital (saldo masuk)
BAYAR:   Scan QR / PIN → Saldo keluar → Merchant terima
TARIK:   Dompet → Rekening (saldo keluar)
```

**Risiko Dompet Digital:**

| Risiko | Penjelasan | Mitigasi |
|---|---|---|
| **Saldo dicuri** | HP hilang → saldo diakses | PIN kuat + 2FA + device lock |
| **Phishing** | Link palsu QRIS | Scan QR dari merchant terpercaya |
| **Top-up salah** | Salah nomor tujuan | Cek 2× sebelum konfirmasi |
| **Saldo menganggur** | Uang di dompet tidak berbunga | Top-up sesuai kebutuhan |

#### Mengaplikasi (85 menit)

**4. Demonstrasi Perbandingan Platform (10 menit)**
- Tampilkan 3 platform: Tokopedia, GoPay, M-Banking
- Tunjukkan fitur keamanan: escrow, 2FA, limit transaksi, PIN

**5. Aktivitas 1 — Analisis Platform (25 menit) — Kelompok**

Setiap kelompok mendapat 1 platform:

| Kelompok | Platform |
|---|---|
| A | Shopee (marketplace) |
| B | GoPay (dompet digital) |
| C | BCA Mobile (m-banking) |
| D | DANA (dompet digital) |

**Tugas (poster digital — Canva):**
1. Logo + deskripsi singkat
2. Fitur utama
3. Fitur keamanan (escrow, 2FA, PIN, limit)
4. 2 kelebihan, 2 kekurangan
5. Tips aman menggunakan platform tersebut

**6. Aktivitas 2 — Simulasi Transaksi Aman (25 menit) — Berpasangan**

Simulasi pembelian di marketplace:

| Langkah | Aman / Tidak Aman | Penjelasan |
|---|---|---|
| Pembeli klik link dari SMS "barang diskon 90%" | ❌ | Phishing |
| Pembeli cek rating toko sebelum beli | ✅ | |
| Pembeli transfer langsung ke rekening penjual (tidak lewat escrow) | ❌ | |
| Pembeli bayar pakai escrow / dompet platform | ✅ | |
| Penjual minta screenshot bukti transfer | ❌ | |
| Pembeli aktivasi 2FA di akun marketplace | ✅ | |

**Tugas:** Tentukan mana yang aman — beri alasan!

**7. Aktivitas 3 — Studi Kasus Penipuan (25 menit) — Individu**

Baca kasus:

> "Andi mendapat notifikasi dari "Shopee": Akun Anda diblokir. Klik link bit.ly/unblock-shopee untuk memulihkan. Andi panik, klik link, masukkan email & password Shopee. 5 menit kemudian: saldo ShopeePay Rp 500.000 raib."

Analisis:
| Pertanyaan | Jawaban |
|---|---|
| Jenis penipuan? | |
| Kesalahan Andi? | |
| Bagaimana seharusnya? | |
| Pasal UU ITE? | |
| Cara melapor? | |

**8. Aktivitas 4 — Tips Berbagi (10 menit) — Pleno**
- Setiap siswa share 1 tips aman bertransaksi online
- Guru catat di papan tulis

#### Merefleksi (15 menit)

**9. Refleksi Jurnal (15 menit)**
- Fitur keamanan platform digital yang baru diketahui?
- 1 kebiasaan baru yang akan diterapkan saat transaksi online
- Dompet digital favorit — mengapa?
- Skala pemahaman 1–10

### Penutup (35 menit)

| Kegiatan | Waktu |
|---|---|
| 1. Rangkuman: Lokapasar (escrow) → M-Banking (2FA) → Dompet Digital (PIN) → Tips Aman | 10 menit |
| 2. Kuis lisan: "Apa itu escrow? Bedanya dompet digital vs m-banking? Tips aman belanja online?" | 10 menit |
| 3. Preview: "Pert 13: Etika Digital & Demokrasi Digital — bijak bermedsos, hoaks, filter bubble" | 5 menit |
| 4. Tugas rumah: Cek fitur keamanan 1 platform yang kalian pakai — screenshot + analisis | 10 menit |

---

## Asesmen

| Kriteria | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| Analisis platform | Tidak selesai | 2–3 fitur | 4–5 fitur | 6+ fitur + tips |
| Simulasi transaksi | 0–2 benar | 3–4 benar | 5–6 benar | 6 + alasan |
| Analisis kasus penipuan | Tidak tepat | 1–2 tepat | 3–4 tepat | 5 tepat + mendalam |
| Poster digital | Tidak buat | Ada, minimal | Ada, lengkap | Ada, menarik + tips |

---

**MGMP Informatika SMAN 6 Cimahi**
