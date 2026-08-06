# MATERI AJAR — TAHAP 3: LOGIKA & ALGORITMA
## Berpikir Komputasional · Flowchart · Pseudocode · Python
*Untuk magang guru Informatika — pendekatan Memahami → Mengaplikasi → Merefleksi*

---

## 🧠 MEMAHAMI — Membangun Pemahaman Awal

### A. Empat Pilar Berpikir Komputasional
1. **Dekomposisi** — memecah masalah besar menjadi sub-masalah kecil.
2. **Pengenalan Pola** — menemukan kesamaan/aturan berulang.
3. **Abstraksi** — membuang detail tak penting, fokus pada yang esensial.
4. **Algoritma** — menyusun langkah-langkah penyelesaian yang urut dan jelas.

> Keterampilan ini berlaku di semua profesi, bukan hanya programmer. Guru harus bisa menjelaskan penerapannya di kehidupan nyata (dokter, akuntan, guru).

### B. Simbol Flowchart yang Benar

| Simbol | Bentuk | Fungsi |
|---|---|---|
| Terminal | Oval | Mulai / selesai |
| Proses | Persegi panjang | Operasi/penghitungan |
| Input/Output | Jajaran genjang | Membaca / menampilkan data |
| Keputusan | Belah ketupat | Percabangan (ya/tidak) |
| Alur | Panah | Arah proses |

**Struktur dasar:**
- **Sequence (urutan):** proses berjalan berurutan dari atas ke bawah.
- **Decision (percabangan):** belah ketupat membagi alur jadi 2 cabang.
- **Loop (perulangan):** panah kembali ke atas (back edge) membentuk lingkaran.

### C. Pseudocode
Bahasa setengah manusia-setengah mesin. Kata kunci baku:
`MULAI`, `BACA`, `TAMPILKAN`, `JIKA...MAKA...SEBALIKNYA`, `UNTUK...SAMPAI`, `SELAMA...`, `AKHIR`, `SELESAI`.

### D. Python & Google Colab
Python = bahasa tingkat tinggi, mudah dibaca, berbasis indentasi. Di kelas digunakan **Google Colab** (`colab.research.google.com`) — gratis, tanpa install.

**Struktur utama Python:** `print()`, variabel, `input()`, `if/elif/else`, `for`, `while`, `list`, `def` (fungsi).

---

## 🔧 MENGAPLIKASI — Praktik & Penerapan

### Praktik 1 — Dekomposisi Aktivitas Nyata
Uraikan "menyeduh kopi" menjadi langkah urut: siapkan alat → panaskan air → masukkan kopi → tuang air panas → saring → sajikan. Lakukan hal yang sama untuk 5 aktivitas lain (mandi, belanja, dst).

### Praktik 2 — Flowchart Percabangan (Cek Kelulusan)
```
[ MULAI ]
    ↘
[Nilai ≥ 70?] --Ya--> [TAMPILKAN "LULUS"]
      ↘ Tidak                 ↘
 [ TAMPILKAN "TIDAK LULUS"] → [ SELESAI ]
```

### Praktik 3 — Pseudocode → Python

**Ke pseudocode:**
```
MULAI
    BACA nilai
    JIKA nilai >= 70 MAKA
        TAMPILKAN "LULUS"
    SEBALIKNYA
        TAMPILKAN "TIDAK LULUS"
    AKHIR JIKA
SELESAI
```

**Ke Python (di Colab):**
```python
nilai = int(input("Masukkan nilai: "))
if nilai >= 70:
    print("LULUS")
else:
    print("TIDAK LULUS")
```

### Praktik 4 — Perulangan (FOR & WHILE)
```python
# FOR: jumlah langkah diketahui (1 sampai 10)
for i in range(1, 11):
    print(i)

# WHILE: jumlah tidak diketahui (password sampai benar)
password = input("Password: ")
while password != "rahasia123":
    print("Salah, coba lagi")
    password = input("Password: ")
print("Berhasil")
```
> **Pola praktis:** jika jumlah langkah diketahui → `for`; jika tidak → `while`.

### Praktik 5 — List & Fungsi
```python
def rata_rata(daftar):
    return sum(daftar) / len(daftar)

nilai = [80, 75, 90, 60, 88]
print("Rata-rata:", rata_rata(nilai))
print("Tertinggi:", max(nilai))
print("Terendah:", min(nilai))
```

### Praktik 6 — Debugging
Baca pesan error **dari bawah ke atas**. Gunakan `print()` strategis untuk melihat nilai variabel di tengah proses. Di era AI: minta AI menulis kode yang **salah**, lalu siswa perbaiki — melatih pemikiran, bukan hafalan.

---

## 🔍 MEREFLEKSI — Refleksi & Evaluasi

- Mana dari 4 pilar berpikir komputasional yang paling kuat mengubah caramu memandang masalah?
- Apa bedanya memakai `for` vs `while`?
- Bagaimana cara kamu menjelaskan "kenapa belajar coding" kepada siswa yang bertanya (sambil ChatGPT bisa menjawab)?
- Skala pemahaman diri: ___/10

---

## Kunci & Latihan
Lihat `magang/TAHAP_03_SOAL_LATIHAN_KUNCI.md` untuk 5 soal lengkap + kunci:
1. Cek kelulusan (IF)
2. Hitung 1–10 (FOR)
3. Password sampai benar (WHILE)
4. Luas persegi panjang (urutan)
5. Sistem antrean (list — tantangan)

---

**MGMP Informatika SMAN 6 Cimahi — Program Magang Guru Informatika TP 2026/2027**