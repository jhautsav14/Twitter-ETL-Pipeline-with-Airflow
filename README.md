# 🐦 Twitter ETL Pipeline with Airflow

An automated ETL pipeline that extracts tweets from [@elonmusk](https://twitter.com/elonmusk), processes them, and stores the results as CSV locally or on AWS S3. The workflow is orchestrated using **Apache Airflow** for scheduled daily execution.

## 🚀 Quick Start

### 1. Clone the Repo & Install Dependencies
```bash
git clone https://github.com/your-username/twitter-etl-airflow.git
cd twitter-etl-airflow
pip install -r requirements.txt
