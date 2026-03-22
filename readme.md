
---

# News Web Scraper & MongoDB Pipeline

## Project Overview

This project implements an automated news data pipeline that scrapes trending articles from multiple Taiwanese news platforms, processes the data, and stores it in a structured MongoDB database for further analysis.

The system is designed to simulate a lightweight **data engineering + data science ingestion workflow**, integrating web scraping, data cleaning, and database storage.

---

## Tech Stack

* **Python** (requests, BeautifulSoup)
* **MongoDB** (NoSQL database)
* **pymongo** (database interface)
* **Linux / Shell** (service setup & automation)

---

##  Features

### 1. Multi-source Data Collection

* Scrapes top news from:

  * UDN (聯合報)
  * Liberty Times (自由時報)
  * Yahoo News
* Handles different HTML structures across platforms

### 2. Data Normalization

* Standardizes fields:

  * `title`
  * `url`
  * `date`
  * `source`
* Ensures consistent schema across heterogeneous sources

### 3. Raw Data Preservation

* Stores **raw HTML** alongside structured data
* Enables:

  * future re-parsing
  * feature extraction (NLP, sentiment analysis)
  * reproducibility

### 4. MongoDB Integration

* Automated insertion into local MongoDB
* Designed for scalability and flexible schema evolution
* Supports downstream analytics and querying

### 5. Debugging & Observability

* Logs MongoDB status and process state
* Outputs:

  * JSON preview
  * raw HTML snapshot
  * database verification results

---

##  Data Schema

```json
{
  "title": "新聞標題",
  "url": "文章連結",
  "date": "抓取時間",
  "source": "新聞來源",
  "raw_html": "原始網頁內容"
}
```

---

## Data Science Value

This project is not just a scraper — it establishes a **data pipeline foundation** for multiple data science applications:

### 1. NLP / Text Mining

* Topic modeling (LDA)
* Keyword extraction
* Named Entity Recognition (NER)

### 2. Sentiment Analysis

* Analyze media bias across sources
* Detect public opinion trends

### 3. Trend Detection

* Identify breaking news patterns
* Compare coverage differences between platforms

### 4. Dataset Creation

* Builds a continuously growing corpus for:

  * training ML models
  * fine-tuning LLMs

---

## Business / Industry Impact

### 1. Media Monitoring System

* Track competitors’ news coverage
* Monitor brand mentions in real-time

### 2. Decision Support

* Extract trends for strategic insights
* Support marketing or PR decisions

### 3. Data Infrastructure Prototype

* Demonstrates ability to build:

  * ETL pipelines
  * data ingestion systems
  * scalable storage solutions

### 4. AI Product Integration

* Can be extended into:

  * news recommendation systems
  * chatbot knowledge base (RAG)
  * automated summarization tools

---

## Skills Demonstrated (Resume-Oriented)

* Data Engineering (ETL pipeline design)
* Web Scraping & Data Extraction
* NoSQL Database Management (MongoDB)
* Data Cleaning & Structuring
* Debugging & System Setup (Linux services)
* Handling Unstructured Data (HTML)

---

## Future Improvements

* Add scheduler (cron / Airflow)
* Implement deduplication logic
* Integrate NLP pipeline (spaCy / transformers)
* Build REST API for data access
* Deploy on cloud (AWS / GCP)

---

## Summary

This project demonstrates the ability to:

* collect real-world unstructured data
* transform it into usable datasets
* design a scalable data pipeline

It reflects practical skills directly applicable to **data science, data engineering, and AI product development roles**.

---

demo in colab: https://colab.research.google.com/drive/13QhNedQt4STnqPZ6iKYDvq-zsu0JRhn1?usp=sharing
