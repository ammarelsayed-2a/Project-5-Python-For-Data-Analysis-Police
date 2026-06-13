# Project-5-Python-For-Data-Analysis-Police
End-to-end EDA on 65,535 police traffic stop records | Analyzing gender disparities, search rates, stop durations &amp; violation patterns using Python, Pandas, Matplotlib &amp; Seaborn

# 🚔 Data Analysis Project — Police Dataset

An end-to-end Data Analysis project on 65,535 police traffic stop records, completed as part of the **Python for Data Analysis** course.

## 📌 Objective
Analyze police stop patterns to uncover gender disparities, search rate differences, stop duration distributions, and age patterns across violation types.

## 📂 Dataset
- **Source:** PoliceData.csv
- **Records:** 65,535 traffic stops
- **Features:** stop_date, stop_time, driver_gender, driver_age, driver_race, violation, search_conducted, search_type, stop_outcome, is_arrested, stop_duration, drugs_related_stop

## 🛠️ Tools & Libraries
| Library | Purpose |
|---|---|
| Pandas | Data cleaning, filtering, groupby, mapping |
| Matplotlib | Base plotting |
| Seaborn | Statistical visualizations |

## 🔧 Pandas Commands Covered
| Command | Purpose |
|---|---|
| `isnull().sum()` | Detect missing values per column |
| `drop()` | Remove fully-null columns |
| `value_counts()` | Count occurrences of each unique value |
| `groupby()` | Aggregate data by category |
| `map()` | Convert categorical values to numerical |
| `mean()` | Calculate column average |
| `groupby().describe()` | Statistical summary per group |

## ❓ Analytical Questions

### Q1 — Data Cleaning: Remove the column that only contains missing values
Identify and drop `country_name` — a column with 65,535 nulls out of 65,535 rows.

### Q2 — Filtering + Value Counts: For Speeding, were Men or Women stopped more often?
Filter to Speeding violations only, then compare stop counts and percentages by gender.

### Q3 — Groupby: Does gender affect who gets searched during a stop?
Calculate the search rate (%) per gender using `groupby()` on the boolean `search_conducted` column.

### Q4 — Mapping + Data Type Casting: What is the mean stop_duration?
Map text categories (`'0-15 Min'`, `'16-30 Min'`, `'30+ Min'`) to numeric midpoints, then compute the mean.

### Q5 — Groupby + Describe: Compare age distributions for each violation
Use `groupby('violation').driver_age.describe()` to get full statistical summaries per violation type.

## 📊 Analysis Structure
1. Imports & Setup
2. Load Dataset
3. First Look (head / tail)
4. Data Structure & Info
5. Descriptive Statistics
6. Categorical Exploration
7. Analytical Questions (Q1 → Q5)
8. Visualizations
   - Univariate (Numerical + Categorical)
   - Bivariate (Num vs Cat · Cat vs Cat)
   - Multivariate
   - Correlation Heatmap · Pairplot
9. Key Insights

## 💡 Key Insights
- Men are stopped for speeding far more often than women — over 75% of speeding stops
- Male drivers face a higher search rate per stop than female drivers
- The average stop duration is approximately 13–15 minutes
- Speeding violations involve younger drivers on average compared to other violations
- Citation is the most common outcome — over 80% of all stops
- The country_name column was entirely null — a real-world data quality issue

## 🚀 How to Run
```bash
git clone https://github.com/ammarelsayed-2a/Project-5-Python-For-Data-Analysis-Police.git
cd Project-5-Python-For-Data-Analysis-Police
jupyter notebook "Project 5 Police.ipynb"
```

## 👤 Author
**Ammar Elsayed** — Python for Data Analysis | 2026  
[LinkedIn](https://www.linkedin.com/in/ammar-elsayed-ibrahim)
