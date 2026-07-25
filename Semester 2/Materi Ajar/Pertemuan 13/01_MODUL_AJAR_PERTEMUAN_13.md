# MODUL AJAR INFORMATIKA – FASE E (KELAS X)

| Komponen | Deskripsi |
|---|---|
| **Mata Pelajaran** | Informatika |
| **Fase / Kelas** | E / X |
| **Semester** | 2 (Genap) |
| **Pertemuan ke-** | 13 |
| **Alokasi Waktu** | 2 JP × 45 menit (90 menit) |
| **Tahun Pelajaran** | 2026/2027 |
| **Satuan Pendidikan** | SMA Negeri 6 Cimahi |

---

## Tujuan Pembelajaran

| TP | IKTP |
|---|---|
| **BK 1.4, BK 2.1** | 2.1.6 Menggunakan FOR dengan range() di Python |
| | 2.1.7 Menggunakan WHILE di Python |
| | 2.1.8 Menggunakan break dan continue |
| | 2.1.9 Mentranslasi pseudocode perulangan ke Python |
| | 2.1.10 Menyelesaikan studi kasus dengan perulangan Python |

---

## Langkah Pembelajaran

### Pembukaan (10 menit)

| Kegiatan | Waktu |
|---|---|
| 1. Salam, doa, cek kehadiran | 2 menit |
| 2. **Review**: "Pert 12 kita belajar Python dasar — variabel, input, output, IF. Sekarang kita tambah **perulangan**." | 3 menit |
| 3. **Apersepsi**: "Pert 10 kita belajar FOR dan WHILE di pseudocode. Hari ini kita **terjemahkan ke Python** — dan lihat langsung hasilnya!" | 5 menit |

### Inti (65 menit)

#### Memahami (20 menit)

**1. FOR di Python — range() (7 menit)**

| Pseudocode | Python |
|---|---|
| `FOR i ← 1 TO 5` | `for i in range(1, 6):` |
| `FOR i ← 0 TO 4` | `for i in range(5):` |
| `FOR i ← 2 TO 10 STEP 2` | `for i in range(2, 11, 2):` |
| `ENDFOR` | *(indentasi)* |

```python
for i in range(1, 6):
    print(i)            # 1 2 3 4 5

for i in range(5):
    print(i)            # 0 1 2 3 4

for i in range(2, 11, 2):
    print(i)            # 2 4 6 8 10
```

**2. WHILE di Python (5 menit)**

| Pseudocode | Python |
|---|---|
| `WHILE kondisi TRUE` | `while kondisi:` |
| `ENDWHILE` | *(indentasi)* |

```python
i = 1
while i <= 5:
    print(i)
    i += 1              # i = i + 1
```

**3. break dan continue (5 menit)**
- `break` → keluar dari perulangan
- `continue` → loncat ke iterasi berikutnya

```python
# break: berhenti jika x=0
while True:
    x = int(input("Angka (0=stop): "))
    if x == 0:
        break

# continue: skip angka genap
for i in range(1, 11):
    if i % 2 == 0:
        continue
    print(i)            # 1 3 5 7 9
```

**4. Translasi Pseudocode → Python (3 menit)**
Tunjukkan tabel translasi FOR dan WHILE.

#### Mengaplikasi (35 menit)

**5. Aktivitas 1 — FOR (10 menit) — Individu**
   - Cetak 1–10 dengan FOR
   - Cetak bilangan genap 2–20
   - Tabel perkalian 7
   - Jumlah 1+2+...+n

**6. Aktivitas 2 — WHILE (10 menit) — Berpasangan**
   - Input angka sampai 0 → jumlah & rata-rata
   - Tebak angka (rahasia: 7)
   - Cetak kelipatan 3 (3–30) dengan WHILE

**7. Aktivitas 3 — Studi Kasus (15 menit) — Kelompok**
   - **Faktorial**: n! = n×(n-1)×...×1
   - **Fibonacci**: cetak deret sampai suku ke-n
   - **Cek prima**: input n → output prima/bukan

#### Merefleksi (5 menit)

**8. Refleksi (5 menit)**

### Penutup (15 menit)

| Kegiatan | Waktu |
|---|---|
| 1. Rangkuman | 3 menit |
| 2. Preview: "Pert 14: Python — List & Fungsi" | 3 menit |
| 3. Tugas rumah: Program tebak angka (lengkap dengan counter tebakan) | 5 menit |
| 4. Doa & salam | 4 menit |

---

## Asesmen

| Kriteria | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| FOR + range() | Tidak bisa | Sebagian | Benar | Benar + step |
| WHILE | Tidak bisa | Sebagian | Benar | Benar + break |
| Studi kasus (faktorial/Fibonacci/prima) | 0 selesai | 1 selesai | 2 selesai | 3 selesai + rapi |

---

**MGMP Informatika SMAN 6 Cimahi**
