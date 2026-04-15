📊 Supervised Learning: Linear Regression

📁 USA Housing Price Prediction

📌 Deskripsi

Project ini mengimplementasikan metode Linear Regression untuk memprediksi harga rumah berdasarkan beberapa faktor numerik seperti pendapatan area, usia rumah, jumlah ruangan, jumlah kamar tidur, dan populasi.

Dataset yang digunakan adalah USA Housing Dataset.

📂 Dataset

File: USA_Housing.csv

Fitur (Independent Variables)
Avg. Area Income
Avg. Area House Age
Avg. Area Number of Rooms
Avg. Area Number of Bedrooms
Area Population
Target (Dependent Variable)
Price

Catatan: Kolom Address dihapus karena tidak relevan dalam pemodelan.

⚙️ Teknologi & Library
Python
numpy
pandas
matplotlib
seaborn
scikit-learn
scipy
🔍 Metodologi
1. Data Preparation
Load dataset menggunakan pandas
Menghapus kolom yang tidak digunakan
Memisahkan data menjadi fitur (X) dan target (y)

2. Exploratory Data Analysis (EDA)
Analisis statistik deskriptif
Visualisasi distribusi data (histogram & density plot)
Analisis hubungan antar variabel (pairplot & heatmap)

3. Data Splitting

Dataset dibagi menjadi:

70% Training Data
30% Testing Data

4. Model Training

Model yang digunakan:

Linear Regression (scikit-learn)

Output model:

Intercept
Koefisien masing-masing fitur

5. Evaluasi Model

Model dievaluasi menggunakan data testing dengan metrik:

MAE (Mean Absolute Error) → rata-rata kesalahan prediksi
RMSE (Root Mean Squared Error) → mengukur error besar (sensitif terhadap outlier)
R² Score → tingkat kemampuan model menjelaskan variansi data

📈 Hasil & Analisis
R² ≈ 0.92 → model memiliki performa sangat baik
MAE rendah → kesalahan prediksi relatif kecil
RMSE lebih tinggi dari MAE → menunjukkan adanya beberapa outlier
Pengaruh Fitur
Avg. Area House Age dan Avg. Area Number of Rooms → pengaruh terbesar terhadap harga
Avg. Area Income → stabil dan signifikan
Avg. Area Number of Bedrooms → kontribusi relatif kecil

🧪 Uji Asumsi Regresi
Normalitas Residual → cukup terpenuhi (Shapiro-Wilk Test)
Homoskedastisitas → tidak ditemukan pola khusus pada residual plot
Outlier → masih terdapat beberapa nilai ekstrem

✅ Kesimpulan

Model Linear Regression mampu memprediksi harga rumah dengan akurasi tinggi dan menjelaskan sebagian besar variasi data. Namun, keberadaan outlier masih mempengaruhi performa model.
