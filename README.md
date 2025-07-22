# California House Price Prediction
Proyek ini bertujuan untuk membangun model prediktif harga rumah berdasarkan dataset California Housing, menggunakan berbagai algoritma regresi dan proses tuning untuk mencapai performa optimal. Fokus utama dari proyek ini adalah membantu stakeholder seperti calon pembeli, investor, dan developer dalam memahami faktor-faktor utama yang memengaruhi harga rumah, serta menyediakan alat bantu dalam pengambilan keputusan berbasis data.

- Business Problem
  Stakeholder saat ini hanya dapat memperkirakan harga rumah secara subjektif tanpa analisis kuantitatif. Tidak adanya dasar yang kuat untuk menentukan harga rumah yang wajar menyebabkan risiko dalam investasi atau pembelian properti.

- Business Goals
  1. Mengembangkan model prediksi harga rumah berdasarkan fitur yang tersedia.
  2. Menilai pengaruh kedekatan dengan laut (ocean proximity) terhadap harga.
  3. Mengidentifikasi fitur-fitur paling signifikan terhadap nilai properti.

- Model & Evaluasi
  Model yang digunakan: Linear Regression, Decision Tree, K-Nearest Neighbors, Random Forest, XGBoost

- Model Evaluation dan Hasil Tuning
  Model terbaik diperoleh dari XGBoost sebelum tuning.
  Hasil evaluasi menunjukkan:
  RMSE: 44,863.17
  MAE: 29,765.89
  MAPE: 16.12%
  R²: 0.8515

  Setelah dilakukan hyperparameter tuning menggunakan RandomizedSearchCV:
  RMSE meningkat menjadi 47,379.61
  MAE menjadi 31,994.83
  MAPE meningkat menjadi 18.45%

- Final Model
  Model terbaik yang digunakan adalah XGBoost sebelum tuning, karena menunjukkan performa evaluasi lebih baik pada test set. Ini menunjukkan bahwa tuning tidak selalu memberikan hasil lebih baik dan harus dievaluasi secara kritis.

- Top 5 Feature Importance
  1. median_income: ∼40% kontribusi terhadap harga rumah
  2. ocean_proximity_ISLAND: signifikan positif
  3. ocean_proximity_INLAND: negatif terhadap harga tinggi
  4. latitude, longitude: lokasi geografis punya pengaruh kuat

- Tools & Libraries
  1. Python
  2. Pandas, Numpy, Matplotlib, Seaborn
  3. Scikit-learn
  4. XGBoost
