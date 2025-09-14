# 🌰 Pistachio Classification

## 📌 Deskripsi
Project ini bertujuan untuk **membedakan dua jenis pistachio** (Kirmizi Pistachio dan Siit Pistachio) berdasarkan **fitur citra** (image features) serta dataset gambar.  
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

3. **Pembersihan Data 🧹**  
   - Cek missing values  
   - Penyelarasan label dan path gambar  

4. **EDA (Exploratory Data Analysis) 🔎**  
   - Distribusi kelas (Kirmizi vs Siit)  
   - Statistik deskriptif fitur utama  
   - Visualisasi distribusi fitur shape & warna  

5. **Preprocessing ⚙️**  
   - Standardisasi fitur numerik (StandardScaler)  
   - PCA (Principal Component Analysis) untuk reduksi dimensi  
   - Augmentasi gambar (ImageDataGenerator) untuk memperkuat data latih  

6. **Modeling 🤖**  
   Algoritma yang diterapkan meliputi:  
   - 🌲 **Random Forest**  
   - ⚡ **Support Vector Machine (SVM)**  
   - 👟 **K-Nearest Neighbors (KNN)**  
   - 📊 **Logistic Regression**  
   - 🧠 **Neural Network (MLPClassifier & Keras Sequential)**  
   - 🚀 **Boosting (AdaBoost, Gradient Boosting)**  

   Evaluasi dilakukan dengan:
   - **Confusion Matrix**  
   - **Classification Report (Precision, Recall, F1-score)**  
   - **Akurasi (%)**

---

## 📈 Hasil Prediksi
Performa model (berdasarkan laporan notebook):

| Model                  | Akurasi | Keterangan Singkat |
|-------------------------|---------|--------------------|
| 🌲 Random Forest        | ± **97–99%** | Performa sangat tinggi, stabil pada kedua kelas |
| ⚡ SVM                  | ± 95%   | Bagus, namun kadang salah klasifikasi di kelas minor |
| 👟 KNN                  | ± 93%   | Cukup baik, sensitif pada parameter k |
| 📊 Logistic Regression  | ± 92%   | Linear model, performa sedikit di bawah tree-based |
| 🧠 Neural Network (MLP) | ± 96%   | Bagus, mampu generalisasi dengan baik |
| 🚀 AdaBoost / GBM       | ± 95–97% | Performa tinggi, sedikit lebih lama dilatih |

---

## 🏆 Kesimpulan
Berdasarkan hasil eksperimen, model **Random Forest** dan **Gradient Boosting** menunjukkan performa terbaik dengan akurasi mendekati 99%, menjadikannya pilihan paling andal untuk klasifikasi pistachio. Fitur berbasis bentuk seperti *Area*, *Perimeter*, dan *Eccentricity* terbukti sangat penting dalam membedakan kedua kelas, sementara fitur warna menambah variasi informasi untuk meningkatkan akurasi model. Penerapan **PCA** membantu mempercepat proses training tanpa mengurangi kualitas prediksi secara signifikan. Selain itu, **Neural Network** juga memberikan performa yang kompetitif, namun Random Forest lebih stabil serta lebih mudah diinterpretasi. Secara keseluruhan, pendekatan berbasis ensemble tree terbukti paling efektif dalam mengklasifikasikan jenis pistachio dengan presisi tinggi.

---
