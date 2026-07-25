# KUNCI JAWABAN – PERTEMUAN 17 (S1)
## PAS — Ujian Praktik Excel
*Mengacu pada Panduan Mapel 2025; INFORMATIKA Fase D-F — pendekatan Pembelajaran Mendalam (Memahami → Mengaplikasi → Merefleksi)*


### 🧠 Memahami — Kunci Jawaban

### A. Kunci Soal 1
NIS format: =LEFT(B2,4)&"-"&RIGHT(B2,3)
Usia: =DATEDIF(D2,TODAY(),"Y")
Email: =LOWER(LEFT(C2,1))&"."&LOWER(MID(C2,FIND(" ",C2)+1,99))&"@sma6.sch.id"


### 🔧 Mengaplikasi — Kunci Jawaban

### B. Kunci Soal 2
Validasi NIS: =IF(LEN(B2)=7,"Valid","Tidak Valid")
Validasi Email: =IF(ISNUMBER(FIND("@",E2)),"Valid","Tidak Valid")
Validasi Usia: =IF(AND(F2>=0,F2<=100),"Valid","Tidak Valid")


### C. Kunci Soal 3
Jumlah: =COUNTA, Rata: =AVERAGE, Max: =MAX, Min: =MIN, Countif: =COUNTIF


### 🔍 Merefleksi — Pedoman Refleksi

- Jawaban refleksi disesuaikan dengan respon masing-masing siswa.
- Guru dapat mendiskusikan jawaban refleksi secara klasikal.

---
**MGMP Informatika SMAN 6 Cimahi — Fase F (Kelas XI) Semester 1**

### Tambahan
Kunci jawaban menyesuaikan aktivitas tambahan di LKPD.
