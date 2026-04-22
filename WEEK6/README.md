# 📊 Machine Learning - WEEK 6 (Classification)

Repository ini berisi materi dan praktik **Supervised Learning (Classification)** yang mencakup implementasi algoritma machine learning menggunakan Python.

---

## 📁 Struktur Folder

```
WEEK6/
│
├── Week 5 - 7 - Introduction to classification.pptx
├── Week_5_6_7_Supervised_Learning_Hands_On_Classification_All_tanpa_tuning.ipynb
├── cara kerja perhitungan naive bayes.xlsx
├── hasil_gridsearch_knn.xlsx
├── titanic.csv
```

---

## 🎯 Tujuan Pembelajaran

Pada minggu ini, pembelajaran difokuskan pada:

* Memahami konsep **Supervised Learning**
* Mempelajari algoritma **Classification**
* Mengimplementasikan model machine learning
* Melakukan evaluasi performa model
* Memahami tuning hyperparameter

---

## 🧠 Materi yang Dibahas

### 1. Supervised Learning (Classification)

Supervised learning adalah metode machine learning yang menggunakan data berlabel untuk melatih model dalam melakukan prediksi.

Contoh:

* Prediksi kelulusan
* Deteksi spam email
* Prediksi survival (Titanic dataset)

---

### 2. Algoritma yang Digunakan

#### 🔹 Naive Bayes

* Berdasarkan probabilitas (Teorema Bayes)
* Cocok untuk data kategorikal
* Digunakan pada file:

  * `cara kerja perhitungan naive bayes.xlsx`

#### 🔹 K-Nearest Neighbors (KNN)

* Mengklasifikasikan berdasarkan tetangga terdekat
* Sensitif terhadap nilai **K**
* Dilakukan tuning menggunakan:

  * `hasil_gridsearch_knn.xlsx`

---

### 3. Dataset

#### 🚢 Titanic Dataset

File: `titanic.csv`

Digunakan untuk:

* Klasifikasi survival penumpang
* Latihan preprocessing data
* Evaluasi model

---

### 4. Proses Machine Learning

Langkah-langkah yang dilakukan dalam notebook:

1. Data Loading
2. Data Cleaning & Preprocessing
3. Splitting Data (Train & Test)
4. Training Model
5. Evaluasi Model
6. Hyperparameter Tuning

---

## 📈 Evaluasi Model

Beberapa metrik yang digunakan:

* Accuracy
* Precision
* Recall
* F1-Score

Evaluasi ini penting untuk menghindari bias pada dataset dan meningkatkan performa model.

---

## ⚙️ Tools & Library

* Python
* Jupyter Notebook
* Pandas
* NumPy
* Scikit-learn
* Matplotlib / Seaborn

---

## 🚀 Cara Menjalankan

1. Clone repository:

```
git clone https://github.com/Wandypurba/Machine-Learning.git
```

2. Masuk ke folder:

```
cd Machine-Learning/WEEK6
```

3. Jalankan notebook:

```
jupyter notebook
```

---

## 📌 Catatan

* File notebook berisi implementasi tanpa tuning lanjutan (baseline model)
* Tuning tambahan dapat meningkatkan performa model
* Dataset dapat dimodifikasi untuk eksperimen lanjutan

---

## 👨‍💻 Author

**Wandy Putra Purba**

---

## 📚 Referensi

* Scikit-learn Documentation
* Machine Learning Course Materials
* Dataset: Titanic (Kaggle)

---

✨ *“Learning by doing is the best way to understand Machine Learning.”*
