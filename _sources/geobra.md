---
title: geobra

---

# Penyelesaian Sistem Persamaan Linear dengan Metode Eliminasi Gauss dan Visualisasi dengan GeoGebra

## 1. Pendahuluan
Sistem persamaan linear adalah kumpulan persamaan yang memiliki beberapa variabel, di mana setiap persamaan berbentuk linear. Salah satu metode untuk menyelesaikan sistem persamaan linear adalah Metode Eliminasi Gauss.

Metode Eliminasi Gauss bertujuan untuk menyederhanakan sistem persamaan ke dalam bentuk segitiga atas (eselon baris), sehingga penyelesaiannya lebih mudah ditemukan dengan substitusi balik.

## 2. Langkah-langkah Metode Eliminasi Gauss
Menyusun Matriks Augmented

Tuliskan sistem persamaan dalam bentuk matriks yang mencakup koefisien variabel dan nilai konstanta.
Mengubah Matriks ke Bentuk Eselon Baris

Gunakan operasi baris elementer untuk membuat nol di bawah elemen diagonal utama.
Menyelesaikan dengan Substitusi Balik

Setelah matriks berbentuk segitiga atas, nilai variabel dapat ditemukan dengan substitusi balik.
## 3. Contoh Soal
Misalkan kita memiliki sistem persamaan berikut:

2x+y=5
x−y=1

Kita akan menyelesaikan sistem ini menggunakan Metode Eliminasi Gauss.

## 4. Menyusun Matriks Augmented
Sistem persamaan di atas dapat dituliskan dalam bentuk matriks augmented:

![image](https://hackmd.io/_uploads/H10CSsMs1g.png)

Di sini, kolom pertama dan kedua mewakili koefisien dari variabel x dan y, sedangkan kolom terakhir adalah nilai konstanta.

5. Mengubah Matriks ke Bentuk Eselon Baris
Langkah 1: Tukar Baris 1 dan Baris 2 (Opsional, agar elemen pertama menjadi 1)

  
![image](https://hackmd.io/_uploads/SkuZIoMjyg.png)

Ini dilakukan agar perhitungan lebih sederhana.

Langkah 2: Eliminasi Elemen di Bawah Elemen Utama Pertama
Kita buat elemen di bawah elemen pertama (2) menjadi nol dengan operasi:

![image](https://hackmd.io/_uploads/SkO78ofike.png)

 
Perhitungannya:

![image](https://hackmd.io/_uploads/B1_ILjGoyl.png)

matriks menjadi:

![image](https://hackmd.io/_uploads/BJvFUiGsyl.png)


Langkah 3: Ubah Elemen Diagonal Menjadi 1
Bagi Baris 2 dengan 3:

![image](https://hackmd.io/_uploads/rJds8sfikx.png)

 
Hasilnya:
![image](https://hackmd.io/_uploads/S1-aUiMjkg.png)

Langkah 4: Eliminasi Elemen di Atas Elemen Utama
Kita nol-kan elemen di atas 1 pada kolom kedua:

![image](https://hackmd.io/_uploads/r1TCLozi1l.png)

Perhitungannya:

![image](https://hackmd.io/_uploads/BkIevozjJl.png)


## 6. Menentukan Solusi

![image](https://hackmd.io/_uploads/rkS8DsMoyx.png)


## 7. Visualisasi dengan GeoGebra

[File GeoGebra](https://www.geogebra.org/calculator/)

![geobra](https://hackmd.io/_uploads/HJu9tsfjJg.png)

eq1: x-y=1

eq2: 2 x+y=5





## 8. Kesimpulan
Metode Eliminasi Gauss adalah cara sistematis untuk menyelesaikan sistem persamaan linear dengan mengubahnya menjadi bentuk segitiga atas. Setelah itu, kita bisa menemukan nilai variabel dengan substitusi balik.

Visualisasi menggunakan GeoGebra membantu memahami solusi secara grafis dengan melihat titik perpotongan garis.

