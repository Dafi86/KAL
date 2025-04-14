---
title: Transformasi Matriks (Bab 5.1 dari *Elementary Linear Algebra*)
tags: [matematika, kalkulus, integral, hackmd]

---

# Transformasi Matriks (Bab 5.1 dari *Elementary Linear Algebra*)

## 1. Pengantar Transformasi
Transformasi adalah suatu **fungsi** yang memetakan vektor dari satu ruang vektor ke ruang vektor lain. Dalam aljabar linear, kita sering berhadapan dengan transformasi dari ruang vektor real berdimensi-n (ℝn) ke ruang vektor real berdimensi-m (ℝm), ditulis:

$$
T: \mathbb{R}^n \rightarrow \mathbb{R}^m
$$

Fungsi ini memetakan setiap vektor input $\mathbf{x} \in \mathbb{R}^n$ ke vektor output $T(\mathbf{x}) \in \mathbb{R}^m$.

## 2. Transformasi Linier
Transformasi \( T \) disebut **transformasi linier** jika memenuhi dua sifat utama:

- **Aditivitas**:
  
  $$
  T(\mathbf{u} + \mathbf{v}) = T(\mathbf{u}) + T(\mathbf{v})
  $$

- **Homogenitas**:
  
  $$
  T(c\mathbf{v}) = cT(\mathbf{v})
  $$

Jika suatu transformasi tidak memenuhi salah satu dari kedua sifat ini, maka transformasi tersebut bukan linier.

## 3. Transformasi Matriks
Transformasi linier dapat diwakili oleh **perkalian matriks**. Jika \( A \) adalah matriks berukuran \( m \times n \), maka kita dapat mendefinisikan transformasi \( T \) sebagai:

$$
T(\mathbf{x}) = A\mathbf{x}
$$

dengan $\mathbf{x} \in \mathbb{R}^n$, dan hasilnya adalah vektor di $\mathbb{R}^m$.

$$
A = \begin{bmatrix} 2 & 0 \\ 1 & 3 \end{bmatrix}, \quad 
\mathbf{x} = \begin{bmatrix} x_1 \\ x_2 \end{bmatrix}
$$

maka:

$$
T(\mathbf{x}) = A\mathbf{x} = \begin{bmatrix} 2x_1 \\ x_1 + 3x_2 \end{bmatrix}
$$

## 4. Interpretasi Geometris
Beberapa transformasi matriks di \( \mathbb{R}^2 \) memiliki interpretasi geometris:

Beberapa transformasi matriks di $\mathbb{R}^2$ memiliki interpretasi geometris sebagai berikut:

| Jenis Transformasi        | Matriks Representasi                         | Penjelasan                                     |
|---------------------------|----------------------------------------------|------------------------------------------------|
| Rotasi 90° CCW            | $\begin{bmatrix} 0 & -1 \\ 1 & 0 \end{bmatrix}$ | Memutar vektor 90° berlawanan arah jarum jam  |
| Refleksi terhadap sumbu x | $\begin{bmatrix} 1 & 0 \\ 0 & -1 \end{bmatrix}$ | Mencerminkan terhadap sumbu x                |
| Proyeksi ke sumbu x       | $\begin{bmatrix} 1 & 0 \\ 0 & 0 \end{bmatrix}$ | Menghapus komponen y dari vektor             |
| Skala (dikali 2)          | $\begin{bmatrix} 2 & 0 \\ 0 & 2 \end{bmatrix}$ | Memperbesar panjang vektor dua kali        |
    

## 5. Ciri-Ciri Transformasi Linier
Transformasi linier selalu:
- Memetakan nol ke nol: $T(\mathbf{0}) = \mathbf{0}$
- Menjaga kolinearitas (vektor tetap sebaris)
- Menjaga kombinasi linier dari vektor

## 6. Visualisasi Transformasi
Untuk memahami efek dari transformasi linier, grid Cartesian, bentuk dasar seperti segitiga, atau kotak sering digunakan. Transformasi seperti rotasi, refleksi, dan proyeksi memberikan efek visual yang dapat dikenali secara langsung.

## 7. Domain dan Range
Dalam $T(\mathbf{x}) = A\mathbf{x}$:
- **Domain** adalah $\mathbb{R}^n$ (jumlah kolom A)
- **Range** adalah subruang dari $\mathbb{R}^m$ yang dibentangkan oleh kolom-kolom A
## 8. Representasi dengan Basis Standar
Jika $A = [T(\mathbf{e}_1)\ T(\mathbf{e}_2)\ \dots\ T(\mathbf{e}_n)]$, maka setiap kolom dari A merupakan hasil transformasi dari basis standar $\mathbf{e}_i$.

### Contoh:

Jika:
$$
T(\mathbf{e}_1) = \begin{bmatrix} 2 \\ 1 \end{bmatrix}, \quad 
T(\mathbf{e}_2) = \begin{bmatrix} 0 \\ 3 \end{bmatrix}
$$

maka:
$$
A = \begin{bmatrix} 2 & 0 \\ 1 & 3 \end{bmatrix}
$$

## 9. Contoh Transformasi
- **Proyeksi ke sumbu x**:

  $$
  A = \begin{bmatrix} 1 & 0 \\ 0 & 0 \end{bmatrix}
  $$

- **Refleksi terhadap garis $y = x$**:

  $$
  A = \begin{bmatrix} 0 & 1 \\ 1 & 0 \end{bmatrix}
  $$

- **Rotasi 180°**:

  $$
  A = \begin{bmatrix} -1 & 0 \\ 0 & -1 \end{bmatrix}
  $$


## 10. Kesimpulan
Transformasi matriks adalah bentuk khusus dari transformasi linier yang dapat direpresentasikan sebagai perkalian antara matriks dan vektor. Mereka sangat penting dalam berbagai aplikasi matematika dan komputasi, termasuk grafik komputer, fisika, serta ilmu data dan rekayasa.

---

*Disarikan dari: Bab 5.1, halaman 225–238, buku "Elementary Linear Algebra" oleh Hartman, Fitzpatrick, Stitz & Zeager.*

---
**Penyelesaian Soal Transformasi Matriks (Soal 1, 2, 5, dan 6)**

---

**Soal 1**

Diberikan:
\[
A = \begin{bmatrix} 1 & -1 \\ 2 & 3 \end{bmatrix}, \quad
x = \begin{bmatrix} 1 \\ 1 \end{bmatrix}, \quad
y = \begin{bmatrix} -1 \\ 2 \end{bmatrix}
\]

Hitung hasil transformasi:
\[
A x = \begin{bmatrix} 1 & -1 \\ 2 & 3 \end{bmatrix} \begin{bmatrix} 1 \\ 1 \end{bmatrix} = \begin{bmatrix} 1 - 1 \\ 2 + 3 \end{bmatrix} = \begin{bmatrix} 0 \\ 5 \end{bmatrix}
\]
\[
A y = \begin{bmatrix} 1 & -1 \\ 2 & 3 \end{bmatrix} \begin{bmatrix} -1 \\ 2 \end{bmatrix} = \begin{bmatrix} -1 - 2 \\ -2 + 6 \end{bmatrix} = \begin{bmatrix} -3 \\ 4 \end{bmatrix}
\]

---

**Soal 2**

Diberikan:
\[
A = \begin{bmatrix} 2 & 0 \\ -1 & 3 \end{bmatrix}
\]

\[
A x = \begin{bmatrix} 2 & 0 \\ -1 & 3 \end{bmatrix} \begin{bmatrix} 1 \\ 1 \end{bmatrix} = \begin{bmatrix} 2 \\ -1 + 3 \end{bmatrix} = \begin{bmatrix} 2 \\ 2 \end{bmatrix}
\]
\[
A y = \begin{bmatrix} 2 & 0 \\ -1 & 3 \end{bmatrix} \begin{bmatrix} -1 \\ 2 \end{bmatrix} = \begin{bmatrix} -2 \\ 1 + 6 \end{bmatrix} = \begin{bmatrix} -2 \\ 7 \end{bmatrix}
\]

---

**Soal 5**

Unit square ditransformasikan menjadi segitiga memanjang:
- Titik (1, 0) menjadi (1, 2)
- Titik (0, 1) menjadi (1, 3)

Matriks transformasi:
\[
A = \begin{bmatrix} 1 & 1 \\ 2 & 3 \end{bmatrix}
\]

---

**Soal 6**

Unit square berubah ke bentuk yang bergeser dan memutar:
- Titik (1, 0) menjadi (1, 1)
- Titik (0, 1) menjadi (-1, 1)

Matriks transformasi:
\[
A = \begin{bmatrix} 1 & -1 \\ 1 & 1 \end{bmatrix}
\]














