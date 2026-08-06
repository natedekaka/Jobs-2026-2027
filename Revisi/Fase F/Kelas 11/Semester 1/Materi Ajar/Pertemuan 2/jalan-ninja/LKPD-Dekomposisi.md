# LKPD – DEKOMPOSISI

**Informatika Kelas XI (Fase F)** – SMAN 6 Cimahi
Nama: ............. Kelas: ............. Kelompok: .............

---

## 1. PEMAHAMAN (isi titik-titik)

> Dekomposisi adalah **mem........... masalah besar menjadi ........... yang lebih mudah diselesaikan**.

Urutan yang benar: Identifikasi masalah → **................** → **Algoritma**

Dekomposisi dilakukan **SEBELUM / SESUDAH** menyusun algoritma *(lingkarilah)*.

---

## 2. PRAKTIK – Pecahkan Masalah Ini!

**Masalah:** Mengadakan Class Meeting sekolah (lomba + peralatan + jadwal + anggaran + panitia + dokumentasi).

Pecah menjadi 6 sub-masalah:

1. ...................................................
2. ...................................................
3. ...................................................
4. ...................................................
5. ...................................................
6. ...................................................

---

## 3. PRAKTIK KELOMPOK (kerja tim)

**Masalah:** Membangun **startup edukasi online**.

| No | Sub-Masalah | Tim yang Bertanggung Jawab |
|----|-------------|----------------------------|
| 1  | ................ | ................ |
| 2  | ................ | ................ |
| 3  | ................ | ................ |
| 4  | ................ | ................ |
| 5  | ................ | ................ |
| 6  | ................ | ................ |

**Mengapa dibagi per tim lebih efektif?**

........................................................................................................................

---

## 4. PRAKTIK – Mengurutkan Angka (Dekomposisi Algoritma)

**Masalah:** Urutkan `9 8 2 7 5 6` dari kecil ke besar.

Ada **2 cara**. Pilih salah satu yang menurutmu paling mudah.

---

### Cara A – Bubble Sort (bandingkan dua angka lalu tukar)

*Langkah dekomposisi: pecah menjadi "bandingkan dua angka lalu tukar"*

| Langkah ke- | Bandingkan & tukar | Hasil sementara |
|-------------|--------------------|-----------------|
| 1 | 9 dan 8 → tukar | `8 9 2 7 5 6` |
| 2 | 9 dan 2 → tukar | `8 2 9 7 5 6` |
| 3 | 9 dan 7 → tukar | `................` |
| 4 | 9 dan 5 → tukar | `................` |
| 5 | 9 dan 6 → tukar | `8 2 7 5 6 9` |
| dst. | ulangi sampai urut | `................` |

**Hasil akhir:** `2 5 6 7 8 9` *(hitung berapa kali tukar: ......)*

---

### Cara B – Selection Sort (pilih yang terkecil, taruh di depan)

*Langkah dekomposisi: pecah menjadi "cari angka terkecil, taruh di paling depan"*

| Putaran ke- | Cari terkecil dari sisa | Hasil |
|-------------|-------------------------|-------|
| 1 | dari `9 8 2 7 5 6`, terkecil = **2** | `2 8 9 7 5 6` |
| 2 | dari `8 9 7 5 6`, terkecil = **5** | `................` |
| 3 | dari `9 7 8 6`, terkecil = **6** | `................` |
| dst. | lanjutkan sampai urut | `2 5 6 7 8 9` |

> *Setiap selesai 1 putaran, angka paling depan sudah benar — lebih cepat & mudah dilacak.*

---

### Strategi Efektif (justifikasi pilihan)

Menurut buku Informatika Kelas XI, berpikir komputasional menuntut **memilih strategi yang efektif & efisien**.

1. Metode mana yang kamu pilih untuk mengurutkan `9 8 2 7 5 6`? **A / B**

2. Berapa banyak **langkah/tukar** yang kamu hitung dengan metode itu? **......**

3. Menurutmu, mengapa metode itu **paling efektif** untuk data ini? (bandingkan dengan metode lainnya)

> ................................................................................................................................
> ................................................................................................................................

---

## 5. PRAKTIK – Masalah Nyata (ala buku SAP-K11-04)

**Masalah:** Kamu punya **5 tugas** dengan durasi pengerjaan sebagai berikut, dan hanya punya waktu **6 jam** sebelum semuanya dikumpulkan. Semua tugas bernilai sama. Pilih tugas mana yang harus dikerjakan agar **hasil maksimal**.

| Tugas | Durasi (jam) |
|-------|--------------|
| A | 3 |
| B | 1 |
| C | 2 |
| D | 1,5 |
| E | 2,5 |

Langkah:
1. **Dekomposisikan** masalah ini → urutkan tugas dari durasi **terkecil** ke terbesar: `B …`
2. Pilih tugas satu per satu dari yang paling cepat sampai total waktumu **habis (≤ 6 jam)**.
3. Tulis tugas yang terpilih & total jamnya: **.............. (total: ...... jam)**
4. Berapa tugas maksimal yang bisa kamu kerjakan? **...... tugas**

> *Ini persis pola soal LATPR SAP-K11-04-U di buku: dekomposisi + strategi pengurutan untuk masalah nyata.*

---

## 6. REFLEKSI

- Konsep penting hari ini: ................
- Manfaat dekomposisi bagi tim: ................
- **Skala pemahaman diri:** ____/10
- Ingin belajar apa lagi? .................

---

> **Ingat rumus 3 detik: BESAR → KECIL → SELESAIKAN SATU PER SATU**

---

**Catatan untuk guru:**

- Bagian **2** dikerjakan berpasangan, bagian **3**, **4**, dan **5** kelompok 3–4 orang, bagian **6** untuk **Merefleksi**.
- Bagian 4: suruh siswa memilih **satu cara** (A atau B) lalu jelaskan **alasannya** di blok "Strategi Efektif" — ini menegaskan poin buku: *pilih strategi yang efektif & efisien*.
- Bagian 5 meniru soal buku **SAP-K11-04-U (Mengerjakan PR)** — kunci: urutkan dari durasi terkecil → **B, D, C, E, A**. Ambil urutan terkecil sampai total tidak lewat 6 jam: **B(1) + D(1,5) + C(2) = 4,5 jam**, lalu **E(2,5) / A(3) tidak muat** lagi (total jadi > 6). Jadi **maksimal 3 tugas** (B, D, C).
- **Kunci 2 contoh sama:** Class Meeting (sub-kegiatan) dan urutkan angka (pilih-bandingkan-tukar) — semua = memecah masalah besar jadi kecil sampai mudah diselesaikan.