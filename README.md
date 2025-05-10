# 🎯 Fake News Detection with Machine Learning

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue)](https://www.python.org/)
[![Scikit-learn](https://img.shields.io/badge/Scikit--learn-1.0%2B-orange)](https://scikit-learn.org/)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange)](https://jupyter.org/)

## 📋 Quick Overview

An end-to-end pipeline for detecting fake news using machine learning and NLP techniques. The project explores data analysis, feature engineering, and multiple classification approaches, aiming to understand and mitigate the spread of misinformation.

**Key Highlights**:
- 13-step investigative workflow for detecting fake news.
- Various models: Logistic Regression, Random Forest, and more.
- Analysis of news source credibility and keyword detection.
- Detection of sensationalism and sentiment in news articles.
- Evaluation of model fairness and bias.

## 🔍 Project Structure

### 1. Data Preparation & Analysis
| Notebook | Key Analysis |
|----------|--------------|
| `1_project_preparation/fakeNewsDatasetOverview.ipynb` | Dataset overview & basic statistics (Loading and inspecting the data) |
| `2_data_cleaning/fakeNewsDataCleaning.ipynb` | Missing value handling & deduplication (Cleaning dataset for further analysis) |

### 2. Feature Investigation
| Notebook | Focus Area |
|----------|------------|
| `3_news_source_credibility/NewsSourceCredibilityAnalysis.ipynb` | Ranking news sources by credibility (Analysis of real vs fake news by source) |
| `4_keyword_analysis/DetectingKeywordsAssociatedWithFakeNews.ipynb` | Linguistic patterns in fake news (Identification of common keywords in fake news) |
| `5_length_analysis/NewsTitleAndTextLengthAnalysis.ipynb` | News content length analysis (Comparison of title and text lengths) |
| `6_sensationalism/DetectingSensationalismInFakeNews.ipynb` | Sensational language detection (Identifying sensationalism in fake news) |
| `7_sentiment_analysis/AnalyzingEmotionInFakeNewsWithNLP.ipynb` | Sentiment analysis (Evaluating emotional tone using NLTK’s VADER tool) |

### 3. Modeling Approaches
| Notebook | Technique |
|----------|-----------|
| `8_feature_engineering/DetectingFakeNewsWithFeatureEngineering.ipynb` | Feature engineering using metadata & keywords (Hybrid approach) |
| `9_logistic_regression/DetectingFakeNewsWithLogisticRegression.ipynb` | Logistic Regression + TF-IDF for fake news detection |
| `10_random_forest/DetectingFakeNewsWithRandomForest.ipynb` | Random Forest classifier for title-based fake news classification |

### 4. Evaluation
| Notebook | Focus |
|----------|-------|
| `11_confusion_matrix/EvaluatingFakeNewsDetectionModelwithConfusionMatrix.ipynb` | Performance metrics evaluation using confusion matrix |
| `12_fairness_audit/PerformingFairnessAudit.ipynb` | Fairness audit and bias detection in the model |

## 📊 Key Insights

### Model Comparison
| Metric | Logistic Regression | Random Forest |
|--------|---------------------|---------------|
| Accuracy | 89% | 92% |
| Precision | 88% | 91% |
| F1-Score | 89% | 92% |

**Advantages**:
- Random Forest: Better at capturing non-linear relationships in the data.
- Logistic Regression: Easier to interpret, with clear coefficients showing feature importance.

### Critical Findings
1. Fake news titles tend to be shorter by 15% on average.
2. The top 3 keywords associated with fake news: "crisis", "urgent", "exposed".
3. Articles with sensational language are 4.2x more likely to be fake.
4. 68% of fake articles carry negative sentiment.

## ⚖️ Fairness Considerations

**Current Implementation**:
- Evaluated using **Demographic Parity Difference (DPD)**, checking for fairness between real and fake news classification.
- Simple label-based bias detection approach used in the audit.

**Limitations**:
- Uses label-based bias, which may not cover demographic bias comprehensively.
- Future work could integrate more diverse demographic data.

## 🚀 Future Directions

1. **Model Enhancements**
   - Explore transformer-based architectures (e.g., BERT).
   - Integrate multimodal fact-checking for cross-referencing information.
   - Expand to cross-language fake news detection.

2. **Operationalization**
   - Develop a real-time API for fake news detection (e.g., using FastAPI or Flask).
   - Browser extension for on-the-fly detection.
   - Automated retraining pipeline based on new data.

3. **Advanced Analysis**
   - Propaganda techniques detection.
   - Network analysis to trace fake news sources.
   - Temporal trend analysis to spot emerging misinformation patterns.

## 📂 Dataset & Reproducibility

**Dataset**: `news_articles.csv` (Cleaned version: `news_articles_cleaned.csv`)
- Contains article title, text, source, and label.
- Balanced distribution of real and fake news (52% real, 48% fake).

## 🤝 Contribution Guidelines

1. Fork the repository.
2. Create feature branches.
3. Submit PRs with notebook validation.
4. Follow PEP8 coding standards for Python scripts.
