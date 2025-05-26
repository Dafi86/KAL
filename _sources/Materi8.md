---
title: "\ Eigenvalue dan Eigenvector: Definisi, Perhitungan, Ortonormalisasi (Contoh Lengkap)"

---

# 💡 Eigenvalue dan Eigenvector: Definisi, Perhitungan, Ortonormalisasi (Contoh Lengkap)

## 📘 Apa itu Eigenvalue dan Eigenvector?

Dalam aljabar linear, konsep **eigenvalue** dan **eigenvector** sangat penting karena sering muncul dalam berbagai bidang seperti:

- Fisika (vibrasi, mekanika kuantum)
- Ilmu komputer (machine learning, PCA)
- Rekayasa (analisis struktur, sistem dinamik)

### 🔹 Definisi

Misalkan \( A \) adalah **matriks persegi** berukuran \( n \times n \), dan \( \mathbf{v} \) adalah **vektor kolom tak nol** berukuran \( n \times 1 \). Jika ada suatu skalar \( \lambda \) sehingga:

\[
A\mathbf{v} = \lambda \mathbf{v}
\]

Maka:

- \( \lambda \) disebut **eigenvalue** dari matriks \( A \)
- \( \mathbf{v} \) disebut **eigenvector** yang terkait dengan eigenvalue tersebut

Artinya: ketika suatu vektor \( \mathbf{v} \) dikalikan dengan matriks \( A \), hasilnya adalah kelipatan dari vektor itu sendiri.

---

## 🧠 Intuisi Geometris

- Eigenvector menunjukkan **arah tetap** dari transformasi oleh matriks \( A \).
- Eigenvalue memberi tahu **seberapa besar** vektor diregangkan atau dipendekkan dalam arah tersebut.

---

## 📊 Contoh Matriks

Misalkan kita punya matriks simetris 2x2 berikut:

\[
A = \begin{bmatrix} 2 & 1 \\ 1 & 2 \end{bmatrix}
\]

Kita akan:

1. Menentukan eigenvalue
2. Menentukan eigenvector
3. Menormalisasi (ortonormalisasi) eigenvector

---

## ✏️ Langkah 1: Mencari Eigenvalue

Gunakan **persamaan karakteristik**:

\[
\det(A - \lambda I) = 0
\]

\[
\Rightarrow \det\left( 
\begin{bmatrix} 
2 - \lambda & 1 \\ 
1 & 2 - \lambda 
\end{bmatrix} 
\right) = 0
\]

Hitung determinan:

\[
(2 - \lambda)^2 - 1 = 0
\Rightarrow (2 - \lambda)^2 = 1
\Rightarrow 2 - \lambda = \pm 1
\]

\[
\Rightarrow \lambda_1 = 1, \quad \lambda_2 = 3
\]

---

## ✏️ Langkah 2: Mencari Eigenvector

### Untuk \( \lambda = 1 \):

\[
A - \lambda I = \begin{bmatrix} 1 & 1 \\ 1 & 1 \end{bmatrix}
\]

Cari solusi:

\[
\begin{bmatrix} 1 & 1 \\ 1 & 1 \end{bmatrix}
\begin{bmatrix} x \\ y \end{bmatrix} = \begin{bmatrix} 0 \\ 0 \end{bmatrix}
\Rightarrow x + y = 0 \Rightarrow y = -x
\]

Pilih \( x = 1 \Rightarrow y = -1 \)

\[
\Rightarrow \mathbf{v}_1 = \begin{bmatrix} 1 \\ -1 \end{bmatrix}
\]

---

### Untuk \( \lambda = 3 \):

\[
A - \lambda I = \begin{bmatrix} -1 & 1 \\ 1 & -1 \end{bmatrix}
\]

\[
\Rightarrow -x + y = 0 \Rightarrow y = x
\Rightarrow \mathbf{v}_2 = \begin{bmatrix} 1 \\ 1 \end{bmatrix}
\]

---

## ✅ Hasil Sementara

- Eigenvalue: \( \lambda_1 = 1 \), \( \lambda_2 = 3 \)
- Eigenvector:
  - Untuk \( \lambda = 1 \): \( \mathbf{v}_1 = \begin{bmatrix} 1 \\ -1 \end{bmatrix} \)
  - Untuk \( \lambda = 3 \): \( \mathbf{v}_2 = \begin{bmatrix} 1 \\ 1 \end{bmatrix} \)

---

## 🔄 Langkah 3: Ortonormalisasi Eigenvector

**Tujuan**: mengubah eigenvector menjadi **vektor satuan** (panjang 1) dan saling ortogonal (sudut 90°), dikenal sebagai **ortonormal basis**.

### Normalisasi \( \mathbf{v}_1 \)

\[
||\mathbf{v}_1|| = \sqrt{1^2 + (-1)^2} = \sqrt{2}
\Rightarrow \hat{\mathbf{v}}_1 = \frac{1}{\sqrt{2}} \begin{bmatrix} 1 \\ -1 \end{bmatrix}
\]

### Normalisasi \( \mathbf{v}_2 \)

\[
||\mathbf{v}_2|| = \sqrt{1^2 + 1^2} = \sqrt{2}
\Rightarrow \hat{\mathbf{v}}_2 = \frac{1}{\sqrt{2}} \begin{bmatrix} 1 \\ 1 \end{bmatrix}
\]

---

## 📌 Ringkasan Akhir

| Komponen            | Nilai |
|---------------------|-------|
| Eigenvalue 1        | \( \lambda_1 = 1 \) |
| Eigenvector 1       | \( \mathbf{v}_1 = \begin{bmatrix} 1 \\ -1 \end{bmatrix} \) |
| Eigenvalue 2        | \( \lambda_2 = 3 \) |
| Eigenvector 2       | \( \mathbf{v}_2 = \begin{bmatrix} 1 \\ 1 \end{bmatrix} \) |
| Vektor Ortonormal 1 | \( \hat{\mathbf{v}}_1 = \frac{1}{\sqrt{2}} \begin{bmatrix} 1 \\ -1 \end{bmatrix} \) |
| Vektor Ortonormal 2 | \( \hat{\mathbf{v}}_2 = \frac{1}{\sqrt{2}} \begin{bmatrix} 1 \\ 1 \end{bmatrix} \) |

---

## 🛠️ Aplikasi Eigenvalue dan Eigenvector

- **Principal Component Analysis (PCA)** dalam data science: reduksi dimensi dengan eigenvector dari matriks kovarians.
- **Fisika kuantum**: solusi dari persamaan Schrödinger menggunakan eigenvalue energi.
- **Sistem Dinamik**: stabilitas sistem linear tergantung pada eigenvalue matriks sistem.
- **Graf Teori**: eigenvalue dari matriks adjacency berhubungan dengan struktur graf.

---

## 🔚 Kesimpulan

Eigenvalue dan eigenvector membantu kita **memahami sifat dalam** suatu matriks dan transformasi liniernya. Proses ortonormalisasi memastikan vektor-vektor tersebut siap digunakan dalam aplikasi numerik dan analitik lanjut.

