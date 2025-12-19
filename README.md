# 🎬 IMDb Movie Reviews Sentiment Analysis (NLP)

## 📌 Project Overview

This project implements an end-to-end **Natural Language Processing (NLP)** pipeline to classify movie reviews as **positive** or **negative** using real user-generated data from IMDb.

The goal is to demonstrate practical NLP skills, including text preprocessing, feature extraction, model training, evaluation, and error analysis, using industry-standard techniques.

---

## 📊 Dataset

* **Dataset:** IMDb Movie Reviews
* **Size:** 50,000 reviews (25,000 training, 25,000 testing)
* **Labels:** Binary sentiment (positive / negative)
* **Source:** TensorFlow Keras built-in dataset

The dataset consists of **real-world movie reviews written by users**, containing informal language, varying lengths, and subjective expressions, making it suitable for realistic NLP modeling.

---

## 🧠 Methodology

### 1️⃣ Data Understanding & Decoding

* Reviews are stored as integer-encoded sequences
* Decoded back into readable text using the official word index
* Verified realism by inspecting raw reviews

### 2️⃣ Text Preprocessing

* Removal of special tokens (`<START>`, `<PAD>`, `<UNK>`)
* Lowercasing
* Removal of non-alphabetic characters
* Extra whitespace normalization

Stemming and lemmatization were intentionally skipped to preserve semantic meaning.

### 3️⃣ Feature Extraction

Two vectorization techniques were compared:

* **Bag of Words (BoW)**
* **TF-IDF (Term Frequency–Inverse Document Frequency)**

Both representations used a maximum vocabulary size of 5,000 words and English stopword removal.

### 4️⃣ Model Training

* **Logistic Regression** was used as the baseline classifier
* Trained separately on BoW and TF-IDF features

### 5️⃣ Evaluation

* Accuracy
* Precision, Recall, F1-score
* Confusion matrix
* Error analysis of misclassified reviews

---

## 📈 Results

| Feature Representation | Accuracy |
| ---------------------- | -------- |
| Bag of Words           | ~85–87%  |
| TF-IDF                 | ~88–90%  |

TF-IDF consistently outperformed Bag of Words by reducing the influence of common words and emphasizing informative terms.

A bar chart visualization was used to compare model performance.

---

## 🔍 Error Analysis

Misclassified reviews often contained:

* Mixed sentiment
* Sarcasm
* Long reviews with conflicting opinions

This highlights a known limitation of traditional vectorization methods, which struggle with contextual understanding and negation.

---

## 🛠 Tools & Technologies

* Python
* Google Colab
* NumPy, Pandas
* Scikit-learn
* TensorFlow (dataset loading)
* Matplotlib

---

## 🚀 Future Improvements

* Add n-grams to capture short phrases
* Compare with Linear SVM
* Apply transformer-based models (e.g., BERT)
* Deploy as a simple web application

---

## 📂 Project Structure

```
IMDb_Sentiment_Analysis_NLP/
│
├── IMDb_Sentiment_Analysis_NLP.ipynb
├── README.md
├── sentiment_model_tfidf.pkl   (optional)
└── tfidf_vectorizer.pkl        (optional)
```

---

## ✅ Conclusion

This project demonstrates a complete and realistic NLP workflow applied to real-world text data.
It emphasizes interpretability, solid baselines, and thoughtful analysis — key skills for practical machine learning applications.

---

