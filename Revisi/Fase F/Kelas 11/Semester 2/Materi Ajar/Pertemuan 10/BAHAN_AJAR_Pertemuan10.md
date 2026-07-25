# BAHAN AJAR – PERTEMUAN 10 (S2)
## Review Python
*Mengacu pada Panduan Mapel 2025; INFORMATIKA Fase D-F — pendekatan Pembelajaran Mendalam (Memahami → Mengaplikasi → Merefleksi)*



### 🧠 Memahami — Membangun Pemahaman Awal

## A. Tujuan: Review Python
Mereview seluruh materi Python S2 (pertemuan 1-9) dan membuat program mandiri.

| Pert | Materi | Skill Kunci |
|------|--------|-------------|
| 1 | Python & Colab | print(), error |
| 2 | Variabel & Tipe Data | int, float, str, bool, casting |
| 3 | Operator | aritmatika, perbandingan, logika |
| 4 | IF Percabangan | if, elif, else, nested |
| 5 | FOR & WHILE | range, break, continue |
| 6 | List & Tuple | indexing, slicing, method |
| 7 | Fungsi | def, parameter, return |
| 8 | Program 1 | Kalkulator, Konversi, BMI |
| 9 | Program 2 | To-Do List, Nilai, Kuis |

## C. Challenge Hari Ini

**Level 1 (Mudah):**
Input nama & umur, cetak "Halo [nama], tahun depan kamu [umur+1]".

**Level 2 (Sedang):**
Input angka, cetak semua faktor. Contoh: 6 -> 1, 2, 3, 6

**Level 3 (Sulit):**
Tebak Kata: program punya list kata, user tebak huruf per huruf (hangman).

**Level 4 (Expert):**
Catatan Keuangan: catat pemasukan & pengeluaran, tampilkan saldo.

## D. Contoh: Faktor Bilangan
```python
def faktor(n):
    return [i for i in range(1, n+1) if n % i == 0]

angka = int(input("Masukkan angka: "))
print(f"Faktor: {faktor(angka)}")
```

## E. Contoh: Tebak Kata
```python
import random
kata = random.choice(["python", "komputer", "program"])
tebak = ["_"] * len(kata)
nyawa = 6
while nyawa > 0 and "_" in tebak:
    print(" ".join(tebak), f"  Nyawa: {nyawa}")
    h = input("Huruf: ").lower()
    if len(h) != 1: continue
    if h in kata:
        for i, ch in enumerate(kata):
            if ch == h: tebak[i] = h
    else: nyawa -= 1
print("Menang!" if "_" not in tebak else f"Kalah! Kata: {kata}")
```

## F. Presentasi (Opsional)
Siswa yang selesai boleh presentasikan programnya ke kelas.


### 🔧 Mengaplikasi — Praktik & Penerapan

### Latihan Pemahaman
1. Jelaskan konsep utama yang telah dipelajari dengan bahasamu sendiri!
2. Berikan 2 contoh penerapan dalam kehidupan sehari-hari!
3. Diskusikan dengan teman: bagaimana materi ini dapat membantu menyelesaikan masalah nyata?

### 🔍 Merefleksi — Refleksi & Evaluasi

- Apa konsep paling penting yang kamu pelajari hari ini?
- Bagaimana konsep ini terkait dengan materi sebelumnya?
- Skala pemahaman diri: ___/10
- Apa yang ingin kamu pelajari lebih lanjut?

---
**MGMP Informatika SMAN 6 Cimahi — Fase F (Kelas XI) S2 Pert 10**
