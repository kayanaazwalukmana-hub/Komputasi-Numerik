# Algoritma Penyelesaian Persamaan Non Linear: Metode Bisection

## 1. Bentuk Persamaan
Mencari nilai x yang memenuhi f(x) = 0 dengan f berupa fungsi non linear.

Contoh yang dipakai: f(x) = x³ − 3x − 5

## 2. Metode yang Dipakai
Metode Bisection (bagi dua). Metode ini dipilih karena pasti konvergen selama f kontinu dan
bertanda berbeda di kedua ujung interval, serta langkahnya sederhana dan mudah dicek manual.

## 3. Input dan Output
- Input: fungsi f(x), batas kiri a, batas kanan b, toleransi ε, iterasi maksimum
- Output: akar hampiran x, nilai f(x), dan jumlah iterasi

## 4. Langkah-langkah
1. Mulai
2. Tentukan fungsi f(x), batas a dan b, toleransi ε, dan iterasi maksimum
3. Hitung f(a) dan f(b). Jika f(a) × f(b) ≥ 0, hentikan: akar tidak dijamin ada di interval ini
4. Ulangi untuk iterasi ke-1 sampai iterasi maksimum:
   a. Hitung titik tengah c = (a + b) / 2
   b. Hitung f(c)
   c. Jika |f(c)| < ε atau (b − a)/2 < ε, hentikan, c adalah akar hampiran
   d. Jika f(a) × f(c) < 0, akar ada di sisi kiri, maka b = c
   e. Jika tidak, akar ada di sisi kanan, maka a = c
5. Tampilkan akar hampiran c, nilai f(c), dan jumlah iterasi
6. Selesai

## 5. Contoh Singkat

Soal: f(x) = x³ − 3x − 5 pada interval [2, 3]

Pengecekan syarat:
- f(2) = 8 − 6 − 5 = −3 (negatif)
- f(3) = 27 − 9 − 5 = 13 (positif)
- Tanda berbeda, jadi ada akar di antara 2 dan 3

| Iterasi | a | b | c | f(c) | Keputusan |
|---|---|---|---|---|---|
| 1 | 2,000000 | 3,000000 | 2,500000 | 3,125000 | f(c) positif, b = c |
| 2 | 2,000000 | 2,500000 | 2,250000 | −0,359375 | f(c) negatif, a = c |
| 3 | 2,250000 | 2,500000 | 2,375000 | 1,271484 | f(c) positif, b = c |
| 4 | 2,250000 | 2,375000 | 2,312500 | 0,428955 | f(c) positif, b = c |
| 5 | 2,250000 | 2,312500 | 2,281250 | 0,028107 | f(c) positif, b = c |

Proses berlanjut sampai iterasi ke-17.

Hasil: akar hampiran x ≈ 2,279015 dengan f(x) ≈ −0,00005
