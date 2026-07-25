# BAHAN AJAR – PERTEMUAN 13
## Algoritma Dijkstra

| TP | BK, AP — Strategi Algoritmik |
|---|---|

---

### A. MASALAH JALUR TERPENDEK

**Masalah**: Diberikan graph berbobot, cari jalur dengan total bobot terkecil dari satu verteks sumber ke semua verteks lainnya.

#### Analogi: Google Maps

| Google Maps | Dijkstra |
|---|---|
| Pilih kota asal | **Start** verteks |
| Pilih kota tujuan | **Target** verteks |
| Lihat jarak/waktu | **Bobot** edge |
| "Rute tercepat" | **Shortest path** |

#### Syarat Dijkstra
- ✅ Graph **berbobot positif** (tidak ada bobot negatif)
- ✅ Bisa graph berarah atau tak berarah
- ❌ **Tidak bisa** jika ada bobot negatif (gunakan Bellman-Ford)

---

### B. ALGORITMA DIJKSTRA

#### 3 Konsep Utama

| Konsep | Arti |
|---|---|
| **Jarak sementara** | Jarak terbaik yang diketahui sejauh ini (bisa berubah) |
| **Relaxation** | Memperbarui jarak tetangga jika ditemukan jalur lebih pendek |
| **Final** | Verteks yang sudah diproses — jaraknya sudah pasti (tidak berubah lagi) |

#### Langkah Dijkstra

```
1. Inisialisasi:
   - jarak[start] = 0
   - jarak[verteks lain] = ∞

2. Selama masih ada verteks yang belum final:
   a. Pilih verteks v dengan jarak terkecil yang belum final
   b. Tandai v sebagai final
   c. Untuk setiap tetangga u dari v:
      jarak_baru = jarak[v] + bobot(v,u)
      IF jarak_baru < jarak[u] THEN
          jarak[u] = jarak_baru  // relaxation!
      ENDIF
```

#### Pseudocode

```
PROCEDURE Dijkstra(graph, start)
    n ← jumlah verteks
    jarak[1..n] ← ∞
    final[1..n] ← FALSE
    jarak[start] ← 0
    
    FOR i ← 1 TO n DO
        // Pilih verteks dengan jarak terkecil yang belum final
        v ← verteks dengan jarak minimum dan final[v] = FALSE
        
        final[v] ← TRUE
        
        // Relaxation
        FOR each tetangga u dari v DO
            IF NOT final[u] THEN
                jarak_baru ← jarak[v] + bobot(v, u)
                IF jarak_baru < jarak[u] THEN
                    jarak[u] ← jarak_baru
                ENDIF
            ENDIF
        ENDFOR
    ENDFOR
    
    RETURN jarak[1..n]
END
```

---

### C. CONTOH LENGKAP

#### Graph

```
   A ──4── B ──1── C
   │       │       │
   2       5       3
   │       │       │
   D ──8── E ──6── F
```

Cari jarak terpendek dari **A** ke semua verteks.

#### Tabel Eksekusi

| Iter | Pilih | final | A | B | C | D | E | F |
|---|---|---|---|---|---|---|---|---|
| 0 | — | — | **0** | ∞ | ∞ | ∞ | ∞ | ∞ |
| 1 | **A** (0) | A | 0* | 4 | ∞ | 2 | ∞ | ∞ |
| 2 | **D** (2) | A,D | 0* | 4 | ∞ | 2* | 10 | ∞ |
| | | | | | | | (2+8) | |
| 3 | **B** (4) | A,D,B | 0* | 4* | 5 | 2* | 9 | ∞ |
| | | | | | (4+1) | | (4+5) | |
| 4 | **C** (5) | A,D,B,C | 0* | 4* | 5* | 2* | 8 | 8 |
| | | | | | | | (5+3) | (5+3) |
| 5 | **E** (8) | A,D,B,C,E | 0* | 4* | 5* | 2* | 8* | 8 |
| | | | | | | | | (8+6=14>8) |
| 6 | **F** (8) | A,D,B,C,E,F | 0* | 4* | 5* | 2* | 8* | 8* |

* = sudah final (tidak berubah lagi)

#### Hasil

| Verteks | Jarak dari A | Jalur |
|---|---|---|
| A | 0 | A |
| B | 4 | A → B |
| C | 5 | A → B → C |
| D | 2 | A → D |
| E | 8 | A → B → E atau A → B → C → E |
| F | 8 | A → B → C → F |

---

### D. VISUALISASI RELAXATION

#### Relaxation Step by Step

```
Step 1: Pilih A (jarak=0)
A(0) ──4──→ B(∞): jarak_baru = 0+4 = 4 < ∞ → B=4 ✅
A(0) ──2──→ D(∞): jarak_baru = 0+2 = 2 < ∞ → D=2 ✅

Step 2: Pilih D (jarak=2)
D(2) ──8──→ E(∞): jarak_baru = 2+8 = 10 < ∞ → E=10 ✅

Step 3: Pilih B (jarak=4)
B(4) ──1──→ C(∞): jarak_baru = 4+1 = 5 < ∞ → C=5 ✅
B(4) ──5──→ E(10): jarak_baru = 4+5 = 9 < 10 → E=9 ✅ (lebih pendek!)

Step 4: Pilih C (jarak=5)
C(5) ──3──→ E(9): jarak_baru = 5+3 = 8 < 9 → E=8 ✅ (lebih pendek!)
C(5) ──3──→ F(∞): jarak_baru = 5+3 = 8 < ∞ → F=8 ✅

Step 5: Pilih E (jarak=8)
E(8) ──6──→ F(8): jarak_baru = 8+6 = 14 > 8 → F tetap 8
```

---

### E. DIJKSTRA = GREEDY!

Dijkstra disebut **algoritma Greedy** karena:

| Karakteristik Greedy | Dijkstra |
|---|---|
| **Greedy Choice** | Ambil verteks dengan jarak terkecil saat ini |
| **Optimal Substructure** | Jarak terpendek ke suatu verteks terdiri dari jarak terpendek ke verteks sebelumnya |
| **Irrevocable** | Setelah verteks di-final-kan, jaraknya tidak berubah |

#### Kompleksitas

| Implementasi | Kompleksitas |
|---|---|
| Sederhana (tanpa heap) | O(V²) |
| Dengan priority queue (heap) | O((V+E) log V) |

---

### F. PENERAPAN DIJKSTRA

| Aplikasi | Graph | Bobot | Start |
|---|---|---|---|
| Google Maps | Jalan + persimpangan | Jarak/waktu | Lokasi sekarang |
| Internet routing (OSPF) | Router + kabel | Latency | Router pengirim |
| GPS navigasi | Jalan raya | Jarak | Posisi GPS |
| Game pathfinding | Peta game | Waktu tempuh | Karakter |
| Jaringan listrik | Gardu + kabel | Hambatan | Gardu induk |

---

### G. RANGKUMAN

| Konsep | Inti |
|---|---|
| **Dijkstra** | Cari jalur terpendek dari start ke semua verteks |
| **Syarat** | Bobot edge harus positif |
| **Relaxation** | Perbarui jarak jika ditemukan jalur lebih pendek |
| **Final** | Verteks sudah pasti jaraknya |
| **Greedy** | Ambil verteks dengan jarak terkecil saat ini |
| **Kompleksitas** | O(V²) sederhana, O((V+E) log V) dengan heap |
| **Contoh** | Google Maps, routing internet, GPS |

---

**MGMP Informatika SMAN 6 Cimahi**
