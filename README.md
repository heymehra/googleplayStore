# 📱 Google Play Store – Data Visualisation Case Study

A data analysis and visualisation project exploring what makes an app perform well on the Google Play Store. This case study was built to understand the relationship between app features (size, price, installs, ratings) and overall app performance.

---

## 📌 Problem Statement

The Google Play Store team wants to develop a feature to **boost visibility for the most promising apps**. To do this, we need to understand what defines a well-performing app:

- Does a higher size or price necessarily mean an app performs better?
- Does a higher number of installs give a clearer picture of an app's rating?

---

## 🎯 Objectives

- Perform exploratory data analysis (EDA) on Play Store app data
- Clean and handle missing values and incorrect data types
- Identify trends and patterns through visualisations
- Derive actionable insights to guide business decisions

---

## 🗂️ Dataset

**File:** `googleplaystore_v2.csv`

The dataset contains information about apps available on the Google Play Store, including:

| Column | Description |
|---|---|
| App | Name of the app |
| Category | App category |
| Rating | User rating (out of 5) |
| Reviews | Number of user reviews |
| Size | App size |
| Installs | Number of installs |
| Type | Free or Paid |
| Price | App price |
| Content Rating | Target audience |
| Genres | App genre(s) |
| Last Updated | Date of last update |
| Current Ver | Current version |
| Android Ver | Minimum Android version required |

---

## 🛠️ Tech Stack

| Library | Purpose |
|---|---|
| `pandas` | Data loading, cleaning, and manipulation |
| `numpy` | Numerical operations and array handling |
| `matplotlib` | Static charts and base visualisations |
| `seaborn` | Statistical visualisations and styled plots |

---

## 🔄 Workflow

### 1. Data Loading
```python
import pandas as pd
inp0 = pd.read_csv('googleplaystore_v2.csv')
inp0.head()
```

### 2. Data Handling & Cleaning

Before analysis, the data was cleaned for:

**Missing Values** — handled using:
- Dropping rows containing missing values
- Imputing missing values
- Retaining missing values where they don't affect the analysis

**Incorrect Data Types** — fixed by:
- Cleaning certain values (e.g. removing `+`, `,`, `$` symbols)
- Converting entire columns to appropriate types (e.g. `Installs` to integer, `Price` to float)

### 3. Exploratory Data Analysis (EDA)
- Distribution of app ratings
- Category-wise install counts
- Free vs Paid app comparison
- Correlation between size, price, installs, and ratings

### 4. Data Visualisation
- Bar plots, histograms, box plots, scatter plots, and heatmaps
- Built using `matplotlib` and `seaborn` for clear and insightful visuals

---

## 💡 Key Insights

- Higher app size or price does **not** necessarily lead to better ratings
- Apps with more installs tend to have **more stable ratings** due to larger review bases
- **Free apps** dominate installs but paid apps show marginally higher average ratings in some categories
- Certain categories consistently outperform others in both installs and ratings

---

## 📁 Project Structure

```
googleplayStore/
│
├── Data Visualisation in Python - Case Study.ipynb   # Main notebook
├── googleplaystore_v2.csv                             # Dataset
└── README.md                                          # Project overview
```

---

## 🚀 How to Run

1. Clone the repository:
   ```bash
   git clone https://github.com/heymehra/googleplayStore.git
   cd googleplayStore
   ```

2. Install dependencies:
   ```bash
   pip install pandas numpy matplotlib seaborn
   ```

3. Launch the notebook:
   ```bash
   jupyter notebook "Data Visualisation in Python - Case Study.ipynb"
   ```

---
