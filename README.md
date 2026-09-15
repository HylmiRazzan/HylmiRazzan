<h1 align="center">Hi 👋, I'm Muhammad Hylmi Razzan</h1>
<h3 align="center"> Mahasiswa S1 Data Science di BINUS University yang mendedikasikan diri untuk mengeksplorasi potensi dari Machine Learning dan Deep Learning. Memiliki ketertarikan mendalam dalam merancang model prediktif, mengolah data kompleks, serta menghadirkan solusi cerdas yang relevan untuk kebutuhan dunia nyata.</h3>

<br>

<div align="center">

> *"Where there's a will, there's a way."*

</div>

<br>

## 🔭 Projects
### 1. [Brazillian E Commerce using OOF, Optuna and 2 LEVEL stacking](https://github.com/HylmiRazzan/Big-Project-ML-DL/tree/main/Brazilian-E-Commerce-Public-Dataset)
*   **Topik:** Tabular Classification, NLP Feature Engineering, Model Deployment
*   **Deskripsi Singkat:** Proyek ini bertujuan memprediksi skor *review* pelanggan (skala 1 hingga 5). Alih-alih menggunakan pendekatan regresi, target diubah menjadi 3 kelas klasifikasi (Kecewa, Netral, Puas). Pemrosesan data menggunakan `ColumnTransformer` yang sangat terstruktur, di mana saya menyematkan ekstraksi **NLP** (`TfidfVectorizer`) sebagai *text feature* tambahan, yang diproses bersamaan dengan fitur *discrete* (`RobustScaler`), *continuous* (`PowerTransformer`), dan *categorical* (`OneHotEncoder`).
*   **Arsitektur Model:** Menggunakan pendekatan **2-Level Stacking Ensemble**. Level 1 dieksekusi oleh model **LGBM** dan **XGB**, kemudian prediksi tersebut diproses lebih lanjut oleh **Logistic Regression** di Level 2. Setiap model dioptimasi secara presisi menggunakan **Optuna** dan divalidasi dengan metode **Out-of-Fold (OOF)** untuk mencegah *overfitting*.
*   **Deployment:** Hasil akhir dari model ini tidak hanya berhenti di *notebook*, melainkan langsung di-*deploy* menjadi aplikasi interaktif berbasis **Streamlit**.

### 2. [Natural Disaster Image Classification Using CNN](https://github.com/HylmiRazzan/Big-Project-ML-DL/tree/main/Natural-Disaster-Image-Classification-Using-Convolal-Neural-Networks(CNN))
*   **Topik:** Computer Vision, Image Classification, Deep Learning
*   **Deskripsi Singkat:** Proyek ini berfokus pada pengenalan dan klasifikasi 4 kategori citra bencana alam dari dataset yang mengalami *class imbalance* sangat ekstrem. Penanganan ketimpangan data diselesaikan menggunakan pendekatan *Class Weighting* agar model tidak bias.
*   **Arsitektur Model:** Eksperimen pemodelan dibangun murni berbasis **CNN**. Prosesnya membandingkan performa antara arsitektur CNN yang dirakit dari awal (*from scratch*) melawan model pratalatih tingkat lanjut yang menggunakan teknik **Transfer Learning** dengan arsitektur **EfficientNetB1**.

### 3. [DANA Sentiment Analysis from Playstore Indonesia Using Sentence Transformers](https://github.com/HylmiRazzan/Big-Project-ML-DL/tree/main/DANA-Sentiment-Analysis-from-Playstore-Indonesia)
*   **Topik:** Natural Language Processing (NLP), Sentiment Analysis, Text Classification
*   **Deskripsi Singkat:** Proyek ini bertujuan untuk mengklasifikasikan sentimen dari ulasan pengguna aplikasi DANA di Playstore. Untuk mengatasi tantangan teks ulasan yang penuh *noise* (seperti singkatan dan bahasa gaul), ekstraksi fitur tidak menggunakan TF-IDF konvensional, melainkan mengimplementasikan **Sentence Transformers**. Teknologi ini memungkinkan model untuk benar-benar mengekstrak konteks dan makna linguistik dari sebuah kalimat.
*   **Arsitektur & Optimasi:** Menggunakan pendekatan **2-Level Stacking Ensemble** (Level 1: **XGBoost** & **Logistic Regression**; Level 2: **Logistic Regression** sebagai *meta-learner*). Pencarian *hyperparameter* pada setiap level dioptimasi secara presisi menggunakan **Optuna**, lalu divalidasi secara ketat dengan **Stratified K-Fold** guna mencegah *overfitting* dan menjaga keseimbangan distribusi kelas.

### 4. [Google & Intel Corp Stock Data Long Short-Term Memory (LSTM)](https://github.com/HylmiRazzan/Big-Project-ML-DL/tree/main/Google%26Intel-Corporation-Stock-Data)
*   **Topik:** Time Series Forecasting, Deep Learning
*   **Deskripsi Singkat:** Proyek ini bertujuan memprediksi harga penutupan (*Close price*) dari saham Google dan Intel. Kedua dataset tersebut diproses secara independen menggunakan teknik *sliding window* untuk mengekstrak pola sekuensial deret waktu sebelum dimasukkan ke dalam jaringan saraf tiruan.
*   **Arsitektur Model & Optimasi:** Pemodelan dibangun menggunakan arsitektur **LSTM**. Masing-masing dataset memiliki model *baseline* dan model *modified/tuned* tersendiri. Pada model yang dimodifikasi, saya menambahkan *layer* **Dropout** serta mengimplementasikan *callbacks* **EarlyStopping** dan **ReduceLROnPlateau** untuk menurunkan *learning rate* secara dinamis guna mencegah *overfitting*.

### 5. [Indonesian Rice Production Prediction in Sumatra](https://github.com/HylmiRazzan/Machine-Learning/tree/main/linear-regression/indonesian-rice-sumatra)
*   **Topik:** Regression, Data Visualization, Tabular Data
*   **Deskripsi Singkat:** Proyek ini bertujuan untuk memprediksi angka produksi padi di wilayah Sumatera. Selain membangun mesin analitik prediktif, proyek ini juga menyertakan dasbor visualisasi interaktif menggunakan <kbd>Power BI</kbd> untuk mengeksplorasi tren historis dan menggali *insight* distribusi data pertanian secara lebih mendalam.
*   **Arsitektur & Optimasi:** Untuk menangani skala nilai target prediksi (produksi padi) yang fluktuatif, model dibangun menggunakan **TransformedTargetRegressor** dengan **StandardScaler** sebagai fungsi transformasinya. Algoritma **Linear Regression** digunakan sebagai *base estimator*. Evaluasi dilakukan dengan membandingkan performa model *baseline* melawan model yang parameternya telah dioptimasi secara sistematis menggunakan **GridSearchCV**.

### 6. [Jakarta Air Quality Analysis Using Logistic Regression](https://github.com/HylmiRazzan/Machine-Learning/tree/main/logistic-regression/jakarta-air-quality-analysis)
*   **Topik:** Tabular Classification, Dimensionality Reduction, Data Visualization
*   **Deskripsi Singkat:** Proyek ini bertujuan untuk mengklasifikasikan kualitas udara di DKI Jakarta ke dalam lima kategori utama (BAIK, BERBAHAYA, SANGAT TIDAK SEHAT, SEDANG, TIDAK SEHAT). Selain pemodelan, dasbor interaktif <kbd>Power BI</kbd> juga buat untuk memvisualisasikan data polusi secara mendalam. Pada tahap pra-pemrosesan, distribusi data yang sangat tidak beraturan (*skewed*) ditangani menggunakan teknik *Log Transformation* agar sebaran data menjadi lebih normal dan optimal untuk dipelajari mesin.
*   **Arsitektur & Optimasi:** Menggunakan algoritma **Logistic Regression** sebagai model klasifikasi utama. Untuk mengekstraksi fitur paling penting dan mengurangi kompleksitas data, proyek ini menerapkan teknik reduksi dimensi **Principal Component Analysis (PCA)**. Performa akhir dievaluasi dengan membandingkan model *baseline* melawan model tingkat lanjut yang parameternya telah dioptimasi secara sistematis menggunakan **GridSearchCV**.

### 7. [EV Battery Failure Classification Using Tree-Based Models](https://github.com/HylmiRazzan/Machine-Learning/tree/main/tree-based-classifier/EV-battery-failure)
*   **Topik:** Tabular Classification, Tree-Based Models, Imbalanced Data
*   **Deskripsi Singkat:** Proyek ini bertujuan untuk mendeteksi potensi kegagalan pada baterai kendaraan listrik (*Electric Vehicle* / EV) ke dalam target klasifikasi biner (1 = *failure*, 0 = *no failure*). Tantangan utama dalam proyek ini adalah distribusi kelas target yang sangat timpang (*imbalanced dataset*), yang kemudian ditangani secara efektif menggunakan teknik *Class Weighting* untuk mencegah model menjadi bias terhadap kelas mayoritas.
*   **Arsitektur & Komparasi:** Proyek ini berfokus pada komparasi performa algoritma keluarga *Tree-Based Model*. Eksperimen dilakukan dengan melatih dan membandingkan tiga model secara independen, yaitu **Random Forest (RF)**, **Gradient Boosting Machine (GBM)**, dan **XGBoost**, untuk menemukan mesin prediktif tunggal yang paling optimal.

### 8. [Housing Price Prediction Using Tree-Based Regressors](https://github.com/HylmiRazzan/Machine-Learning/tree/main/tree-based-regressor/housing-price)
*   **Topik:** Regression, Tree-Based Models, Hyperparameter Tuning
*   **Deskripsi Singkat:** Proyek ini bertujuan untuk memprediksi harga rumah (*housing price*) menggunakan pendekatan regresi. Fokus utama dari eksperimen ini adalah mengevaluasi sejauh mana optimasi *hyperparameter* dapat meningkatkan akurasi dari algoritma berbasis pohon (*tree-based models*) saat dihadapkan pada data harga yang kontinu.
*   **Arsitektur & Komparasi:** Eksperimen ini membandingkan empat algoritma secara komprehensif, yaitu **Decision Tree (DT)**, **Random Forest (RF)**, **Gradient Boosting Machine (GBM)**, dan **XGBoost (XGB)**. Setiap algoritma dievaluasi melalui dua tahap, yakni performa model *base* (parameter bawaan) melawan model *tuned*. Seluruh proses optimasi untuk mencari kombinasi parameter terbaik pada keempat model tersebut dieksekusi secara terukur menggunakan metode **GridSearchCV**.

<br>

---

<br>

📫 **Email:** hylmirazzan5@gmail.com  


<h3 align="left">Connect with me:</h3>
<p align="left">
<a href="https://www.linkedin.com/in/muhammad-hylmi-razzan-4752a02b9/" target="blank"><img align="center" src="https://raw.githubusercontent.com/rahuldkjain/github-profile-readme-generator/master/src/images/icons/Social/linked-in-alt.svg" alt="muhammad hylmi razzan" height="30" width="40" /></a>
</p>

<h3 align="left">Languages and Tools:</h3>
<p align="left"> <a href="https://aws.amazon.com" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/amazonwebservices/amazonwebservices-original-wordmark.svg" alt="aws" width="40" height="40"/> </a> <a href="https://www.cprogramming.com/" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/c/c-original.svg" alt="c" width="40" height="40"/> </a> <a href="https://www.figma.com/" target="_blank" rel="noreferrer"> <img src="https://www.vectorlogo.zone/logos/figma/figma-icon.svg" alt="figma" width="40" height="40"/> </a> <a href="https://www.mysql.com/" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/mysql/mysql-original-wordmark.svg" alt="mysql" width="40" height="40"/> </a> <a href="https://www.python.org" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/python/python-original.svg" alt="python" width="40" height="40"/> </a> <a href="https://scikit-learn.org/" target="_blank" rel="noreferrer"> <img src="https://upload.wikimedia.org/wikipedia/commons/0/05/Scikit_learn_logo_small.svg" alt="scikit_learn" width="40" height="40"/> </a> <a href="https://www.tensorflow.org" target="_blank" rel="noreferrer"> <img src="https://www.vectorlogo.zone/logos/tensorflow/tensorflow-icon.svg" alt="tensorflow" width="40" height="40"/> </a> </p>
