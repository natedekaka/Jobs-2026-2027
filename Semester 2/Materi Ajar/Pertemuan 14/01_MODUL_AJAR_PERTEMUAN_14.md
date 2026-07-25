# MODUL AJAR INFORMATIKA – FASE E (KELAS X)

| Komponen | Deskripsi |
|---|---|
| **Mata Pelajaran** | Informatika |
| **Fase / Kelas** | E / X |
| **Semester** | 2 (Genap) |
| **Pertemuan ke-** | 14 |
| **Alokasi Waktu** | 2 JP × 45 menit (90 menit) |
| **Tahun Pelajaran** | 2026/2027 |
| **Satuan Pendidikan** | SMA Negeri 6 Cimahi |

---

## Tujuan Pembelajaran

| TP | IKTP |
|---|---|
| **BK 1.4, BK 2.1, BK 2.2** | 2.2.1 Membuat dan mengakses list di Python |
| | 2.2.2 Menggunakan method list (append, insert, remove, sort) |
| | 2.2.3 Menulis fungsi dengan def, parameter, return |
| | 2.2.4 Membuat program pengelolaan data dengan list + fungsi |
| | 2.2.5 Menghubungkan konsep array (Pert 1) dengan list Python |

---

## Langkah Pembelajaran

### Pembukaan (10 menit)

| Kegiatan | Waktu |
|---|---|
| 1. Salam, doa, cek kehadiran | 2 menit |
| 2. **Review**: "Pert 1 kita belajar **Array** — struktur data dasar. Pert 12–13 kita belajar Python. Hari ini keduanya bertemu: **List = Array di Python**!" | 3 menit |
| 3. **Apersepsi**: "Bayangkan daftar nilai 30 siswa. Tanpa list: 30 variabel terpisah. Dengan list: 1 variabel!" | 5 menit |

### Inti (65 menit)

#### Memahami (20 menit)

**1. List = Array di Python (7 menit)**

| Konsep (Pert 1) | Python List |
|---|---|
| Array indeks 0 | `list[0]` |
| Simpan banyak data | `nilai = [85, 90, 78]` |
| Array 2D | `matriks = [[1,2],[3,4]]` |

```python
# Membuat list
buah = ["apel", "mangga", "jeruk"]
angka = [5, 3, 8, 1, 6]
campur = ["Andi", 16, True, 85.5]

# Akses indeks
print(buah[0])      # apel
print(angka[-1])    # 6 (indeks negatif = dari belakang)
print(buah[1:3])    # slicing: ["mangga", "jeruk"]

# Method list
angka.append(10)    # tambah di akhir → [5,3,8,1,6,10]
angka.sort()        # urutkan → [1,3,5,6,8,10]
angka.remove(3)     # hapus 3
```

**2. Fungsi (def) — Modularisasi (7 menit)**

```python
def nama_fungsi(parameter):
    # kode
    return nilai
```

| Konsep | Contoh |
|---|---|
| Tanpa parameter | `def sapa():` |
| Dengan parameter | `def sapa(nama):` |
| Dengan return | `def luas(p, l): return p*l` |
| Default param | `def sapa(nama="Andi"):` |

**3. Translasi Array → List (6 menit)**
Tunjukkan tabel lengkap di Bahan Ajar.

#### Mengaplikasi (35 menit)

**4. Aktivitas 1 — List Dasar (10 menit) — Individu**
   - Buat list nilai [85, 90, 78, 92, 88]
   - Akses indeks ke-2, indeks terakhir, slicing 2-4
   - Tambah nilai 95 dengan append
   - Urutkan dengan sort
   - Cari rata-rata dengan loop FOR

**5. Aktivitas 2 — Fungsi (10 menit) — Berpasangan**
   - Buat fungsi `sapa(nama)` → "Halo, {nama}!"
   - Buat fungsi `luas_segitiga(alas, tinggi)`
   - Buat fungsi `faktorial(n)`
   - Buat fungsi `cek_prima(n)` → True/False

**6. Aktivitas 3 — Studi Kasus: Data Nilai Siswa (15 menit) — Kelompok**
   - Program pengelolaan nilai:
     - Input jumlah siswa
     - Input nama dan nilai per siswa
     - Simpan di list of lists: `[[nama1, nilai1], [nama2, nilai2], ...]`
     - Hitung rata-rata kelas
     - Tampilkan siswa dengan nilai tertinggi
     - Tampilkan siswa yang lulus (≥75) dan remidi (<75)

#### Merefleksi (5 menit)

**7. Refleksi (5 menit)**

### Penutup (15 menit)

| Kegiatan | Waktu |
|---|---|
| 1. Rangkuman | 3 menit |
| 2. Preview: "Pert 15: Proyek Akhir & Review PAS — Membuat program Python lengkap!" | 3 menit |
| 3. Tugas rumah: Selesaikan program data nilai siswa + tambah fitur urutkan nilai | 5 menit |
| 4. Doa & salam | 4 menit |

---

## Asesmen

| Kriteria | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| List (akses, method) | Tidak bisa | Sebagian | Benar | Benar + eksplorasi |
| Fungsi (def, return) | Tidak bisa | Struktur salah | Benar | Benar + parameter |
| Studi kasus data nilai | Tidak selesai | Sebagian fitur | Lengkap | Lengkap + rapi + fitur tambahan |

---

**MGMP Informatika SMAN 6 Cimahi**
