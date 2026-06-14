# Perbandingan Performa MLP Menggunakan Fungsi Aktivasi Sigmoid, Tanh, dan ReLU pada Dataset Iris

## Deskripsi

Proyek ini bertujuan untuk membandingkan performa algoritma Multilayer Perceptron (MLP) dengan menggunakan tiga fungsi aktivasi yang berbeda, yaitu Sigmoid, Tanh, dan ReLU pada dataset Iris dari Kaggle. Performa model dievaluasi menggunakan nilai Accuracy dan Loss setelah proses pelatihan.

Selain itu, implementasi Perceptron juga digunakan untuk mensimulasikan gerbang logika AND, OR, dan NOT sebagai dasar pemahaman jaringan saraf tiruan.

## Dataset

Dataset yang digunakan adalah Iris Dataset yang terdiri dari 150 data bunga Iris dengan empat fitur:

1. Sepal Length
2. Sepal Width
3. Petal Length
4. Petal Width

Target klasifikasi terdiri dari tiga kelas:

1. Iris-setosa
2. Iris-versicolor
3. Iris-virginica

File dataset yang digunakan:

iris.csv

## Library yang Digunakan

numpy
pandas
matplotlib
scikit-learn

## Tahapan Pengerjaan

### 1. Implementasi Perceptron

Perceptron digunakan untuk mensimulasikan gerbang logika:

* AND Gate
* OR Gate
* NOT Gate

### 2. Preprocessing Dataset

Tahapan preprocessing meliputi:

* Membaca dataset iris.csv
* Memisahkan fitur dan label
* Membagi data menjadi data training dan testing
* Normalisasi data menggunakan StandardScaler

### 3. Pelatihan Model MLP

Model MLP dilatih menggunakan tiga fungsi aktivasi:

#### Sigmoid

activation='logistic'

#### Tanh

activation='tanh'


#### ReLU

activation='relu'

Parameter yang digunakan:

hidden_layer_sizes=(10,)
max_iter=1000
random_state=42

### 4. Evaluasi Model

Performa model diukur menggunakan:

* Accuracy
* Loss

Hasil kemudian disajikan dalam bentuk tabel dan grafik.

## Hasil Perbandingan

Tabel hasil pengujian berisi:

| Activation Function | Accuracy      | Loss          |
| ------------------- | ------------- | ------------- |
| Sigmoid             | Hasil Program | Hasil Program |
| Tanh                | Hasil Program | Hasil Program |
| ReLU                | Hasil Program | Hasil Program |

## Visualisasi

Visualisasi dilakukan menggunakan grafik batang untuk:

1. Perbandingan Accuracy
2. Perbandingan Loss

## Kesimpulan

Berdasarkan hasil pengujian MLP pada dataset Iris menggunakan fungsi aktivasi Sigmoid, Tanh, dan ReLU, diperoleh bahwa ketiga fungsi aktivasi menghasilkan akurasi yang sangat tinggi. Namun, nilai loss yang dihasilkan berbeda. Fungsi aktivasi ReLU memiliki nilai loss paling kecil dibandingkan Sigmoid dan Tanh, sehingga menunjukkan performa pembelajaran yang lebih baik. Oleh karena itu, pada percobaan ini fungsi aktivasi ReLU dapat dianggap sebagai fungsi aktivasi terbaik untuk dataset Iris.

## Cara Menjalankan Program

1. Install library yang dibutuhkan:

pip install numpy pandas matplotlib scikit-learn

2. Pastikan file `iris.csv` berada pada folder yang sama dengan notebook atau script Python.

3. Jalankan seluruh cell pada Jupyter Notebook secara berurutan.

## Author

Moh Syuril Iswan
