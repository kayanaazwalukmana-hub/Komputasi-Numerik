# Algoritma Penyelesaian SPL 3 Variabel

## 1. Bentuk Sistem
a11x + a12y + a13z = b1
a21x + a22y + a23z = b2
a31x + a32y + a33z = b3

## 2. Metode yang Dipakai
Eliminasi Gauss dengan pivoting parsial (tulis alasan lo milih metode ini, 1-2 kalimat).

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
(isi satu contoh angka sendiri beserta hasilnya)
