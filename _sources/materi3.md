---
title: 'Materi: Determinan Matriks'

---

# Materi: Determinan Matriks

Determinan adalah suatu nilai skalar yang dapat dihitung dari matriks persegi. Nilai determinan ini memiliki peran penting dalam berbagai aplikasi aljabar linier, seperti:

- Menentukan apakah suatu matriks invertibel (dapat diinverskan).
- Menghitung volume (atau luas) dalam transformasi linier.
- Menyelesaikan sistem persamaan linear (misalnya menggunakan aturan Cramer).

---

## 1. Definisi Determinan

### Matriks 2×2

Untuk matriks 2×2
$$
A = \begin{bmatrix} a & b \\ c & d \end{bmatrix},
$$
determinan \( \det(A) \) didefinisikan sebagai:
$$
\det(A) = ad - bc.
$$

### Matriks 3×3

Untuk matriks 3×3
$$
A = \begin{bmatrix}
a_{11} & a_{12} & a_{13} \\
a_{21} & a_{22} & a_{23} \\
a_{31} & a_{32} & a_{33}
\end{bmatrix},
$$
determinan dapat dihitung dengan menggunakan aturan Sarrus atau ekspansi kofaktor. Menggunakan ekspansi kofaktor pada baris pertama:
$$
\det(A) = a_{11} \cdot \det\begin{bmatrix} a_{22} & a_{23} \\ a_{32} & a_{33} \end{bmatrix}
- a_{12} \cdot \det\begin{bmatrix} a_{21} & a_{23} \\ a_{31} & a_{33} \end{bmatrix}
+ a_{13} \cdot \det\begin{bmatrix} a_{21} & a_{22} \\ a_{31} & a_{32} \end{bmatrix}.
$$

Contoh perhitungan untuk matriks 3×3:
Misalkan
$$
A = \begin{bmatrix}
1 & 2 & 3 \\
4 & 5 & 6 \\
7 & 8 & 9
\end{bmatrix}.
$$
Maka,
\[
\begin{aligned}
\det(A) &= 1 \cdot \det\begin{bmatrix} 5 & 6 \\ 8 & 9 \end{bmatrix} - 2 \cdot \det\begin{bmatrix} 4 & 6 \\ 7 & 9 \end{bmatrix} + 3 \cdot \det\begin{bmatrix} 4 & 5 \\ 7 & 8 \end{bmatrix} \\
&= 1 \cdot (5 \cdot 9 - 6 \cdot 8) - 2 \cdot (4 \cdot 9 - 6 \cdot 7) + 3 \cdot (4 \cdot 8 - 5 \cdot 7) \\
&= 1 \cdot (45 - 48) - 2 \cdot (36 - 42) + 3 \cdot (32 - 35) \\
&= 1 \cdot (-3) - 2 \cdot (-6) + 3 \cdot (-3) \\
&= -3 + 12 - 9 \\
&= 0.
\end{aligned}
\]
Nilai determinan \( \det(A) = 0 \) menandakan bahwa matriks tersebut tidak invertibel.

---

## 2. Sifat-Sifat Determinan

Beberapa sifat penting dari determinan yang perlu diketahui:

1. **Jika dua baris (atau kolom) suatu matriks identik, maka determinannya nol.**

2. **Pertukaran baris (atau kolom):**  
   Menukar dua baris (atau kolom) akan mengubah tanda determinan.
   $$
   \det(A') = -\det(A).
   $$

3. **Perkalian baris (atau kolom) dengan skalar:**  
   Jika salah satu baris dikalikan dengan skalar \( k \), maka determinan akan juga dikalikan dengan \( k \).
   $$
   \det(A') = k \cdot \det(A).
   $$

4. **Matriks Segitiga:**  
   Untuk matriks segitiga (atas atau bawah), determinan adalah hasil perkalian elemen-elemen diagonal utama.
   $$
   \det(A) = a_{11} \cdot a_{22} \cdot \ldots \cdot a_{nn}.
   $$

5. **Determinan dari Perkalian Matriks:**  
   Jika \( A \) dan \( B \) adalah matriks persegi berukuran sama, maka:
   $$
   \det(AB) = \det(A) \cdot \det(B).
   $$

6. **Matriks Invers:**  
   Jika \( A \) invertibel, maka:
   $$
   \det(A^{-1}) = \frac{1}{\det(A)}.
   $$

---

## 3. Contoh Perhitungan Determinan

### Contoh 1: Matriks 2×2
Misalkan
$$
A = \begin{bmatrix} 4 & 7 \\ 2 & 6 \end{bmatrix}.
$$
Maka,
$$
\det(A) = (4 \times 6) - (7 \times 2) = 24 - 14 = 10.
$$

### Contoh 2: Matriks 3×3
Misalkan
$$
B = \begin{bmatrix}
2 & 3 & 1 \\
0 & 4 & 5 \\
7 & 2 & 6
\end{bmatrix}.
$$
Kita hitung dengan ekspansi kofaktor pada baris pertama:
\[
\begin{aligned}
\det(B) &= 2 \cdot \det\begin{bmatrix} 4 & 5 \\ 2 & 6 \end{bmatrix} - 3 \cdot \det\begin{bmatrix} 0 & 5 \\ 7 & 6 \end{bmatrix} + 1 \cdot \det\begin{bmatrix} 0 & 4 \\ 7 & 2 \end{bmatrix} \\
&= 2 \cdot (4 \times 6 - 5 \times 2) - 3 \cdot (0 \times 6 - 5 \times 7) + 1 \cdot (0 \times 2 - 4 \times 7) \\
&= 2 \cdot (24 - 10) - 3 \cdot (0 - 35) + 1 \cdot (0 - 28) \\
&= 2 \cdot 14 - 3 \cdot (-35) - 28 \\
&= 28 + 105 - 28 \\
&= 105.
\end{aligned}
\]

---

## 4. Aplikasi Determinan

### a. Menentukan Apakah Matriks Invertibel
Sebuah matriks \( A \) adalah invertibel jika dan hanya jika \( \det(A) \neq 0 \).  
Contoh:  
Jika \( \det(A) = 10 \) (seperti pada contoh matriks 2×2 di atas), maka \( A \) invertibel.

### b. Menggunakan Determinan dalam Aturan Cramer
Aturan Cramer memungkinkan penyelesaian sistem persamaan linear \( n \) variabel jika \( \det(A) \neq 0 \).  
Misalkan sistem:
$$
A \times X = B,
$$
solusi untuk \( x_i \) diberikan oleh:
$$
x_i = \frac{\det(A_i)}{\det(A)},
$$
di mana \( A_i \) adalah matriks yang dibentuk dengan mengganti kolom ke-\( i \) dari \( A \) dengan vektor \( B \).

---

## 5. Penulisan di HackMD dengan LaTeX

Agar tampilan materi lebih rapi di HackMD, pastikan untuk menggunakan delimiter LaTeX. Contoh:
- Untuk tampilan mode block (display mode), gunakan `$$ ... $$` di awal dan akhir.
- Pastikan setiap baris matriks diakhiri dengan `\\` dan elemen dipisahkan dengan `&`.

Contoh penulisan matriks di HackMD:
```markdown
$$
\begin{bmatrix}
a & b \\
c & d
\end{bmatrix}
$$
