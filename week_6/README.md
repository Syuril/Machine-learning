Titanic Survival Prediction using Machine Learning
Deskripsi Project

Project ini merupakan implementasi Supervised Learning (Classification) menggunakan dataset Titanic untuk memprediksi apakah seorang penumpang akan selamat (Survived = 1) atau tidak selamat (Survived = 0) berdasarkan beberapa fitur seperti kelas penumpang, jenis kelamin, usia, jumlah saudara/pasangan, jumlah orang tua/anak, tarif, dan pelabuhan keberangkatan.

Pada project ini dilakukan beberapa tahapan, mulai dari Exploratory Data Analysis (EDA), Feature Engineering, Data Preprocessing, Training model, Evaluation, hingga Hyperparameter Tuning menggunakan GridSearchCV.

Dataset

Dataset yang digunakan adalah dataset Titanic (titanic.csv) yang berisi informasi penumpang kapal Titanic.

Fitur pada dataset:
PassengerId = ID penumpang
Survived = Status keselamatan (0 = Tidak Selamat, 1 = Selamat)
Pclass = Kelas penumpang (1, 2, 3)
Name = Nama penumpang
Sex = Jenis kelamin
Age = Umur penumpang
SibSp = Jumlah saudara/pasangan di kapal
Parch = Jumlah orang tua/anak di kapal
Ticket = Nomor tiket
Fare = Harga tiket
Cabin = Nomor kabin
Embarked = Pelabuhan keberangkatan
Library yang Digunakan

Project ini menggunakan library Python berikut:

pandas
numpy
matplotlib
seaborn
scikit-learn

Install library dengan perintah:

pip install pandas numpy matplotlib seaborn scikit-learn
Tahapan Project
1. Exploratory Data Analysis (EDA)

Pada tahap ini dilakukan analisis data untuk memahami karakteristik dataset, seperti:

Informasi dataset (info())
Statistik deskriptif (describe())
Visualisasi jumlah penumpang selamat dan tidak selamat
Analisis hubungan survival dengan:
Jenis kelamin
Kelas penumpang
Jumlah saudara/pasangan
Distribusi umur penumpang
Analisis rata-rata umur berdasarkan kelas penumpang
2. Feature Engineering & Preprocessing

Tahapan preprocessing yang dilakukan:

Mengisi nilai kosong pada kolom Age menggunakan rata-rata umur berdasarkan Pclass
Menghapus kolom Cabin karena terlalu banyak missing value
Menghapus data kosong yang tersisa
Menghapus kolom yang tidak digunakan:
PassengerId
Name
Ticket
Mengubah data kategorikal menjadi numerik menggunakan LabelEncoder:
Sex
Embarked
3. Data Splitting

Dataset dibagi menjadi:

Training data = 70%
Testing data = 30%

Menggunakan train_test_split() dari scikit-learn.

4. Model Machine Learning

Tiga model klasifikasi yang digunakan:

K-Nearest Neighbor (KNN)

Model klasifikasi berbasis tetangga terdekat.

Gaussian Naive Bayes

Model probabilistik berdasarkan Teorema Bayes.

Decision Tree

Model berbasis pohon keputusan untuk klasifikasi data.

5. Evaluasi Model

Setiap model dievaluasi menggunakan:

Accuracy Score
Confusion Matrix
Classification Report:
Precision
Recall
F1-Score
6. Pemilihan Model Terbaik

Berdasarkan hasil evaluasi, model dengan performa terbaik adalah:

Gaussian Naive Bayes

Model ini kemudian digunakan untuk melakukan prediksi pada data penumpang baru.

7. Hyperparameter Tuning

Untuk meningkatkan performa model KNN, digunakan:

GridSearchCV

Parameter yang diuji:

n_neighbors = [3, 5, 7]
weights = ['uniform', 'distance']
metric = ['euclidean', 'manhattan']

Evaluasi dilakukan menggunakan beberapa metrik:

Accuracy
Precision
Recall
F1-Score

Hasil tuning disimpan ke file:

hasil_gridsearch_knn.xlsx

Contoh Prediksi Data Baru

Format input:

[Pclass, Sex, Age, SibSp, Parch, Fare, Embarked]

Contoh:

[3, 0, 25.0, 0, 0, 7.25, 2]

Output:

0 = Tidak Selamat
1 = Selamat

Model juga dapat memberikan probabilitas prediksi.

Cara Menjalankan Project
Download atau salin file notebook/script.
Pastikan dataset titanic.csv berada di folder yang sama.
Install library yang dibutuhkan.
Jalankan script menggunakan Jupyter Notebook atau Google Colab.
Struktur File
project/
│── titanic.csv
│── titanic_classification.ipynb
│── hasil_gridsearch_knn.xlsx
│── README.md

Kesimpulan

Project ini menunjukkan bagaimana menerapkan Machine Learning Classification untuk memprediksi keselamatan penumpang Titanic dengan membandingkan beberapa algoritma klasifikasi. Setelah dilakukan evaluasi, model Naive Bayes memberikan hasil terbaik pada dataset ini. Selain itu, dilakukan juga hyperparameter tuning pada KNN untuk mencari parameter optimal dan meningkatkan performa model.