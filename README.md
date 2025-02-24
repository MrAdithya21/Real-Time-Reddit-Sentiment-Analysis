# 📌 Reddit Sentiment Analysis Using Azure & NLP

## 🔍 About the Project

This project is designed to extract, process, and analyze real-time comments from Reddit, storing them in Azure Storage for further sentiment analysis. The extracted comments undergo sentiment classification using VADER and BERT NLP models, and the results are visualized for insights.

## 🚀 Objectives

- Extract real-time Reddit comments using `praw`.
- Store the extracted data in Azure Storage Queue and process it with Azure Blob Storage.
- Convert JSON data into structured CSV format.
- Perform sentiment analysis using VADER and BERT models.
- Visualize sentiment trends, most active users, common words, and trending topics.

## 🏗 Architecture Overview

1. **Data Extraction** - Using `praw` to stream comments from Reddit.
2. **Storage Pipeline** - Sending the data to Azure Storage Queue and Blob Storage.
3. **Data Processing** - Transforming raw JSON comments into structured CSV.
4. **Sentiment Analysis** - Using VADER and BERT for sentiment classification.
5. **Data Visualization** - Creating insightful charts to understand trends and user engagement.

## 📜 Step-by-Step Workflow

### 🔹 1. Extracting Reddit Comments
- The script fetches live comments from the `r/technology` subreddit using `praw`.
- Each comment's text, timestamp, and author are stored.

### 🔹 2. Storing Data in Azure Storage
- The extracted comments are pushed into Azure Storage Queue.
- A consumer script retrieves and stores them in Azure Blob Storage for further processing.

### 🔹 3. Converting JSON to CSV
- JSON data stored in Azure Blob is retrieved and structured into a CSV format.
- The CSV file is used for further processing and analysis.

### 🔹 4. Sentiment Analysis with NLP Models
- **VADER** is used for quick lexicon-based sentiment analysis.
- **BERT** (`nlptown/bert-base-multilingual-uncased-sentiment`) is used for advanced deep-learning-based sentiment classification.

### 🔹 5. Data Visualization
- **Sentiment Distribution Pie Chart**
- **Top 10 Most Active Users**
- **Word Cloud for Most Common Words in Positive Comments**
- **Sentiment Trends Over Time**
- **Trending Topics (NER-based)**

## 🛠 Technologies Used

- **Programming Language:** Python
- **Reddit API:** `praw`
- **Cloud Platform:** Azure (Storage Queue, Blob Storage)
- **NLP Models:** VADER, BERT
- **Data Processing:** Pandas, JSON
- **Visualization:** Matplotlib, Seaborn, WordCloud

## 📊 Visualizations

## **Sentiment Distribution of Reddit Comments**
  ![image](https://github.com/user-attachments/assets/ef51ac61-0da5-40cb-96fb-6d15fb5fac0e)

## **Top 10 Most Active Users**
  ![image](https://github.com/user-attachments/assets/ddeac2ef-8cb9-4543-90f1-7c2f71914d2d)

## **Most Common Words in Positive Comments**
  ![image](https://github.com/user-attachments/assets/8cbbc190-4422-4490-9e7d-b27e71d2e6fc)

## **Sentiment Analysis using VADER & BERT**
  ![image](https://github.com/user-attachments/assets/15dd797a-4c02-4179-a840-603a2baecbdc)

## **Trending Topics Extracted from Comments**

**Top 10 Trending Topics:** `Trump (15), USA (9), US (6), Russia (5), Musk (5), Tesla (4), China (4), Ukraine (4), YouTube (3), Congress (3)`

## 📌 How to Run the Project

### 🔹 Prerequisites

- Azure Account
- Python 3.7+
- Install dependencies:
  ```bash
  pip install praw azure-storage-queue azure-storage-blob transformers pandas matplotlib wordcloud
  ```

### 🔹 Running the Scripts

#### Extract Reddit Comments
```bash
python extract_reddit_comments.py
```

#### Store in Azure Storage
```bash
python store_in_azure.py
```

#### Convert JSON to CSV
```bash
python json_to_csv.py
```

#### Perform Sentiment Analysis
```bash
python sentiment_analysis.py
```

#### Generate Visualizations
```bash
python visualize_results.py
```

## 🏆 Key Learnings

- Hands-on experience with Azure Storage and Queue Processing.
- Application of NLP models (VADER, BERT) for sentiment analysis.
- Data extraction and real-time processing using Reddit API.
- Creating impactful data visualizations to derive insights.

## 📢 Future Enhancements

- Implementing **Topic Modeling (LDA)** for deeper insights.
- Enhancing sentiment classification with **fine-tuned transformer models**.
- Deploying a **real-time dashboard** for monitoring sentiment trends.

## 🚀 Contributions & Feedback

Feel free to contribute by opening a PR or suggesting improvements!

---

**🔗 Author:** [Your GitHub Profile](https://github.com/your-profile)
