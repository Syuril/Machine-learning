# WineQT Clustering Using K-Means

## Deskripsi Project
Project ini bertujuan untuk melakukan analisis data dan clustering pada dataset WineQT menggunakan algoritma K-Means Clustering. Dataset WineQT berisi berbagai fitur kimia dari wine seperti fixed acidity, volatile acidity, citric acid, residual sugar, chlorides, pH, alcohol, dan quality. Clustering digunakan untuk mengelompokkan data wine berdasarkan kemiripan karakteristik fitur tanpa menggunakan label secara langsung.

## Tujuan
1. Melakukan Exploratory Data Analysis (EDA) pada dataset WineQT.
2. Melakukan preprocessing data sebelum clustering.
3. Melakukan feature scaling agar semua fitur memiliki skala yang seimbang.
4. Menentukan jumlah cluster terbaik menggunakan Elbow Method dan Via Score Plot.
5. Menerapkan algoritma K-Means Clustering pada dataset WineQT.
6. Membandingkan hasil clustering dengan label asli (quality).

## Library yang Digunakan
- NumPy
- Pandas
- Seaborn
- Matplotlib
- Scikit-Learn
- Yellowbrick

## Tahapan Project

### 1. Import Library
Pada tahap awal dilakukan import library yang digunakan untuk analisis data, visualisasi, preprocessing, dan clustering.

### 2. Load Dataset
Dataset WineQT dimuat menggunakan Pandas dengan format CSV agar dapat diproses pada tahap selanjutnya.

### 3. Exploratory Data Analysis (EDA)
EDA dilakukan untuk melihat karakteristik data sebelum clustering. Beberapa visualisasi yang digunakan:
- Scatter Plot
- Box Plot
- Histogram
- Statistik deskriptif

Tujuan EDA adalah untuk mengetahui distribusi data, penyebaran fitur, serta mendeteksi adanya outlier.

### 4. Preprocessing Data

#### Drop Duplicate
Dilakukan pengecekan dan penghapusan data duplikat agar data yang digunakan lebih bersih.

#### Feature Selection
Fitur input (X) diambil dari seluruh kolom kecuali kolom `quality`, sedangkan `quality` digunakan sebagai label pembanding.

#### Feature Scaling
Dilakukan StandardScaler untuk menormalkan data sehingga semua fitur memiliki rata-rata mendekati 0 dan standar deviasi mendekati 1.

Feature scaling sangat penting pada K-Means karena algoritma ini menggunakan perhitungan jarak antar data.

### 5. Evaluasi Sebelum dan Sesudah Scaling
Distribusi data sebelum dan sesudah scaling divisualisasikan menggunakan KDE Plot untuk melihat perubahan skala data.

Hasil:
- Sebelum scaling, setiap fitur memiliki rentang nilai yang berbeda.
- Setelah scaling, semua fitur berada pada skala yang sama.
- Bentuk distribusi tetap, namun skala menjadi lebih seimbang.

### 6. K-Means Clustering

#### Elbow Method
Metode ini digunakan untuk menentukan jumlah cluster (K) terbaik dengan melihat titik elbow pada grafik inertia.

Tahapan:
- Menghitung inertia dari K=1 sampai K=10
- Membuat grafik elbow
- Menentukan nilai K optimal

#### Implementasi K-Means
Setelah nilai K diperoleh, algoritma K-Means diterapkan untuk menghasilkan cluster.

Hasil cluster kemudian disimpan ke dalam dataframe.

### 7. Visualisasi Hasil Clustering
Scatter plot digunakan untuk melihat hasil clustering berdasarkan dua fitur.

Visualisasi dilakukan dengan:
- Warna berdasarkan cluster hasil K-Means
- Warna berdasarkan label asli (`quality`)

### 8. Via Score Plot
Metode kedua menggunakan Yellowbrick KElbowVisualizer untuk membantu menentukan jumlah cluster terbaik secara visual.

Tahapan:
- Menjalankan KElbowVisualizer
- Menentukan nilai K terbaik
- Menerapkan K-Means berdasarkan hasil visualisasi

### 9. Evaluasi Hasil Clustering
Hasil cluster dibandingkan dengan distribusi label asli (`quality`) untuk melihat pola pengelompokan data.

## Hasil Analisis
1. Data wine dapat dikelompokkan ke beberapa cluster berdasarkan kemiripan fitur.
2. Feature scaling membantu menyeimbangkan pengaruh setiap fitur pada proses clustering.
3. Elbow Method dan Via Score Plot dapat digunakan untuk menentukan jumlah cluster terbaik.
4. Hasil clustering menunjukkan adanya pola pengelompokan yang cukup mendekati distribusi label quality.
5. K-Means dapat membantu mengidentifikasi kelompok data wine berdasarkan karakteristik fitur kimia.

## Kesimpulan
K-Means Clustering berhasil diterapkan pada dataset WineQT untuk mengelompokkan data berdasarkan kemiripan karakteristik fitur. Proses preprocessing seperti drop duplicate dan feature scaling sangat penting untuk meningkatkan kualitas clustering. Penentuan jumlah cluster menggunakan Elbow Method dan Via Score Plot membantu mendapatkan hasil clustering yang lebih optimal. Hasil akhir menunjukkan bahwa data wine dapat dikelompokkan dengan baik berdasarkan fitur-fitur yang dimiliki.

## Author
Nama: MOH SYURIL ISWAN  
NIM: 4222301069  
Kelas: A MALAM