---
title: soal3
tags: [matematika, kalkulus, integral, hackmd]

---

---
title: "Ringkasan Bab 5 - Integral Lipat Dua"
---

# 📘 Ringkasan Bab 5: Integral Lipat Dua 

## 5.3 Integral Lipat Dua di Daerah Umum

### 🔹 Definisi
Integral lipat dua digunakan untuk menghitung volume, massa, dan area dari suatu daerah di bidang. Ketika daerah integrasi bukan persegi panjang, kita menyebutnya **daerah umum**.

### 🔹 Notasi dan Bentuk Umum
Jika $D$ adalah daerah yang dibatasi oleh kurva $x = g_1(y)$ dan $x = g_2(y)$ dari $y = c$ sampai $y = d$, maka:
$$
\iint_D f(x, y) \, dA = \int_c^d \int_{g_1(y)}^{g_2(y)} f(x, y) \, dx \, dy
$$
Sebaliknya, jika $D$ dibatasi oleh $y = h_1(x)$ dan $y = h_2(x)$ dari $x = a$ sampai $x = b$, maka:
$$
\iint_D f(x, y) \, dA = \int_a^b \int_{h_1(x)}^{h_2(x)} f(x, y) \, dy \, dx
$$

### 🔹 Strategi Penghitungan
1. Gambar grafik daerah $D$.
2. Tentukan batas-batas fungsi.
3. Pilih urutan integrasi yang mempermudah perhitungan.
4. Lakukan integrasi berlapis sesuai urutan.

### 🔹 Ilustrasi Contoh
Jika $D$ adalah daerah yang dibatasi oleh kurva $y = x^2$ dan $y = \sqrt{x}$, pertama kita tentukan titik potong: $x^2 = \sqrt{x} \Rightarrow x = 0$ atau $x = 1$. Maka kita integrasikan dari $x=0$ ke $x=1$, dan batas bawah $y=x^2$, batas atas $y=\sqrt{x}$.

$$
\iint_D f(x, y) \, dA = \int_0^1 \int_{x^2}^{\sqrt{x}} f(x, y) \, dy \, dx
$$

---

## 5.4 Integral Lipat Dua dalam Koordinat Polar

### 🔹 Kapan Menggunakan Koordinat Polar?
Gunakan saat:
- Daerah berbentuk lingkaran, cincin, atau sektor.
- Fungsi atau batas lebih mudah dalam $r$ dan $\theta$.

### 🔹 Transformasi Koordinat
- $x = r\cos\theta$
- $y = r\sin\theta$
- Elemen luas: $dA = r\,dr\,d\theta$

### 🔹 Rumus Umum
Jika $D$ adalah daerah dalam koordinat polar:
$$
\iint_D f(x, y) \, dA = \int_{\theta_1}^{\theta_2} \int_{r_1(\theta)}^{r_2(\theta)} f(r\cos\theta, r\sin\theta) \cdot r \, dr \, d\theta
$$

### 🔹 Contoh Perhitungan
Untuk cakram berjari-jari $a$:
$$
\int_0^{2\pi} \int_0^a f(r\cos\theta, r\sin\theta) \, r \, dr \, d\theta
$$
Jika $f(x, y) = 1$, maka:
$$
\int_0^{2\pi} \int_0^a r \, dr \, d\theta = \int_0^{2\pi} \left[\frac{r^2}{2}\right]_0^a \, d\theta = \int_0^{2\pi} \frac{a^2}{2} \, d\theta = \pi a^2
$$

---

## 5.5 Aplikasi Integral Lipat Dua

### 🔹 Luas Daerah
$$
\text{Luas} = \iint_D 1 \, dA
$$

### 🔹 Volume Di Bawah Permukaan
$$
V = \iint_D f(x, y) \, dA
$$

### 🔹 Massa Daerah
$$
m = \iint_D \rho(x, y) \, dA
$$

### 🔹 Koordinat Pusat Massa
$$
\bar{x} = \frac{1}{m} \iint_D x \rho(x, y) \, dA \quad \bar{y} = \frac{1}{m} \iint_D y \rho(x, y) \, dA
$$

### 🔹 Momen Inersia
$$
I_x = \iint_D y^2 \rho(x, y) \, dA \quad I_y = \iint_D x^2 \rho(x, y) \, dA
$$

### 🔹 Radius Gyrasi dan Momen Poler Inersia
$$
k_x = \sqrt{\frac{I_x}{m}} \quad k_y = \sqrt{\frac{I_y}{m}} \quad I_o = \iint_D (x^2 + y^2) \rho(x, y) \, dA
$$

---

## 📘 Penyelesaian Soal Halaman 239

### Soal 1
Hitunglah:
$$
\iint_D (x + 2y) \, dA, \quad D = [0, 2] \times [1, 3]
$$

➤ **Langkah-langkah:**
- Ini adalah daerah persegi panjang: $x$ dari 0 ke 2, $y$ dari 1 ke 3.
- Lakukan integrasi terhadap $x$ dulu:

$$
\int_0^2 (x + 2y) \, dx = \left[\frac{x^2}{2} + 2yx\right]_0^2 = 2 + 4y
$$

- Lalu integrasi hasilnya terhadap $y$:

$$
\int_1^3 (2 + 4y) \, dy = [2y + 2y^2]_1^3 = (6 + 18) - (2 + 2) = 20
$$

**✅ Jawaban: 20**

### Soal 2
$$
\iint_D \sqrt{x^2 + y^2} \, dA, \quad D: \text{lingkaran } r = 3
$$

➤ **Langkah-langkah:**
- Karena $\sqrt{x^2 + y^2} = r$, kita ubah ke koordinat polar.
- Batas $r$: dari 0 ke 3. Batas $\theta$: dari 0 ke $2\pi$.
- Gunakan elemen luas $dA = r \, dr \, d\theta$:

$$
\int_0^{2\pi} \int_0^3 r \cdot r \, dr \, d\theta = \int_0^{2\pi} \int_0^3 r^2 \, dr \, d\theta
$$

- Hitung:

$$
\int_0^3 r^2 \, dr = \left[\frac{r^3}{3}\right]_0^3 = 9
$$
$$
\int_0^{2\pi} 9 \, d\theta = 18\pi
$$

**✅ Jawaban: 18\pi**

### Soal 3
Volume di bawah $z = x^2 + y^2$, di atas cakram $r \leq 2$.

➤ **Langkah-langkah:**
- Karena $z = x^2 + y^2 = r^2$, maka integrasi jadi:

$$
\int_0^{2\pi} \int_0^2 r^2 \cdot r \, dr \, d\theta = \int_0^{2\pi} \int_0^2 r^3 \, dr \, d\theta
$$

- Hitung:

$$
\int_0^2 r^3 \, dr = \left[\frac{r^4}{4}\right]_0^2 = 4
$$
$$
\int_0^{2\pi} 4 \, d\theta = 8\pi
$$

**✅ Jawaban: 8\pi**

