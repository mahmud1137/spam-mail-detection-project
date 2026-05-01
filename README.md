# spam-mail-detection-project
Spam mail detection system using machine learning and NLP to classify emails as spam or not spam. Includes data preprocessing, feature extraction, and model training to improve accuracy and enhance email security by filtering unwanted messages automatically.

## Project Overview
This project focuses on building a robust text classification pipeline to detect spam emails. The workflow involves extensive text preprocessing, feature extraction, and model training. The notebook is originally set up to run in Google Colab, leveraging a dataset stored in Google Drive, but can easily be adapted for local execution.

## Features & NLP Preprocessing
To prepare the raw email text for the machine learning model, the following Natural Language Processing steps are applied:
* **Lowercasing:** Standardizing the dataset by converting all text to lowercase.
* **Punctuation Removal:** Stripping out special characters and punctuation to reduce textual noise.
* **Lemmatization:** Reducing words to their base or dictionary form using NLTK's `WordNetLemmatizer`.
* **Feature Extraction (TF-IDF):** Transforming the cleaned, lemmatized text into numerical vectors using Scikit-Learn's `TfidfVectorizer` (capped at 5,000 maximum features).
* **Label Encoding:** Converting the categorical target labels ('spam', 'ham') into a binary numerical format (0 and 1) using `LabelEncoder`.

## Model & Evaluation
While the notebook imports several popular algorithms (such as Multinomial Naive Bayes, Logistic Regression, Random Forest, and Decision Trees), the primary model trained in this pipeline is a **Linear Support Vector Classifier (`LinearSVC`)**. 

The model's performance is thoroughly evaluated using:
* **Accuracy Score**
* **Classification Report:** Detailed metrics including Precision, Recall, and F1-Score.
* **Confusion Matrix:** Visualized as an easy-to-read heatmap using `seaborn` and `matplotlib` to analyze false positives and false negatives.

## Technologies & Libraries Used
* **Data Manipulation:** `pandas`, `string`, `re`
* **NLP Processing:** `nltk` (WordNet, Stopwords)
* **Machine Learning:** `scikit-learn` (TF-IDF, LinearSVC, metrics, train_test_split)
* **Class Imbalance Handling:** `imblearn` (SMOTE)
* **Data Visualization:** `matplotlib.pyplot`, `seaborn`
* **Environment:** Google Colab / Jupyter Notebook
