# Phishing Email Detector — Behavioral & Lexical Machine Learning Approach

A machine learning classifier that detects phishing emails by combining
hand-crafted behavioral features (urgency, authority, URL count) with
TF-IDF text vectorization, achieving 97.3% accuracy.

## Overview
This project investigates whether combining psychologically-grounded
behavioral indicators (urgency and authority cues, empirically linked to
phishing susceptibility in prior research) with broader lexical text
features improves phishing email detection compared to either approach
alone.

## Dataset
- Combined dataset of 68,921 emails from the CEAS_08 and Enron corpora
  (Kaggle: "Phishing Email Dataset")
- 51.97% phishing, 48.03% legitimate

## Method
- Behavioral features: urgency keyword count, authority keyword count, URL count
- TF-IDF vectorization (max 1,000 features) on email subject + body
- Logistic Regression classifier, 80/20 train-test split

## Results
|        Model                    |Accuracy    |
|---------------------------------|------------|
| Majority-class baseline         |   51.97%   |
| Behavioral features only        |   49.47%   |
| **TF-IDF + behavioral (final)** | **97.30%** |

## How to Run
1. Download the dataset from Kaggle:[(https://www.kaggle.com/datasets/naserabdullahalam/phishing-email-dataset)]
2. Install dependencies: `pip install -r requirements.txt`
3. Open `phishing_detector.ipynb` and run all cells

## Future Work
- Test generalization on out-of-distribution phishing samples
- Expand behavioral features (scarcity, social proof)
- Compare additional algorithms (Random Forest, XGBoost)

## Author
Zainab S. Shaikh — MSc IT Student
