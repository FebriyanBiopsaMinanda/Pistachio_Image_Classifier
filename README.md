# 🌰 Pistachio Classification

## 📌 Deskripsi
Project ini bertujuan untuk **membedakan dua jenis pistachio** (Kirmizi Pistachio dan Siit Pistachio) berdasarkan **fitur citra** (image features), dataset gambar serta data excel.  
Dengan memanfaatkan algoritma **machine learning dan deep learning**, project ini melakukan klasifikasi menggunakan berbagai pendekatan seperti Random Forest, SVM, KNN, Logistic Regression, Neural Network, dan Boosting Models.

---

## 📂 Dataset
### 📑 Sumber Data
Dataset diperoleh dari Kaggle:  
🔗 [Pistachio Image Dataset – Kaggle](https://www.kaggle.com/datasets/muratkokludataset/pistachio-image-dataset/data)

### 📊 Keterangan Data
Dataset terdiri dari:
- **Gambar pistachio** terbagi dalam 2 kelas:
  - 🌰 **Kirmizi Pistachio** (1.232 gambar)
  - 🌰 **Siit Pistachio** (916 gambar)
- **File Excel/CSV** berisi 28 fitur citra (shape, warna, statistik), seperti:
  - **Area** → luas objek
  - **Perimeter** → keliling objek
  - **Eccentricity** → keoval-an bentuk
  - **Roundness** → kebulatan
  - **Solidity, Aspect Ratio, Compactness**
  - **Statistik Warna (Mean, StdDev, Skewness, Kurtosis)**
  - **Class** → Label target (Kirmizi / Siit)

---

## 🧹 Tahapan Analisis
1. **Import Library 📚**  
   Menggunakan Python dengan library seperti `scikit-learn`, `tensorflow/keras`, `pandas`, `numpy`, `matplotlib`, `seaborn`.

2. **Load Dataset 📂**  
   - Membaca data Excel (28 fitur)  
   - Memetakan gambar ke tiap label

3. **EDA (Exploratory Data Analysis) 🔎**  
   - Distribusi kelas (Kirmizi vs Siit)  
   - Statistik deskriptif fitur utama  
   - Visualisasi distribusi fitur shape & warna  

4. **Data Mining ⛏️**  
   - Standardisasi fitur numerik (StandardScaler)  
   - PCA (Principal Component Analysis) untuk reduksi dimensi  

6. **Modeling 🤖**  
   Algoritma yang diterapkan meliputi:  
   - 🌲 **Random Forest**  
   - 🌀 **Support Vector Classifier (SVC)**  
   - 🗺️ **K-Nearest Neighbors (KNN)**  
   - 🎯 **Logistic Regression**  
   - 🧠 **Neural Network (MLPClassifier & Keras Sequential)**  
   - 🔥 **Boosting (AdaBoost, Gradient Boosting)**  

   Evaluasi dilakukan dengan:
   - **Confusion Matrix**  
   - **Classification Report (Precision, Recall, F1-score)**  
   - **Akurasi (%)**

---

## 📈 Hasil Prediksi
Performa model berdasarkan evaluasi:

| Model                  | Accuracy | Precision (avg) | Recall (avg) | F1-Score (avg) |
|-------------------------|----------|-----------------|--------------|----------------|
| 🌲 Random Forest        | 89.07%   | 0.89            | 0.89         | 0.89           |
| 🌀 Support Vector Classifier | 93.02%   | 0.93            | 0.93         | 0.93           |
| 🎯 Logistic Regression  | 91.86%   | 0.92            | 0.92         | 0.92           |
| 🗺️ KNN Classifier       | 90.00%   | 0.90            | 0.90         | 0.90           |
| 🔥 AdaBoost             | 91.16%   | 0.91            | 0.91         | 0.91           |
| 🌟 Gradient Boost       | 90.93%   | 0.91            | 0.91         | 0.91           |
| 🧠 Multi-Layer Perceptron (MLP) | **93.26%** | **0.93** | **0.93** | **0.93** |

---

## 🏆 Kesimpulan
Hasil evaluasi menunjukkan bahwa Multi-Layer Perceptron (MLP) dan Support Vector Classifier (SVC) adalah model dengan performa terbaik, masing-masing mencapai akurasi lebih dari 93% dengan nilai precision, recall, dan f1-score yang konsisten tinggi. Model linear seperti Logistic Regression serta metode ensemble seperti AdaBoost dan Gradient Boosting juga memberikan hasil yang kompetitif dengan akurasi sekitar 91%. Sementara itu, Random Forest dan KNN masih memberikan hasil yang baik, namun sedikit lebih rendah dibandingkan model lainnya.  

Secara keseluruhan, pendekatan berbasis Neural Network (MLP) terbukti paling efektif untuk klasifikasi pistachio dalam eksperimen ini karena mampu menangkap pola kompleks dalam data dengan performa seimbang di semua metrik evaluasi.
---
