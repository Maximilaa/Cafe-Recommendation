☕ Sistem Rekomendasi Café Berbasis Analisis Sentimen
Proyek ini merupakan implementasi **Sistem Rekomendasi Café berbasis Natural Language Processing (NLP)** yang memanfaatkan **embedding teks**, **Cosine Similarity**, serta **analisis sentimen ulasan pelanggan** untuk menghasilkan rekomendasi café yang relevan.
Proyek ini dikembangkan untuk **keperluan akademik, penelitian, dan portofolio**, khususnya pada bidang **Machine Learning, NLP, dan Recommender System**.

📂 Struktur Proyek
📁 Repository GitHub – Cafe Recommendation
    Cafe-Recommendation/
    *br*│
    *br*├── Coffee Recommender.ipynb        # Notebook utama pengolahan data & rekomendasi
    *br*├── app.py                          # Aplikasi demo rekomendasi café
    *br*├── requirements.txt                # Daftar library Python
    *br*├── Streamlit App Record.webm       # Rekaman demo aplikasi Streamlit
    *br*└── README.md                       # Dokumentasi proyek

🤗 Repository Hugging Face – Model Sentimen
    cafe-sentimen-bert/
    *br*│
    *br*├── app.py                          # Demo penggunaan model sentimen
    *br*├── cafe_embedding.npy              # Embedding café hasil pemrosesan
    *br*├── processed_coffee.csv            # Dataset ulasan café yang telah diproses
    *br*├── sentiment_score.npy             # Nilai sentiment score tiap café
    *br*└── requirements.txt                # Dependency model

🔗 Model tersedia di:
(https://huggingface.co/lattezice/cafe-sentimen-bert)

🎯 Tujuan Proyek
    * Membangun sistem rekomendasi café berbasis konten (*content-based recommendation*).
    * Memanfaatkan ulasan pelanggan sebagai sumber utama pembentukan profil café.
    * Menghasilkan embedding semantik café menggunakan pendekatan NLP.
    * Mengintegrasikan analisis sentimen sebagai indikator persepsi pelanggan.
    * Menyediakan aplikasi demo untuk menampilkan hasil rekomendasi.
    
🔹 Fitur Utama
    * Preprocessing teks ulasan café
    * Klasifikasi sentimen ulasan (positif / negatif)
    * Perhitungan **sentiment score café**
    * Pembentukan embedding café
    * Rekomendasi café menggunakan **Cosine Similarity**
    * Demo aplikasi berbasis Python / Streamlit

🧠 Model Analisis Sentimen
    Model sentimen yang digunakan adalah **BERT yang telah di-*fine-tune*** pada domain ulasan café.
    **Detail Model:**
    * Arsitektur: BERT (Transformer)
    * Tugas: Klasifikasi Sentimen Biner
    * Label: Positif / Negatif
    * Platform: Hugging Face
     Model ini digunakan untuk mengklasifikasikan setiap ulasan, kemudian hasilnya diagregasi untuk membentuk **sentiment score café**.

📊 Sentiment Score Café
    Sentiment score merepresentasikan kecenderungan sentimen pelanggan terhadap sebuah café secara keseluruhan.
    * Rentang nilai: **-1 hingga 1**
    * Mendekati **1** → dominasi sentimen positif
    * **0** → sentimen netral
    * Mendekati **-1** → dominasi sentimen negatif
    Nilai ini dihitung berdasarkan proporsi ulasan positif dan negatif pada masing-masing café.

📐 Metode Rekomendasi
    * Representasi café: **Embedding teks berbasis BERT**
    * Metode pengukuran kemiripan: **Cosine Similarity**
    * Jenis sistem: **Content-Based Recommendation System**
    Café dengan tingkat kemiripan tertinggi direkomendasikan sebagai alternatif yang paling relevan.

▶️ Menjalankan Proyek

1. Clone repository:

```bash
git clone https://github.com/Maximilaa/Cafe-Recommendation.git
cd Cafe-Recommendation
```

2. Install dependency:

```bash
pip install -r requirements.txt
```

3. Menjalankan notebook:

```bash
jupyter notebook "Coffee Recommender.ipynb"
```

4. Menjalankan aplikasi demo:

```bash
streamlit run app.py
```

---

📦 Library yang Digunakan
    * pandas
    * numpy
    * scikit-learn
    * transformers
    * torch
    * streamlit

📝 Catatan
    * Seluruh proses preprocessing dilakukan secara konsisten.
    * Model sentimen diambil dari repository Hugging Face dan bersifat *reusable*.
    * Proyek ini dibuat untuk **keperluan akademik dan penelitian**, serta dapat dikembangkan lebih lanjut.
