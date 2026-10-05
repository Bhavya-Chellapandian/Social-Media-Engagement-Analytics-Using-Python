# 📊 Social Media Engagement Analytics Using Python

> An end-to-end data analysis project using Python to explore social media engagement patterns, identify high-performing content, and visualize key engagement metrics.

---

## 📌 Project Overview

This project analyzes a **5,000-record social media engagement dataset** using Python.

The analysis covers:

- Data loading and inspection
- Data cleaning and transformation
- Missing-value handling
- Duplicate detection
- Exploratory Data Analysis (EDA)
- Feature engineering
- Statistical analysis
- Correlation analysis
- Group-based analysis
- Data visualization
- Engagement performance analysis

---

## 🎯 Objectives

- Understand social media engagement patterns.
- Analyze likes, comments, shares, impressions, and watch time.
- Compare engagement across different post types and categories.
- Analyze engagement across countries.
- Examine sentiment and engagement relationships.
- Create meaningful derived metrics.
- Present insights through static and interactive visualizations.

---

## 📂 Dataset

The project uses the `social_media_engagement_5000.csv` dataset.

**Dataset source:**

[Social Media Engagement Dataset](https://github.com/GeethaGunasekaran1/Dataset_rep/blob/main/social_media_engagement_5000.csv)

### Dataset Size

- **Rows:** 5,000
- **Columns:** 19
- **Countries:** 10
- **Post Types:** 4
- **Content Categories:** 8
- **Devices:** 3
- **Sentiments:** 3

### Dataset Columns

| Category | Columns |
|---|---|
| User Information | `user_id`, `age`, `gender`, `country`, `follower_count`, `is_verified` |
| Post Information | `post_id`, `post_type`, `post_category`, `posted_at`, `hashtags` |
| Engagement | `likes`, `comments`, `shares`, `watch_time_sec`, `impression_count`, `engagement_rate` |
| Context | `device_type`, `sentiment` |

---

## 🛠️ Technologies & Libraries

- **Python**
- **Pandas**
- **NumPy**
- **Matplotlib**
- **Seaborn**
- **Plotly**
- **Google Colab / Jupyter Notebook**

---

## 🔄 Data Analysis Workflow

```text
Data Import
     ↓
Data Inspection
     ↓
Data Cleaning
     ↓
Data Transformation
     ↓
Exploratory Data Analysis
     ↓
Feature Engineering
     ↓
Statistical Analysis
     ↓
Data Visualization
     ↓
Performance Comparison
     ↓
Insights
```

---

## 🧹 Data Cleaning

The dataset was prepared using the following steps:

- Checked missing values.
- Checked duplicate records.
- Standardized categorical values.
- Converted numeric columns to appropriate numeric types.
- Converted `posted_at` into datetime format.
- Converted `is_verified` into Boolean format.
- Handled negative values in numeric fields.
- Treated ages below 13 and above 100 as missing.
- Filled missing numeric values using the median.
- Filled missing categorical values using the mode.
- Standardized sentiment values to:
  - Positive
  - Neutral
  - Negative

### Missing Values

The initial dataset contained missing values in:

- `age`
- `gender`
- `likes`
- `comments`
- `shares`
- `sentiment`

The analysis reported **0 duplicate rows**.

---

## ⚙️ Feature Engineering

Two important features were created during the analysis.

### Hashtag Count

Counts the number of hashtags used in each post.

```python
df["hashtag_count"] = df["hashtags"].apply(count_hashtags)
```

### Engagement Score

A combined engagement metric was created using:

```python
df["engagement_score"] = (
    df["likes"] +
    df["comments"] +
    df["shares"]
)
```

Additional date-based features were created from `posted_at`:

- `year`
- `month`
- `month_name`
- `day_of_week`

---

## 📈 Exploratory Data Analysis

The project uses Pandas to analyze:

- Categorical distributions
- Post-type performance
- Country-level performance
- Content-category performance
- Sentiment performance
- Engagement metrics
- Correlations between numerical variables

Functions used include:

```python
head()
tail()
shape
columns
info()
describe()
unique()
nunique()
value_counts()
groupby()
agg()
corr()
```

---

## 📊 Statistical Analysis

Key engagement statistics from the analysis include:

| Metric | Mean | Median | Standard Deviation |
|---|---:|---:|---:|
| Likes | 10,107.00 | 10,105.50 | 5,702.29 |
| Comments | 1,502.04 | 1,497.00 | 856.39 |
| Shares | 1,002.91 | 1,012.00 | 570.86 |
| Watch Time | 4,014.50 | 4,034.50 | 2,308.10 |
| Engagement Rate | 0.9644 | 0.2539 | 5.3180 |
| Follower Count | 393,698.22 | 388,982.00 | 230,927.88 |

The engagement-rate distribution shows strong right skewness and high kurtosis, indicating the presence of extreme values.

---

## 📉 Data Visualizations

### Matplotlib

The project uses Matplotlib for:

- Scatter plots
- Line charts
- Bar charts
- Pie charts
- Histograms
- Box plots

### Seaborn

The project uses Seaborn for:

- Count plots
- Bar plots
- Violin plots
- Pair plots
- Heatmaps
- Swarm plots

### Plotly

Plotly is used to create interactive visualizations, including:

- Interactive line charts
- Bubble charts

---

## 🔍 Key Findings

### Post Type

The grouped analysis shows:

- **Video** has the highest average engagement rate: **1.1224**
- Average likes:
  - Video: **10,188.60**
  - Image: **10,104.87**
  - Text: **10,100.15**
  - Reel: **10,037.80**

### Content Category

The displayed category analysis shows:

- **Food:** 1.3586 average engagement rate
- **Tech:** 1.1605
- **Lifestyle:** 1.0910
- **Travel:** 0.7022

### Country

The displayed country analysis shows:

- **Brazil:** 1.5407 average engagement rate
- Australia: 1.3243
- France: 1.1464
- UAE: 1.1124
- Canada: 0.9167
- UK: 0.8510
- Japan: 0.7696
- Germany: 0.7590
- India: 0.6550
- USA: 0.5766

### Sentiment

The grouped sentiment analysis shows **negative sentiment** with the highest average engagement rate of **1.0385**.

---

## 📁 Project Structure

```text
Social-Media-Engagement-Analytics/
│
├── Social_Media_Engagement_Analytics.ipynb
├── social_media_engagement_5000.csv
├── README.md
└── Social_Media_Engagement_Analytics_Summary.docx
```

---

## 🚀 How to Run

### 1. Clone the Repository

```bash
git clone <your-repository-url>
```

### 2. Open the Notebook

Open:

```text
Social_Media_Engagement_Analytics.ipynb
```

using:

- Google Colab
- Jupyter Notebook
- JupyterLab

### 3. Install Required Libraries

```bash
pip install pandas numpy matplotlib seaborn plotly
```

### 4. Load the Dataset

Place:

```text
social_media_engagement_5000.csv
```

in the same working directory as the notebook, or upload it directly in Google Colab.

---

## 📌 Project Highlights

- 5,000 social media records analyzed
- 19 original dataset columns
- Complete data-cleaning workflow
- Missing-value treatment
- Feature engineering
- Engagement-score calculation
- Correlation analysis
- Statistical analysis
- Multiple visualization techniques
- Interactive Plotly visualizations
- Country, category, sentiment and post-type comparisons

---

## 👩‍💻 Author

**Bhavya C**

Data Analyst | Python | Power BI | SQL | Excel | Data Visualization

### Connect

- 🔗 [LinkedIn](https://www.linkedin.com/in/bhavya-chellapandian)
- 💻 [GitHub](https://github.com/Bhavya-Chellapandian)
- 🌐 [Portfolio](https://portfolio-from-resume-mocha.vercel.app/)

---

## 🏷️ Tags

`#Python` `#DataAnalytics` `#DataAnalysis` `#Pandas` `#NumPy` `#Matplotlib` `#Seaborn` `#Plotly` `#EDA` `#DataVisualization` `#SocialMediaAnalytics` `#DataCleaning` `#FeatureEngineering`

---

## 📄 License

This project is created for educational and portfolio purposes.
