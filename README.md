# Adult Census Income — Data Cleaning & Visualization

A simple, structured project focused on:
- Cleaning the Adult dataset (Kaggle version) and standardizing columns.
- Handling missing values and duplicates.
- Creating clear visualizations with **matplotlib** 

##  Data
- Source: Kaggle — *Adult Census Income*.
"https://www.kaggle.com/datasets/uciml/adult-census-income"
- Raw file path: `data/raw/adult.csv`.
- Cleaned file saved as: `data/processed/adult_clean.csv`.




##  Installation & Usage




### 1) Install requirements
```bash
pip install -r requirements.txt
```

### 2) Run Jupyter Notebook
From project root:
```bash
jupyter notebook
```

##  Data Cleaning Decisions
- **Duplicates:** Removed duplicate rows.
- **Whitespace:** Stripped leading/trailing spaces in string columns.
- **Missing values (Categorical):** Filled with `"Unknown"` for `workclass`, `occupation`, `native.country`.
- **Dropped columns:** 
  - `fnlwgt` (sample weight — not needed for analysis).
  - `education.num` (redundant with `education`).
- **Target transformation:** 
  - Created boolean `income_above_50k` from `income`, then dropped original.
  - Comment: *'income' has only two categories, so we converted it to boolean (`income_above_50k`).*
- **Renamed columns (snake_case):**
  - `workclass → work_class`
  - `marital.status → marital_status`
  - `capital.gain → capital_gain`
  - `capital.loss → capital_loss`
  - `hours.per.week → hours_per_week`
  - `native.country → native_country`

- **Index reset:**




This project was developed using two Jupyter Notebooks:

1. Adult_UCI_exploration_and_cleaning.ipynb
`Responsible for data cleaning and preprocessing.`

2. visualization.ipynb
`Responsible for data visualization and presentation.`


##  Visualizations (matplotlib only)
> **Rule:** no custom colors, use clear axis labels.

All figures saved in `outputs/figures/`:

1. `age_distribution.png` — Histogram: Age distribution.
2. `education_distribution_ordered.png` — Bar: Education distribution in logical order.
3. `income_distribution.png` — Bar: Income distribution (*50K or less* vs *Above 50K*).
4. `income_by_sex.png` — Stacked Bar: Income distribution by sex.
5. `income_by_education.png` — Grouped Bar: Income distribution by education level.
6. `top_10_countries.png` — Bar: Top 10 countries by number of people.

##  Quick Start



