---
title: Refleksi Matriks 2D dan 3D

---


# Refleksi Matriks 
## Kode Lengkap Refleksi

```python
%matplotlib inline
import matplotlib.pyplot as plt
import numpy as np

# Titik awal bentuk
titik = np.array([[0, 0], [0.5, 0.5], [0.5, 1.5], [0, 1], [0, 0]])
koordinats = titik.T
x = koordinats[0, :]
y = koordinats[1, :]

# Matriks refleksi
refleksi_y = np.array([[-1, 0], [0, 1]])         # sumbu-y
refleksi_x = np.array([[1, 0], [0, -1]])         # sumbu-x
refleksi_y_eq_x = np.array([[0, 1], [1, 0]])     # garis y = x

# Fungsi refleksi terhadap x = a dan y = a
def refleksi_terhadap_x_a(a, koordinat):
    M = np.array([[-1, 0], [0, 1]])
    T = koordinat - np.array([[a], [0]])
    R = M @ T
    return R + np.array([[a], [0]])

def refleksi_terhadap_y_a(a, koordinat):
    M = np.array([[1, 0], [0, -1]])
    T = koordinat - np.array([[0], [a]])
    R = M @ T
    return R + np.array([[0], [a]])

# Lakukan semua transformasi
B_y = refleksi_y @ koordinats
B_x = refleksi_x @ koordinats
B_diag = refleksi_y_eq_x @ koordinats
B_x2 = refleksi_terhadap_x_a(2, koordinats)
B_y2 = refleksi_terhadap_y_a(2, koordinats)

# Plotting
fig, ax = plt.subplots(figsize=(8, 8))

# Bentuk asli
ax.plot(x, y, 'ro--', label='Asli')

# Refleksi-refleksi
ax.plot(B_y[0, :], B_y[1, :], 'bo-', label='Refleksi sumbu-y')
ax.plot(B_x[0, :], B_x[1, :], 'go-', label='Refleksi sumbu-x')
ax.plot(B_diag[0, :], B_diag[1, :], 'mo-', label='Refleksi y = x')
ax.plot(B_x2[0, :], B_x2[1, :], 'co-', label='Refleksi x = 2')
ax.plot(B_y2[0, :], B_y2[1, :], 'yo-', label='Refleksi y = 2')

# Tambahan sumbu dan grid
ax.axvline(x=0, color="k", ls=":")
ax.axhline(y=0, color="k", ls=":")
ax.grid(True)
ax.set_aspect('equal', adjustable='box')
ax.set_title("Refleksi terhadap beberapa garis")
ax.legend()
plt.show()
```

## Penjelasan Kode

* `titik` menyimpan bentuk awal dalam koordinat 2D.
* Refleksi dilakukan dengan perkalian matriks transformasi.
* Fungsi `refleksi_terhadap_x_a` dan `refleksi_terhadap_y_a` digunakan untuk merefleksikan terhadap garis yang sejajar sumbu.
* Semua hasil transformasi diplot dengan warna dan label berbeda.
* `ax.set_aspect('equal', adjustable='box')` menjaga rasio sumbu dan menghindari warning.

## Hasil Visualisasi

![RefrelsiMatrik](https://hackmd.io/_uploads/HyA01zwegx.png)


Grafik yang dihasilkan menampilkan bentuk asli dan hasil refleksi terhadap:

* Sumbu-y (biru)
* Sumbu-x (hijau)
* Garis y = x (magenta)
* Garis x = 2 (cyan)
* Garis y = 2 (kuning)

Setiap transformasi divisualisasikan agar lebih mudah dipahami secara geometri.

---

Dengan pendekatan ini, kita bisa melihat bagaimana berbagai refleksi memengaruhi bentuk objek dalam bidang 2D. Cocok untuk pembelajaran transformasi matriks dalam grafika komputer atau geometri analitik.
s