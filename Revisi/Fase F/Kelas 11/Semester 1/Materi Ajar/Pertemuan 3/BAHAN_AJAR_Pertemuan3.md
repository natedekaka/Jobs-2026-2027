# BAHAN AJAR – PERTEMUAN 3 (S1)
## Pola & Abstraksi
*Mengacu pada Panduan Mapel 2025; INFORMATIKA Fase D-F — pendekatan Pembelajaran Mendalam (Memahami → Mengaplikasi → Merefleksi)*

| Informasi | Keterangan |
|---|---|
| **Fase / Kelas** | F / Kelas XI |
| **Alokasi Waktu** | 5 JP × 45 menit (225 menit) |
| **Elemen CP** | Berpikir Komputasional (BK) |
| **Tujuan Pembelajaran** | Mengidentifikasi pola dalam data, menjelaskan pengertian abstraksi, membedakan informasi penting dan tidak penting, serta menerapkan pola dan abstraksi pada kasus nyata |
| **Materi Prasyarat** | Pertemuan 1–2 — Algoritma dan Dekomposisi |

---

## A. Kisah Pemantik 🎬

> **"Antrean di Kantin"**
>
> Setiap hari Senin pukul 09.00, kantin sekolah selalu ramai dan antreannya panjang. Sinta memperhatikan: yang paling cepat keluar dari antrean adalah pembeli yang **sudah tahu mau membeli apa**, sedangkan yang lama adalah yang bingung. Sinta menyimpulkan sebuah pola: *semakin jelas niat beli, semakin cepat antrean selesai*. Ia juga meringkas antrean menjadi satu informasi penting saja — **waktu tunggu** — tanpa peduli warna baju pembeli.
>
> **Pertanyaan pemantik:** Pola apa yang sering kamu amati di sekitarmu (macet, diskon, cuaca)? Informasi apa yang harus diabaikan agar kamu bisa mengambil keputusan dengan cepat?

---

## B. Pengenalan Pola (Pattern Recognition)

**Pengenalan pola** adalah kemampuan mengamati kesamaan, keteraturan, atau hubungan dalam data untuk membuat prediksi atau pengelompokan. Ini adalah **pilar kedua** Computational Thinking.

**Contoh Pola dalam Kehidupan:**
- **Deret angka:** 1, 4, 7, 10, ... (pola: +3)
- **Pola visual:** motif batik, ubin lantai, wallpaper
- **Pola perilaku:** macet setiap jam 7 pagi, diskon setiap akhir bulan
- **Pola alam:** siang-malam, musim hujan-kemarau

---

## C. Jenis-Jenis Pola

| Jenis Pola | Contoh | Pola |
|---|---|---|
| **Aritmatika** | 2, 5, 8, 11, ... | Selisih tetap (+3) |
| **Geometri** | 2, 6, 18, 54, ... | Dikali tetap (×3) |
| **Kuadrat** | 1, 4, 9, 16, 25, ... | n² (n = 1,2,3,...) |
| **Fibonacci** | 1, 1, 2, 3, 5, 8, ... | Jumlah 2 bilangan sebelumnya |
| **Visual** | ❄️❄️❄️ (3 keping salju berulang) | Pengulangan bentuk |

> 💡 **Manfaat pola:** dengan mengenali pola, kita dapat **memprediksi** apa yang akan terjadi selanjutnya — misalnya memperkirakan deret berikutnya atau memprediksi waktu macet.

---

## D. Abstraksi

**Abstraksi** adalah teknik menyaring informasi dengan hanya mengambil detail esensial dan mengabaikan detail yang tidak relevan. Abstraksi menyederhanakan masalah kompleks agar mudah dipahami. Ini adalah **pilar ketiga** Computational Thinking.

| Situasi | Detail Penting (dipertahankan) | Detail Tidak Penting (diabaikan) |
|---|---|---|
| Membeli HP baru | RAM, penyimpanan, harga, merek | Warna kotak, posisi toko |
| Mendaftar sekolah | Nilai rapor, jarak rumah, akreditasi | Warna seragam, halaman sekolah |
| Membuat kue | Bahan, takaran, suhu oven | Merek mixer, warna apron |
| Naik angkot | Rute, tarif, tujuan | Warna angkot, plat nomor |

---

## E. Langkah Melakukan Abstraksi & Hubungan 4 Pilar

**Langkah melakukan abstraksi:**
1. Identifikasi semua informasi yang tersedia
2. Tentukan tujuan — untuk apa informasi ini digunakan?
3. Tanyakan: "Apakah informasi ini penting untuk mencapai tujuan?"
4. Simpan yang penting, buang yang tidak penting
5. Sajikan dalam bentuk sederhana

**Hubungan 4 pilar** — contoh membuat aplikasi cuaca:
1. **Dekomposisi:** ambil data, olah data, tampilkan
2. **Pola:** cuaca cenderung sama dalam 3 jam
3. **Abstraksi:** hanya suhu, kelembaban, kecepatan angin (abaikan tekanan udara, indeks UV)
4. **Algoritma:** langkah mengambil data dari API → proses → tampilkan

---

## F. Contoh Soal & Penyelesaian 📝

**Contoh 1:** Tentukan 2 angka berikutnya: 3, 6, 12, 24, ?, ?
**Jawaban:** Pola geometri (×2): 3, 6, 12, 24, **48, 96**.

**Contoh 2:** Tentukan pola: A, C, E, G, ?, ?
**Jawaban:** Pola huruf ganjil (loncat 1 huruf): A, C, E, G, **I, K**.

**Contoh 3:** Abstraksi 5 informasi penting dari paragraf berikut!
*"Budi membeli laptop Asus ROG pukul 10 pagi di Toko ABC Senen dengan harga 15 juta. Ia memilih warna hitam. Laptop itu punya RAM 16GB, SSD 512GB, dan layar 15 inci. Budi membayar pakai kartu kredit."*
**Jawaban (tergantung tujuan):** Jika tujuan = membeli laptop, informasi penting: **RAM 16GB, SSD 512GB, layar 15 inci, harga 15 juta, dibayar kartu kredit**. Warna kotak, waktu beli, dan nama toko tidak esensial untuk keputusan membeli.

**Contoh 4:** Apa perbedaan pola dan abstraksi? Berikan contoh masing-masing!
**Jawaban:** **Pola** = menemukan keteraturan/kesamaan dalam data untuk prediksi (contoh: deret 2,4,6,8 → +2). **Abstraksi** = menyaring detail agar hanya esensial yang tersisa (contoh: untuk memilih HP, cukup RAM, harga, penyimpanan — abaikan warna kotak).

**Contoh 5:** Deret 1, 1, 2, 3, 5, 8 tergolong pola apa? Sebutkan 2 suku berikutnya!
**Jawaban:** Pola **Fibonacci** (suku ke-n = jumlah 2 suku sebelumnya): 8 + 5 = **13**, 13 + 8 = **21**.

---

## G. Miskonsepsi / Kesalahan Umum 🚫

| Miskonsepsi | Fakta yang Benar |
|---|---|
| "Pola hanya tentang angka" | Pola bisa berupa visual, perilaku, suara, maupun urutan |
| "Abstraksi = menghilangkan informasi" | Abstraksi menyimpan yang esensial dan membuang yang tidak relevan **sesuai tujuan** |
| "Semakin banyak informasi semakin baik" | Terlalu banyak detail justru menyulitkan pengambilan keputusan |
| "Pola dan abstraksi adalah hal yang sama" | Pola mencari keteraturan; abstraksi menyederhanakan. Dua pilar berbeda |

---

## H. Tantangan Praktik (Mengaplikasi) 🎯

**Tantangan 1 — Deret Angka (mudah):** Tentukan 2 suku berikutnya: 5, 10, 20, 40, ?, ? dan 100, 90, 80, ?, ?.

**Tantangan 2 — Abstraksi Paragraf (sedang):** Abstraksikan informasi penting dari paragraf tentang laptop Budi (Contoh 3) dengan tujuan **"membandingkan harga"**.

**Tantangan 3 — Pola Visual (sulit):** Amati motif batik/ubin/keramik di sekitarmu. Gambar 1 pola yang berulang dan jelaskan aturan pengulangannya.

**Tantangan 4 — Aplikasi Cuaca (paling sulit):** Terapkan 4 pilar CT (dekomposisi, pola, abstraksi, algoritma) untuk merancang aplikasi **cuaca sekolah** yang menampilkan suhu, kelembaban, dan prakiraan 3 jam ke depan.

---

## I. Rangkuman Kunci 🔑

- **Pengenalan pola** = menemukan keteraturan untuk prediksi (pilar ke-2 CT).
- **Abstraksi** = menyaring detail esensial, membuang yang tidak relevan (pilar ke-3 CT).
- Pola membantu **memprediksi**; abstraksi membantu **menyederhanakan**.
- Urutan 4 pilar: **Dekomposisi → Pola → Abstraksi → Algoritma**.
- Abstraksi selalu dilakukan **berdasarkan tujuan**.

---

## J. Glosarium 📖

| Istilah | Arti |
|---|---|
| **Pola** | Keteraturan yang bisa diamati dan diprediksi |
| **Abstraksi** | Penyederhanaan dengan fokus pada informasi esensial |
| **Pola Aritmatika** | Deret dengan selisih tetap |
| **Pola Geometri** | Deret dengan pengali tetap |
| **Fibonacci** | Deret di mana suku = jumlah 2 suku sebelumnya |
| **Esensial** | Sangat penting dan harus dipertahankan |

---

## K. Refleksi (Merefleksi) 🔍

- Konsep apa yang paling penting kamu pelajari hari ini?
- Bagaimana pola dan abstraksi membantu kamu mengambil keputusan sehari-hari?
- Bagian mana yang masih sulit dipahami?
- **Skala pemahaman diri:** ____/10
- Apa yang ingin kamu pelajari lebih lanjut?

---

**MGMP Informatika SMAN 6 Cimahi — Fase F (Kelas XI) Semester 1**