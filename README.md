# Employee Experience & Workplace Culture Analysis using NLP

> **Sentiment Analysis for Emirates Airlines** - A comprehensive NLP pipeline analyzing employee experiences and public perception across multiple platforms


## Overview

This project performs **large-scale sentiment analysis** on employee discussions and customer reviews related to Emirates Airlines. By combining web scraping, NLP preprocessing, machine learning classification, and topic modeling, we extract actionable insights about workplace culture, employee satisfaction, and organizational reputation.

### Why This Project?

- **Real-world data**: Custom scraped datasets from 5+ platforms (Reddit, YouTube, Indeed, Trustpilot, Glassdoor)
- **Complete pipeline**: Data collection → preprocessing → feature extraction → modeling → insights
- **Practical approach**: Simulates real-world industry NLP workflows beyond benchmark datasets

### Objectives

Our analysis addresses:
- **Sentiment Detection**: Classify reviews as Positive / Neutral / Negative
- **Theme Discovery**: Identify recurring workplace topics and concerns  
- **Model Comparison**: Benchmark multiple ML algorithms for text classification
- **Insights Extraction**: Visualize trends using topic modeling and analytics

---

## Key Features

### Multi-Source Data Collection

Data extracted from **5 diverse platforms** for linguistic variety and reduced bias:

| Platform | Data Type | Volume |
|----------|-----------|--------|
| Reddit | Employee discussions & community insights | Discussions threads |
| YouTube | Viewer & customer comments | Comment threads |
| Indeed | Employee workplace reviews | Review submissions |
| Trustpilot | Customer experience reviews | Service reviews |
| Glassdoor | Employee feedback & company ratings | Review submissions |

### NLP Preprocessing Pipeline

Comprehensive text normalization including:
- Text cleaning & URL removal
- Emoji handling & standardization
- Tokenization & lowercasing
- Stopword removal & lemmatization
- Contraction expansion
- TF-IDF vectorization

### Sentiment Analysis

**Methods used:**
- VADER Sentiment Analyzer for lexicon-based analysis
- Manual sentiment labeling for training data
- Hybrid labeling workflow for quality assurance

### Machine Learning Models

**Trained and evaluated:**
- LinearSVC
- Logistic Regression
- Multinomial Naive Bayes
- Random Forest
- XGBoost

### Topic Modeling & Insights

Using **Latent Dirichlet Allocation (LDA)** to uncover:
- Positive workplace themes (career growth, benefits, opportunities)
- Negative employee concerns (workload, management, stress)
- Neutral operational discussions (recruitment, policies, operations)

### Data Visualizations

- Sentiment distribution charts
- Topic modeling outputs & pyLDAvis interactive visualizations
- Word clouds & frequency analysis
- Model performance comparisons
- Confusion matrices

---

## Tech Stack

**Language:**
- Python 3.8+

**Core Libraries:**
- `pandas` – Data manipulation
- `numpy` – Numerical computing
- `scikit-learn` – Machine learning & preprocessing
- `nltk` – Natural language processing
- `vaderSentiment` – Lexicon-based sentiment analysis
- `TextBlob` – Text processing
- `gensim` – Topic modeling
- `matplotlib` & `seaborn` – Visualization
- `wordcloud` – Word cloud generation
- `pyLDAvis` – Interactive topic visualization
- `BeautifulSoup` – Web scraping
- `requests` – HTTP library
- `praw` – Reddit API
- `google-api-python-client` – YouTube API

---

## Dataset Information

### Data Pipeline

```
Scrape & Collect → Filter & Clean → Preprocess → Label Sentiment → Train/Test Split → Train Models → Generate Insights
```

---

## Machine Learning Workflow

### 1. Data Collection

Data scraped from multiple platforms to maximize linguistic diversity and minimize source bias.

### 2. Data Cleaning

The preprocessing pipeline handles:
- Duplicate removal
- URL & link cleaning
- Emoji filtering & standardization
- Lowercasing & normalization
- Stopword removal
- Token standardization

### 3. Feature Extraction

Text representation techniques:
- Bag of Words (BoW)
- N-grams
- TF-IDF vectorization

### 4. Model Training

Multiple supervised learning models trained with consistent cross-validation methodology.

### 5. Evaluation Metrics

Models evaluated using:
- Accuracy
- Precision, Recall & F1-score
- Confusion matrices
- ROC-AUC analysis

---

## Results & Findings

### Key Observations

**Positive Sentiments** were strongly associated with:
- Career growth opportunities
- Competitive salary & benefits
- Travel perks
- Professional development

**Negative Sentiments** frequently referenced:
- High workload pressure
- Management challenges
- Customer-facing stress
- Operational inefficiencies

**Neutral Comments** focused on:
- Recruitment processes
- Aviation operations
- Company policies
- Factual discussions

### Model Performance

**Best Performers:**
- **LinearSVC** – Strongest performance for sparse, high-dimensional text
- **Logistic Regression** – Consistent accuracy with TF-IDF features

**Findings:**
- Tree-based methods (Random Forest) showed limitations with sparse TF-IDF features
- Linear models outperformed ensemble methods for this text classification task

### Example Outputs

The repository includes:
- Sentiment distribution charts
- Topic modeling visualizations
- Word clouds for each sentiment class
- Interactive pyLDAvis topic explorer
- Model comparison graphs

---

## Quick Start

### Prerequisites
- Python 3.8+
- pip or conda

### Installation

Clone the repository:
```bash
git clone https://github.com/your-username/employee-experience-nlp.git
cd employee-experience-nlp
```

Install dependencies:
```bash
pip install -r requirements.txt
```

Run the analysis notebook:
```bash
jupyter notebook Notebooks/employee_sentiment_analysis_pipeline.ipynb
```

---

## Project Structure

```
├── README.md
├── Datasets/
│   ├── emirates_data_final_glassdoor.csv
│   ├── emirates_employee_comments_youtube_emoji_new.csv
│   ├── final_dataset_with_manually_labelled_reddit_subset.csv
│   └── Scraped Pages/
│       ├── indeed_pages/
│       ├── reddit_pages/
│       └── trustpilot_pages/
├── Notebooks/
│   └── employee_sentiment_analysis_pipeline.ipynb
└── requirements.txt
```

---

## Team

| Contributor |
|-------------|
| **Janya Rathnakumar** |
| **Vinayak Parayil Nair** |
| **Kumail Rizvi** |
| **Laiba Shehzad** |

---

## License

This repository is intended for **educational and portfolio purposes**.