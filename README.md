# Spam-Classifier

A Python-based machine learning pipeline for detecting SMS spam messages using classic text-classification techniques.

---

## Overview

This project implements a spam-filtering system that:  
- Ingests and cleans the **SMS Spam Collection** dataset  
- Extracts features via **CountVectorizer** and **TF–IDF**  
- Trains multiple classifiers (Multinomial Naive Bayes, Logistic Regression, SVM)  
- Evaluates performance using accuracy, precision, recall, and ROC–AUC metrics

---

## Dataset

The **SMS Spam Collection** is a public set of 5,574 English, real and non-encoded messages tagged as “ham” (legitimate) or “spam”.

---

## Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/SoheilMehrizi/Spam-Classifier.git
   cd Spam-Classifier
   ```

2. **Create and activate a virtual environment**
   ```bash
   python3 -m venv venv
   source venv/bin/activate      # Windows: venv\Scripts\activate
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Download the dataset**
   Place `spam.csv` (or `SMSSpamCollection`) into the `data/` directory.

---

## Usage

1. **Run the Jupyter notebook**
   ```bash
   jupyter notebook main_lab.ipynb
   ```
   This notebook performs data preprocessing, feature extraction, model training, and evaluation.

2. **Or run the training script**
   ```bash
   python train.py
   ```

3. **Inspect results**
   - Classification reports (accuracy, precision, recall, F1)
   - ROC curves for each classifier

---

## Modeling Pipeline

1. **Text Cleaning & Tokenization**  
2. **Vectorization**  
   - `CountVectorizer`  
   - `TfidfTransformer`  
3. **Model Training**  
   - **Multinomial Naive Bayes**  
   - **Logistic Regression**  
   - **Support Vector Machine**  
4. **Hyperparameter Tuning** (Grid Search)  
5. **Model Evaluation**  

---

## Evaluation

| Model                   | Accuracy | Precision | Recall | ROC–AUC |
|-------------------------|:--------:|:---------:|:------:|:-------:|
| Multinomial Naive Bayes |  0.98    |   0.97    |  0.94  |  0.98   |
| Logistic Regression     |  0.99    |   0.98    |  0.95  |  0.99   |
| SVM                     |  0.99    |   0.98    |  0.94  |  0.99   |

*Note: Metrics may vary depending on train/test split.*

---

## Contributing

Contributions are welcome! Please fork the repository and submit a pull request with your changes.

---

## License

This project is licensed under the **MIT License**. See [LICENSE](LICENSE) for details.
