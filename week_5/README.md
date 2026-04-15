📊 Supervised Learning - Classification (Iris Dataset)
📌 Deskripsi Project

Project ini bertujuan untuk mengimplementasikan algoritma K-Nearest Neighbors (KNN) dalam melakukan klasifikasi pada dataset Iris. Model digunakan untuk memprediksi spesies bunga Iris berdasarkan karakteristik fisiknya.

Dataset yang digunakan adalah Iris Dataset, yang terdiri dari beberapa fitur numerik seperti panjang dan lebar sepal serta petal.

📂 Dataset
Nama file: iris.csv
Jumlah data: 150 sampel
Jumlah fitur: 4 fitur numerik
🔢 Fitur (Independent Variables)
Sepal Length (cm)
Sepal Width (cm)
Petal Length (cm)
Petal Width (cm)
🎯 Target (Dependent Variable)
Species:
Setosa
Versicolor
Virginica
⚙️ Library yang Digunakan

Project ini menggunakan beberapa library Python berikut:

pandas
numpy
matplotlib
seaborn
scikit-learn
🔍 Tahapan Project
1. Data Loading

Dataset dimuat menggunakan pandas:

train = pd.read_csv('iris.csv')
2. Exploratory Data Analysis (EDA)

Analisis dilakukan untuk memahami distribusi data:

Informasi dataset (info())
Statistik deskriptif (describe())
Visualisasi:
Countplot spesies
Histogram Sepal Length
Boxplot distribusi fitur
3. Data Preprocessing

Langkah preprocessing meliputi:

Mengecek missing values
Encoding label menggunakan LabelEncoder
Pembagian data:
70% training
30% testing
4. Feature Scaling

Karena KNN sensitif terhadap skala data, dilakukan normalisasi menggunakan:

from sklearn.preprocessing import StandardScaler
5. Model Training (KNN)

Model KNN dilatih menggunakan:

from sklearn.neighbors import KNeighborsClassifier

Parameter default dan tuning parameter digunakan untuk membandingkan performa model.

6. Hyperparameter Tuning

Dilakukan menggunakan GridSearchCV dengan parameter:

n_neighbors: [3, 5, 7]
weights: ['uniform', 'distance']
metric: ['euclidean', 'manhattan']

Evaluasi menggunakan beberapa metrik:

Accuracy
Precision
Recall
F1-Score
7. Evaluasi Model

Model dievaluasi menggunakan:

Accuracy Score
Confusion Matrix
Classification Report
📈 Hasil

Model KNN menunjukkan performa yang sangat baik dalam mengklasifikasikan data Iris dengan akurasi tinggi (mendekati 100% tergantung parameter).

Hasil terbaik diperoleh dari kombinasi parameter optimal hasil GridSearch.

🔮 Prediksi Data Baru

Model dapat digunakan untuk memprediksi data baru, contoh:

new_data = np.array([[5.1, 3.5, 1.4, 0.2]])
prediction = best_model.predict(new_data)

Hasil prediksi dikembalikan dalam bentuk label spesies.

📁 Output
Hasil GridSearch disimpan dalam file:
hasil_gridsearch_knn.xlsx