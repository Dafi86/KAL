---
title: Perkalian Titik (Dot Product)

---

# Perkalian Titik (Dot Product)

## Pengertian

Perkalian titik (dot product) adalah salah satu operasi aljabar vektor yang menghasilkan sebuah **skalar** (bukan vektor). Operasi ini sangat penting dalam matematika, fisika, dan komputer grafis karena berkaitan dengan proyeksi, sudut antar vektor, dan kerja gaya.

Dua vektor $\vec{a}$ dan $\vec{b}$ di ruang dua dimensi atau tiga dimensi memiliki perkalian titik:

$\vec{a} \cdot \vec{b} = |\vec{a}|\,|\vec{b}|\cos(\theta)$

Di mana:

* $|\vec{a}|$ dan $|\vec{b}|$ adalah panjang (magnitudo) vektor $\vec{a}$ dan $\vec{b}$
* $\theta$ adalah sudut antara dua vektor

Dalam bentuk komponen:

* Jika $\vec{a} = \langle a_1, a_2 \rangle$ dan $\vec{b} = \langle b_1, b_2 \rangle$, maka:

$\vec{a} \cdot \vec{b} = a_1b_1 + a_2b_2$

* Untuk vektor tiga dimensi:

$\vec{a} = \langle a_1, a_2, a_3 \rangle, \quad \vec{b} = \langle b_1, b_2, b_3 \rangle$

$\vec{a} \cdot \vec{b} = a_1b_1 + a_2b_2 + a_3b_3$

## Sifat-sifat Dot Product

1. Komutatif: $\vec{a} \cdot \vec{b} = \vec{b} \cdot \vec{a}$
2. Distributif: $\vec{a} \cdot (\vec{b} + \vec{c}) = \vec{a} \cdot \vec{b} + \vec{a} \cdot \vec{c}$
3. Perkalian skalar: $(k\vec{a}) \cdot \vec{b} = k(\vec{a} \cdot \vec{b})$
4. $\vec{a} \cdot \vec{a} = |\vec{a}|^2$

## Interpretasi Geometris

* Jika $\vec{a} \cdot \vec{b} > 0$: sudut antar vektor < 90 derajat
* Jika $\vec{a} \cdot \vec{b} = 0$: vektor saling tegak lurus
* Jika $\vec{a} \cdot \vec{b} < 0$: sudut antar vektor > 90 derajat

## Contoh Perhitungan

Misalkan:
$\vec{a} = \langle 3, 4 \rangle$, $\vec{b} = \langle 2, -1 \rangle$

Maka:
$\vec{a} \cdot \vec{b} = 3 \times 2 + 4 \times (-1) = 6 - 4 = 2$

## Contoh Visualisasi di GeoGebra


![Screenshot 2025-05-27 134950](https://hackmd.io/_uploads/ryXAeymMxl.png)



![geogebra-export (1)](https://hackmd.io/_uploads/B1tIe1Xfge.png)


![geogebra-export](https://hackmd.io/_uploads/rkahkkQMge.png)




