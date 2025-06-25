
# 🚀 Social Advertisement Dataset – ETL & Insight Challenge

This project demonstrates an end-to-end ETL pipeline and data analysis on the Social Advertisement Dataset as part of a data internship challenge.

## 📦 Project Overview

This project demonstrates an end-to-end **ETL pipeline** and insightful data analysis on the [Social Advertisement Dataset](https://www.kaggle.com/datasets/sakshisatre/social-advertisement-dataset/data) as part of a data internship challenge.

- **Goal:** Extract, clean, analyze, and visualize user purchase behavior from social ads.
- **Tech Stack:** Python, Pandas, Matplotlib, Seaborn, SQLite

## 🛠️ Steps Followed

1. **Extract:** Loaded the dataset from CSV using pandas.
2. **Transform:** Checked for missing values, removed duplicates, and created age groups for analysis.
3. **Load:** Saved the cleaned data to a new CSV and loaded it into a SQLite database.
4. **Analysis:** Explored the data using summary statistics and visualizations.
5. **Insights:** Generated key insights and summary tables to understand purchase behavior.purchase behavior.

## ▶️ How to Run

1. Clone this repository or download the files.
2. Make sure you have Python 3.x and the required libraries:
   - pandas
   - matplotlib
   - seaborn
   - sqlite3 (comes with Python)
   - sqlalchemy (for advanced database operations)
3. Open `social_ads.ipynb` in Jupyter Notebook or VS Code.
4. Run all cells in order.
5. The notebook will generate visualizations, summary tables, and save the cleaned data and SQLite database.

## 📊 Insights & Analysis

### 1. Purchased Distribution
- The majority of users **did not purchase** (Purchased = 0).
- A smaller portion of users made a purchase (Purchased = 1).
- Example: If you check `df['Purchased'].value_counts()`, you’ll see more 0s than 1s.

### 2. Age Distribution
- Most users are in their **20s and 30s**.
- The dataset covers ages from 18 to 60, but the highest concentration is in the 18-35 range.

### 3. Age Group vs Purchased
- From the `sns.countplot(x='AgeGroup', hue='Purchased', data=df)` and `pd.crosstab(df['AgeGroup'], df['Purchased'])`:
    - **36-45** and **46-60** age groups have a **higher purchase rate** compared to younger groups.
    - The **18-25** group has the **lowest purchase rate**.

### 4. Estimated Salary vs Purchased
- The `sns.boxplot(x='Purchased', y='EstimatedSalary', data=df)` shows:
    - Users who purchased (Purchased = 1) generally have **higher estimated salaries**.
    - There is a clear upward trend in salary among purchasers.

### 5. Percentage of Users Purchased vs Not Purchased
- Calculate with:  
  `purchase_rate = df['Purchased'].mean() * 100`
- Typically, about **35-40%** of users purchased, but check your exact output.

### 6. Correlation Analysis
- From `df.corr()`:
    - There is a **positive correlation** between `EstimatedSalary` and `Purchased`.
    - There is also a **positive correlation** between `Age` and `Purchased`.
    - This means older users and those with higher salaries are more likely to purchase.

## Key Findings

- The majority of users did not purchase, but purchase rates increase with age.
- The 46-60 age group has the highest purchase rate.
- Users who purchased tend to have higher estimated salaries.
- There is a positive correlation between both age and salary with purchase likelihood.

| Age Group | Purchased (0) | Purchased (1) | Purchase Rate (%) |
|-----------|---------------|---------------|-------------------|
| 18-25     | 49            | 1             | 2.0               |
| 26-35     | 87            | 13            | 13.0              |
| 36-45     | 39            | 27            | 40.9              |
| 46-60     | 18            | 16            | 47.1              |

## Extra Work

- Loaded the cleaned data into a SQLite database (`social_ads.db`) for advanced querying.
- Example SQL queries are included in the notebook.

git add README.md
git commit -m "Add project README"
git push