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
