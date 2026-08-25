# BAHAN AJAR – PERTEMUAN 13 (S2)
## Keamanan Digital — Password, Phishing, dan Perlindungan Data
*Mengacu pada Panduan Mapel 2025; INFORMATIKA Fase D-F — pendekatan Pembelajaran Mendalam (Memahami → Mengaplikasi → Merefleksi)*

| Informasi | Keterangan |
|---|---|
| **Fase / Kelas** | F / Kelas XI |
| **Alokasi Waktu** | 5 JP × 45 menit (225 menit) |
| **Elemen CP** | Jaringan Komputer dan Internet (JKI) & Dampak Sosial Informatika (DSI) |
| **Tujuan Pembelajaran** | Menjelaskan ancaman keamanan digital, menerapkan praktik password kuat dan 2FA, mengenali phishing, serta melakukan backup data |
| **Materi Prasyarat** | Jaringan Dasar & Jaringan di Sekitar Kita (Pertemuan 11-12) |

---

## A. Kisah Pemantik 🎬

> **"Dompet yang Dibuka dari Jarak Jauh"**
>
> Suatu hari Sinta menerima email "dari banknya" yang meminta mengisi ulang data karena "akun akan ditutup dalam 24 jam". Panik, ia langsung mengisi nomor kartu dan password. Keesokan harinya saldonya raib.
>
> Sinta menjadi korban **phishing** — penipuan yang berpura-pura menjadi pihak terpercaya untuk mencuri data. Di era digital, data pribadi adalah "dompet" kita. Menjaganya sama pentingnya dengan mengunci pintu rumah.
>
> **Pertanyaan pemantik:** Pernahkah kamu atau orang terdekatmu menerima pesan mencurigakan yang meminta data pribadi? Apa yang seharusnya dilakukan sebelum mengklik atau mengisi data tersebut?

---

## B. Mengapa Keamanan Digital Penting? 🔐

- Data pribadi tersimpan di HP, laptop, dan cloud (email, sosmed, rekening).
- Ancaman nyata: kebocoran data, peretasan akun, penipuan finansial.
- Contoh nyata: data jutaan penduduk Indonesia pernah bocor dan dijual di internet.
- Data yang bocor bisa disalahgunakan untuk pinjaman ilegal, penipuan, atau pemerasan.

| Istilah | Arti |
|---|---|
| **Malware** | Perangkat lunak berbahaya |
| **Phishing** | Penipuan berpura-pura jadi pihak terpercaya |
| **Hacking** | Akses ilegal ke sistem/akun |
| **Password** | Kunci akses akun |
| **2FA** | Autentikasi dua faktor |
| **Backup** | Salinan data untuk pengamanan |

---

## C. Jenis-Jenis Ancaman Digital ☠️

**1. Malware** — perangkat lunak berbahaya:

| Jenis | Cara Kerja | Dampak |
|---|---|---|
| **Virus** | Menempel pada file | Merusak atau menginfeksi file lain |
| **Worm** | Menyebar sendiri ke perangkat lain | Menghabiskan bandwidth dan sumber daya |
| **Trojan** | Menyamar sebagai program baik | Mencuri data secara diam-diam |
| **Ransomware** | Mengunci file dan minta tebusan | Data terkunci/tidak bisa diakses |
| **Spyware** | Memata-matai aktivitas | Mencuri password dan data pribadi |

**2. Phishing** — penipuan mengelabui:
Pelaku berpura-pura menjadi bank, sekolah, atau lembaga resmi untuk mencuri data. Sering lewat email, SMS, atau pesan WhatsApp.

**3. Hacking** — peretasan:
Akses ilegal ke sistem atau akun orang lain. Motifnya beragam: mencuri data, merusak website, hingga menjadikan perangkat sebagai alat crypto mining.

**Ciri-ciri phishing yang harus dikenali:**

| Ciri Phishing | Contoh |
|---|---|
| Domain email aneh meniru lembaga | `bank-aman.support@gmail.com` |
| Ada link "klik untuk verifikasi" | "Klik tautan untuk mengaktifkan akun" |
| Ancaman mendesak | "Akun akan ditutup 24 jam!" |
| Minta data pribadi | Password, PIN, nomor kartu |
| Bahasa aneh / banyak typo | Kalimat tidak profesional |

---

## D. Praktik Keamanan Digital 🛡️

**1. Password Kuat**

| Lemah ❌ | Kuat ✅ |
|---|---|
| 123456 | G4L4ngS3nja!2025 |
| password | Kucing_Belajar_Python! |
| tanggal lahir | Saya_Lulus_SMA_2026# |

**Aturan password kuat:**
- Minimal **12 karakter**.
- Kombinasi huruf besar, huruf kecil, angka, dan simbol.
- Jangan memakai data pribadi (nama, tanggal lahir).
- **Berbeda untuk setiap akun**.
- Gunakan kalimat yang mudah diingat namun sulit ditebak, misal `Kucing_Saya_Makan_3Ikan!`.

**2. Autentikasi Dua Faktor (2FA)**

2FA menambah lapisan keamanan: setelah password, diminta kode OTP / sidik jari / face ID.

```text
Langkah 1: Password  →  Langkah 2: Kode OTP dari SMS/app  →  Masuk
```

Aktifkan 2FA di akun penting: email, media sosial, WhatsApp, dan aplikasi perbankan.

**3. Backup Data**

- Backup file penting ke Google Drive, OneDrive, atau hard disk eksternal.
- **Aturan 3-2-1**: 3 salinan data, di 2 media berbeda, 1 di luar lokasi (off-site).

**4. Kebiasaan aman lain:**
- Jangan klik tautan mencurigakan.
- Logout dari perangkat publik.
- Update perangkat lunak secara rutin (patch keamanan).
- Aktifkan verifikasi login / peringatan perangkat baru.

---

## E. Contoh Soal & Penyelesaian 📝

**Contoh 1:** Sebutkan 3 jenis malware dan cara kerjanya!
**Jawaban:** (1) **Virus** menempel pada file dan menginfeksi file lain yang dibuka. (2) **Trojan** menyamar sebagai program baik lalu mencuri data diam-diam. (3) **Ransomware** mengunci file dan meminta tebusan agar data dikembalikan.

**Contoh 2:** Apa itu phishing? Sebutkan 3 cirinya!
**Jawaban:** Phishing adalah penipuan yang berpura-pura menjadi pihak terpercaya untuk mencuri data. Cirinya: (1) email dari domain mencurigakan meniru lembaga resmi; (2) ada link "klik untuk verifikasi"; (3) ancaman mendesak seperti "akun akan ditutup".

**Contoh 3:** Buat contoh password yang kuat dan jelaskan mengapa kuat!
**Jawaban:** Contoh: `Saya_Belajar_Python#2026`. Kuat karena panjang (24 karakter), menggabungkan huruf besar, huruf kecil, simbol (`_`, `#`), dan angka, serta tidak memakai data pribadi yang mudah ditebak.

**Contoh 4:** Apa fungsi 2FA dan mengapa penting?
**Jawaban:** 2FA menambah lapisan autentikasi kedua setelah password, misal kode OTP atau sidik jari. Penting karena walau password bocor, penyerang tetap tidak bisa masuk tanpa kode tambahan, sehingga akun jauh lebih aman.

**Contoh 5:** Kamu menerima SMS "Akun kamu diblokir! Klik link ini untuk memulihkan." Apa yang akan kamu lakukan?
**Jawaban:** Jangan klik link atau isi data apa pun. Verifikasi langsung ke saluran resmi (misal aplikasi bank/sekolah atau kontak resmi), dan laporkan pesan tersebut. Hindari mengetik data pribadi di link yang tidak dikenali.

---

## F. Miskonsepsi & Kesalahan Umum 🚫

| Miskonsepsi | Fakta yang Benar |
|---|---|
| "Password panjang tapi mudah ditebak tidak masalah" | Data pribadi (tanggal lahir, nama) justru mudah ditebak penyerang |
| "2FA ribet, tidak perlu" | 2FA adalah pengaman terbaik kedua setelah password |
| "Phishing hanya lewat email" | Phishing juga lewat SMS, WhatsApp, dan media sosial |
| "Antivirus cukup untuk semua ancaman" | Antivirus tidak melindungi dari phishing yang mengandalkan kelengahan manusia |
| "Backup hanya untuk file kantor" | Semua data penting (foto, tugas) perlu di-backup |
| "Klik link dari teman pasti aman" | Akun teman bisa diretas dan dipakai menyebar phishing |

---

## G. Tantangan Praktik (Mengaplikasi) 🎯

**Tantangan 1 — Audit Password (Mudah):** Periksa password akun-akunmu (tanpa membagikannya!). Nilailah kekuatannya: panjang, kombinasi karakter, dan apakah memakai data pribadi.

**Tantangan 2 — Analisis Email (Sedang):** Guru menampilkan contoh email phishing dan email asli. Identifikasi ciri-ciri phishing pada masing-masing dan jelaskan alasannya.

**Tantangan 3 — Buat Password Kuat (Sedang):** Buat 3 contoh password kuat dengan pola yang mudah kamu ingat. Jelaskan mengapa masing-masing kuat.

**Tantangan 4 — Rencana Backup (Sulit):** Buat rencana backup pribadi memakai aturan 3-2-1 untuk data pentingmu (tugas, foto, dokumen), lalu praktikkan minimal satu salinan.

**Tantangan 5 — Kampanye Keamanan (Sulit):** Buat poster/infografis "Cara Melindungi Akun Digital" berisi password kuat, 2FA, ciri phishing, dan backup — lalu tampilkan di kelas.

---

## H. Rangkuman Kunci 🔑

- Data pribadi bernilai tinggi; keamanan digital adalah keharusan.
- **Malware**: virus, worm, trojan, ransomware, spyware.
- **Phishing** = penipuan mengelabui; kenali domain aneh, link "verifikasi", dan ancaman mendesak.
- Password kuat: ≥12 karakter, kombinasi huruf besar/kecil, angka, simbol, unik tiap akun.
- **2FA** menambah lapisan keamanan kedua setelah password.
- **Backup 3-2-1**: 3 salinan, 2 media, 1 off-site.
- Jangan klik tautan mencurigakan dan verifikasi selalu lewat saluran resmi.

---

## I. Glosarium 📖

| Istilah | Arti |
|---|---|
| **Malware** | Perangkat lunak berbahaya |
| **Virus** | Malware yang menempel di file |
| **Trojan** | Malware yang menyamar sebagai program baik |
| **Ransomware** | Malware pengunci file dengan tebusan |
| **Phishing** | Penipuan berpura-pura jadi pihak terpercaya |
| **Hacking** | Akses ilegal ke sistem/akun |
| **2FA** | Autentikasi dua faktor |
| **Backup** | Salinan data untuk pengamanan |
| **Data pribadi** | Informasi identitas seseorang |

---

## J. Refleksi (Merefleksi) 🔍

- Seberapa rentan akunmu saat ini? Langkah apa yang akan kamu lakukan untuk mengamankannya?
- Mengapa kelengahan manusia sering menjadi titik lemah keamanan, bukan teknologinya?
- Apa yang akan kamu lakukan jika menemukan pesan phishing di grup atau sosial media?
- **Skala pemahaman diri:** ____/10
- Apa yang ingin kamu pelajari lebih lanjut tentang keamanan digital?

---

**MGMP Informatika SMAN 6 Cimahi — Fase F (Kelas XI) Semester 2**