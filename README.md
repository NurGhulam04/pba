# Analisis Sentimen Ulasan Aplikasi Okejek dari Google Play Store

Repositori ini berisi kumpulan *notebook* dan data untuk analisis sentimen pada ulasan aplikasi Okejek yang diambil dari Google Play Store.

## Deskripsi

Proyek ini bertujuan untuk menganalisis dan mengklasifikasikan sentimen (positif, negatif, atau netral) dari ulasan pengguna aplikasi Okejek. Analisis ini dapat memberikan wawasan berharga bagi pengembang aplikasi untuk memahami umpan balik pengguna dan meningkatkan kualitas aplikasi.

## Dataset

Dataset yang digunakan dalam proyek ini diambil dengan melakukan *scraping* dari halaman aplikasi Okejek di Google Play Store. Terdapat dua versi dataset yang tersedia:

* `dataset/dirty_okejek_review.csv`: Dataset mentah hasil *scraping*.
* `dataset/cleaned_okejek_review.csv`: Dataset yang telah melalui tahap pra-pemrosesan.

## Metodologi

Alur kerja proyek ini dibagi menjadi beberapa tahap yang terdokumentasi dalam *notebook* Jupyter yang berbeda:

1.  **Scrapping dan Lowercasing**: Mengambil data ulasan dari Google Play Store dan mengubah semua teks menjadi huruf kecil.
2.  **Pra-pemrosesan Teks**:
    * **Tokenization**: Memecah teks ulasan menjadi token atau kata-kata individual.
    * **Stemming**: Mengubah kata-kata ke bentuk dasarnya.
3.  **Analisis Data Eksplorasi (EDA)**: Menganalisis dataset untuk memahami distribusi skor, tren ulasan dari waktu ke waktu, dan kata-kata yang paling sering muncul.
4.  **Ekstraksi Fitur**:
    * **Bag of Words (BoW)**: Merepresentasikan teks sebagai sekumpulan kata tanpa memperhatikan urutan.
    * **TF-IDF**: Memberikan bobot pada kata-kata berdasarkan frekuensinya dalam dokumen dan di seluruh korpus.
5.  **Pemodelan Analisis Sentimen**: Membangun dan melatih model klasifikasi (dalam kasus ini, Regresi Logistik) untuk memprediksi sentimen ulasan.
6.  **Visualisasi**:
    * **Word Cloud**: Membuat visualisasi kata-kata yang paling sering muncul dalam ulasan positif dan negatif.

## Struktur Repositori

.
├── dataset
│   ├── cleaned_okejek_review.csv
│   └── dirty_okejek_review.csv
├── notebook
│   ├── BoW.ipynb
│   ├── EDA.ipynb
│   ├── Finding_common_words.ipynb
│   ├── Scrapping_and_lowercasing.ipynb
│   ├── Sentiment_Analysis.ipynb
│   ├── Stemmer.ipynb
│   ├── TFIDF.ipynb
│   ├── Tokenization.ipynb
│   └── WordCloud.ipynb
└── README.md


## Cara Menjalankan

1.  **Instalasi Dependensi**: Pastikan Anda telah menginstal semua pustaka yang diperlukan. Anda dapat melakukannya dengan menjalankan perintah berikut:
    ```bash
    pip install google-play-scraper textblob seaborn sastrawi wordcloud matplotlib pandas numpy nltk scikit-learn
    ```
2.  **Jalankan Notebook**: Jalankan *notebook* `Sentiment_Analysis.ipynb`, notebook ini merupakan gabungan dari proses yang sebelumnya telah dilakukan.

## Hasil

Model analisis sentimen yang dibangun menggunakan Regresi Logistik berhasil mencapai akurasi sekitar **79.4%** pada data uji. Laporan klasifikasi menunjukkan rincian performa model untuk setiap kelas sentimen.

## Kontributor

* [Nama Anda](Link ke profil GitHub Anda)
