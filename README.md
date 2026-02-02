# 🎬 IMDB Movie Review Sentiment Analysis

![Python](https://img.shields.io/badge/Python-3.9-blue)
![NLTK](https://img.shields.io/badge/Library-NLTK-green)
![Scikit-Learn](https://img.shields.io/badge/Library-Scikit_Learn-orange)
![Status](https://img.shields.io/badge/Status-Completed-success)

## 📌 Project Overview
In the era of digital marketing, understanding customer feedback is crucial. However, analyzing thousands of reviews manually is impossible. This project utilizes **Natural Language Processing (NLP)** to automatically classify movie reviews as either **Positive** or **Negative**.

The goal is to build a model that can understand unstructured text data and determine the underlying sentiment with high accuracy.

**Key Result:** Achieved a solid **85% Accuracy** using TF-IDF Vectorization and a Multinomial Naive Bayes classifier.

---

## 📂 Dataset
* **Source:** [IMDB Dataset of 50K Movie Reviews](https://www.kaggle.com/lakshmi25npathi/imdb-dataset-of-50k-movie-reviews)
* **Description:** The dataset contains 50,000 reviews.
* **Balance:** The dataset is perfectly balanced (50% Positive, 50% Negative), making **Accuracy** a valid metric for evaluation.

---

## 🛠️ Methodology
NLP projects rely heavily on data cleaning. The following pipeline was implemented:

1.  **Text Preprocessing (The most critical step):**
    * **HTML Tag Removal:** Cleaning raw text from web scraping artifacts.
    * **Tokenization & Lowercasing:** Standardizing the text.
    * **Stopwords Removal:** Removing common words (e.g., "is", "the", "and") using the NLTK library.
    * **Stemming:** Reducing words to their root form (e.g., "acting" -> "act") using `PorterStemmer`.
2.  **Feature Extraction:**
    * Used **TF-IDF (Term Frequency-Inverse Document Frequency)** to convert text into numerical vectors, giving more weight to unique and meaningful words.
3.  **Modeling:**
    * Algorithm: **Multinomial Naive Bayes**.
    * Why? It is computationally efficient and highly effective for text classification tasks.

---

## 📊 Evaluation & Results
Unlike imbalance classification problems, this dataset is balanced. Therefore, the model shows consistent performance across both classes.

| Metric | Score | Insight |
| :--- | :---: | :--- |
| **Accuracy** | **85%** | The model correctly predicts sentiment 85 out of 100 times. |
| **Precision** | 0.85 | Consistent for both Positive and Negative classes. |
| **Recall** | 0.85 | The model is equally good at detecting Positive and Negative reviews. |

### Confusion Matrix Analysis
> *Insert your heatmap image here*
![Confusion Matrix](path_to_your_purple_image.png)

* **True Negatives (848):** Successfully identified 848 negative reviews.
* **True Positives (854):** Successfully identified 854 positive reviews.
* **Error Rate:** The False Positives (148) and False Negatives (150) are nearly symmetrical, indicating the model is **unbiased**.

---

## 💡 Key Takeaways
1.  **Text Cleaning is King:** The high accuracy is largely due to effective preprocessing (Stemming and Stopwords removal).
2.  **Balanced Data = Stable Model:** Unlike Churn prediction (which requires techniques like SMOTE), a balanced dataset yields identical Precision, Recall, and F1-Scores.
3.  **TF-IDF Effectiveness:** Using TF-IDF proved to be a robust method for capturing the context of words compared to a simple Bag of Words.

---

## 💻 Tech Stack
* **Language:** Python
* **NLP Library:** NLTK (Natural Language Toolkit)
* **Machine Learning:** Scikit-Learn
* **Visualization:** Matplotlib, Seaborn, WordCloud

## 📂 How to Run
1.  Clone the repository.
2.  Install dependencies:
    ```bash
    pip install pandas numpy scikit-learn nltk matplotlib seaborn wordcloud
    ```
3.  Run the notebook `Sentiment_Analysis.ipynb`.

---
*Created by Zinedine Daffa Izaaz*
