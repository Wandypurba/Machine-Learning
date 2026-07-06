# 📈 Machine Learning - Overfitting & Underfitting (Transfer Learning)

Repository ini berisi materi dan praktik **Deep Learning (Transfer Learning)** menggunakan **MobileNetV2** untuk mempelajari konsep **underfitting**, **overfitting**, serta teknik meningkatkan performa model klasifikasi gambar melalui proses **fine-tuning** dan **regularisasi**.

---

## 📁 Struktur Folder

```
WEEK13/
│
├── overfitting_underfitting.ipynb
├── trash_classifier_model.keras
└── README.md
```

---

## 🎯 Tujuan Pembelajaran

Pada proyek ini, pembelajaran difokuskan pada:

* Memahami konsep **Underfitting** dan **Overfitting**
* Mempelajari penggunaan **Transfer Learning** pada klasifikasi gambar
* Mengimplementasikan model **MobileNetV2** menggunakan TensorFlow/Keras
* Melakukan evaluasi performa model klasifikasi gambar
* Memahami teknik penanganan overfitting seperti **Data Augmentation**, **Dropout**, **Early Stopping**, dan **Fine-Tuning**

---

## 🧠 Materi yang Dibahas

### 1. Transfer Learning dengan MobileNetV2

Transfer Learning merupakan teknik yang memanfaatkan model yang telah dilatih pada dataset besar (ImageNet) sehingga model dapat digunakan kembali untuk menyelesaikan permasalahan klasifikasi gambar dengan proses training yang lebih cepat.

Keuntungan Transfer Learning:

* Mempercepat proses training
* Membutuhkan dataset yang lebih sedikit
* Menghasilkan performa model yang lebih baik
* Mengurangi risiko underfitting

---

### 2. Dataset

#### 🗑️ Trash Type Image Dataset

Dataset diunduh langsung melalui **KaggleHub**:

```python
kagglehub.dataset_download("farzadnekouei/trash-type-image-dataset")
```

Dataset terdiri dari 6 kelas:

* cardboard
* glass
* metal
* paper
* plastic
* trash

Digunakan untuk:

* Klasifikasi jenis sampah berdasarkan gambar
* Latihan Transfer Learning
* Analisis underfitting dan overfitting
* Evaluasi performa model

---

### 3. Arsitektur Model

Model dibangun menggunakan **MobileNetV2** sebagai feature extractor dengan struktur:

* MobileNetV2 (Pre-trained ImageNet)
* GlobalAveragePooling2D
* Dense Layer
* Dropout
* Dense Output (Softmax)

Model dikompilasi menggunakan:

* Optimizer: **Adam**
* Loss: **Categorical Crossentropy**
* Metrik: **Accuracy**

---

### 4. Proses Machine Learning

Langkah-langkah yang dilakukan dalam notebook:

1. Persiapan library
2. Pengunduhan dataset menggunakan KaggleHub
3. Konfigurasi dataset training dan validation
4. Resize gambar menjadi 224 × 224 piksel
5. Data Augmentation
6. Pembangunan model Transfer Learning MobileNetV2
7. Training model baseline
8. Visualisasi hasil training (Accuracy & Loss)
9. Analisis Underfitting dan Overfitting
10. Penambahan Dropout dan Regularization
11. Implementasi Early Stopping
12. Fine-Tuning MobileNetV2
13. Evaluasi model akhir
14. Penyimpanan model (`.keras`)

---

## 📈 Evaluasi Model

Beberapa metrik yang digunakan:

* Accuracy
* Training Loss
* Validation Loss
* Training Accuracy
* Validation Accuracy

Visualisasi kurva accuracy dan loss digunakan untuk mengetahui apakah model mengalami:

* Underfitting
* Overfitting
* Good Fit

---

## ⚙️ Tools & Library

* Python
* Jupyter Notebook
* TensorFlow / Keras
* MobileNetV2
* KaggleHub
* NumPy
* Matplotlib
* Scikit-learn

---

## 🚀 Cara Menjalankan

1. Clone repository:

```bash
git clone https://github.com/roni-gm/Machine-Learning.git
```

2. Masuk ke folder:

```bash
cd Machine-Learning/WEEK13
```

3. Install dependencies:

```bash
pip install tensorflow keras kagglehub scikit-learn matplotlib numpy
```

4. Jalankan notebook:

```bash
jupyter notebook
```

---

## 📌 Catatan

* Dataset diunduh otomatis melalui KaggleHub saat notebook dijalankan.
* Model menggunakan MobileNetV2 yang telah dilatih pada dataset ImageNet.
* Data Augmentation digunakan untuk meningkatkan variasi data training.
* Early Stopping membantu menghentikan proses training ketika validation loss tidak lagi membaik.
* Fine-Tuning dilakukan dengan membuka beberapa layer MobileNetV2 untuk meningkatkan akurasi model.
* Model hasil training disimpan dalam format `.keras` sehingga dapat digunakan kembali tanpa melakukan training ulang.

---

## 👨‍💻 Author

**Wandy Putra Purba**

**NIM:** 4222311004

**Kelas:** Robotika A Malam

---

## 📚 Referensi

* TensorFlow Documentation
* Keras Documentation
* MobileNetV2 Documentation
* KaggleHub Documentation
* Dataset: Trash Type Image Dataset (Kaggle - farzadnekouei)

---

✨ *"Transfer Learning enables us to build accurate image classification models with less data and shorter training time."*