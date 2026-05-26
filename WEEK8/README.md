# Week 8 — K-Means Clustering: Wine Quality

## Informasi Praktikum

| Keterangan | Detail |
|---|---|
| **Nama** | Wandy Putra Purba |
| **NIM** | 4222311004 |
| **Kelas** | Robotika A Malam |
| **Topik** | K-Means Clustering pada Dataset Wine Quality |

---

# Deskripsi Praktikum

Praktikum ini bertujuan untuk menerapkan algoritma **K-Means Clustering** pada dataset kualitas wine guna mengelompokkan data berdasarkan karakteristik tertentu tanpa menggunakan label kelas secara langsung.

Dataset yang digunakan adalah **WineQT.csv**, dengan beberapa fitur utama yang berpengaruh terhadap kualitas wine.

---

# Dataset

Dataset yang digunakan:

```bash
WineQT.csv
```

## Fitur yang Digunakan

| Fitur | Deskripsi |
|---|---|
| `alcohol` | Kandungan alkohol pada wine |
| `volatile acidity` | Tingkat keasaman volatil |
| `quality` | Nilai kualitas wine dari anotator |

---

# Alur Kerja Praktikum

## 1. Exploratory Data Analysis (EDA)

Tahap awal dilakukan untuk memahami karakteristik data melalui visualisasi:

- **Scatter Plot**  
  Untuk melihat hubungan antar fitur.

- **Box Plot**  
  Untuk mendeteksi distribusi data dan outlier.

- **Histogram**  
  Untuk mengetahui persebaran nilai pada setiap fitur.

---

## 2. Feature Engineering

Tahapan preprocessing data meliputi:

- Menghapus data duplikat
- Memilih fitur yang relevan
- Standardisasi fitur menggunakan:

```python
from sklearn.preprocessing import StandardScaler

scaler = StandardScaler()
```

Tujuan standardisasi adalah agar seluruh fitur memiliki skala yang seimbang sebelum proses clustering dilakukan.

---

# 3. K-Means Clustering

Algoritma **K-Means** digunakan untuk mengelompokkan data berdasarkan kemiripan karakteristik.

## A. Elbow Method

Metode ini digunakan untuk menentukan jumlah cluster optimal berdasarkan nilai inertia.

Hasil yang diperoleh:

```python
K = 3
```

Interpretasi cluster:

- Cluster 0 → Low Quality
- Cluster 1 → Medium Quality
- Cluster 2 → High Quality

---

## B. Yellowbrick / Silhouette Visualization

Visualisasi menggunakan library **Yellowbrick** digunakan untuk mengevaluasi kualitas cluster.

Hasil yang diperoleh:

```python
K = 4
```

Metode ini memberikan alternatif jumlah cluster dengan pemisahan data yang lebih detail.

---

# 4. Evaluasi Hasil Clustering

Hasil clustering dibandingkan dengan label asli `quality` menggunakan visualisasi scatter plot untuk melihat:

- Tingkat pemisahan cluster
- Konsistensi pola antar kualitas wine
- Distribusi data pada masing-masing cluster

---

# Library yang Digunakan

```python
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns

from sklearn.cluster import KMeans
from sklearn.preprocessing import StandardScaler

from yellowbrick.cluster import KElbowVisualizer
```

---

# Kesimpulan

Pada praktikum ini berhasil diterapkan algoritma **K-Means Clustering** untuk mengelompokkan kualitas wine berdasarkan karakteristik data.

Dua metode penentuan jumlah cluster digunakan:

- **Elbow Method** menghasilkan **3 cluster**
- **Yellowbrick / Silhouette Score** menghasilkan **4 cluster**

Hasil clustering menunjukkan bahwa fitur seperti `alcohol` dan `volatile acidity` cukup berpengaruh dalam membedakan kualitas wine.

---
