# 🐦 Twitter ETL Pipeline with Airflow

An automated ETL pipeline that extracts tweets from [@elonmusk](https://twitter.com/elonmusk), processes them, and stores the results as CSV locally or on AWS S3. The workflow is orchestrated using **Apache Airflow** for scheduled daily execution.

---

## 🧠 How It Works

This project follows a classic **ETL (Extract-Transform-Load)** workflow, automated using **Apache Airflow**:

1. **Extract**  
   Using the Twitter API via the Tweepy library, the script fetches the latest tweets from the user **@elonmusk** (or any handle you configure). This includes tweet text, timestamp, likes, and retweets.

2. **Transform**  
   The raw data is cleaned and refined:
   - Only relevant columns are selected
   - Null values are removed
   - Timestamps are formatted
   - Text is stripped of unwanted characters or formatting

3. **Load**  
   The cleaned data is:
   - Saved locally as `refined_tweets.csv`, or
   - Uploaded to AWS S3 (optional) for scalable cloud storage

4. **Schedule**  
   Apache Airflow manages and schedules this workflow:
   - DAG (Directed Acyclic Graph) defines daily execution
   - You can change the schedule in `twitter_dag.py`
   - All logs and history are visible in the Airflow web UI

---

## 🚀 Quick Start

### 1. Clone the Repo & Install Dependencies
```bash
git clone https://github.com/your-username/twitter-etl-airflow.git
cd twitter-etl-airflow
pip install -r requirements.txt
