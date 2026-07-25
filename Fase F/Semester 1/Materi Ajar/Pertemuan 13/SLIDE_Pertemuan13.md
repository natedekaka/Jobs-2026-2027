---
marp: true
theme: uncover
class: invert
---

# PERTEMUAN 13 — FASE F
## Algoritma Dijkstra
### Informatika – Fase F / Kelas XI
#### SMA Negeri 6 Cimahi

---

## Review — Strategi Algoritmik

| Pert | Topik |
|---|---|
| 8 | Greedy |
| 9 | D&C |
| 10 | Backtracking |
| 11 | Latihan Soal |
| 12 | Graph, BFS, DFS |

> Hari ini: **Dijkstra** — penutup Strategi Algoritmik!

---

## Apersepsi

"Google Maps — masukkan asal & tujuan. Hitungan detik dapat rute tercepat!"

> Itu **Algoritma Dijkstra**!

---

# TUJUAN PEMBELAJARAN

1. ✅ Masalah jalur terpendek
2. ✅ Langkah Dijkstra
3. ✅ Praktik Dijkstra manual
4. ✅ Penerapan nyata

---

## Masalah Jalur Terpendek

**Input:** Graph berbobot positif
**Output:** Jarak terpendek dari start ke semua verteks

```
A ──5── B ──3── C
│               │
2               1
│               │
D ──6── E ──2── F
```

> Dari A ke F — lewat mana?

---

## Syarat Dijkstra

| ✅ Boleh | ❌ Tidak Boleh |
|---|---|
| Bobot positif | Bobot negatif |
| Graph berarah | — |
| Graph tak berarah | — |

> Dijkstra hanya bekerja untuk **bobot positif**!

---

## 3 Konsep Utama

| Konsep | Arti |
|---|---|
| **Jarak sementara** | Jarak terbaik yang diketahui (bisa berubah) |
| **Relaxation** | Perbarui jarak jika ditemukan jalur lebih pendek |
| **Final** | Jarak sudah pasti — tidak berubah lagi |

---

## Langkah Dijkstra

```
1. jarak[start] = 0, lainnya = ∞
2. Ulangi sampai semua final:
   a. Pilih verteks v dengan jarak terkecil yg belum final
   b. Finalkan v
   c. Relaxation: perbarui jarak tetangga
```

---

## Relaxation — Step by Step

```
A(0) ──4──→ B(∞)
jarak_baru = 0 + 4 = 4 < ∞ → B = 4 ✅

B(4) ──1──→ C(∞)
jarak_baru = 4 + 1 = 5 < ∞ → C = 5 ✅

C(5) ──3──→ E(10)
jarak_baru = 5 + 3 = 8 < 10 → E = 8 ✅ (lebih pendek!)
```

> Relaxation = "Bukankah ini lebih pendek?"

---

## Contoh Lengkap

```
   A ──4── B ──1── C
   │       │       │
   2       5       3
   │       │       │
   D ──8── E ──6── F
```

| Iter | Pilih | A | B | C | D | E | F |
|---|---|---|---|---|---|---|---|
| 1 | A | 0* | 4 | ∞ | 2 | ∞ | ∞ |
| 2 | D | | 4 | ∞ | 2* | 10 | ∞ |
| 3 | B | | 4* | 5 | | 9 | ∞ |
| 4 | C | | | 5* | | 8 | 8 |
| 5 | E | | | | | 8* | 8 |

---

## Pseudocode Dijkstra

```
PROCEDURE Dijkstra(graph, start)
    jarak[1..n] ← ∞
    final[1..n] ← FALSE
    jarak[start] ← 0
    
    FOR i ← 1 TO n DO
        v ← verteks dg jarak minimum & belum final
        final[v] ← TRUE
        
        FOR tetangga u dari v DO
            IF NOT final[u] THEN
                jarak_baru ← jarak[v] + bobot(v,u)
                IF jarak_baru < jarak[u] THEN
                    jarak[u] ← jarak_baru
                ENDIF
            ENDIF
        ENDFOR
    ENDFOR
END
```

---

## Dijkstra = Greedy!

| Greedy | Dijkstra |
|---|---|
| Ambil pilihan terbaik saat ini | Pilih verteks jarak terkecil saat ini |
| Optimal substructure | Jarak sub-jalur = jarak terpendek sementara |
| Irrevocable | Sekali final, tidak berubah |

> **Dijkstra adalah algoritma Greedy pada graph!**

---

## Aktivitas 1: Dijkstra Manual

### 30 menit — Individu

```
   A ──5── B ──3── C
   │               │
   2               1
   │               │
   D ──6── E ──2── F
```

Dari A → semua verteks. Isi tabel!

> A → F lewat mana?

---

## Aktivitas 2: Dijkstra + Graph 2

### 30 menit — Berpasangan

```
Sekolah ──3── Toko ──5── Pasar
   │                  │
   4                  6
   │                  │
Rumah ──2── Klinik ──1── Kantor
```

Dari Sekolah → Rumah. Berapa jarak terpendek?

---

## Aktivitas 3: Peta Sekolah

### 20 menit — Kelompok

Buat peta 4-5 tempat di sekitar sekolah!

1. Gambar graph
2. Tentukan bobot (jarak meter)
3. Jalankan Dijkstra
4. Presentasikan!

---

## Penerapan Dijkstra

| Aplikasi | Start | Bobot |
|---|---|---|
| Google Maps | Lokasi | Jarak/waktu |
| Routing internet | Router | Latency |
| GPS navigasi | Posisi | Jarak |
| Game pathfinding | Karakter | Waktu tempuh |

---

## Rangkuman

| Konsep | Inti |
|---|---|
| **Dijkstra** | Cari jalur terpendek — bobot positif |
| **Relaxation** | Perbarui jarak tetangga |
| **Final** | Jarak sudah pasti |
| **Greedy** | Pilih jarak terkecil saat ini |
| **Kompleksitas** | O(V²) / O((V+E) log V) |

---

## Materi Esensial Berikutnya

### Pengolahan Data Bervolume Besar (Big Data)
> Pert 14: Konsep Big Data & Data Mining

---

## Tugas Rumah

Cari jalur terpendek dari rumah ke sekolah pakai Dijkstra!

> Gambar graph + tabel + jalur

---

# Terima Kasih

### MGMP Informatika SMAN 6 Cimahi

> "Dijkstra: selalu ambil yang terpendek untuk sampai ke tujuan."
