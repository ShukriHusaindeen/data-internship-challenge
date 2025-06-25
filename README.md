
# Social Advertisement Dataset – ETL & Insight Challenge

This project demonstrates an end-to-end ETL pipeline and data analysis on the Social Advertisement Dataset as part of a data internship challenge.

## Steps Followed

1. **Extract:** Loaded the dataset from CSV using pandas.
2. **Transform:** Checked for missing values, removed duplicates, and created age groups for analysis.
3. **Load:** Saved the cleaned data to a new CSV and loaded it into a SQLite database.
4. **Analysis:** Explored the data using summary statistics and visualizations (matplotlib, seaborn).
5. **Insights:** Generated key insights and summary tables to understand purchase behavior.

## How to Run

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