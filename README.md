## 🌍 Klasifikasi Gambar Satelit

Proyek ini bertujuan untuk membangun model klasifikasi gambar satelit menggunakan dataset **RSI-CB256** dari Kaggle. Model ini dikembangkan dengan TensorFlow dan diekspor ke dalam beberapa format (SavedModel, TensorFlow\.js, dan TensorFlow Lite)

---

### 📁 Dataset

- **Nama:** Satellite Image Classification (RSI-CB256)
- **Jumlah Kelas:** 4 kelas berbeda
- **Sumber:** [Kaggle - Satellite Image Classification](https://www.kaggle.com/datasets/mahmoudreda55/satellite-image-classification)

---

### 📊 Distribusi Data

- Data dibagi menjadi:
  - 80% untuk pelatihan (`latihan`)
  - 10% untuk validasi (`validasi`)
  - 10% untuk pengujian (`uji`)

---

### 🧪 Arsitektur Model

Model yang digunakan adalah model CNN sederhana dengan struktur:

```
- Rescaling
- Conv2D(16) + MaxPooling2D
- Conv2D(32) + MaxPooling2D
- Conv2D(64) + MaxPooling2D
- Flatten
- Dense(128)
- Dense(4, activation='softmax')
```

Optimizer: `Adam`\
Loss Function: `Sparse Categorical Crossentropy`

---

### 🔀 Training

- Training dilakukan selama maksimal 10 epoch
- Callback `EarlyStopping` custom digunakan untuk menghentikan pelatihan jika akurasi training dan validasi mencapai 99%.

---

### 📈 Evaluasi

- Visualisasi akurasi dan loss untuk training dan validasi
- Confusion matrix dan classification report digunakan untuk mengevaluasi performa akhir di data uji

---

### 🔮 Prediksi

- Sistem dapat melakukan prediksi untuk gambar input baru
- Menampilkan gambar dan hasil prediksi dengan probabilitas untuk semua kelas

---

### 💾 Ekspor Model

Model diekspor ke 3 format:

- `SavedModel` (untuk kebutuhan TensorFlow langsung)
- `TensorFlow.js` (untuk deployment ke web)
- `TensorFlow Lite` (untuk deployment ke mobile)

---

### 🛠 Tools & Library

- TensorFlow
- Keras
- Matplotlib, Seaborn (Visualisasi)
- Skimage, OpenCV, PIL (Pengolahan gambar)
- Scikit-learn (Evaluasi)

---

> Proyek ini dibuat oleh **Muhammad Fauzani Akbar** sebagai bagian dari project submission untuk course pengembangan machine learning. 


