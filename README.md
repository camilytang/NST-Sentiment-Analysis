# NST Sentiment Analysis Using Apache Spark & Kafka

Real-time sentiment analysis on New Straits Times news using Apache Spark and Kafka. Compares Logistic Regression (Spark MLlib) vs LSTM (Keras) for sentiment classification in batch and streaming modes.

## Team Members

| Team Member | Role |
|-------------|------|
| Wong Qiao Ying | Team Leader |
| Camily Tang Jia Lei | Developer |
| Ng Shu Yu | Developer |
| Muhammad Luqman Hakim | Developer |

## Technologies

| Component | Tools |
|-----------|-------|
| Web Scraping | Playwright, BeautifulSoup |
| Message Queue | Apache Kafka |
| Data Processing | Apache Spark |
| Deep Learning | Keras with TensorFlow |
| Storage & Visualization | Elasticsearch, Kibana |
| NLP | NLTK, VADER |

## System Architecture

- New Straits Times Website
  - Batch Scraper (20,000 articles) -> Elasticsearch -> Batch Training -> Spark LR + Keras LSTM
  - Live Scraper (every 60s) -> Apache Kafka -> Real-time Inference -> Predictions -> Elasticsearch + Kibana Dashboard

## Results

| Model | Accuracy | Avg Latency |
|-------|----------|-------------|
| Spark Logistic Regression | ~80% | 1325.55 ms |
| Keras LSTM | ~86% | 181.19 ms |
