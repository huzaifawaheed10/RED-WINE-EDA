# 🍷 WINE QUALITY DATA ANALYSIS - EDA
---

## PROJECT OVERVIEW:
This project performs Exploratory Data Analysis (EDA) on the Red Wine Quality dataset using Python libraries such as Pandas, NumPy, Matplotlib, and Seaborn.

The main goal of this project is to analyze wine quality data, understand feature distributions, detect outliers, identify relationships between variables, and visualize important insights using statistical and graphical techniques.

![Wine Quality EDA](./winequality.jpg)

---

## OBJECTIVES:
- Understand the structure and quality of the dataset
- Clean and preprocess raw wine data for analysis
- Explore wine quality distribution and feature patterns
- Analyze relationships between physicochemical properties
- Detect outliers in numerical features
- Identify features affecting wine quality
- Perform correlation analysis between variables

---

## DATASET:
THE DATASET CONTAIN **1599 ROWS** AND **12 COLUMNS**

- `fixed acidity` — Fixed acids present in wine
- `volatile acidity` — Volatile acids affecting wine taste
- `citric acid` — Amount of citric acid
- `residual sugar` — Remaining sugar after fermentation
- `chlorides` — Salt concentration
- `free sulfur dioxide` — Free SO₂ concentration
- `total sulfur dioxide` — Total SO₂ concentration
- `density` — Density of wine
- `pH` — Acidity/basicity level
- `sulphates` — Sulphate concentration
- `alcohol` — Alcohol percentage
- `quality` — Wine quality score

---

## Project Workflow:

```text
1. Import Libraries
       ↓
2. Load Dataset
       ↓
3. Initial Exploration
       ↓
4. Data Cleaning
       ↓
5. Exploratory Data Analysis & Visualization
```

---

## 📊 Step 1 — Initial Exploration

Performed an initial inspection of the dataset to understand its structure:

```python
df.shape
df.head()
df.tail()
df.info()
df.describe()
```

### Key Findings:
- Dataset contains **1,599 wine records** with **12 features**
- All columns are numerical
- Wine quality scores range from **3 to 8**
- Most wines have quality ratings between **5 and 7**
- Several numerical columns contain noticeable outliers
- Alcohol and acidity show strong variation across samples

---

## 🧹 Step 2 — Data Cleaning

### Missing Values Detected:

| Column | Missing Values |
|--------|---------------|
| All Columns | 0 |

### Actions Taken:
- Verified zero null values in the dataset
- Identified duplicate records
- Removed duplicate rows using `drop_duplicates()`
- Confirmed clean dataset after preprocessing

```python
df.isnull().sum()
df.duplicated().sum()
df.drop_duplicates(inplace=True)
```

### Dataset After Cleaning:
- Duplicate rows removed successfully
- Final cleaned dataset prepared for analysis

---

## Step 3 — Exploratory Data Analysis:

### 3.1 Wine Quality Distribution

Analyzed wine quality ratings using count plots:

- Most wines have quality ratings between **5 and 6**
- Very few wines have extremely low or high quality scores
- Dataset is slightly imbalanced toward average-quality wines

### 3.2 Alcohol vs Wine Quality

Explored the relationship between alcohol content and wine quality:

- Wines with higher alcohol content generally have better quality ratings
- Higher-quality wines show higher median alcohol values
- Alcohol positively correlates with quality

### 3.3 Correlation Analysis

Generated a heatmap to identify relationships between variables:

- **Alcohol** positively affects wine quality
- **Volatile acidity** negatively affects quality
- **Density** has inverse relation with alcohol
- Several features show moderate correlations with quality

### 3.4 Outlier Detection

Used box plots to detect extreme values in numerical columns:

- Significant outliers exist in:
  - residual sugar
  - chlorides
  - sulphates
- Outliers contribute to skewed feature distributions

### 3.5 Pairplot Analysis

Explored relationships between key numerical variables:
- `alcohol`
- `volatile acidity`
- `sulphates`
- `density`
- `quality`

Key observations:
- Higher-quality wines tend to cluster together
- Some variables show strong skewness due to outliers
- Multiple physicochemical properties influence wine quality

---

## Key Insights:

| # | Insight |
|---|---------|
| 1 | Most wines have quality ratings between **5–7** |
| 2 | **Alcohol content positively impacts** wine quality |
| 3 | **Volatile acidity negatively affects** wine quality |
| 4 | Several numerical columns contain **extreme outliers** |
| 5 | Higher-quality wines generally contain **more alcohol** |
| 6 | **Density decreases** as alcohol increases |
| 7 | Correlation heatmaps help identify **strong feature relationships** |
| 8 | Wine quality depends on multiple physicochemical properties |

---

## 📊 Visualizations Included

- Histograms
- KDE plots
- Count plots
- Box plots
- Scatter plots
- Pair plots
- Correlation heatmaps

---

## How to Run:

1. Clone the repository:

```bash
git clone https://github.com/huzaifawaheed10/RED-WINE-EDA
```

2. Install required libraries:

```bash
pip install pandas numpy matplotlib seaborn
```

3. Open the notebook:

```bash
jupyter notebook RED_WINE_EDA.ipynb
```

4. Run all cells from top to bottom ✅

---

## 📁 Project Structure

```text
│── RED_WINE_EDA.ipynb
│── winequality-red.csv
│── README.md
```

---

## Contact:
For any queries, feel free to reach out at:

GitHub:     https://github.com/huzaifawaheed10/RED-WINE-EDA

LinkedIn:    www.linkedin.com/in/malak-huzaifa-waheed-5654a2384

---

## ⭐ If you found this project helpful, please give it a star!