---
title: perkalian silang

---

#  Materi Ringkasan Perkalian Silang (Cross Product)

## 🔹 Pengertian Perkalian Silang
Perkalian silang adalah operasi antara dua **vektor dalam ruang tiga dimensi (3D)** yang menghasilkan vektor baru yang **tegak lurus** terhadap kedua vektor asal.

Jika diberikan:
\[
\vec{u} = \begin{bmatrix} u_1 \\ u_2 \\ u_3 \end{bmatrix}, \quad
\vec{v} = \begin{bmatrix} v_1 \\ v_2 \\ v_3 \end{bmatrix}
\]

Maka:
\[
\vec{u} \times \vec{v} =
\begin{bmatrix}
u_2 v_3 - u_3 v_2 \\
u_3 v_1 - u_1 v_3 \\
u_1 v_2 - u_2 v_1
\end{bmatrix}
\]

Vektor hasil ini **tegak lurus** terhadap \( \vec{u} \) dan \( \vec{v} \), dan panjangnya sama dengan **luas jajaran genjang** yang dibentuk oleh kedua vektor.

---

## 🔹 Luas Jajaran Genjang
Jika dua vektor \( \vec{u} \) dan \( \vec{v} \) membentuk sisi jajaran genjang, maka luasnya adalah:

\[
L = |\vec{u} \times \vec{v}|
\]

---

## 🔹 Luas Segitiga
Jika tiga titik \( A, B, C \) diberikan, maka:
1. Hitung dua vektor:  
\[
\vec{AB} = \vec{B} - \vec{A}, \quad \vec{AC} = \vec{C} - \vec{A}
\]

2. Hitung vektor silang \( \vec{AB} \times \vec{AC} \)

3. Panjang vektor silang adalah dua kali luas segitiga:
\[
\text{Luas segitiga} = \frac{1}{2} |\vec{AB} \times \vec{AC}|
\]

---

# Penyelesaian Soal

## Soal 1
Tentukan luas jajaran genjang dari:
\[
\vec{u} = \begin{bmatrix} 1 \\ 2 \end{bmatrix}, \quad
\vec{v} = \begin{bmatrix} 2 \\ 1 \end{bmatrix}
\]

Kita tambahkan koordinat z = 0 untuk membuatnya 3D:
\[
\vec{u} = (1, 2, 0), \quad \vec{v} = (2, 1, 0)
\]

Hitung:
\[
\vec{u} \times \vec{v} = 
\begin{vmatrix}
\mathbf{i} & \mathbf{j} & \mathbf{k} \\
1 & 2 & 0 \\
2 & 1 & 0
\end{vmatrix} = (0, 0, 1\cdot1 - 2\cdot2) = (0, 0, -3)
\]

Luas:
\[
L = |\vec{u} \times \vec{v}| = \sqrt{0^2 + 0^2 + (-3)^2} = 3
\]

 **Jawaban: 3**

---

## Soal 2
\[
\vec{u} = \begin{bmatrix} 2 \\ 0 \end{bmatrix}, \quad
\vec{v} = \begin{bmatrix} 0 \\ 3 \end{bmatrix}
\]

Tambahkan z = 0:
\[
\vec{u} = (2, 0, 0), \quad \vec{v} = (0, 3, 0)
\]

\[
\vec{u} \times \vec{v} = (0, 0, 2\cdot3 - 0\cdot0) = (0, 0, 6)
\]

\[
L = |\vec{u} \times \vec{v}| = 6
\]

 **Jawaban: 6**

---

## Soal 3
Titik: A = (0,0,0), B = (1,3,-1), C = (2,1,1)

Hitung vektor:
\[
\vec{AB} = (1-0, 3-0, -1-0) = (1, 3, -1) \\
\vec{AC} = (2-0, 1-0, 1-0) = (2, 1, 1)
\]

Cross product:
\[
\vec{AB} \times \vec{AC} = 
\begin{vmatrix}
\mathbf{i} & \mathbf{j} & \mathbf{k} \\
1 & 3 & -1 \\
2 & 1 & 1
\end{vmatrix} = (3\cdot1 - (-1)\cdot1, -((1\cdot1 - (-1)\cdot2)), 1\cdot1 - 3\cdot2) \\
= (4, -3, -5)
\]

\[
|\vec{AB} \times \vec{AC}| = \sqrt{4^2 + (-3)^2 + (-5)^2} = \sqrt{50}
\]

\[
\text{Luas segitiga} = \frac{1}{2} \sqrt{50} = \frac{5\sqrt{2}}{2}
\]

 **Jawaban: (5√2)/2**

---

## Soal 4
Titik: A = (5,2,-1), B = (3,6,2), C = (1,0,4)

\[
\vec{AB} = (3-5, 6-2, 2-(-1)) = (-2, 4, 3) \\
\vec{AC} = (1-5, 0-2, 4-(-1)) = (-4, -2, 5)
\]

Cross product:
\[
\vec{AB} \times \vec{AC} = 
\begin{vmatrix}
\mathbf{i} & \mathbf{j} & \mathbf{k} \\
-2 & 4 & 3 \\
-4 & -2 & 5
\end{vmatrix} = (26, -2, 20)
\]

Panjang:
\[
|\vec{AB} \times \vec{AC}| = \sqrt{26^2 + (-2)^2 + 20^2} = \sqrt{1080}
\]

\[
\text{Luas segitiga} = \frac{1}{2} \sqrt{1080} = 3\sqrt{30}
\]

**Jawaban: 3√30**
