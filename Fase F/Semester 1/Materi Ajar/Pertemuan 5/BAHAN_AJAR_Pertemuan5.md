# BAHAN AJAR – PERTEMUAN 5
## Pengujian (Testing) & Debugging

| TP | BK, AP — Proses Rekayasa |
|---|---|

---

### A. MENGAPA TESTING PENTING?

**Bug** adalah cacat, error, atau kelemahan dalam kode yang menyebabkan program tidak berjalan sebagaimana mestinya.

#### Sejarah Bug yang Mengguncang Dunia

| Kasus | Tahun | Dampak |
|---|---|---|
| **Y2K Bug** | 1999 | Kepanikan global — sistem tanggal hanya 2 digit. Biaya pencegahan ~$300M |
| **Mars Climate Orbiter** | 1999 | Konversi satuan imperial↔metric salah → satelit hancur. Rugi $327,6 juta |
| **Knight Capital** | 2012 | Bug software trading → rugi $440 juta dalam 45 menit → perusahaan bangkrut |
| **Boeing 737 MAX** | 2018–2019 | Bug MCAS → 2 kecelakaan, 346 orang meninggal |
| **CrowdStrike** | 2024 | Update bug → Blue Screen of Death jutaan komputer global |

#### Testing = Nyawa Aplikasi

| Tanpa Testing | Dengan Testing |
|---|---|
| Aplikasi error di produksi | Bug tertangkap sebelum rilis |
| User frustrasi | User puas |
| Biaya perbaikan mahal | Biaya perbaikan murah |
| Reputasi jelek | Reputasi baik |

---

### B. JENIS-JENIS TESTING

#### Piramida Testing

```
        ╱╲
       ╱UAT╲
      ╱─────╲
     ╱System╲
    ╱─────────╲
   ╱Integration╲
  ╱───────────────╲
 ╱   Unit Test     ╲     ← Paling banyak
╱─────────────────────╲
```

#### 1. Unit Test

Menguji satu unit (fungsi/komponen) terkecil secara terisolasi.

| Contoh | Kode | Input | Expected |
|---|---|---|---|
| Fungsi `tambah(a,b)` | `def tambah(a,b): return a+b` | `(2,3)` | `5` |
| Fungsi `cek_login` | Cek NISN & password | NISN benar, PW benar | `True` |

#### 2. Integration Test

Menguji dua atau lebih komponen yang bekerja sama.

| Contoh | Komponen 1 | Komponen 2 | Test |
|---|---|---|---|
| Login → Dashboard | Form login | Halaman dashboard | Setelah login sukses, dashboard muncul? |

#### 3. System Test

Menguji seluruh sistem secara end-to-end meniru pengguna nyata.

#### 4. User Acceptance Test (UAT)

User sungguhan (siswa, guru) mencoba aplikasi dan memvalidasi apakah sesuai kebutuhan.

#### 5. Black-box vs White-box

| Aspek | Black-box | White-box |
|---|---|---|
| Fokus | Input → Output | Struktur internal kode |
| Pengetahuan | Tidak lihat kode | Lihat kode |
| Contoh | Masukkan data, lihat hasil | Periksa setiap cabang IF |

---

### C. TEST CASE

**Test Case** adalah seperangkat kondisi yang digunakan untuk memverifikasi apakah fitur berjalan dengan benar.

#### Format Test Case

| ID | Skenario | Langkah | Input | Expected Result | Status |
|---|---|---|---|---|---|
| TC-01 | Login sukses | 1. Buka form login | NISN: 12345 | Dashboard muncul | ✅ / ❌ |
| | | 2. Isi NISN | PW: abcde | | |
| | | 3. Isi password | | | |
| | | 4. Klik MASUK | | | |
| TC-02 | Login gagal — NISN salah | Sama | NISN: 99999 | Pesan error: "NISN tidak ditemukan" | |
| TC-03 | Login gagal — password salah | Sama | NISN: 12345 | Pesan error: "Password salah" | |
| | | | PW: xxxxx | | |

#### Panduan Membuat Test Case

1. **Positif**: Input valid → berhasil
2. **Negatif**: Input invalid → error handling
3. **Boundary**: Nilai batas (misal: password min 6 karakter — coba 5 dan 6)
4. **Edge case**: Kasus ekstrem (input kosong, karakter spesial)

---

### D. DEBUGGING

**Debugging** adalah proses mencari dan memperbaiki bug.

#### Langkah Debugging

```
┌──────────────────┐
│ 1. Identifikasi  │ ← "Aplikasi crash saat klik login"
└────────┬─────────┘
         ▼
┌──────────────────┐
│ 2. Reproduksi    │ ← Coba lagi dengan langkah yang sama
└────────┬─────────┘
         ▼
┌──────────────────┐
│ 3. Cari penyebab │ ← Cek kode, log error, trace
└────────┬─────────┘
         ▼
┌──────────────────┐
│ 4. Perbaiki      │ ← Edit kode
└────────┬─────────┘
         ▼
┌──────────────────┐
│ 5. Verifikasi    │ ← Uji lagi, pastikan bug hilang
└──────────────────┘
```

#### Debugging Teknik Umum

| Teknik | Cara |
|---|---|
| **Print / Console.log** | Cetak nilai variabel ke konsol |
| **Rubber Duck** | Jelaskan kode ke bebek karet → biasanya ketemu bug sendiri |
| **Step-by-step** | Jalankan kode baris per baris |
| **Bandingkan** | Bandingkan dengan kode yang berfungsi |
| **Cari typo** | Seringkali hanya typo (salah huruf, lupa titik koma) |

#### Contoh Debugging — HTML Rusak

❌ **Kode Error:**
```html
<body>
  <h1>Selamat Datang<h1>
  <p>Ini adalah halaman login</p
</body>
```

✅ **Kode Diperbaiki:**
```html
<body>
  <h1>Selamat Datang</h1>
  <p>Ini adalah halaman login</p>
</body>
```

| Bug | Baris | Perbaikan |
|---|---|---|
| Tag `<h1>` tidak ditutup dengan `/` | 2 | `</h1>` |
| Tag `<p>` tidak ditutup | 3 | `</p>` |

---

### E. TOOLS TESTING & DEBUGGING

| Tool | Fungsi |
|---|---|
| **Browser DevTools** (F12) | Debug HTML, CSS, JS langsung di browser |
| **Chrome Lighthouse** | Tes performa, aksesibilitas |
| **Python Debugger (pdb)** | Debug Python baris per baris |
| **Jest / Pytest** | Framework unit testing |

---

### F. RANGKUMAN

| Konsep | Inti |
|---|---|
| **Testing** | Mencari bug sebelum aplikasi dipakai |
| **Unit Test** | Uji satu fungsi |
| **Integration Test** | Uji antar komponen |
| **System Test** | Uji seluruh sistem |
| **UAT** | User validasi |
| **Test Case** | Skenario uji (input → expected) |
| **Debugging** | Proses 5 langkah mencari & perbaiki bug |

---

**MGMP Informatika SMAN 6 Cimahi**
