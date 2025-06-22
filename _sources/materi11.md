---
title: Singular Value Decomposition (SVD) - Penjelasan Lengkap dan Mudah Dipahami

---

# Singular Value Decomposition (SVD) - 

## Apa itu SVD?

Singular Value Decomposition (SVD) adalah metode dalam aljabar linear untuk memecah sebuah matriks menjadi tiga matriks lain yang lebih sederhana dan mudah dianalisis:

$$
A = U \Sigma V^T
$$

### Komponen:

* **A**: Matriks asli berukuran $m \times n$
* **U**: Matriks ortonormal berukuran $m \times m$
* **\Sigma**: Matriks diagonal $m \times n$ berisi nilai-nilai singular (positif)
* **V^T**: Transpose dari matriks ortonormal $V \in \mathbb{R}^{n \times n}$

## Langkah-langkah Menghitung SVD (Contoh Lengkap)

Diberikan:

$$
A = \begin{bmatrix}
4 & 1 \\
2 & 7 \\
1 & 4
\end{bmatrix}
$$

### Langkah 1: Hitung Matriks $A^T A$

Langkah pertama adalah menghitung hasil perkalian transpose dari A dengan A itu sendiri.

$$
A^T = \begin{bmatrix} 4 & 2 & 1 \\ 1 & 7 & 4 \end{bmatrix}
$$

Kemudian:

$$
A^T A = A^T \cdot A =
\begin{bmatrix}
4\cdot4 + 2\cdot2 + 1\cdot1 & 4\cdot1 + 2\cdot7 + 1\cdot4 \\
4\cdot1 + 2\cdot7 + 1\cdot4 & 1\cdot1 + 7\cdot7 + 4\cdot4
\end{bmatrix} =
\begin{bmatrix}
21 & 25 \\
25 & 66
\end{bmatrix}
$$

### Langkah 2: Hitung Eigenvalue dari $A^T A$

Gunakan determinan untuk mencari eigenvalue $\lambda$:

$$
\det(A^T A - \lambda I) = 0
$$

Susun persamaan determinan:

$$
\left|\begin{array}{cc} 21 - \lambda & 25 \\ 25 & 66 - \lambda \end{array}\right| = 0
$$

Hitung determinannya:

$$
(21 - \lambda)(66 - \lambda) - 25^2 = 0
$$

Kembangkan:

$$
1386 - 87\lambda + \lambda^2 - 625 = 0 \Rightarrow \lambda^2 - 87\lambda + 761 = 0
$$

Gunakan rumus kuadrat:

$$
\lambda = \frac{87 \pm \sqrt{87^2 - 4\cdot1\cdot761}}{2} = \frac{87 \pm \sqrt{4525}}{2}
$$

$$
\Rightarrow \lambda_1 \approx 77.12, \quad \lambda_2 \approx 9.88
$$

### Langkah 3: Hitung Eigenvector dari $A^T A$

Untuk $\lambda_1 = 77.12$, substitusi ke:

$$
(A^T A - \lambda I) v = 0
$$

$$
\begin{bmatrix}
21 - 77.12 & 25 \\
25 & 66 - 77.12
\end{bmatrix} = \begin{bmatrix} -56.12 & 25 \\ 25 & -11.12 \end{bmatrix}
$$

Misalkan $v = \begin{bmatrix} x \\ y \end{bmatrix}$, maka:

$$
-56.12x + 25y = 0 \Rightarrow y = \frac{56.12}{25}x \approx 2.2448x
$$

Ambil x = 1:

$$
v_1 = \begin{bmatrix} 1 \\ 2.2448 \end{bmatrix}, \quad \text{Normalisasi: } v_1 = \frac{1}{\sqrt{1^2 + (2.2448)^2}} \begin{bmatrix} 1 \\ 2.2448 \end{bmatrix}
$$

### Langkah 4: Hitung Nilai Singular ($\sigma$)

Singular values diperoleh dari akar kuadrat eigenvalue:

$$
\sigma_1 = \sqrt{77.12} \approx 8.78, \quad \sigma_2 = \sqrt{9.88} \approx 3.14
$$

### Langkah 5: Bentuk Matriks $\Sigma$

Karena matriks A berukuran 3x2, maka $\Sigma$ berukuran 3x2 dengan elemen diagonal:

$$
\Sigma = \begin{bmatrix}
8.78 & 0 \\
0 & 3.14 \\
0 & 0
\end{bmatrix}
$$

### Langkah 6: Hitung Matriks $V$

Gabungkan eigenvector $v_1$ dan $v_2$ menjadi matriks $V$:

$$
V = [v_1 \; v_2], \quad V^T = \text{transpose-nya}
$$

### Langkah 7: Hitung Matriks $U$ Menggunakan Dot Product

Gunakan rumus:

$$
u_i = \frac{1}{\sigma_i} A v_i
$$

Contoh perhitungan dot product:

$$
A v_1 = \begin{bmatrix} 4 & 1 \\ 2 & 7 \\ 1 & 4 \end{bmatrix} \cdot \begin{bmatrix} 1 \\ 2.2448 \end{bmatrix} = \begin{bmatrix} 4 + 2.2448 \\ 2 + 15.7136 \\ 1 + 8.9792 \end{bmatrix} = \begin{bmatrix} 6.2448 \\ 17.7136 \\ 9.9792 \end{bmatrix}
$$

Kemudian:

$$
u_1 = \frac{1}{8.78} \begin{bmatrix} 6.2448 \\ 17.7136 \\ 9.9792 \end{bmatrix}
$$

Lakukan hal serupa untuk $v_2$ agar mendapat $u_2$. Tambahkan $u_3$ agar membentuk matriks $U$ ukuran 3x3, misalnya menggunakan metode ortonormalisasi Gram-Schmidt.

## Hasil Akhir:

$$
A = U \Sigma V^T
$$

Dengan:

* $U$: Matriks ortonormal dari hasil $u_1, u_2, u_3$
* $\Sigma$: Matriks diagonal dengan nilai singular
* $V^T$: Transpose dari vektor eigen yang dinormalisasi

## Kegunaan SVD:

* Kompresi data & gambar
* Reduksi dimensi (PCA)
* Sistem rekomendasi (Netflix, YouTube)
* Pengenalan pola dan machine learning
