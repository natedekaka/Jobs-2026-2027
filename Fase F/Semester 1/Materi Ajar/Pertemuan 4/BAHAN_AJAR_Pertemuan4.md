# BAHAN AJAR – PERTEMUAN 4
## Implementasi & Development

| TP | BK, AP — Proses Rekayasa |
|---|---|

---

### A. TAHAP IMPLEMENTASI

**Implementasi (Development)** adalah tahap menerjemahkan **desain** (wireframe, mockup) menjadi **kode program** yang bisa dijalankan.

#### Analogi: Membangun Rumah

| Rumah | Aplikasi |
|---|---|
| Arsitek membuat denah | **Design** (Pert 3) |
| **Tukang membangun** | **Implementation** (Pert 4) |
| Material: bata, semen, cat | **Kode: HTML, CSS, Python, dll.** |
| Alat: palu, obeng | **Tools: VS Code, Git** |

---

### B. ARSITEKTUR APLIKASI — 3 LAYER

#### 1. Frontend (Client-side)

Yang dilihat dan diinteraksi pengguna.

| Komponen | Contoh Teknologi |
|---|---|
| **HTML** | Struktur halaman |
| **CSS** | Warna, font, tata letak |
| **JavaScript** | Interaktivitas (klik, animasi) |
| **Framework** | React, Vue, Bootstrap |

**Contoh:** Saat kalian buka Instagram — tampilan feed, story, tombol like itu semua **frontend**.

#### 2. Backend (Server-side)

Logika dan pemrosesan data. Pengguna tidak bisa melihat kode backend.

| Tugas Backend | Contoh Teknologi |
|---|---|
| Proses login | Python (Django/Flask), PHP (Laravel) |
| Simpan data | Node.js, Java (Spring) |
| Kirim notifikasi | Ruby on Rails |
| API (antar-aplikasi) | REST API, GraphQL |

**Contoh:** Saat kalian klik "Login" — backend memeriksa NISN dan password di database.

#### 3. Database

Tempat penyimpanan data.

| Jenis Database | Contoh |
|---|---|
| Relational (tabel) | MySQL, PostgreSQL |
| Non-relational (dokumen) | MongoDB, Firebase |

**Contoh:** Data siswa, nilai, presensi — semuanya tersimpan di database.

#### Diagram 3 Layer

```
┌──────────┐     ┌──────────┐     ┌──────────┐
│ FRONTEND │────▶│ BACKEND  │────▶│ DATABASE │
│ (Browser)│     │ (Server) │     │ (MySQL)  │
├──────────┤     ├──────────┤     ├──────────┤
│ Tampilan │     │ Proses   │     │ Simpan   │
│ HTML/CSS │     │ Python   │     │ Data     │
│ JS       │     │ Logika   │     │ Query    │
└──────────┘     └──────────┘     └──────────┘
```

---

### C. VERSION CONTROL — GIT

#### Masalah Tanpa Version Control

| Situasi | Masalah |
|---|---|
| "Tolong kirimkan file yang sudah diperbaiki" | "File mana yang terbaru?" |
| "Kode saya error, kemarin masih jalan!" | "Apa yang diubah?" |
| "Saya dan Budi edit file yang sama" | "Timpakan — hasilnya chaos!" |

#### Git = Solusinya

**Git** adalah sistem **version control** yang melacak setiap perubahan pada kode.

#### Konsep Dasar Git

| Konsep | Analogi | Penjelasan |
|---|---|---|
| **Repository** | Folder proyek | Tempat semua file dan riwayat perubahan |
| **Commit** | Save point | Snapshot kode pada waktu tertentu |
| **Branch** | Cabang | Jalur pengembangan terpisah (fitur baru) |
| **Merge** | Gabung | Menggabungkan branch |
| **Push** | Upload | Kirim kode ke server (GitHub) |
| **Pull** | Download | Ambil kode terbaru dari server |

#### Alur Kerja Git Sederhana

```
1. git init           → Buat repositori
2. git add .          → Stage file yang akan di-commit
3. git commit -m "pesan" → Simpan snapshot
4. git push           → Upload ke GitHub
5. git pull           → Ambil perubahan terbaru
```

#### Kenapa Git Penting?

| Tanpa Git | Dengan Git |
|---|---|
| ❌ File dengan nama `final_v2_revisi_akhir_benar.zip` | ✅ Riwayat commit jelas |
| ❌ "Siapa yang menghapus baris ini?" | ✅ `git blame` — lihat siapa & kapan |
| ❌ Takut mencoba fitur baru (takut rusak) | ✅ Branch — aman bereksperimen |

#### GitHub

**GitHub** adalah platform hosting untuk repositori Git. Di GitHub:
- Developer dari seluruh dunia berkolaborasi
- Open source project (kode bisa dilihat semua orang)
- Portofolio untuk programmer

---

### D. DARI WIREFRAME KE HTML

#### Wireframe (Pert 3)

```
┌────────────────────────┐
│ [LOGO APLIKASI]        │
│   Masuk ke Akun Anda   │
│ ┌──────────────────┐   │
│ │ NISN              │   │
│ └──────────────────┘   │
│ ┌──────────────────┐   │
│ │ Password          │   │
│ └──────────────────┘   │
│ ┌──────────────────┐   │
│ │     MASUK        │   │
│ └──────────────────┘   │
│ Lupa password?         │
│ Belum punya akun?      │
└────────────────────────┘
```

#### HTML dari Wireframe

```html
<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8">
  <title>Login — Aplikasi Sekolah</title>
  <style>
    body { font-family: Arial; background: #f0f2f5; 
           display: flex; justify-content: center; }
    .login-box { background: white; padding: 30px; 
                 border-radius: 8px; width: 350px; }
    input { width: 100%; padding: 10px; margin: 8px 0; }
    button { width: 100%; padding: 10px; 
             background: #1a5e9c; color: white; }
  </style>
</head>
<body>
  <div class="login-box">
    <h2 style="text-align: center;">Aplikasi Sekolah</h2>
    <p>Masuk ke Akun Anda</p>
    
    <label>NISN</label>
    <input type="text" placeholder="Masukkan NISN">
    
    <label>Password</label>
    <input type="password" placeholder="Masukkan password">
    
    <button>MASUK</button>
    
    <p style="text-align: center; margin-top: 15px;">
      <a href="#">Lupa password?</a><br>
      <a href="#">Belum punya akun?</a>
    </p>
  </div>
</body>
</html>
```

---

### E. RANGKUMAN

| Konsep | Inti |
|---|---|
| **Frontend** | Tampilan — HTML, CSS, JS |
| **Backend** | Logika — Python, PHP, Node.js |
| **Database** | Penyimpanan — MySQL, MongoDB |
| **Git** | Version control — lacak perubahan kode |
| **Commit** | Save point snapshot kode |
| **GitHub** | Hosting repositori Git |

---

**MGMP Informatika SMAN 6 Cimahi**
