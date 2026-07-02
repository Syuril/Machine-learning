# ♻️ Trash Type Classification using MobileNetV2

## 📌 Overview

Project ini merupakan implementasi **Image Classification** untuk mengenali jenis sampah menggunakan metode **Transfer Learning** dengan arsitektur **MobileNetV2**. Model dilatih menggunakan dataset **TrashType Image Dataset** yang terdiri dari enam kategori sampah.

Model memanfaatkan bobot pretrained ImageNet sehingga proses pelatihan menjadi lebih cepat dan menghasilkan akurasi yang lebih baik dibandingkan melatih model dari awal.

---

## 📂 Dataset

Dataset yang digunakan adalah:

```
TrashType_Image_Dataset/
│
├── cardboard/
├── glass/
├── metal/
├── paper/
├── plastic/
└── trash/
```

Jumlah kelas:

- Cardboard
- Glass
- Metal
- Paper
- Plastic
- Trash

Jumlah data:

| Dataset | Jumlah |
|---------|--------|
| Training | 2150 gambar |
| Validation | 377 gambar |
| Total | 2527 gambar |

---

## 🚀 Features

- Transfer Learning menggunakan MobileNetV2
- Data Augmentation
- Image Rescaling
- Dropout untuk mengurangi overfitting
- Early Stopping
- Reduce Learning Rate on Plateau
- Confusion Matrix
- Classification Report
- Accuracy & Loss Visualization

---

## 🧠 Model Architecture

Model yang digunakan:

```
Input Image (224x224x3)
        │
MobileNetV2 (ImageNet)
        │
GlobalAveragePooling2D
        │
Dropout (0.5)
        │
Dense (Softmax)
```

Base model dibekukan (freeze) sehingga hanya layer klasifikasi yang dilatih.

---

## ⚙️ Hyperparameter

| Parameter | Nilai |
|-----------|--------|
| Image Size | 224 × 224 |
| Batch Size | 32 |
| Optimizer | Adam |
| Learning Rate | 0.001 |
| Validation Split | 15% |
| Dropout | 0.5 |
| Epoch | Menggunakan EarlyStopping |

---

## 📚 Library

Project menggunakan:

```python
TensorFlow
Keras
NumPy
Matplotlib
Scikit-learn
```

Install dependency:

```bash
pip install tensorflow matplotlib scikit-learn numpy
```

---

## 📁 Project Structure

```
project/
│
├── TrashType_Image_Dataset/
│
├── train.py
│
├── README.md
│
└── requirements.txt
```

---

## ▶️ Running

Clone repository

```bash
git clone https://github.com/username/repository.git
```

Masuk folder

```bash
cd repository
```

Jalankan

```bash
python train.py
```

---

## 📊 Evaluation

Model dievaluasi menggunakan:

- Accuracy
- Validation Accuracy
- Loss
- Validation Loss
- Confusion Matrix
- Classification Report

---

## 🔄 Data Augmentation

Data augmentation yang digunakan:

- Rotation
- Zoom
- Horizontal Flip
- Width Shift
- Height Shift
- Rescaling

Hal ini bertujuan meningkatkan kemampuan generalisasi model dan mengurangi overfitting.

---

## 🎯 Transfer Learning

Model menggunakan **MobileNetV2** pretrained pada ImageNet.

Keuntungan:

- Training lebih cepat
- Membutuhkan data lebih sedikit
- Akurasi lebih tinggi
- Cocok untuk perangkat dengan resource terbatas

---

## 📈 Output

Program menghasilkan:

- Grafik Accuracy
- Grafik Loss
- Confusion Matrix
- Classification Report
- Model klasifikasi enam jenis sampah

---

## 👨‍💻 Author

**Moh Syuril Iswan**

Politeknik Negeri Batam

Robotics Engineering