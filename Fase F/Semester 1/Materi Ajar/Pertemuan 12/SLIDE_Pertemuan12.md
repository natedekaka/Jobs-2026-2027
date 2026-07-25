---
marp: true
theme: uncover
class: invert
---

# PERTEMUAN 12 — FASE F
## Graph, BFS & DFS
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

> Hari ini: **Graph** — struktur data yang ada di mana-mana!

---

## Apersepsi

"Facebook tahu kalian punya teman yang sama. Google Maps tahu rute terpendek. **Bagaimana caranya?** "

> Jawaban: **Graph!**

---

# TUJUAN PEMBELAJARAN

1. ✅ Struktur Graph (V + E)
2. ✅ Jenis Graph
3. ✅ BFS — Breadth-First Search
4. ✅ DFS — Depth-First Search

---

## Apa itu Graph?

**G = (V, E)**
- **V** = Vertex (simpul)
- **E** = Edge (sisi/hubungan)

```
      Andi
     /    \
  Budi — Citra
    |       |
  Dewi — Eka
```

| Istilah | Arti |
|---|---|
| Vertex | Akun (Andi, Budi, ...) |
| Edge | Pertemanan |
| Derajat Andi | 2 (Budi & Citra) |

---

## Jenis Graph

| Jenis | Ilustrasi | Contoh |
|---|---|---|
| **Tak berarah** | A — B | Facebook |
| **Berarah** | A → B | Twitter |
| **Berbobot** | A ─5─ B | Google Maps |

---

## Representasi Graph

### Adjacency Matrix
```
   A B C D
A [0 1 1 0]
B [1 0 1 0]
C [1 1 0 1]
D [0 0 1 0]
```

### Adjacency List
```
A: [B, C]
B: [A, C]
C: [A, B, D]
D: [C]
```

---

## BFS — Breadth-First Search

**Queue (FIFO)** — Level by level!

```
A — B — C — D
|         |
E — F — G
```

BFS dari A:
```
Queue: [A] → [B, E] → [E, C] → [C, F] → [F, G] → [G]
Kunjungan: A → B → E → C → F → G
```

> **BFS = tetangga dulu, baru tetangganya tetangga**

---

## BFS — Pseudocode

```
PROCEDURE BFS(graph, start)
    queue ← [start]
    
    WHILE queue tidak kosong DO
        v ← queue.hapusDepan()
        IF v belum dikunjungi THEN
            tandai v dikunjungi
            FOR tetangga u dari v DO
                IF u belum dikunjungi THEN
                    queue.tambah(u)
                ENDIF
            ENDFOR
        ENDIF
    ENDWHILE
END
```

---

## DFS — Depth-First Search

**Stack (LIFO)** — Masuk terdalam dulu!

```
A — B — C — D
|         |
E — F — G
```

DFS dari A:
```
Stack: [A] → [B, E] → [B, F] → [B, G] → ... → [B] → [C]
Kunjungan: A → E → F → G → B → C
```

> **DFS = jalan terus sampai ujung, baru mundur**

---

## DFS — Pseudocode

```
PROCEDURE DFS(graph, start)
    stack ← [start]
    
    WHILE stack tidak kosong DO
        v ← stack.hapusAtas()
        IF v belum dikunjungi THEN
            tandai v dikunjungi
            FOR tetangga u dari v DO
                IF u belum dikunjungi THEN
                    stack.tambah(u)
                ENDIF
            ENDFOR
        ENDIF
    ENDWHILE
END
```

---

## BFS vs DFS

| Aspek | BFS | DFS |
|---|---|---|
| Struktur data | Queue | Stack |
| Cara | Level by level | Kedalaman dulu |
| Jalur terpendek? | ✅ Ya | ❌ |
| Memori | O(V) — 1 level | O(V) — 1 path |
| Contoh | Maps, Facebook | Maze, Puzzle |

---

## Aktivitas 1: Representasi Graph

### 20 menit — Individu

```
Andi — Budi — Citra
  |             |
Dewi — Eka — Fani
```

Buat:
- ✅ Adjacency Matrix
- ✅ Adjacency List
- ✅ Derajat setiap verteks

---

## Aktivitas 2: BFS

### 25 menit — Berpasangan

Graph yang sama. BFS dari **Andi**!

Isi tabel: Langkah, Queue, Kunjungan

> Urutan BFS: ?

---

## Aktivitas 3: DFS

### 25 menit — Berpasangan

Graph yang sama. DFS dari **Andi**!

Isi tabel: Langkah, Stack, Kunjungan

> Urutan DFS: ?

---

## Aktivitas 4: Graph Nyata

### 25 menit — Kelompok

Cari contoh graph di kehidupan sehari-hari!

- Gambar graph-nya
- Jenis graph
- Bagaimana BFS/DFS bisa dipakai?

> Presentasi!

---

## Rangkuman

| Konsep | Inti |
|---|---|
| **Graph** | V + E |
| **Tak berarah** | Dua arah |
| **BFS** | Queue — level — terpendek |
| **DFS** | Stack — depth — eksplorasi |
| **Matriks** | O(1) cek, O(V²) memori |
| **List** | Hemat memori |

---

## Tugas Rumah

Cari 1 contoh graph di dunia nyata!

> Gambar, jenis, dan bagaimana BFS/DFS diterapkan

---

## Pertemuan Depan

### Algoritma Dijkstra
> Mencari jalur terpendek di graph berbobot!

---

# Terima Kasih

### MGMP Informatika SMAN 6 Cimahi

> "Graph: semua terhubung — BFS menyapu, DFS menyelam."
