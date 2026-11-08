# Algoritma Penyelesaian SPL 3 Variabel

## 1. Bentuk Sistem
a11x + a12y + a13z = b1
a21x + a22y + a23z = b2
a31x + a32y + a33z = b3

## 2. Metode yang Dipakai
Eliminasi Gauss dengan pivoting parsial, untuk mengatasi kelemahan utama dari Eliminasi Gauss standar, yaitu ketidakstabilan numerik akibat pembagian dengan angka nol atau angka yang sangat kecil.

## 3. Input dan Output
- Input: koefisien a11..a33 dan konstanta b1..b3
- Output: nilai x, y, z

## 4. Langkah-langkah
1. Mulai
2. Baca koefisien dan konstanta, susun jadi matriks augmented 3x4
3. Untuk tiap kolom pivot (kolom 1 dan 2):
   a. Cari baris dengan elemen terbesar di kolom itu, tukar ke posisi pivot
   b. Kalau pivot = 0, hentikan: tidak ada solusi tunggal
   c. Nolkan elemen di bawah pivot dengan operasi baris
4. Hitung z dari baris ke-3
5. Hitung y dari baris ke-2 memakai z
6. Hitung x dari baris ke-1 memakai y dan z
7. Cetak x, y, z
8. Selesai

## 5. Contoh Singkat
Soal:
3x + 2y − z = 7
x − y + 2z = 5
2x + 3y + z = 12

Matriks augmented awal:
[ 3   2  −1 |  7 ]
[ 1  −1   2 |  5 ]
[ 2   3   1 | 12 ]

Kolom 1: pivot terbesar adalah 3 (baris 1), tidak perlu tukar baris.
- B2 ← B2 − (1/3)·B1  →  [ 0, −5/3, 7/3 | 8/3 ]
- B3 ← B3 − (2/3)·B1  →  [ 0,  5/3, 5/3 | 22/3 ]

Kolom 2: |−5/3| sama dengan |5/3|, baris 2 tetap jadi pivot.
- B3 ← B3 − (−1)·B2  →  [ 0, 0, 4 | 10 ]

Substitusi mundur:
- 4z = 10  →  z = 2,5
- −(5/3)y + (7/3)(2,5) = 8/3  →  y = 1,9
- 3x + 2(1,9) − 2,5 = 7  →  x = 1,9

Hasil: x = 1,9; y = 1,9; z = 2,5
