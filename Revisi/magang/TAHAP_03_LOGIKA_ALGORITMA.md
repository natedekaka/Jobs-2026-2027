# TAHAP 3 — LOGIKA & ALGORITMA
## Rencana Harian (21 Hari) — Berpikir Komputasional → Flowchart → Pseudocode → Python

**Tujuan tahap:** Menguasai jalan logika yang diajarkan di Kelas XI sehingga bisa mengajarkan, bukan sekadar memberi contoh.

**Syarat kelulusan (produk bukti):**
- ✅ 5 flowchart simbol-benar dari masalah nyata
- ✅ 5 pasangan pseudocode + Python (siap jadi kunci jawaban)
- ✅ 3 program utuh: kalkulator, tebak angka, sistem antrean
- ✅ 1 sesi mengajar yang dievaluasi rekan mengenai "menolak jawaban instan dari AI"

---

## MINGGU 1 — BERPIKIR KOMPUTASIONAL (7 hari)

### Hari 1 — Empat Pilar Berpikir Komputasional
- **Tugas:** Pelajari dekomposisi, pengenalan pola, abstraksi, algoritma.
- **Latihan:** Ambil "persiapan ulangan" → dekomposisi jadi langkah-langkah.
- **Istimewa:** Setiap masalah dipecah **minimal 3 sub-masalah** sebelum solusi.

### Hari 2 — Dekomposisi (Latihan Beruntun)
- **Tugas:** Pecah 5 aktivitas hidup: menyeduh kopi, mandi pagi, belanja pasar, naik transportasi umum, kirim paket.
- **Bukti:** Setiap aktivitas jadi ≥3 langkah urut.

### Hari 3 — Pengenalan Pola & Abstraksi
- **Tugas:** Dari 5 aktivitas Hari 2, temukan pola umum (mulai → proses → selesai) & buang detail tak penting (abstraksi).
- **Bukti:** 1 diagram pola umum berlaku utk semua aktivitas.

### Hari 4 — Butuhkasus: Antrean Bank
- **Tugas:** Berpikir komputasional utk "sistem antrean mesin antrean". Terapkan 4 pilar.
- **Simpan:** Catatan solusi (dipakai lagi di Hari 21 & program antrean).

### Hari 5 — Aktivitas Unplugged (Tanpa Komputer)
- **Tugas:** Rancang permainan kertas utk siswa: kartu instruksi, simulasi "robot manusia".
- **Sumber:** pola dari `code.org/csd`.
- **Bukti:** 1 permainan unplugged siap dipakai di kelas.

### Hari 6 — Tautkan ke Kehidupan & Profesi
- **Tugas:** Riset: cara dokter/akuntan/guru memakai dekomposisi-pola-abstraksi-algoritma.
- **Simulasi nyata:** Siapkan jawaban utk pertanyaan siswa "kenapa belajar ini?"

### Hari 7 — Review & Kuis
- **Tugas:** Ulangi semua pilar tanpa catatan. Buat 5 soal + kunci utk siswa (siap jadi LKPD).

---

## MINGGU 2 — FLOWCHART & PSEUDOCODE (7 hari)

### Hari 8 — Simbol Flowchart yang Benar
- **Tugas:** Hapal makna simbol: terminal (oval), proses (persegi), input/output (jajaran genjang/parallelogram), kondisi/keputusan (belah ketupat), alur (panah).
- **Tantangan:** Simbol harus benar & satu arah alur.

### Hari 9 — Flowchart Urutan (Sequence)
- **Tugas:** Buat flowchart utk proses sekuensial minimal (mis. hitung luas persegi: input → hitung → output).
- **Bukti:** 1 flowchart sequence yang mengalir dari atas ke bawah.

### Hari 10 — Flowchart Percabangan (Decision)
- **Tugas:** Buat flowchart "cek kelulusan" (nilai ≥ KKM → LULUS, dan tidak → TIDAK LULUS) + 1 contoh hidup (masuk kelas saat hujan/gak bawa payung, dst).
- **Kunci:** Jalur tepat 2 cabang dari belah ketupat.

### Hari 11 — Flowchart Perulangan (Loop)
- **Tugas:** Buat flowchart "hitung 1 sampai 10" + "masukkan password sampai benar".
- **Kunci:** Lingkaran balik (back edge) tanda loop.

### Hari 12 — Pseudocode Dasar (IF, FOR, WHILE)
- **Tugas:** Ubah 3 flowchart Hari 10-11 → pseudocode. Pakai kata: `MULAI`, `INPUT`, `JIKA...MAKA...SEBALIKNYA`, `ULANGI...HINGGA`, `TAMPILKAN`, `SELESAI`.
- **Kunci:** Pseudocode = bahasa setengah manusia setengah mesin, tetap bisa dibaca.

### Hari 13 — Studi Kasus: Kalkulator & Nilai Rata-rata
- **Tugas:** Flowchart + pseudocode utk 3 studi kasus. Cek di `TAHAP_03_SOAL_LATIHAN_KUNCI.md`.
- **Bukti:** Solusi bisa jadi kunci jawaban siswa.

### Hari 14 — Uji Coba & Galeri
- **Tugas:** Pajang flowchart di dinding (gallery walk). Diskusikan perbedaan solusi. Buat koreksi simbol.

---

## MINGGU 3 — PYTHON (7 hari) — Google Colab

### Hari 15 — Setup Colab & Print/Variabel
- **Tugas:** Buka `colab.research.google.com`. Terapkan shortcut (Shift+Enter, Ctrl+Enter, Alt+Enter). Buat variabel & `print()`.
- **Jalan pintas:** Colab auto-save ke Drive.

### Hari 16 — Input & Percabangan (IF)
- **Tugas:** Buat program cek kelulusan dari Hari 10 dalam Python: `nilai = int(input())`, `if nilai >= 70`.

### Hari 17 — Perulangan FOR & WHILE
- **Tugas:** Buat "hitung 1..10" pakai `for`, dan "password sampai benar" pakai `while`.
- **Jalan pintas siswa:** `range()`, break/continue. Baca error dari bawah.

### Hari 18 — List & Fungsi
- **Tugas:** Buat list nilai siswa → `sum()`, `max()`, `min()`. Bungkus logika jadi `def`.

### Hari 19 — Pembuatan Program: Kalkulator
- **Tugas:** Kalkulator dengan menu (tambah/kurang/kali/bagi) — loop menu sampai "keluar". Gunakan `def` untuk tiap operasi.

### Hari 20 — Pembuatan Program: Tebak Angka
- **Tugas:** `random.randint()` → pemain menebak, program bilang "terlalu besar/kecil", hitung percobaan. Latihan `while` + kondisi.

### Hari 21 — Sistem Antrean (Tantangan) + Simulasi Nyata
- **Tugas:** Simulasikan antrean: tambah antrean, layani pertama keluar, tampilkan antrean (pakai list). Kaitkan dengan Hari 4 (antrean bank).
- **Simulasi akhir:** Ajarkan sesi "kenapa coding / strategi menghadapi AI" ke dewan rekan guru (siapkan jawaban anti-jawaban-instans).

---

## Checklist Penyelesaian Tahap 3
- [ ] 5 flowchart, simbol benar (Hari 8-13)
- [ ] 5 pasangan pseudocode → Python (Hari 12-13, 16-17)
- [ ] 3 program utuh (Hari 19-21)
- [ ] 1 sesi mengajar + umpan balik rekan (Hari 21)

**Catatan penting:** Di era AI, ajarkan **dekomposisi & debugging**, bukan menghafal sintaks. Minta AI menulis kode SALAH → siswa perbaiki.

---

**MGMP Informatika SMAN 6 Cimahi — Program Magang Guru Informatika TP 2026/2027**