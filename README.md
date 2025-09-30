---

# 📊 Sentiment Analysis – Okejek App Reviews

Repositori ini berisi proyek **Analisis Sentimen** terhadap ulasan pengguna aplikasi **Okejek** yang diambil dari **Google Play Store**.
Proyek ini dibuat sebagai bagian dari tugas analisis teks menggunakan teknik **Natural Language Processing (NLP)**.

---

## 📂 Struktur Proyek

```
.
├── dataset
│   ├── dirty_okejek_review.csv     # Dataset mentah hasil scraping
│   └── cleaned_okejek_review.csv   # Dataset setelah preprocessing
│
├── notebook
│   ├── Scrapping_and_lowercasing.ipynb   # Scraping + pembersihan awal
│   ├── Tokenization.ipynb                # Tokenisasi teks
│   ├── Stemmer.ipynb                     # Stemming kata
│   ├── TFIDF.ipynb                       # Representasi TF-IDF
│   ├── BoW.ipynb                         # Representasi Bag-of-Words
│   ├── Finding_common_words.ipynb        # Analisis kata yang sering muncul
│   ├── WordCloud.ipynb                   # Visualisasi Word Cloud
│   ├── EDA.ipynb                         # Exploratory Data Analysis
│   └── Sentiment_Analysis.ipynb          # Notebook utama (klasifikasi sentimen)
│
└── README.md
```

---

## ⚙️ Teknologi yang Digunakan

* **Python** (Jupyter Notebook)
* **Library NLP & ML**:

  * `pandas`, `numpy` → manipulasi data
  * `scikit-learn` → machine learning (TF-IDF, klasifikasi)
  * `nltk` / `Sastrawi` → preprocessing teks (stopwords, stemming)
  * `matplotlib`, `seaborn`, `wordcloud` → visualisasi

---

## 🚀 Langkah Menjalankan Proyek

1. **Clone repositori**

   ```bash
   git clone https://github.com/NurGhulam04/pba.git
   cd pba
   ```

2. **Buat environment baru (opsional)**

   ```bash
   python -m venv venv
   source venv/bin/activate   # Linux/Mac
   venv\Scripts\activate      # Windows
   ```

3. **Install dependencies**

   ```bash
   pip install -r requirements.txt
   ```

   > Jika `requirements.txt` belum ada, jalankan `pip freeze > requirements.txt` setelah semua library terpasang.

4. **Jalankan Jupyter Notebook**

   ```bash
   jupyter notebook
   ```

   Buka file pada folder `notebook/`, misalnya `Sentiment_Analysis.ipynb`.

---

## 📊 Alur Analisis

1. **Scraping Data** → Mengambil review dari Google Play Store.
2. **Preprocessing** → Lowercasing, cleaning, tokenisasi, stemming, stopword removal.
3. **Representasi Teks**:

   * Bag-of-Words (BoW)
   * Term Frequency - Inverse Document Frequency (TF-IDF)
4. **EDA & Visualisasi** → WordCloud, distribusi kata, analisis kata umum.
5. **Modeling** → Klasifikasi sentimen positif/negatif menggunakan algoritma ML.
6. **Evaluasi** → Mengukur performa model dengan metrik (accuracy, precision, recall, f1-score).

---

## 📌 Hasil & Temuan

* Dataset berhasil dibersihkan dari noise seperti emoji, angka, tanda baca, dan stopwords.
* WordCloud dan analisis kata membantu memahami kata dominan yang muncul.
* Model berbasis **TF-IDF + klasifikasi** memberikan performa yang lebih baik dibandingkan representasi BoW.

---

## ✍️ Kontributor

* [NurGhulam04](https://github.com/NurGhulam04)

---

Mau aku bikinin juga file **`requirements.txt`** biar gampang install dependensinya, atau cukup README aja?
