# BAHAN AJAR – PERTEMUAN 2
## Analisis Kebutuhan & Spesifikasi

| TP | BK, LD — Proses Rekayasa |
|---|---|

---

### A. MENGAPA ANALISIS KEBUTUHAN PENTING?

Bayangkan skenario ini:

> **Tanpa analisis kebutuhan:** Tim developer langsung coding aplikasi "Sekolahku". Setelah 3 bulan, aplikasi jadi. Tapi guru protes: "Kok tidak ada fitur rekap presensi? Yang kami butuhkan itu!"

> **Dengan analisis kebutuhan:** Tim mewawancarai guru, mencatat "butuh rekap presensi per bulan", lalu merancang fitur tersebut. Aplikasi sesuai kebutuhan.

> **Masalah #1 dalam pengembangan aplikasi adalah **salah kebutuhan**, bukan **salah kode**!**

---

### B. JENIS-JENIS KEBUTUHAN

#### 1. Kebutuhan Fungsional

Kebutuhan yang berkaitan dengan **fitur** atau **fungsi** yang harus dimiliki sistem.

**Contoh Aplikasi Perpustakaan Sekolah:**
| Kebutuhan Fungsional | Keterangan |
|---|---|
| Siswa bisa meminjam buku | Fitur transaksi peminjaman |
| Pustakawan bisa menambah buku | Fitur input data buku |
| Sistem bisa mencari buku | Fitur pencarian berdasarkan judul/penulis |
| Sistem bisa mengirim notifikasi | Pemberitahuan jatuh tempo |

#### 2. Kebutuhan Non-Fungsional

Kebutuhan yang berkaitan dengan **kualitas**, **batasan**, atau **atribut** sistem.

| Jenis | Contoh |
|---|---|
| **Performance** | Pencarian buku < 3 detik |
| **Security** | Hanya pustakawan bisa ubah data buku |
| **Usability** | Aplikasi bisa dipakai dalam 5 menit tanpa pelatihan |
| **Reliability** | Aplikasi tidak down selama jam sekolah (99.9% uptime) |
| **Scalability** | Mendukung 1000 pengguna sekaligus |

#### Tabel Perbandingan

| Aspek | Fungsional | Non-Fungsional |
|---|---|---|
| **Pertanyaan** | "Apa yang sistem lakukan?" | "Seberapa baik sistem melakukannya?" |
| **Bentuk** | Fitur, menu, aksi | Kualitas, batasan, standar |
| **Contoh** | Login, cetak laporan | Login < 2 detik, laporan PDF rapi |
| **Diukur?** | Ada/tidak (ya/tidak) | Skala (detik, persen, dll.) |

---

### C. TEKNIK PENGGALIAN KEBUTUHAN

#### 1. Wawancara (Interview)

**Cara:** Tanya jawab langsung dengan pengguna.
**Kelebihan:** Mendapat detail mendalam, bisa klarifikasi langsung.
**Kekurangan:** Hanya mewakili pendapat individu.

**Pertanyaan efektif:**
| ❌ Hindari | ✅ Pakai |
|---|---|
| "Apa fitur yang Anda mau?" | "Ceritakan bagaimana Anda melakukan presensi sekarang?" |
| (pertanyaan tertutup) | (pertanyaan terbuka) |
| "Apa aplikasinya harus cepat?" | "Berapa lama waktu yang ideal untuk presensi satu kelas?" |

#### 2. Observasi

**Cara:** Melihat langsung bagaimana pengguna bekerja.
**Kelebihan:** Melihat realitas di lapangan (bisa beda dengan cerita).
**Kekurangan:** Memakan waktu.

#### 3. Kuesioner

**Cara:** Menyebarkan angket ke banyak calon pengguna.
**Kelebihan:** Banyak responden, data kuantitatif.
**Kekurangan:** Kurang mendalam.

#### 4. Studi Dokumen

**Cara:** Mempelajari dokumen sistem yang sudah ada.
**Kelebihan:** Data historis, acuan regulasi.
**Kekurangan:** Mungkin sudah tidak relevan.

---

### D. MENULIS USER STORY

**User Story** adalah format sederhana untuk menulis kebutuhan dari sudut pandang pengguna.

#### Format Standar

```
Sebagai [PERAN / TIPE PENGGUNA],
saya ingin [FITUR / AKSI],
sehingga [MANFAAT / TUJUAN].
```

#### Contoh

```
Sebagai guru piket,
saya ingin melihat daftar siswa yang tidak hadir hari ini,
sehingga saya bisa melaporkan ke wali kelas.

Sebagai siswa,
saya ingin melihat jadwal pelajaran,
sehingga saya tahu buku apa yang harus dibawa.

Sebagai pustakawan,
saya ingin menambah data buku baru,
sehingga koleksi perpustakaan selalu terupdate.
```

#### Tips Menulis User Story

1. **Fokus pada pengguna** — bukan pada teknis
2. **Sederhana** — cukup 1 kalimat per fitur
3. **Bernilai** — harus jelas manfaatnya
4. **Dapat diuji** — bisa dicek apakah sudah selesai

---

### E. CONTOH: ANALISIS KEBUTUHAN APLIKASI PRESENSI SEKOLAH

#### Skenario

SMAN 6 Cimahi ingin membuat **aplikasi presensi digital** untuk menggantikan presensi kertas.

#### Hasil Wawancara dengan Guru BK

| Pertanyaan | Jawaban |
|---|---|
| "Bagaimana cara presensi sekarang?" | "Guru menandatangani daftar hadir kertas tiap jam." |
| "Apa masalahnya?" | "Sering hilang, susah rekap bulanan, orang tua tidak tahu." |
| "Fitur apa yang diinginkan?" | "Scan QR, rekap otomatis, notifikasi ke orang tua." |

#### Kebutuhan Fungsional

| ID | User Story |
|---|---|
| F1 | Sebagai **guru**, saya ingin **scan QR siswa** sehingga presensi cepat. |
| F2 | Sebagai **wali kelas**, saya ingin **melihat rekap presensi bulanan** sehingga saya tahu siapa yang sering tidak hadir. |
| F3 | Sebagai **orang tua**, saya ingin **mendapat notifikasi** jika anak tidak hadir. |
| F4 | Sebagai **admin BK**, saya ingin **mengekspor data presensi ke Excel** untuk laporan. |
| F5 | Sebagai **siswa**, saya ingin **melihat riwayat kehadiran saya**. |

#### Kebutuhan Non-Fungsional

| ID | Kebutuhan |
|---|---|
| NF1 | Scan QR selesai dalam < 2 detik (performance) |
| NF2 | Data presensi aman — hanya guru yang bisa mengubah (security) |
| NF3 | Aplikasi bisa dipakai 500 siswa bersamaan (scalability) |
| NF4 | Notifikasi sampai ke HP orang tua < 1 menit (reliability) |
| NF5 | Tampilan mudah dipahami, tanpa pelatihan (usability) |

---

### F. LANGKAH ANALISIS KEBUTUHAN

1. **Identifikasi pengguna** — Siapa saja yang akan memakai sistem?
2. **Gali kebutuhan** — Wawancara, observasi, kuesioner
3. **Klasifikasikan** — Fungsional vs non-fungsional
4. **Tulis user story** — Format standar
5. **Validasi** — Konfirmasi ke pengguna: "Apakah ini yang dimaksud?"
6. **Dokumentasi** — SRS (Software Requirements Specification)

---

### G. RANGKUMAN

| Konsep | Inti |
|---|---|
| Analisis kebutuhan | Proses menggali apa yang pengguna butuhkan |
| Fungsional | Fitur yang harus ada (apa yang sistem lakukan) |
| Non-fungsional | Kualitas sistem (seberapa baik) |
| User story | Format: Sebagai... saya ingin... sehingga... |
| Teknik | Wawancara, observasi, kuesioner, studi dokumen |

> **Ingat:** "Kegagalan terbesar bukan salah coding, tapi salah kebutuhan!"

---

**MGMP Informatika SMAN 6 Cimahi**
