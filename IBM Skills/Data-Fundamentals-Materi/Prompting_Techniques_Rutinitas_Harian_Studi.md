# Using Prompting Techniques to Organize a Daily Work and Personal Routine — Materi Belajar Offline

> Disusun dari materi IBM SkillsBuild (Prompt Engineering & Generative AI Roadmap) + study guide program JA SkillsBuild Jawa Barat. Kursus aslinya: praktik menyusun prompt AI untuk mengorganisir rutinitas harian kerja & pribadi.

---

## 1. Apa itu Prompt & Prompt Engineering?

> **Prompt** = instruksi/perintah yang Anda berikan ke AI (mis. ChatGPT, IBM Granite).
> **Prompt Engineering** = seni menyusun instruksi agar AI memberi jawaban yang Anda inginkan.

**Analogi:** seperti memberi tugas ke asisten. Perintah "tolong buatkan jadwal" hasilnya umum dan berantakan. Perintah yang jelas, spesifik, dengan format & target → hasilnya langsung bisa dipakai.

### 1.1 Kenapa Penting untuk Mengatur Rutinitas Harian?
AI bisa menjadi **asisten pribadi** yang membantu Anda:
- Menyusun jadwal harian kerja
- Membuat to-do list yang terprioritas
- Merencanakan jadwal mengajar & kegiatan pribadi
- Mengelompokkan/mengorganisir informasi
- Meringkas catatan rapat
- Mengingatkan hal yang sering terlewat

Tapi AI hanya sebagus prompt-nya. Prompt yang buruk → jawaban umum. Prompt yang baik → jawaban siap pakai.

---

## 2. Konsep Dasar yang Harus Dikuasai

### 2.1 Komponen Prompt Efektif (5 Elemen)

Prompt yang bagus mengandung:

| No | Elemen | Pertanyaan | Contoh |
|---|---|---|---|
| 1 | **Tugas** | Apa yang diminta? | "Buatkan jadwal..." |
| 2 | **Topik** | Tentang apa? | "...untuk guru yang mengajar 6 kelas..." |
| 3 | **Target audiens** | Untuk siapa? | "...untuk guru SMA..." |
| 4 | **Format** | Bentuk hasil? | "dalam bentuk tabel..." |
| 5 | **Detail tambahan** | Batasan & preferensi | "maksimal 8 poin, waktu istirahat di jam 12" |

### 2.2 Formula Praktis (ingat 5 W + H versi AI)

```
[Perintah/Tugas] + [Topik] + [Audiens] + [Format] + [Detail/Batasan]
```

**Contoh prompt rutinitas harian:**
> "Buatkan jadwal harian untuk guru yang mulai kerja jam 7 pagi, dengan 5 jam mengajar, sisipkan jeda istirahat, dan sisakan waktu untuk mengoreksi tugas. Format tabel, urutkan dari pagi ke malam."

---

## 3. Perbandingan Prompt Buruk vs Baik

### 3.1 Untuk Jadwal Harian

| | Prompt Buruk | Prompt Baik |
|---|---|---|
| Teks | "Buatkan jadwal harian" | "Buatkan jadwal harian untuk guru yang mulai kerja pukul 07.00, mengajar 5 jam, ingin pulang tidak lebih dari 15.00, dengan waktu istirahat. Format tabel." |
| Hasil | Umum, tidak sesuai kebutuhan | Spesifik, langsung bisa dipakai |

### 3.2 Untuk To-Do List

| | Prompt Buruk | Prompt Baik |
|---|---|---|
| Teks | "Buat daftar tugas" | "Buat to-do list hari ini berdasarkan ini: rapat MGMP jam 9, koreksi 40 lembar ulangan, beli sembako, jemput anak jam 4 sore. Urutkan berdasarkan prioritas, 4 poin saja." |
| Hasil | Daftar acak | Prioritas jelas sesuai kebutuhan |

---

## 4. Teknik-Teknik Prompt Engineering (untuk Rutinitas Harian)

### 4.1 Beri Konteks (Context)
Berikan informasi latar agar AI paham situasi Anda.

> "Saya seorang guru yang juga menjadi panitia acara sekolah. Saya sering kewalahan mengatur waktu antara mengajar dan urusan panitia."

### 4.2 Tentukan Format Output
AI bisa menghasilkan tabel, bullet points, atau paragraf. Tentukan dengan jelas.

> "Tampilkan dalam bentuk tabel dengan kolom: Waktu, Aktivitas, Prioritas, Catatan."

### 4.3 Tentukan Batasan (Constraints)
Batasi agar hasil tidak melebar.

> "Hanya untuk hari Senin sampai Jumat.", "Maksimal 8 aktivitas per hari.", "Jangan masukkan hari Minggu."

### 4.4 Iterasi / Perbaiki Prompt (Iterative Prompting)
Jika hasil kurang pas → **perbaiki prompt, jangan ganti topik**. Tambah detail atau beri instruksi lanjutan.

> "Bagus, tapi pindahkan aktivitas 'koreksi ulangan' ke sore hari setelah pukul 14.00. Buatkan ulang."

### 4.5 Beri Peran (Role Prompting)
Suruh AI berperan sebagai ahli tertentu agar hasil lebih tepat.

> "Bertindaklah sebagai asisten manajemen waktu untuk seorang guru."

### 4.6 Contoh Prompt (Few-Shot)
Beri contoh jawaban yang diinginkan agar AI meniru polanya.

> "Contoh format yang saya mau: [07.00-07.30] Persiapan kelas | Prioritas Tinggi. Sekarang buatkan untuk hari Rabu saya."

---

## 5. Contoh Prompt Siap Pakai untuk Guru

### 5.1 Jadwal Harian Kerja
```
"Buatkan jadwal harian untuk guru yang mengajar di SMAN 6 Cimahi, 
mulai pukul 07.00 sampai 16.00. Sertakan waktu istirahat dan waktu 
khusus untuk mengoreksi tugas siswa. Format tabel, prioritas per 
kegiatan, Bahasa Indonesia."
```

### 5.2 To-Do List Terprioritas
```
"Buatkan to-do list hari ini dari daftar berikut: menyiapkan RPP, 
rapat guru jam 9, mengoreksi ulangan kelas X, membalas email orang 
tua, latihan upacara. Urutkan berdasarkan tingkat urgensi, maksimal 
6 poin, beri perkiraan waktu tiap tugas."
```

### 5.3 Membagi Kerja & Pribadi (Work-Life Balance)
```
"Bagi aktivitas berikut ke dua kolom: KERJA dan PRIBADI, lalu buat 
jadwal yang seimbang agar tidak kelelahan. Aktivitas: mengajar 5 
jam, koreksi, olahraga, mengurus anak, rapat panitia, istirahat, 
membaca buku. Sisakan minimal 1 jam untuk keluarga di malam hari."
```

### 5.4 Merencanakan Minggu (Weekly Planning)
```
"Rencanakan minggu depan untuk guru dengan 24 jam mengajar. Sebar 
tugas mengoreksi di 3 hari, jadwalkan 1 sesi olahraga, dan 1 malam 
khusus keluarga. Gunakan tabel Senin-Minggu."
```

### 5.5 Mengatur Ulang Saat Ada Perubahan (Re-organize)
```
"Jadwal saya berubah: besok ada rapat mendadak jam 10 selama 2 jam. 
Susun ulang jadwal saya hari ini agar koreksi ulangan tetap selesai, 
tanpa mengorbankan istirahat makan siang."
```

### 5.6 Rangkum & Evaluasi (Review)
```
"Ringkas kebiasaan harian saya berikut dan beri 3 saran untuk lebih 
produktif tapi tetap istirahat: [tempel daftar kegiatan]. Jawab 
dalam 5 poin."
```

---

## 6. Best Practices Menulis Prompt Efektif

1. **Mulai dengan kata kerja jelas**: *buatkan, susun, ringkas, ubah, pisahkan, terjemahkan, urutkan*.
2. **Satu prompt = satu tugas** — jangan campur banyak permintaan sekaligus.
3. **Gunakan Bahasa Indonesia** bila mau hasil berbahasa Indonesia — tulis eksplisit "Bahasa Indonesia".
4. **Beri batasan** agar hasil tidak melebar: *"maksimal 6 poin", "dalam tabel", "sebelum pukul 16.00"*.
5. **Perjelas prioritas**: *"urgensi tinggi dulu", "yang penting diletakkan di pagi hari"*.
6. **Iterasi**: hasil kurang pas → perbaiki prompt, tambah detail, jangan ganti topik.
7. **Cek & verifikasi hasil AI** — AI bisa salah; Anda yang paling tahu konteks sebenarnya.

### Checklist Sebelum Kirim Prompt
- [ ] Tugasnya jelas? (buat / susun / urutkan...)
- [ ] Ada konteks? (siapa saya, situasi apa)
- [ ] Formatnya ditentukan? (tabel, daftar, paragraf)
- [ ] Batasan & detail ada? (jumlah, waktu, prioritas)
- [ ] Bahasa output ditentukan?

---

## 7. Hal yang Sering Ditanyakan di Quiz

### 7.1 Pilihan Kata yang Tepat
- **Prompt** = instruksi/perintah ke AI (bukan kode program, bukan data, bukan output).
- **Prompt Engineering** = menyusun instruksi agar hasil AI sesuai keinginan.
- **Context/konteks** = informasi latar yang membuat AI memahami situasi.
- **Constraints/batasan** = aturan yang membatasi hasil (jumlah kata, waktu, format).
- **Iterative prompting** = memperbaiki prompt berdasarkan hasil sebelumnya.

### 7.2 Pilihan Ganda Khas
- "Apa langkah terbaik jika hasil AI terlalu umum?" → **Tambahkan detail & batasan pada prompt** (bukan mengganti topik, bukan mengulang kata-kata yang sama).
- "Prompt mana yang paling efektif untuk membuat jadwal harian?" → Pilih yang **paling spesifik** (ada waktu, kegiatan, format).
- "Apa fungsi 'format tabel' dalam prompt?" → **Menentukan bentuk output** yang diinginkan.
- "Mengapa konteks penting dalam prompt?" → **Agar AI memahami situasi dan memberi jawaban yang relevan**.

### 7.3 Trik Jawaban Quiz IBM
- Soal "yang PALING TEPAT" → pilih jawaban paling lengkap/spesifik.
- Soal memilih prompt terbaik → pilih yang berisi **tugas + detail + format + batasan**.
- Pilihan memakai kata "selalu/pasti" → biasanya salah.
- Soal "BUKAN teknik prompt engineering" → cari pilihan yang tidak masuk akal (mis. "menghafal seluruh jawaban AI").

---

## 8. Ringkasan Cepat (Siap Hafal)

- **Prompt** = instruksi ke AI. **Prompt Engineering** = seni membuat instruksi agar hasil sesuai.
- Prompt efektif = **Tugas + Topik + Audiens + Format + Detail/Batasan**.
- Teknik kunci: beri **konteks**, tentukan **format**, beri **batasan**, **iterasi** jika kurang pas, beri **peran** (role), beri **contoh** (few-shot).
- Untuk rutinitas harian: prompt yang baik menyebutkan **waktu, aktivitas, prioritas, dan format output**.
- AI membantu mengatur kerja & kehidupan pribadi, tapi **tetap Anda yang memverifikasi** hasilnya.
- Jika hasil kurang pas → **perbaiki prompt, bukan ganti topik**.