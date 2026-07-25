---
marp: true
theme: uncover
class: invert
---

# PERTEMUAN 5 — FASE F (S2)
## FOR & WHILE — Perulangan
*Mengacu pada Panduan Mapel 2025; INFORMATIKA Fase D-F — pendekatan Pembelajaran Mendalam (Memahami → Mengaplikasi → Merefleksi)*
### Informatika – Kelas XI

---

## Tujuan

- Menggunakan FOR loop
- Menggunakan WHILE loop
- Memahami break dan continue

---

## FOR Loop

**Diketahui jumlah ulangan**

```python
for i in range(5):      # 0-4
    print(i)

for i in range(1, 6):   # 1-5
    print(i)
```

---

## WHILE Loop

**Tidak diketahui jumlah ulangan**

```python
i = 1
while i <= 5:
    print(i)
    i += 1
```

Berhenti saat kondisi False

---

## break & continue

```python
for i in range(10):
    if i == 5: break     # berhenti di 5
    print(i)

for i in range(5):
    if i == 2: continue  # loncat 2
    print(i)             # 0 1 3 4
```

---

## Aktivitas 1 — FOR (Deret)

1–20, genap 2–20, mundur 10–1

---

## Aktivitas 2 — WHILE (Tebak Angka)

Tebak 1–10, beri petunjuk!

---

## Aktivitas 3 — break & continue

Cetak 1–10, skip 5, berhenti di 8

---

## Refleksi

- Kapan pakai FOR? Kapan WHILE?
- Skala 1–10?

---

# Terima Kasih

**MGMP Informatika SMAN 6 Cimahi — Fase F (Kelas XI) Semester 2**
