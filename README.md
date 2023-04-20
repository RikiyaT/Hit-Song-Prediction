# 🎵 Hit Song Predictor

Predict the likelihood of a song becoming a hit with **audio features** and **lyric sentiment analysis**! This project combines music information retrieval techniques, natural language processing, and machine learning to create an exciting and innovative approach to predicting hit songs. Stay ahead of the curve in the music industry by leveraging the power of data!

## My Project Overview

- Scrapes a dataset of **Top 200 songs** from the US in 2023/Jan&Feb using `BeautifulSoup`
- Retrieves audio data of all songs using the `Spotify API`
- Retrieves lyrics of all songs using the `Musixmatch API`
- Cleans and preprocesses the lyrics text using `nltk`
- Performs sentiment analysis on the lyrics using `BERT` and `VADER` for sentiment scores
- Compares the performance of datasets with only audio features (default dataset) and datasets with sentiment analysis (new dataset)
- Predicts hit songs using `Gradient Boosting`, `Random Forest`, and `SVM` classifiers
- Analyzes the predictions using `Ridge recursion` and `ElasticNet` analysis

## Explanation of Folders

**rankingdata.ipynb** : this file retrieves the top charts from Spotify using BeautifulSoup.

**makingcsvfile.ipynb**, **combine.ipynb**, **addlyrics.ipynb** : these file retrieves and combines the data to make csv files.

**eval_lyrics.ipynb** : this file analyzes the sentiment of the lyrics using `BERT` and `VADER`.

**evaluation.ipynb** : this file uses `Gradient Boosting`, `Random Forest`, and `SVM` classifiers to predict hit songs. It also contains `Ridge recursion` and `ElasticNet recursion` to analyze the predictions made.



## Libraries and Dependencies

This project relies on numerous Python libraries to work with data, APIs, and machine learning models. All dependencies can be found in the `requirements.txt` file. To install the required packages, simply run the following command:

`pip install -r requirements.txt`

## Dataset Preparation

1. **Scraping the Data**

   - Use `BeautifulSoup` to scrape weekly Top 200 songs from a specified source
   - Store the scraped song data in a DataFrame

2. **Spotify API**

   - Authenticate with `Spotify API` using `SpotifyClientCredentials`
   - Retrieve audio features for each song using `spotipy`

3. **Musixmatch API**

   - Authenticate with `Musixmatch API`
   - Retrieve lyrics for each song using `lyricsgenius` package

4. **Lyrics Text Cleaning**

   - Use `nltk` to tokenize, remove stopwords, and perform other text preprocessing tasks

5. **Sentiment Analysis**

   - Analyze the sentiment of the cleaned lyrics using `BERT` and `VADER`
   - Assign a sentiment score for each song

6. **Creating Datasets**

   - Create a dataset with only audio features (default dataset)
   - Create a dataset with audio features and sentiment scores (new dataset)

## Model Training and Evaluation

1. **Splitting the Data**

   - Use `train_test_split` to split the datasets into training and testing sets

2. **Model Selection**

   - Train `Gradient Boosting`, `Random Forest`, and `SVM` classifiers on both datasets

3. **Model Evaluation**

   - Evaluate the performance of the classifiers using metrics like `classification_report` and `confusion_matrix`

4. **Ridge Recursion and ElasticNet Analysis**

   - Perform `Ridge recursion` and `ElasticNet` analysis to compare predictions
   
## My Results

Using the dataset of January and Feburary 2023 TopChart US, my results show that the Gradient Boost is the best method to make a hit song prediction.



## 🚀 Getting Started

1. Clone this repository:

git clone `https://github.com/your_username/hit-song-science-predictor.git`


2. Install the required packages:

pip install -r requirements.txt


3. Set up your API keys for Spotify and Musixmatch as environment variables or add them to the script.

4. Run the Jupyter Notebook to start predicting hit songs! If you want to know the latest hit song predictions, I recommend you to get the dataset of the latest top chart from `Spotify API` and analyze it
