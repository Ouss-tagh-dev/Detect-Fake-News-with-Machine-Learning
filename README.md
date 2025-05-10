# Detect-Fake-News-with-Machine-Learning

## Project Preparation - Fake News Classification

### 1. Dataset Overview

This project uses the **Fake News dataset** to classify news articles as real or fake. The dataset is loaded and explored using a Jupyter notebook located in the `1 project preparation` folder.

### 2. Notebook: `fakeNewsDatasetOverview.ipynb`

The notebook **fakeNewsDatasetOverview.ipynb** contains code for the following tasks:
- **Loading the dataset**: The dataset is loaded from a CSV file `news_articles.csv` located in the `dataset` folder.
- **Exploration**: The code prints the first few rows of the dataset, checks basic information, and displays the data types and column names.

#### Key actions in the notebook:
- **Data Loading**: The dataset is read into a Pandas DataFrame.
- **Data Inspection**: Displays the first few records, the shape of the dataset, column names, and data types.


### 3. Data Cleaning and Preprocessing

The **data cleaning** is done in the notebook **fakeNewsDataCleaning.ipynb** located in the `2_data_cleaning` folder. This notebook performs the following steps:
- Identifies and displays rows with missing values.
- Identifies and displays duplicated rows.
- Removes rows with missing values and duplicates.
- Saves the cleaned dataset as `news_articles_cleaned.csv` in the `dataset` folder.

### 4. News Source Credibility Analysis

The **credibility analysis** is performed in the notebook **NewsSourceCredibilityAnalysis.ipynb**, located in the `3 news source credibility analysis` folder.

This notebook includes:
- **Grouping articles by `site_url` and `label`** (Real/Fake).
- **Calculating the percentage** of real and fake news for each news source.
- **Sorting the sources** to identify:
  - The **top 10 most credible** sources (highest percentage of real news).
  - The **top 10 least credible** sources (lowest percentage of real news).
- **Displaying the results** in a clear, ranked list.

### 5. Detecting Keywords Associated with Fake News

The **keyword detection** is performed in the notebook **DetectingKeywordsAssociatedWithFakeNews.ipynb**, located in the `4 detecting keywords associated with fake news` folder.

This notebook includes:
- **Tokenizing** the words in article titles and texts.
- **Removing stopwords** (common words) and non-alphabetic tokens.
- **Counting word frequencies** specifically for articles labeled as "Fake."
- **Identifying the top 5 most common keywords** in:
  - Fake news titles.
  - Fake news texts.
- **Displaying the results** with the most frequent words and their counts.

### 6. News Title & Text Length Analysis

The **length analysis** is performed in the notebook **NewsTitleAndTextLengthAnalysis.ipynb**, located in the `5 news title & text length analysis` folder.

This notebook includes:
- **Calculating the length** (in characters) of news titles and texts.
- **Separating data** between real and fake news articles.
- **Computing the average length** for:
  - Real news titles.
  - Fake news titles.
  - Real news texts.
  - Fake news texts.
- **Visualizing the comparison** with a bar chart showing average lengths.

### 7. Detecting Sensationalism in Fake News

The **sensationalism detection** is performed in the notebook **DetectingSensationalismInFakeNews.ipynb**, located in the `6_detecting_sensationalism_in_fake_news` folder.

This notebook includes:
- **Defining sensational keywords** (e.g., shocking, unbelievable, explosive).
- **Applying detection** on news text to mark sensationalism.
- **Building a contingency table** comparing sensationalism presence with article labels (real or fake).
- **Running a chi-square test** to check if there is a statistically significant association between sensationalism and fake news.

### 8. Analyzing Emotion in Fake News with NLP

The **sentiment analysis** is carried out in the notebook **AnalyzingEmotionInFakeNewsWithNLP.ipynb**, located in the `7 analyzing emotion in fake news with nlp` folder.

This notebook performs:
- **Sentiment analysis** using NLTK’s VADER tool.
- **Classifying each article’s text** as positive, negative, or neutral.
- **Adding a new column** `Sentiment` to the dataset showing the detected sentiment.
- **Displaying results** for manual inspection of sentiment labels.

This step helps understand the emotional tone often used in fake vs. real news.

### 9. Detecting Fake News with Feature Engineering

The notebook **DetectingFakeNewsWithFeatureEngineering.ipynb**, located in the `8_detecting_fake_news_with_feature_engineering` folder, implements a simple feature engineering approach to predict fake news.

Key components:
- **Top keywords extraction**: Identifies the top 10 most frequent words in fake news articles.
- **Source analysis**: Calculates the percentage of fake news per `site_url`.
- **Prediction function**: Uses both title keyword presence and the source’s fake news percentage to predict whether a given article is fake or real.
- **Test predictions**: Runs example predictions to demonstrate the approach.

This part integrates keyword features and metadata to enhance fake news detection.


### 10. Detecting Fake News with Logistic Regression

The notebook **DetectingFakeNewsWithLogisticRegression.ipynb**, located in the `9 detecting fake news with logistic regression` folder, demonstrates the use of **Logistic Regression** combined with **TF-IDF vectorization** for fake news detection.

Key components:
- **Data Preprocessing**: The dataset is checked for missing values, and label encoding is applied to the target labels.
- **Feature Extraction**: **TF-IDF** is used to convert text data into numerical features.
- **Modeling**: A **Logistic Regression** model is trained using the vectorized text data.
- **Prediction**: The model predicts whether a given news article is real or fake, achieving an accuracy score on the test set.
- **Test Prediction**: An example news article is used to demonstrate the prediction function.

This approach showcases a basic yet effective pipeline for fake news classification.
