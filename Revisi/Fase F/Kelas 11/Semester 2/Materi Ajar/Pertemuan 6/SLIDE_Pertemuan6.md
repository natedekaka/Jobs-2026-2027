---
marp: true
theme: uncover
class: invert
---

# PERTEMUAN 6 — FASE F (S2)
## List & Tuple
*Mengacu pada Panduan Mapel 2025; INFORMATIKA Fase D-F — pendekatan Pembelajaran Mendalam (Memahami → Mengaplikasi → Merefleksi)*
### Informatika – Kelas XI

---

## Tujuan

- Membuat dan mengolah list
- Mengenal tuple
- Membedakan list dan tuple

---

## List

Kumpulan data dalam `[]`, **bisa diubah**

```python
buah = ["apel", "mangga", "jeruk"]
buah.append("pisang")
buah.remove("mangga")
```

✅ append, insert, remove, sort

---

## Akses List

```python
buah[0]      # apel
buah[-1]     # elemen terakhir
len(buah)    # jumlah elemen
```

---

## Tuple

Kumpulan data dalam `()`, **tidak bisa diubah**

```python
warna = ("merah", "kuning", "hijau")
warna[0] = "biru"  # ❌ Error!
```

✅ Untuk data tetap (konstanta)

---

## Loop pada List

```python
for b in buah:
    print(b)
```

---

## Aktivitas 1 — Daftar Belanja

Buat list, tambah 3 item, cetak

---

## Aktivitas 2 — Nilai

Max, min, rata-rata dari list nilai

---

## Aktivitas 3 — Tuple

Buat tuple lampu lalin, coba ubah

---

## Refleksi

- Bedanya list dan tuple?
- Kapan pakai list?
- Skala 1–10?

---

# Terima Kasih

**MGMP Informatika SMAN 6 Cimahi — Fase F (Kelas XI) Semester 2**
