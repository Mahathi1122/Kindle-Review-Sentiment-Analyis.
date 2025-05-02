## 📚 Amazon Kindle Store Review Sentiment Analysis

### 🔍 **About the Dataset**
This project uses a 5-core dataset of Amazon Kindle Store product reviews, spanning from **May 1996 to July 2014**, containing **982,619 entries**. Each reviewer has reviewed at least 5 products, and each product has received at least 5 reviews.

**📁 Dataset Columns:**
- `asin`: Product ID (e.g., B000FA64PK)
- `helpful`: Helpfulness rating (e.g., 2/3)
- `overall`: Product rating (target variable for some analyses)
- `reviewText`: Full text of the review
- `reviewTime`: Review date
- `reviewerID`: Reviewer ID
- `reviewerName`: Reviewer's name
- `summary`: Short description/summary of review
- `unixReviewTime`: Review time in Unix timestamp

**🔗 Source:**  
Amazon Product Data by Julian McAuley, UCSD  
[http://jmcauley.ucsd.edu/data/amazon](http://jmcauley.ucsd.edu/data/amazon)

---

### 🎯 **Project Goals**
- Perform sentiment analysis on Kindle product reviews.
- Understand how review sentiment correlates with product ratings.
- Explore relationships between sentiment and review helpfulness.
- Build and evaluate a sentiment classification model.

---

### 🧼 **Best Practices Followed**

#### ✅ 1. Preprocessing and Cleaning
- Removed missing or null reviews.
- Cleaned text (lowercasing, removed HTML, URLs, special characters).
- Removed extra whitespace and standardized formatting.

#### ✅ 2. Train-Test Split
- Filtered reviews with neutral sentiment for binary classification.
- Performed 80/20 train-test split for model training and validation.

#### ✅ 3. Feature Engineering
- Created `clean_review` column with processed text.
- Computed `sentiment_score` using **TextBlob** (range: -1 to 1).
- Classified sentiment as `positive`, `negative`, or `neutral`.

#### ✅ 4. Vectorization
- Used **TF-IDF** with a maximum of 5,000 features to vectorize cleaned text.

#### ✅ 5. Model Training
- Trained a **Logistic Regression** model on vectorized features.
- Evaluated using accuracy, precision, recall, F1-score, and confusion matrix.

#### ✅ 6. Oversampling
- Applied **SMOTE** to handle class imbalance in training data.

---

### 📈 **Visualizations**
- Sentiment distribution and rating boxplots
- Confusion matrix heatmap
- Word clouds for positive and negative reviews
- Histogram of sentiment scores
- Count plot of sentiment per rating


---

### 🧠 **ML & NLP Techniques Used**
- **Logistic Regression** for sentiment classification
- **TF-IDF Vectorization** for converting text into numerical features
- **SMOTE (Synthetic Minority Oversampling Technique)** for class imbalance
- **TextBlob** for computing sentiment polarity
- **GloVe (Global Vectors for Word Representation)** for word embeddings (✅ if you used it for feature extraction or visualizations)
-


