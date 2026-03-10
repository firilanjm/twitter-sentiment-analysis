# Multi-Brand Twitter Sentiment Analysis

## Project Overview
This project analyzes public sentiment toward multiple brands and games using Twitter data. It classifies tweets into **Positive, Negative, Neutral, or Irrelevant** categories using **machine learning and NLP techniques**.  

**Goals:**  
1. Clean and preprocess messy social media data (remove duplicates, normalize text).  
2. Explore sentiment patterns across different topics with visualizations.  
3. Build a **Logistic Regression model** for sentiment classification.  
4. Provide insights into public perception of brands and games.  

---

## Dataset

- **Training dataset:** For model training.  
- **Validation dataset:** For model evaluation.  

**Columns:**  

| Column | Description |
|--------|-------------|
| `id` | Unique tweet identifier |
| `topic` | Brand or game the tweet is about (e.g., Google, Microsoft, FIFA) |
| `sentiment` | Sentiment label: Positive / Negative / Neutral / Irrelevant |
| `tweet` | Raw text of the tweet |

---

## Project Structure
project_root/
│
├── data/ # CSV datasets
│ ├── train_twitter_sentiment.csv
│ └── validation_twitter_sentiment.csv
├── images/ # Folder where all plots and word clouds are saved
├── twitter_sentiment.ipynb # Jupyter notebook with full analysis
├── README.md # This file
└── requirements.txt # Python dependencies


---

## Methodology

1. **Data Cleaning**  
   - Remove duplicates and missing values.  
   - Normalize text (lowercasing, trimming spaces).  

2. **Exploratory Data Analysis (EDA)**  
   - Visualize overall sentiment distribution.  
   - Visualize number of tweets per topic (top 10).  
   - Generate **word clouds** for each sentiment.  
   - Plot sentiment distribution per topic (top 10) using stacked bar charts with soft RGB colors.  

3. **Feature Engineering**  
   - Convert tweets to numerical features using **TF-IDF Vectorization**.  

4. **Model Training**  
   - Train a **Logistic Regression classifier**.  

5. **Evaluation**  
   - Evaluate the model on the validation dataset using **accuracy, precision, recall, F1-score**.  
   - Visualize results using a **confusion matrix**.  

6. **Insights**  
   - Identify which topics are generally positive or negative.  
   - Analyze common words driving each sentiment.  
   - Professional visualizations ready for portfolio or presentation.

---

## Visualizations

All plots are saved in the `images/` folder:

| Image | Description |
|-------|-------------|
| `general_dist.png` | Overall tweet sentiment distribution |
| `tweet_count_top10.png` | Number of tweets for top 10 topics |
| `sentiment_distribution_top10.png` | Stacked bar chart of sentiment distribution for top 10 topics |
| `wordcloud_all.png` | Word cloud of all tweets |
| `wordcloud_positive.png` | Word cloud of positive tweets |
| `wordcloud_negative.png` | Word cloud of negative tweets |
| `wordcloud_neutral.png` | Word cloud of neutral tweets |
| `wordcloud_irrelevant.png` | Word cloud of irrelevant tweets |

| `confusion_matrix.png` | Confusion matrix showing model performance on validation data |

---

## Tech Stack

- **Python Libraries:** pandas, matplotlib, seaborn, scikit-learn, wordcloud  
- **Machine Learning:** Logistic Regression  
- **NLP:** TF-IDF Vectorization for text features  
- **Visualization:** Matplotlib & Seaborn, WordCloud  

---

## How to Run

1. Clone the repository or download the files.  
2. Ensure the CSV datasets (`train_twitter_sentiment.csv` and `validation_twitter_sentiment.csv`) are in the root folder.  
3. Open the Jupyter notebook `twitter_sentiment_notebook.ipynb`.  
4. Run all cells to generate cleaned data, visualizations, and model results.  
5. All plots will be automatically saved in the `images/` folder.  
