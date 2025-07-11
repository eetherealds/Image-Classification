# Image-Classification


# Mango Leaf Disease Classification

## Deskripsi Proyek

Proyek ini bertujuan untuk mengembangkan model klasifikasi gambar menggunakan **Convolutional Neural Network (CNN)** untuk mengenali **jenis-jenis penyakit pada daun mangga**. 

## Dataset

Dataset digunakan dari Kaggle, terdiri dari 8 kelas:

- Anthracnose  
- Bacterial Canker  
- Cutting Weevil  
- Die Back  
- Gall Midge  
- Healthy  
- Powdery Mildew  
- Sooty Mould

📥 [Link Dataset - (https://www.kaggle.com/datasets/warcoder/mango-leaf-disease-dataset)]

## Tools & Library

- Python  
- TensorFlow & Keras  
- OpenCV & Skimage  
- Matplotlib & Seaborn  
- TensorFlow Lite & TensorFlow.js  
- Kaggle API for dataset download  



## Langkah Implementasi

### 1. Setup dan Persiapan Data

- Menggunakan **API Token Kaggle** untuk mengunduh dataset langsung ke Colab.
- Ekstraksi file dan visualisasi gambar dari setiap kelas.
- Analisis distribusi data untuk memastikan keseimbangan antar kelas.

### 2. Preprocessing

- Pembagian dataset menjadi `train`, `validation`, dan `test` dengan rasio 70:15:15.
- Normalisasi gambar menggunakan `ImageDataGenerator`.

### 3. Pembangunan Model CNN

```python
Model(
    Conv2D(32 → 64 → 128 → 256) + MaxPooling,
    Flatten → Dense(256) + Dropout(0.5),
    Dense(8, activation='softmax')
)
```

- Optimizer: `Adam`  
- Loss: `Categorical Crossentropy`  
- Metrics: `Accuracy`  
- Callback: `EarlyStopping`, `ModelCheckpoint`

### 4. Pelatihan & Validasi

- Training hingga 40 epoch (dengan early stopping).
- Visualisasi hasil training dan validasi (akurasi & loss).

### 5. Evaluasi Model

- Evaluasi menggunakan data test.
- Menampilkan akurasi akhir model dan performa prediksi.

### 6. Export & Deployment

- **TensorFlow SavedModel**  
- **TensorFlow Lite (`.tflite`)**  
- **TensorFlow.js (untuk deployment web)**

---
