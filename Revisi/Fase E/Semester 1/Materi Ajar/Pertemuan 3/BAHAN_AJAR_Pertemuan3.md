# BAHAN AJAR – PERTEMUAN 3 (S1)
## File Management
*Mengacu pada Panduan Mapel 2025; INFORMATIKA Fase D-F — pendekatan Pembelajaran Mendalam (Memahami → Mengaplikasi → Merefleksi)*

| Informasi | Keterangan |
|---|---|
| **Fase / Kelas** | E / Kelas X |
| **Alokasi Waktu** | 2 JP × 45 menit (90 menit) |
| **Elemen CP** | Sistem Komputer (SK) |
| **Tujuan Pembelajaran** | Mengelola file dan folder dengan struktur rapi; membaca path; mengenali ekstensi file; menguasai operasi dasar (copy, cut, paste, rename, delete) |
| **Materi Prasyarat** | Software & sistem operasi (Pertemuan 2), khususnya peran File Explorer |

---

## A. Kisah Pemantik 🎬

> **"Lemari Arsip yang Kacau"**
>
> Pak Dedi seorang pegawai kelurahan. Suatu hari warga datang meminta fotokopi akta kelahiran. Pak Dedi mencari ke lemari pertama — tidak ada. Lemari kedua — kosong. Ternyata semua arsip ditumpuk di satu meja tanpa label, tercampur akta, KTP, dan surat pindah. Warga menunggu satu jam, Pak Dedi masih belum menemukan arsipnya!
>
> Komputermu juga punya "lemari arsip" bernama **file management**. Jika file dibiarkan berantakan, mencari satu dokumen bisa memakan waktu lama.
>
> **Pertanyaan pemantik:** Pernahkah kamu menghabiskan waktu lama mencari file tugas di laptop/HP? Di mana biasanya file itu "bersembunyi" dan bagaimana kamu akhirnya menemukannya?

---

## B. Apa Itu File Management?

**File management** adalah cara mengatur, menyimpan, dan mengelola file di komputer agar mudah ditemukan dan digunakan. Bayangkan komputer sebagai **lemari arsip**: tanpa rak berlabel, semua dokumen akan kacau balau.

| Konsep | Analogi Lemari Arsip |
|---|---|
| **Folder** | Rak / map tempat menyimpan dokumen |
| **File** | Dokumen isinya (laporan, foto, musik) |
| **Path** | Alamat rak (Lantai 2, Lemari B, Map 3) |
| **Backup** | Fotokopi cadangan dokumen penting |

---

## C. Struktur Folder (Directory)

Folder membentuk struktur seperti **pohon** (hierarki). Semakin ke bawah, folder semakin rinci:

```
Drive C: (System)
├── Program Files
├── Users
│   ├── User1
│   │   ├── Documents
│   │   ├── Pictures
│   │   └── Downloads
│   └── Public
└── Windows
```

> 💡 **Ingat:** Folder adalah **wadah**, file adalah **isi**. Satu folder boleh berisi banyak file atau folder lain (subfolder).

---

## D. Path (Alamat File)

**Path** adalah alamat lengkap sebuah file, dengan format:

```
Drive:/Folder/Subfolder/NamaFile
```

Contoh nyata:
`C:/Users/Budi/Documents/Tugas Informatika/LKPD1.docx`

| Bagian Path | Arti |
|---|---|
| `C:` | Drive penyimpanan |
| `Users/Budi` | Folder pengguna Budi |
| `Documents` | Subfolder dokumen |
| `Tugas Informatika` | Subfolder tugas |
| `LKPD1.docx` | Nama file + ekstensi |

Dengan path, sistem dan manusia tahu persis lokasi file dalam hitungan detik.

---

## E. Ekstensi File

Ekstensi (suffix setelah titik) menunjukkan **jenis file** dan aplikasi yang membukanya:

| Ekstensi | Jenis File | Aplikasi Pembuka |
|---|---|---|
| .docx | Dokumen Word | Microsoft Word |
| .xlsx | Spreadsheet | Microsoft Excel |
| .pptx | Presentasi | Microsoft PowerPoint |
| .pdf | Dokumen portabel | PDF Reader |
| .jpg / .png | Gambar | Photo Viewer |
| .mp4 | Video | Media Player |
| .mp3 | Audio | Music Player |
| .txt | Teks biasa | Notepad |

> 💡 **Tips:** Nama file sebaiknya deskriptif, misal `LKPD1_Siti.docx`, bukan `blabla (1).docx` — agar mudah dicari di kemudian hari.

---

## F. Operasi Dasar File Management

| Operasi | Shortcut | Cara Lain |
|---|---|---|
| **Copy** | Ctrl+C | Klik kanan → Copy |
| **Cut** | Ctrl+X | Klik kanan → Cut |
| **Paste** | Ctrl+V | Klik kanan → Paste |
| **Rename** | F2 | Klik lambat 2x pada nama |
| **Delete** | Delete/Del | Klik kanan → Delete |
| **New Folder** | Ctrl+Shift+N | Klik kanan → New → Folder |

**Perbedaan penting — Copy vs Cut:**
- **Copy (Ctrl+C):** file asli tetap ada, dibuat salinan.
- **Cut (Ctrl+X):** file asli dipindahkan ke lokasi baru (tidak ada salinan).

---

## G. Tips File Management

1. Gunakan nama folder yang jelas (Tugas, Foto, Musik, Backup).
2. **Backup** file penting ke cloud (Google Drive, OneDrive) secara rutin.
3. Hapus file tidak perlu secara berkala agar drive tidak penuh.
4. Gunakan **search** (Ctrl+F / kolom pencarian) untuk mencari cepat.
5. Sortir file berdasarkan tanggal "modified" untuk melacak perubahan.

> 💡 **Aturan praktis:** Buat subfolder per mata pelajaran di dalam folder "Tugas", misal `Tugas/Informatika/`, `Tugas/Matematika/`. Rapi sejak awal = hemat waktu saat ujian!

---

## H. Contoh Soal & Penyelesaian 📝

**Contoh 1:** Tuliskan path lengkap untuk file `LKPD1.docx` di folder Documents milik user Budi!
**Jawaban:** `C:/Users/Budi/Documents/LKPD1.docx`

**Contoh 2:** Sebutkan 3 ekstensi file beserta fungsinya!
**Jawaban:**
1. **.docx** — dokumen pengolah kata (Word).
2. **.pdf** — dokumen portabel yang tampilannya sama di semua perangkat.
3. **.mp4** — file video.

**Contoh 3:** Apa perbedaan copy (Ctrl+C) dan cut (Ctrl+X)?
**Jawaban:** Copy membuat salinan dan **file asli tetap berada di lokasi awal**, sedangkan cut **memindahkan** file sehingga file asli pindah ke lokasi tujuan. Cut biasanya diikuti paste (Ctrl+V) agar file tidak hilang.

---

## I. Miskonsepsi yang Sering Terjadi 🚫

| Miskonsepsi | Fakta yang Benar |
|---|---|
| "Menghapus file = file hilang permanen" | File masuk **Recycle Bin** dan bisa dipulihkan selama belum dikosongkan |
| "Folder dan file itu sama" | Folder adalah **wadah**, file adalah **isi** |
| "Cut tanpa paste membuat file hilang" | File hanya menunggu di clipboard; harus **paste** ke lokasi baru |
| "Rename bisa mengubah jenis file" | Rename hanya mengubah nama; jenis file ditentukan **ekstensi** |

---

## J. Tantangan Praktik (Mengaplikasi) 🎯

**Tantangan 1 — Rapi-kan Folder:** Buat struktur folder `Tugas/Informatika` dan `Tugas/Matematika` di Documents. Pindahkan minimal 3 file tugas ke folder yang sesuai menggunakan Ctrl+X lalu Ctrl+V. Tuliskan path salah satu file tersebut.

**Tantangan 2 — Kenali File:** Cari 5 file berbeda di komputermu, catat ekstensinya, lalu tebak aplikasi yang membukanya. Verifikasi dengan membuka file tersebut.

**Tantangan 3 — Backup Cerdas:** Buat folder `Backup_Tugas`. Salin (copy) 3 file penting ke folder tersebut dan ke Google Drive/OneDrive. Setelah itu, jelaskan: apa jadinya jika kamu menyalin file yang sama ke cloud dan harddisk hilang?

---

## K. Rangkuman Kunci 🔑

1. **File management** = cara mengatur file agar rapi dan mudah dicari.
2. **Folder = wadah, file = isi**; struktur berbentuk pohon (hierarki).
3. **Path** = alamat lengkap file: `Drive:/Folder/Subfolder/NamaFile`.
4. Ekstensi menentukan jenis file & aplikasi pembukanya (.docx, .pdf, .mp4, dll).
5. Operasi dasar: **copy (Ctrl+C), cut (Ctrl+X), paste (Ctrl+V), rename (F2), delete**.
6. **Backup rutin** ke cloud mencegah data hilang.

---

## L. Glosarium 📖

| Istilah | Arti |
|---|---|
| **File Management** | Pengelolaan/penataan file agar mudah ditemukan |
| **Folder / Directory** | Wadah penyimpanan file |
| **Path** | Alamat lengkap lokasi file |
| **Ekstensi** | Akhiran nama file penentu jenis (contoh .docx) |
| **Backup** | Salinan cadangan data penting |
| **Recycle Bin** | Tempat sampah file yang dihapus |
| **Clipboard** | Area penyimpanan sementara hasil copy/cut |

---

## M. Refleksi (Merefleksi) 🔍

- Apa konsep paling penting yang kamu pelajari hari ini?
- Folder apa yang ingin kamu rapikan pertama kali di komputermu, dan kenapa?
- Apa kejadian nyata yang membuatmu sadar pentingnya backup file?
- **Skala pemahaman diri:** ____/10
- Apa yang ingin kamu pelajari lebih lanjut tentang pengelolaan file?

---

**MGMP Informatika SMAN 6 Cimahi — Fase E (Kelas X) Semester 1**