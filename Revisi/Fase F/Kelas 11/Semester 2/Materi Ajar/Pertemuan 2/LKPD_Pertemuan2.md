# LKPD Pert 2 (S2) – Variabel & Tipe Data
*Mengacu pada Panduan Mapel 2025; INFORMATIKA Fase D-F — pendekatan Pembelajaran Mendalam (Memahami → Mengaplikasi → Merefleksi)*
| Nama | ____________________ |
|---|---|
| Kelas | ____________________ |





### 🧠 Memahami — Membangun Pemahaman Awal

### Aktivitas 1 — Membuat Variabel (Individu, 20 menit)
Buat variabel berikut di Colab, lalu print:
```python
nama = "Andi"
usia = 17
tinggi = 165.5
menikah = False
print(nama, type(nama))
print(usia, type(usia))
print(tinggi, type(tinggi))
print(menikah, type(menikah))
```
Catat tipe data masing-masing:
a) nama: _____ b) usia: _____ c) tinggi: _____ d) menikah: _____

### Aktivitas 2 — Input User (Berpasangan, 25 menit)
Buat program profil diri:
```python
nama = input("Nama: ")
umur = input("Umur: ")
hobi = input("Hobi: ")
print("Halo", nama)
print("Umur", umur, "tahun")
print("Hobi", hobi)
```
Kembangkan: minta input 2 angka, lalu cetak jumlahnya.





### 🔧 Mengaplikasi — Praktik & Penerapan

### Aktivitas 3 — Konversi Tipe Data (Individu, 20 menit)
```python
umur_str = "17"
umur_int = int(umur_str)
print(umur_int + 3)  # Berapa? _____
```
Buat program: input Celsius -> konversi ke Fahrenheit.
Rumus: F = C * 9/5 + 32


Uji: barang=Buku, harga=5000, jumlah=3 -> Total: _____
```
print("Total belanja", nama, ":", total)
total = harga * jumlah
jumlah = int(input("Jumlah: "))
harga = int(input("Harga: "))
nama = input("Nama barang: ")
```python
Buat program: input nama barang, harga, jumlah. Output total.
Jelaskan perbedaannya! ___________________________________
```
print(int(a) + int(b))  # ? (setelah di-cast)
print(a + b)  # ? (tanpa di-cast)
a = "10"; b = "20"
```python
Coba dan catat:
Skala: ___/10. Tipe data: _________________
### Aktivitas 4 — Studi Kasus (Kelompok, 20 menit)
Buat program: input nama, nilai matematika, nilai bahasa, nilai IPA.
Output: "Halo [nama], rata-rata nilai kamu: [rata-rata]"

### Aktivitas 5 — Tantangan (Individu, 10 menit)
Buat program: input 2 angka, cetak hasil penjumlahan, pengurangan, perkalian, pembagian.

Skala: ___/10. Tipe data: _________________

### Aktivitas 6 — Type Casting (Individu, 10 menit)
Coba dan catat:
```python
a = "10"; b = "20"
print(a + b)  # ? (tanpa di-cast)
print(int(a) + int(b))  # ? (setelah di-cast)
```
Jelaskan perbedaannya! ___________________________________

### Aktivitas 7 — Program Kasir Sederhana (Berpasangan, 10 menit)
Buat program: input nama barang, harga, jumlah. Output total.
```python
nama = input("Nama barang: ")
harga = int(input("Harga: "))
jumlah = int(input("Jumlah: "))
total = harga * jumlah
print("Total belanja", nama, ":", total)
```
Uji: barang=Buku, harga=5000, jumlah=3 -> Total: _____



- Apa konsep paling penting yang kamu pelajari hari ini?
- Bagian mana yang masih sulit dipahami?
- Skala pemahaman diri: ___/10


### 🔍 Merefleksi — Refleksi & Evaluasi

- Apa konsep paling penting yang kamu pelajari hari ini?
- Bagian mana yang masih sulit dipahami?
- Skala pemahaman diri: ___/10

---
**MGMP Informatika SMAN 6 Cimahi — Fase F (Kelas XI) Semester 2**
