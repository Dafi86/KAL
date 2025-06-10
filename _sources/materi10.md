---
title: materi10

---


# 📘 Materi Ringkasan Perkalian Silang (Cross Product)

## 🔹 Pengertian Perkalian Silang
Perkalian silang adalah operasi antara dua **vektor dalam ruang tiga dimensi (3D)** yang menghasilkan vektor baru yang **tegak lurus** terhadap kedua vektor asal.

Jika diberikan:

```
u = [u1, u2, u3]
v = [v1, v2, v3]
```

Maka hasil cross product:

```
u × v = [
    u2 * v3 - u3 * v2,
    u3 * v1 - u1 * v3,
    u1 * v2 - u2 * v1
]
```

---

## 🔹 Luas Jajaran Genjang
Jika dua vektor **u** dan **v** membentuk sisi jajaran genjang, maka luasnya:

```
L = ||u × v||
```

---

## 🔹 Luas Segitiga
Jika tiga titik A, B, dan C diberikan:

1. Hitung dua vektor:
```
AB = B - A
AC = C - A
```

2. Hitung cross product:
```
AB × AC
```

3. Luas segitiga:
```
L = 1/2 * ||AB × AC||
```

---

# 📝 Penyelesaian Soal

## Soal 1
```
u = [1, 2, 0]
v = [2, 1, 0]

u × v = [0, 0, -3]
Luas = ||[0, 0, -3]|| = 3
```
✅ **Jawaban: 3**

---

## Soal 2
```
u = [2, 0, 0]
v = [0, 3, 0]

u × v = [0, 0, 6]
Luas = ||[0, 0, 6]|| = 6
```
✅ **Jawaban: 6**

---

## Soal 3
Titik: A = (0, 0, 0), B = (1, 3, -1), C = (2, 1, 1)

```
AB = [1, 3, -1]
AC = [2, 1, 1]

AB × AC = [
    (3*1 - (-1)*1),
    (-1*2 - 1*1),
    (1*1 - 3*2)
] = [4, -3, -5]

||AB × AC|| = sqrt(4² + (-3)² + (-5)²) = sqrt(50)
Luas = 1/2 * sqrt(50) = (5√2)/2
```
✅ **Jawaban: (5√2)/2**

---

## Soal 4
Titik: A = (5, 2, -1), B = (3, 6, 2), C = (1, 0, 4)

```
AB = [-2, 4, 3]
AC = [-4, -2, 5]

AB × AC = [
    (4*5 - 3*(-2)),
    (3*(-4) - (-2)*5),
    (-2)*(-2) - 4*(-4)
] = [20 + 6, -12 + 10, 4 + 16] = [26, -2, 20]

||AB × AC|| = sqrt(26² + (-2)² + 20²) = sqrt(1080)
Luas = 1/2 * sqrt(1080) = 3√30
```
✅ **Jawaban: 3√30**
