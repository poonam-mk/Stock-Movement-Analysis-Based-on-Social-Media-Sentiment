# Stock-Movement-Analysis-Based-on-Social-Media-Sentiment
Created a Stock Movement Analysis Based on Social Media Sentiment by scrapping reddit data and perfomed ML algorithms on it to get appropriate model
Stock Prediction Using Reddit Data

This project aims to predict stock movements by leveraging insights from Reddit discussions. By analyzing user sentiment, engagement, and content relevance from subreddits like r/wallstreetbets, we build a machine learning model to make informed predictions.
Overview-
The stock market is heavily influenced by public sentiment and discussion. This project collects and analyzes Reddit data to predict stock market trends. By using machine learning and natural language processing techniques, we aim to understand the relationship between online chatter and stock performance.

Data Collection
We used the praw library to scrape Reddit posts and comments from finance-focused subreddits. The collected data includes:
-Post titles and bodies
-Timestamps
-Engagement metrics (upvotes, comment counts)

Key Steps:
Extract posts within specific timeframes relevant to stock market hours.
Filter posts based on financial keywords like "stock," "buy," or specific ticker symbols.
Store data in a structured format for further processing.

Feature Extraction
We extracted meaningful features from the Reddit data:
Sentiment Analysis: Used TextBlob to calculate polarity and subjectivity scores.
Text Representations: Converted post content into TF-IDF vectors.
Engagement Metrics: Included metrics like upvote ratios and comment counts.
Temporal Features: Aligned post timestamps with stock market trading hours.
These features help capture the essence of public sentiment and its potential influence on stock movements.

Modeling and Evaluation
Models Used:
-Logistic Regression: A baseline model for binary classification.
-Random Forest Classifier: A more sophisticated model to capture complex patterns.

Evaluation Metrics:
Accuracy: Measures overall correctness.
Confusion Matrix: Evaluates false positives and false negatives.
Precision and Recall: Ensures accurate buy/sell signal predictions.

Performance Insights:
The Random Forest model achieved an accuracy of ~78%, significantly outperforming the baseline Logistic Regression model. However, it struggled with predicting rare market spikes.

Challenges and Solutions
API Rate Limits: Managed by optimizing requests and implementing caching mechanisms.
Noisy Data: Addressed by filtering irrelevant content and deduplication.
Timezone Alignment: Used pytz to standardize timestamps to market hours.

Future Expansions
Data Sources: Integrate data from Twitter, news headlines, and economic indicators.
Advanced NLP Models: Replace TextBlob with BERT or similar models for better sentiment analysis.
Granular Stock Analysis: Shift focus from general trends to specific stock ticker mentions.
Real-Time Predictions: Develop an automated pipeline for live sentiment tracking and predictions.

How to Use

Clone the repository.
git clone <[repo-url](https://github.com/poonam-mk/Stock-Movement-Analysis-Based-on-Social-Media-Sentiment/tree/main)>

Install required dependencies:
pip install -r requirements.txt

Set up your Reddit API credentials in a .env file:
CLIENT_ID=<your-client-id>
CLIENT_SECRET=<your-client-secret>
USER_AGENT=<your-user-agent>

Run the data collection script:

python scrape_reddit.py




Process the data and train the model:

python train_model.py

Evaluate predictions and visualize results.

Contributing

Feel free to fork this repository and submit pull requests. Suggestions and improvements are always welcome!
