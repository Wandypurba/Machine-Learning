# 🗑️ Machine Learning - Trash Classification (CNN)

Repository ini berisi materi dan praktik **Deep Learning (Image Classification)** menggunakan **Convolutional Neural Network (CNN)** untuk mengklasifikasikan jenis sampah berdasarkan gambar.

---

## 📁 Struktur Folder

```
Trash-Classification/
│
├── trash_classification_cnn.ipynb
├── model_klasifikasi_sampah.keras
└── README.md
```

---

## 🎯 Tujuan Pembelajaran

Pada proyek ini, pembelajaran difokuskan pada:

* Memahami konsep **Convolutional Neural Network (CNN)**
* Mempelajari proses klasifikasi gambar (image classification)
* Mengimplementasikan model deep learning menggunakan TensorFlow/Keras
* Melakukan evaluasi performa model
* Memahami proses preprocessing dan augmentasi data gambar

---

## 🧠 Materi yang Dibahas

### 1. Image Classification dengan CNN

CNN (Convolutional Neural Network) adalah arsitektur deep learning yang banyak digunakan untuk pengolahan data gambar, karena mampu mengenali pola spasial seperti tepi, tekstur, dan bentuk objek.

Contoh penerapan:

* Klasifikasi jenis sampah (organik, anorganik, kertas, plastik, dll)
* Deteksi objek pada gambar
* Pengenalan pola visual lainnya

---

### 2. Dataset

#### 🗑️ Trash Type Image Dataset

Dataset diunduh langsung melalui **KaggleHub**:

```python
kagglehub.dataset_download("farzadnekouei/trash-type-image-dataset")
```

Digunakan untuk:

* Klasifikasi jenis sampah berdasarkan gambar
* Latihan preprocessing dan augmentasi data gambar
* Evaluasi model CNN

---

### 3. Arsitektur Model CNN

Model dibangun menggunakan `keras.models.Sequential` dengan struktur:

* 3 blok **Conv2D + BatchNormalization + MaxPooling2D** (filter 16 → 32 → 64)
* **Flatten** layer
* **Dense (128)** dengan aktivasi ReLU
* **Dropout (0.4)** untuk mengurangi overfitting
* **Dense output** dengan aktivasi Softmax sesuai jumlah kelas

Model dikompilasi menggunakan:

* Optimizer: **Adam** (learning rate 0.001)
* Loss: **Sparse Categorical Crossentropy**
* Metrik: **Accuracy**

---

### 4. Proses Machine Learning

Langkah-langkah yang dilakukan dalam notebook:

1. Persiapan library
2. Pengunduhan dataset (KaggleHub)
3. Konfigurasi parameter dataset (ukuran gambar, batch size, seed)
4. Pembuatan dataset training & validasi
5. Visualisasi contoh gambar dataset
6. Optimasi pipeline data (caching, shuffling, prefetching)
7. Pembangunan arsitektur model CNN
8. Training model
9. Visualisasi hasil training (akurasi & loss)
10. Evaluasi model pada data validasi
11. Classification report & confusion matrix
12. Visualisasi contoh prediksi
13. Penyimpanan model (`.keras`)

---

## 📈 Evaluasi Model

Beberapa metrik yang digunakan:

* Accuracy
* Precision
* Recall
* F1-Score
* Confusion Matrix

Evaluasi ini penting untuk mengetahui seberapa baik model mengenali setiap kategori sampah dan mengidentifikasi kelas yang sering tertukar.

---

## ⚙️ Tools & Library

* Python
* Jupyter Notebook
* TensorFlow / Keras
* KaggleHub
* NumPy
* Pandas
* Scikit-learn
* Matplotlib / Seaborn

---

## 🚀 Cara Menjalankan

1. Clone repository:

```
git clone https://github.com/username/Trash-Classification.git
```

2. Masuk ke folder:

```
cd Trash-Classification
```

3. Install dependencies (jika diperlukan):

```
pip install tensorflow keras kagglehub scikit-learn seaborn matplotlib numpy
```

4. Jalankan notebook:

```
jupyter notebook
```

---

## 📌 Catatan

* Dataset diunduh otomatis melalui KaggleHub saat notebook dijalankan
* Model menggunakan BatchNormalization untuk mempercepat konvergensi training
* Hyperparameter (epoch, dropout, learning rate) dapat disesuaikan untuk eksperimen lanjutan
* Model hasil training disimpan dalam format `.keras` agar dapat digunakan kembali tanpa training ulang

---

## 👨‍💻 Author

**Wandy Putra Purba**

---

## 📚 Referensi

* TensorFlow & Keras Documentation
* KaggleHub Documentation
* Dataset: Trash Type Image Dataset (Kaggle - farzadnekouei)

---

✨ *"Learning by doing is the best way to understand Machine Learning."*
