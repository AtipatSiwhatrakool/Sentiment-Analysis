# Sentiment-Analysis Pipeline

This is a side project to show a real-time sentiment analysis pipeline using Docker.

1.  A Python script (`kafka-producer`) uses `Faker` to create random sentences every 5 seconds.
2.  It sends these sentences to a Kafka topic called `sentence`.
3.  A second Python script (`kafka-consumer`) listens to that topic.
4.  It uses `nltk` (Vader) to check the sentiment (a positive/negative score) of each sentence.
5.  It saves the sentence and its score to a PostgreSQL database.
6.  A Streamlit app (`ui`) shows the data from the database and refreshes every 5 seconds.

## Tech Stack

* Docker & Docker Compose
* Kafka (as the message queue)
* PostgreSQL (to store data)
* Python
* Streamlit (for the dashboard)
* NLTK (for analysis)
* Faker (to generate data)

Open your browser and go to:
**`http://localhost:8501`**

You should see new sentences appearing on the dashboard.
