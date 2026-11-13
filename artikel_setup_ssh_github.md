# Cara Mudah Setup SSH Key untuk GitHub (Biar Gak Capek Login Terus)

Pernah merasa kesel setiap kali mau `git push` atau `git pull` harus masukkan username dan password GitHub? Tenang, ada solusinya: **SSH Key**. Sekali setup, selamanya nyaman. Berikut cara lengkapnya — plus beberapa jebakan yang sering bikin gagal di tengah jalan.

---

## Apa Itu SSH Key?

SSH Key adalah pasangan kunci kriptografi yang terdiri dari:

- **Private key** — disimpan rahasia di laptop kamu, di file `~/.ssh/id_ed25519`
- **Public key** — didaftarkan ke GitHub, di file `~/.ssh/id_ed25519.pub`

Saat kamu terhubung ke GitHub via SSH, sistem akan mencocokkan public key yang kamu daftarkan dengan private key di laptop. Cocok? Langsung masuk, tanpa password.

---

## Langkah 1: Cek SSH Key yang Sudah Ada

```bash
ls -la ~/.ssh/
```

Kalau muncul `id_ed25519` dan `id_ed25519.pub`, berarti kamu **sudah punya key** — jangan generate ulang, cukup lanjut ke **Langkah 4** (dan **Langkah 3** kalau key kamu pakai passphrase).

Kalau folder-nya kosong atau muncul error `No such file or directory`, lanjut ke **Langkah 2**.

---

## Langkah 2: Generate SSH Key Baru

```bash
ssh-keygen -t ed25519 -C "emailkamu@example.com"
```

Ganti `emailkamu@example.com` dengan email yang terdaftar di GitHub.

Nanti bakal muncul pertanyaan:

```
Enter file in which to save the key (/home/user/.ssh/id_ed25519):
```

**Tekan Enter saja** untuk pakai path default.

> **Jebakan:** kalau soal ini muncul, jangan ketik apa-apa. Kalau tidak sengaja kepotong nempel string aneh (misalnya hasil salin dari password manager), key kamu akan gagal disimpan dengan pesan `Saving key ... failed`. Kalau sudah terlanjur, hapus file salahnya, ulangi, dan **kasih Enter kosong**.

Setelah itu muncul:

```
Enter passphrase (empty for no passphrase):
```

Ini opsional. Kalau pengen praktis, **Enter** saja (kosongkan). Kalau khawatir laptop hilang, isi passwordnya — tapi lihat **Langkah 3** dulu, karena ada konsekuensinya.

---

## Langkah 3: Supaya Gak Ditanya Passphrase Tiap Push

Kalau di Langkah 2 kamu **mengisi passphrase**, setiap kali `git push` SSH akan menanyakan password itu lagi. Supaya gak repot, daftarkan key ke `ssh-agent`:

```bash
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_ed25519
```

Masalahnya: **setiap restart, `ssh-agent` kosong lagi** dan key harus di-`add` ulang. Supaya otomatis, tambahkan baris ini ke `~/.ssh/config`:

```
Host github.com
    AddKeysToAgent yes
    IdentityFile ~/.ssh/id_ed25519
    IdentitiesOnly yes
```

Buka file config-nya dengan `nano ~/.ssh/config` (kalau belum ada, `nano` akan membuatnya otomatis).

Dengan konfigurasi ini, key otomatis Offer ke agent tiap dipakai — setelah reboot juga gak perlu `ssh-add` manual lagi.

Kalau key kamu **tidak pakai passphrase**, langkah ini boleh dilewati.

---

## Langkah 4: Copy Public Key

```bash
cat ~/.ssh/id_ed25519.pub
```

Akan muncul teks panjang seperti ini:

```
ssh-ed25519 AAAAC3NzaC1lZDI1NTE5AAAAI... emailkamu@example.com
```

**Copy seluruh teks tersebut**, dari `ssh-ed25519` sampai email. Jangan sampai ada baris baru di tengah.

---

## Langkah 5: Daftarkan Public Key ke GitHub

1. Buka [github.com/settings/ssh/new](https://github.com/settings/ssh/new)
2. Login kalau belum
3. Isi form:
   - **Title**: misalnya `Laptop Lenovo` atau `PC Rumah` (terserah)
   - **Key type**: pilih **Authentication Key**
   - **Key**: paste teks public key tadi
4. Klik tombol hijau **Add SSH key**

Selesai! GitHub sekarang kenal dengan laptop kamu.

---

## Langkah 6: Test Koneksi

```bash
ssh -T git@github.com
```

Kalau berhasil, akan muncul:

```
Hi natedekaka! You've successfully authenticated, but GitHub does not provide shell access.
```

Kalimat `does not provide shell access` **bukan error** — itu pesan normal, karena GitHub memang tidak menyediakan shell. Yang penting kalimat `successfully authenticated`.

Kalau yang muncul `Host key verification failed`, ikut Langkah 6a.

### Langkah 6a: Mengatasi `Host key verification failed`

Error ini muncul karena laptop kamu belum "kenal" GitHub, dan `ssh` menolak connection demi keamanan. Ada dua cara.

**Cara A — daftarkan manual, lalu verifikasi (disarankan):**

```bash
ssh-keyscan -t rsa,ecdsa,ed25519 github.com 2>/dev/null | ssh-keygen -lf -
```

Outputnya kira-kira begini:

```
256 SHA256:p2QAMXNIC1TJYWeIOttrVc98/R1BUFWu3/LiyKgUfQM github.com (ECDSA)
3072 SHA256:uNiVztksCsDhcc0u9e8BujQXVUpKZIDTMczCvj3tD2s github.com (RSA)
256 SHA256:+DiY3wvvV6TuJJhbpZisF/zLDA0zPMSvHdkr4UvCOqU github.com (Ed25519)
```

Cocokkan dengan fingerprint resmi di [docs.github.com](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/githubs-ssh-key-fingerprints). **Kalau sama persis**, baru daftarkan:

```bash
ssh-keyscan -t rsa,ecdsa,ed25519 github.com 2>/dev/null >> ~/.ssh/known_hosts
```

Kalau berbeda, **jangan daftarkan** — bisa berarti koneksi kamu dicegat.

> **Kenapa wajib pakai `-t rsa,ecdsa,ed25519`?** GitHub punya 3 tipe host key. Tanpa `-t`, `ssh-keyscan` cuma mengambil satu tipe secara acak, dan kalau yang kebetulan tidak didukung, `Host key verification failed` akan muncul lagi. Perintah di atas mengambil ketiganya sekaligus, sekali hajar.

**Cara B — pakai blok resmi dari GitHub:**

GitHub menyediakan blok `known_hosts` siap pakai di halaman dokumentasi di atas. Salin ketiga barisnya (untuk `github.com`, `ecdsa-sha2-nistp256`, dan `ssh-rsa`) ke `~/.ssh/known_hosts`.

---

## Langkah 7: Clone Repo Pakai SSH

Gunakan URL SSH, bukan HTTPS.

```bash
# ❌ HTTPS — tiap push bisa minta login
git clone https://github.com/natedekaka/nama-repo.git

# ✅ SSH — sekali setup, langsung jalan
git clone git@github.com:natedekaka/nama-repo.git
```

Gimana cara dapetin URL SSH-nya:

1. Buka repo di GitHub
2. Klik tombol hijau **Code**
3. Pilih tab **SSH**
4. Copy URL yang muncul

> **Jebakan:** `git@github.com:...` itu **URL**, bukan perintah. Kalau diketik langsung ke terminal tanpa `git clone` di depannya, bash akan mengira itu nama file dan muncul error `No such file or directory`.

---

## Tips & Catatan Penting

| Hal | Keterangan |
| --- | --- |
| **Private key jangan bocor** | File `id_ed25519` (tanpa `.pub`) jangan pernah dibagikan ke siapa pun |
| **Satu key untuk banyak repo** | Cukup daftarkan 1 public key, bisa dipakai untuk semua repo kamu |
| **Ganti laptop?** | Generate key baru dan daftarkan lagi |
| **Bisa pakai banyak key** | Kamu bisa menambahkan beberapa SSH key (misal untuk laptop kerja dan pribadi) |
| **Passphrase** | Kalau khawatir laptop hilang, tambahkan passphrase — tapi pastikan `AddKeysToAgent yes` sudah disetel di `~/.ssh/config` |
| **Backup `~/.ssh`** | Simpan salinan di tempat aman. Kalau hilang, harus daftar ulang ke GitHub |

---

## Troubleshooting

### `Permission denied (publickey)`

Penyebab: public key belum terdaftar di GitHub, atau private key tidak ditemukan.

Solusi:

1. Cek key yang terdaftar di GitHub: buka **Settings → SSH and GPG keys**, lalu bandingkan dengan `cat ~/.ssh/id_ed25519.pub`
2. Pastikan `~/.ssh/config` punya blok `Host github.com` seperti di Langkah 3
3. Kalau masih gagal, tambahkan `-v` untuk lihat detailnya:
   ```bash
   ssh -vT git@github.com
   ```
   Cari bagian `Offering public key` — kalau key yang ditawarkan bukan `id_ed25519`, berarti `IdentityFile` belum benar.

### `Host key verification failed`

Penyebab: GitHub belum dikenal di laptop kamu.

Solusi: ikuti **Langkah 6a** di atas.

### `Could not resolve hostname github.com`

Penyebab: koneksi internet bermasalah.

Solusi: cek koneksi dulu, lalu ulangi.

---

## Penutup

Dengan SSH key, workflow Git kamu jadi jauh lebih cepat dan nyaman. Cukup setup sekali dan kamu bisa push, pull, clone sepuasnya tanpa bolak-balik login.

Ada pertanyaan? Tulis di kolom komentar ya!

Happy coding!
