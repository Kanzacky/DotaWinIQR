# 🎮 Dota 2 Win Prediction: Robust Data Cleaning via IQR & Feature Engineering

<p align="center">
  <a href="https://colab.research.google.com/github/Kanzacky/Dota-2-Win-Prediction-Robust-Data-Cleaning-via-IQR-Feature-Engineering/blob/main/Dota_2_Dataset.ipynb">
    <img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/>
  </a>
  <img src="https://img.shields.io/badge/Python-3.8+-blue.svg?logo=python&logoColor=white" alt="Python">
  <img src="https://img.shields.io/badge/Jupyter-Notebook-orange.svg?logo=jupyter&logoColor=white" alt="Jupyter">
  <img src="https://img.shields.io/badge/Machine%20Learning-Scikit--Learn-yellow.svg?logo=scikit-learn&logoColor=white" alt="Scikit-Learn">
</p>

Proyek ini bertujuan untuk mengolah dataset mentah hasil pertandingan Dota 2 menjadi dataset yang siap digunakan untuk model Machine Learning, dan melatih berbagai model klasifikasi untuk memprediksi kemenangan tim. Fokus utama proyek ini adalah pada ketahanan (robustness) data melalui pembersihan outlier yang ketat (menggunakan metode IQR) dan transformasi fitur untuk meningkatkan akurasi prediksi kemenangan tim (Radiant vs Dire).

## 🚀 Fitur Utama

Proyek ini dibagi menjadi dua modul utama yang dirangkum dalam notebook `Dota_2_Dataset.ipynb`:

### Modul 1: Pemrosesan Data (Data Preprocessing & EDA)
- **Inisialisasi & Load Data**: Memuat dataset mentah pertandingan Dota 2.
- **Cleaning & Outlier (IQR)**: Membersihkan data dari nilai anomali/outlier secara ketat menggunakan metode Interquartile Range (IQR).
- **Data Inspection**: Memeriksa kualitas dan konsistensi data setelah dibersihkan.
- **Transformasi, Encoding & Scaling**: Melakukan rekayasa fitur (feature engineering), mengubah data kategorikal menjadi numerik (encoding), dan normalisasi skala data.
- **EDA & Visualisasi (Exploratory Data Analysis)**: Menganalisis distribusi data, korelasi antar fitur, dan karakteristik target prediksi untuk mendapatkan *insight* mendalam.
- **Penyimpanan Dataset Final**: Menyimpan dataset yang sudah bersih dan terstandarisasi untuk pemodelan.

### Modul 2: Machine Learning Klasifikasi
- **Pemisahan Fitur dan Target**: Memisahkan variabel independen (fitur pertandingan) dan variabel dependen (target kemenangan: Radiant/Dire).
- **Train-Test Split (80:20)**: Membagi dataset menjadi data latih (80%) dan data uji (20%).
- **Pelatihan Model Klasifikasi**: Melatih berbagai macam algoritma klasifikasi (seperti Logistic Regression, Decision Tree, Random Forest, SVM, dll).
- **Evaluasi dan Perbandingan Akurasi**: Membandingkan performa metrik evaluasi dari semua model yang telah dilatih.
- **Classification Report & Confusion Matrix**: Menganalisis performa secara rinci (Precision, Recall, F1-Score) untuk model terbaik beserta *Confusion Matrix*-nya.
- **Simpan Model Terbaik**: Mengekspor model prediktif terbaik ke dalam format `.pkl` untuk *deployment* atau penggunaan lebih lanjut.

## 📁 Struktur Berkas

- `Dota_2_Dataset.ipynb` : Notebook utama (Jupyter Notebook) yang memuat semua alur pengerjaan mulai dari *data preprocessing* hingga evaluasi *machine learning*.
- `dota2Train.csv` : Berkas sumber data asli / mentah mengenai pertandingan Dota 2 yang digunakan.

## 🛠️ Prasyarat (Prerequisites)

Untuk menjalankan proyek ini secara lokal, pastikan pustaka Python berikut telah diinstal. Anda bisa menjalankannya di Jupyter Notebook maupun Google Colab.

```bash
pip install pandas numpy scikit-learn matplotlib seaborn
```

## 💻 Cara Penggunaan

1. *Clone* repositori ini ke dalam direktori komputer Anda.
2. Buka berkas `Dota_2_Dataset.ipynb` menggunakan antarmuka Jupyter Notebook, Jupyter Lab, atau import ke Google Colab.
3. Pastikan berkas dataset `dota2Train.csv` berada di lokasi yang sesuai agar dapat dibaca oleh *script*.
4. Jalankan satu per satu *cell* yang ada dalam notebook berurutan mulai dari Modul 1 hingga Modul 2 untuk memproses data dan menghasilkan model klasifikasi.

## 📊 Output yang Dihasilkan

Setelah kode dijalankan sepenuhnya, Anda akan mendapatkan keluaran berupa:
1. Dataset Dota 2 yang telah melalui proses pembersihan dan rekayasa fitur yang komprehensif.
2. Grafik visualisasi yang menggambarkan distribusi antar fitur serta korelasi dalam data.
3. Hasil perbandingan akurasi, matriks konfusi (*confusion matrix*), dan laporan performa klasifikasi dari masing-masing algoritma.
4. Model terbaik yang otomatis tersimpan dalam ekstensi `.pkl`.
