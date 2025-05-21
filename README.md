# 🌱 ESG Score Prediction Project

This project aims to **predict ESG (Environmental, Social, Governance) grades of companies** based on ESG scores from 2020 to 2023. We collected publicly available ESG tables through web scraping, performed thorough preprocessing and visualization, and built machine learning models to classify ESG performance levels.

---

## 📁 Project Structure

```
ESG-Score-Prediction/
├── #1_esg_table_scraper.ipynb             # Web scraping ESG tables (2020–2023)
├── #2_data_preprocessing_visualization.ipynb  # Data cleaning and visualization
├── #3_ML.ipynb                             # ML classification model and evaluation
├── esg_2020.csv ~ esg_2023.csv                 # Raw yearly ESG data
├── esg_after_preprocessing.csv                 # Cleaned data for modeling
├── esg_merge.csv                               # Merged data across all years
└── README.md                                   # You are here
```

---

## 🧾 Project Overview

- **Objective**: Predict ESG grade classes (e.g., Excellent, Moderate, Poor) based on tabular ESG indicators.
- **Approach**:
  - Scrape ESG tables from multiple years (2020–2023)
  - Preprocess and visualize numerical/categorical variables
  - Build classification models using scikit-learn

---

## 🧹 Data Preprocessing

- Removed null and redundant columns
- Standardized numeric features (`E`, `S`, `G`, total ESG score)
- Merged annual datasets into a single CSV (`esg_merge.csv`)
- Visualizations included:
  - ESG score distributions by year
  - Correlation heatmaps
  - ESG category performance by industry/size

---

## 🤖 Machine Learning

- **Goal**: Predict ESG class label using structured features
- **Target Variable**: ESG class (categorized into multiple bins)
- **Features**:
  - Environmental, Social, Governance scores
  - Total ESG score
  - Industry type, company size, year

### Models Used

| Model                  | Notes                              |
|------------------------|-------------------------------------|
| Random Forest Classifier | Best performing model (accuracy > 85%) |
| K-Nearest Neighbors    | Moderate performance                |
| Logistic Regression    | Baseline linear classifier          |
| SVM (Support Vector Machine) | Evaluated with kernel options    |

- **Evaluation Metrics**:
  - Accuracy
  - Classification report
  - Confusion matrix

---

## 📊 Key Findings

- `G (Governance)` score had the highest feature importance in most models.
- Companies with high total ESG scores were consistently classified as "Excellent".
- Random Forest outperformed other models with strong generalization across years.

---

## 🔧 Technologies

- Python 3.x
- `pandas`, `numpy`
- `matplotlib`, `seaborn`
- `scikit-learn`

---

## 🚀 Future Improvements

- Use SHAP or LIME to interpret feature impact more deeply
- Predict ESG score trends using LSTM or time series models
- Extend to unstructured data (e.g., ESG reports, news) using NLP

---

## 📬 Contact

For questions or collaborations, feel free to reach out via GitHub or email.
