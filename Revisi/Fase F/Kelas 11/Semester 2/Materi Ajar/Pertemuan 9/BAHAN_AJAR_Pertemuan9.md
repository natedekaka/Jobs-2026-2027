# BAHAN AJAR – PERTEMUAN 9 (S2)
## Program Sederhana 2
*Mengacu pada Panduan Mapel 2025; INFORMATIKA Fase D-F — pendekatan Pembelajaran Mendalam (Memahami → Mengaplikasi → Merefleksi)*



### 🧠 Memahami — Membangun Pemahaman Awal

## A. Tujuan Pembelajaran
Setelah mempelajari materi ini, siswa mampu:
1. Membuat program To-Do List sederhana
2. Membuat program pengelolaan nilai siswa
3. Membuat program kuis interaktif
4. Menggabungkan fungsi, list, dan loop dalam 1 program

## B. Program 1: To-Do List
```python
tugas = []
while True:
    print("\n1. Lihat  2. Tambah  3. Hapus  4. Keluar")
    p = input("Pilih: ")
    if p == "1":
        for i, t in enumerate(tugas, 1):
            print(f"{i}. {t}")
        if not tugas: print("[Kosong]")
    elif p == "2":
        tugas.append(input("Tugas baru: "))
    elif p == "3":
        try:
            no = int(input("No: ")) - 1
            if 0 <= no < len(tugas):
                print(f"'{tugas.pop(no)}' dihapus")
        except: print("Error")
    elif p == "4":
        break
```

## C. Program 2: Pengelolaan Nilai
```python
siswa = []
n = int(input("Jumlah siswa: "))
for i in range(n):
    nama = input(f"Nama {i+1}: ")
    nilai = float(input(f"Nilai {nama}: "))
    siswa.append({"nama": nama, "nilai": nilai})

print("\n=== LAPORAN NILAI ===")
total = 0
for s in siswa:
    status = "Lulus" if s["nilai"] >= 70 else "Tidak Lulus"
    print(f"{s['nama']:15} {s['nilai']:<8.1f} {status}")
    total += s["nilai"]

rata = total / n
nilai_max = max(s["nilai"] for s in siswa)
nilai_min = min(s["nilai"] for s in siswa)
print(f"\nRata-rata: {rata:.1f}")
print(f"Tertinggi: {nilai_max}")
print(f"Terendah: {nilai_min}")
```

## D. Program 3: Kuis Interaktif
```python
soal = [
    {"q": "Ibu kota Indonesia?", "a": ["a.Bandung","b.Surabaya","c.Jakarta","d.Jogja"], "k": "c"},
    {"q": "Penemu gravitasi?", "a": ["a.Einstein","b.Newton","c.Galileo","d.Archimedes"], "k": "b"},
]
skor = 0
for i, s in enumerate(soal, 1):
    print(f"\n{i}. {s['q']}")
    for o in s['a']: print(o)
    if input("Jawab: ").lower() == s['k']:
        print("Benar!"); skor += 1
    else: print(f"Salah! Jawaban: {s['k']}")
print(f"Skor: {skor}/{len(soal)}")
```

## E. Tantangan
1. To-Do List dengan simpan data ke file
2. Program nilai dengan predikat (A/B/C/D)
3. Kuis dengan 10 soal dan acak urutan
4. Program catatan keuangan (pemasukan/pengeluaran + saldo)
5. Program tebak angka dengan skor


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
**MGMP Informatika SMAN 6 Cimahi — Fase F (Kelas XI) S2 Pert 9**
