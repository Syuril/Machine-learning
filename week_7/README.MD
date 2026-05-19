Deskripsi Project

Project ini merupakan implementasi K-Means Clustering untuk mengelompokkan data berdasarkan berat dan tinggi badan menggunakan metode unsupervised learning.

Dataset

Dataset yang digunakan adalah berat_tinggi.csv dengan fitur:

berat = Berat badan (kg)
tinggi = Tinggi badan (cm)
deskripsi = Label anotator sebagai pembanding hasil clustering
Library yang Digunakan
pandas
numpy
matplotlib
seaborn
scikit-learn
yellowbrick

Install library:

pip install pandas numpy matplotlib seaborn scikit-learn yellowbrick
Tahapan Project
1. Exploratory Data Analysis (EDA)
Visualisasi scatter plot berat vs tinggi
Statistik deskriptif data
Boxplot untuk melihat outlier
Histogram distribusi data
2. Preprocessing
Cek dan hapus data duplikat
Memilih fitur berat dan tinggi
Menyiapkan label anotator untuk evaluasi
3. Feature Scaling
Menggunakan StandardScaler
Menyamakan skala antar fitur
Membandingkan distribusi sebelum dan sesudah scaling
4. Penentuan Jumlah Cluster

Menggunakan dua metode:

Elbow Method → hasil optimal K = 4
Via Score Plot → hasil optimal K = 3
5. K-Means Clustering
Clustering dengan Elbow Method
Clustering dengan Via Score Plot
Menyimpan hasil cluster ke dataframe
6. Evaluasi
Membandingkan hasil cluster dengan label anotator
Visualisasi hasil clustering
Menentukan metode terbaik berdasarkan distribusi cluster
Struktur File
project/
│── berat_tinggi.csv
│── kmeans_clustering.ipynb
│── README.md
Kesimpulan

Project ini menunjukkan bahwa algoritma K-Means Clustering dapat digunakan untuk mengelompokkan data berdasarkan berat dan tinggi badan. Berdasarkan hasil evaluasi, Elbow Method dengan K = 4 memberikan hasil clustering yang paling sesuai dengan label anotator.