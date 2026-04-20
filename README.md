# SMS Spam Classification 

##  Overview

This project implements an **SMS Spam Classifier** using:

*  **Naive Bayes**
*  **Support Vector Machine (SVM)** with RBF kernel

The dataset used is the **SMS Spam Collection v.1**, containing **5,574 labeled SMS messages**.

---

##  Dataset

* **Total messages:** 5,574
* **Ham (legitimate):** 4,827 (86.6%)
* **Spam:** 747 (13.4%)

Each message is labeled as:

* `ham` → legitimate message
* `spam` → unwanted message

---

##  Data Processing Pipeline

### 1. Text Preprocessing

* Split messages into words using spaces
* Convert all words to lowercase

### 2. Dictionary Creation

* Build a word-to-index mapping
* Only include words appearing in **at least 5 messages**

### 3. Feature Extraction

* Convert messages into a **word count matrix**
* Rows = messages
* Columns = words

---

##  Naive Bayes Model

### Approach

We implement a **Multinomial Naive Bayes classifier**:

* Compute:

  * ( P(word | spam) )
  * ( P(word | ham) )
  * ( P(spam) )

* Use **Laplace smoothing**:
  [
  P(w_k | y) = \frac{count(w_k, y) + 1}{\sum count(w, y) + V}
  ]

### Prediction

* Use **log probabilities** to avoid underflow:
  [
  \log P(y|x) = \sum x_i \log P(w_i|y) + \log P(y)
  ]

* Predict class with higher probability

### Output

* Accuracy on test set
* Top 5 most indicative spam words

---

## ⚙️ Support Vector Machine (SVM)

### Model Details

We implement a custom **kernel SVM** using:

* **RBF (Gaussian) kernel**
* Binary classification: spam (1) vs ham (0)

### Kernel Function

[
K(x, z) = \exp\left(-\frac{||x - z||^2}{2r^2}\right)
]

Where:

* ( r ) = radius (hyperparameter)

---

### Training Algorithm

* Convert features to **binary (presence/absence)**
* Use **stochastic gradient descent-like updates**
* Maintain:

  * `alpha` (dual variables)
  * `alpha_avg` (averaged for stability)

---

### Prediction

* Compute kernel between test and training data
* Predict using:

[
\hat{y} = \text{sign}(K \cdot \alpha)
]

* Convert output to:

  * `1` → spam
  * `0` → ham

---

### Hyperparameter Tuning

We select the best radius from:

```python
[0.01, 0.1, 1, 10]
```

Based on **validation accuracy**.

---

##  Project Structure

```
project/
│
├── data/
│   ├── train.tsv
│   ├── val.tsv
│   └── test.tsv
│
├── output/
│
├── main.py
├── svm.py
├── util.py
└── README.md
```

---

##  How to Run

```bash
python main.py
```

---

##  Outputs

Generated in `output/`:

* `dictionary.json` → word dictionary
* `sample_train_matrix.txt` → sample feature matrix
* `naive_bayes_predictions.txt` → predictions
* `top_indicative_words.json` → top spam words
* `optimal_radius.json` → best SVM parameter

---

##  Results

The program prints:

* Naive Bayes accuracy
* Top 5 spam-indicative words
* Best SVM radius
* SVM accuracy

---

##  License

Dataset provided by:

* Tiago Agostinho de Almeida
* José María Gómez Hidalgo

Usage:

* Free for research
* Must cite original paper

---

##  Summary

This project demonstrates:

* Text preprocessing & feature engineering
* Probabilistic classification (Naive Bayes)
* Kernel-based classification (SVM)
* Model comparison & tuning


