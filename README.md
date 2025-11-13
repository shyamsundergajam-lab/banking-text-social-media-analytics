# banking-text-social-media-analytics
“Text and social media analytics of banking tweets using Python and NLP techniques.”
# Text, Social Media & Web Analytics in Banking  
### MBA Capstone Project – University of Hyderabad  
**Author:** Gajam Shyam Sunder  
**Roll No:** 24MBMB32  

---

## 📌 Project Overview  
This project applies **Natural Language Processing (NLP)** techniques to analyze banking-related tweets and extract insights about customer experience, sentiment, complaints, and fraud concerns.  

A synthetic dataset of 1,500+ tweets was analyzed using five major NLP use cases:

1. **Sentiment Analysis**  
2. **Topic Modeling (LDA)**  
3. **Complaint Category Classification (Machine Learning)**  
4. **Named Entity Recognition (NER)**  
5. **Keyword Extraction (YAKE & RAKE)**  

The goal is to understand customer pain points in digital banking (UPI issues, customer service delays, fraud alerts, etc.) and compare public vs private banks.
## 🧵 Dataset Description

**File:** `synthetic_bank_tweets_1500_with_names.csv`

| Column Name | Description |
|------------|-------------|
| `tweet_id`          | Unique ID for each tweet |
| `text`              | Tweet content |
| `bank_type`         | Public or Private bank |
| `category`          | complaint category (failure, service, promotion, fraud) |
| `name`              | Synthetic username |
| `timestamp`         | Date/time of tweet |
| Additional columns generated in notebooks include: `vader_score`, `vader_label`, `tokens`, etc. |

Dataset is synthetic and created for academic purposes.

---

## 🚀 Use Cases

### **Use Case 1 — Sentiment Analysis (VADER)**
- Computes positive, neutral, and negative sentiment.  
- Compares sentiment distribution between public vs private banks.  
- Helps identify which bank type receives more complaints.

### **Use Case 2 — Topic Modeling (LDA)**
- Focuses on **negative tweets only**.  
- Identifies themes such as:
  - UPI/transaction failures  
  - Customer service delays  
  - App/OTP login issues  
  - Cashback/offer complaints  

### **Use Case 3 — Complaint Classification (ML Model)**
- TF-IDF vectorization + Logistic Regression  
- Classifies tweets into: *failure, service, promotion, fraud*  
- Achieved **100% accuracy** (clean synthetic dataset)  
- Includes saved ML model + vectorizer.

### **Use Case 4 — Named Entity Recognition**
- spaCy model extracts:  
  - Bank names (ORG)  
  - Monetary values (MONEY)  
  - Dates/locations (DATE, GPE)  
- Custom phrase matcher extracts:
  - UPI, debit card, net banking  
  - fraud, scam, phishing  
  - cashback, reward  

### **Use Case 5 — Keyword Extraction**
- YAKE + RAKE used to extract important keywords.  
- Highlights repeating issues like:  
  - “payment failed”  
  - “server down”  
  - “customer care delay”  
  - “cashback not received”

---

## 🛠️ Tools & Technologies

- **Python**  
- **Google Colab**  
- Libraries:  
  - pandas, numpy  
  - nltk, spaCy  
  - gensim (LDA)  
  - scikit-learn  
  - vaderSentiment  
  - YAKE, RAKE  
  - Matplotlib, Seaborn  
