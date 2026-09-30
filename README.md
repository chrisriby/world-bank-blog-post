# World Bank Development Indicators — Data Science Blog Post

Udacity Data Science Nanodegree | Project 1

---

## Motivation

What makes a country a good place to live — and can economic data tell us?

This project uses World Bank development data from 2000 to 2022 to answer five
questions about global economic growth, investment, livability, and the human
cost of economic crises. The final section builds a machine learning model that
predicts life expectancy from economic indicators and asks: how much longer would
people live if a country doubled its healthcare spending?

---

## Questions Explored

1. **Which countries have grown richest since 2000?**
2. **Where is the relationship between investment and economic growth strongest?**
3. **Which countries offer the best combination of income, life expectancy, and low inequality?**
4. **How did the 2008 financial crisis and COVID-19 affect growth and employment globally?**
5. **Can we predict a country's life expectancy from economic indicators?** *(machine learning)*

---

## Libraries Used

| Library | Purpose |
|---|---|
| `pandas` | Data loading, reshaping, and aggregation |
| `numpy` | Numerical operations and array handling |
| `matplotlib` | Base plotting |
| `seaborn` | Statistical visualizations and chart styling |
| `scikit-learn` | Machine learning models, evaluation, and preprocessing |

Python version: 3.11+

---

## Repository Files

| File | Description |
|---|---|
| `analysis.ipynb` | Main Jupyter notebook — full CRISP-DM analysis from data loading to prediction |
| `README.md` | This file |

**Data files** are not committed to this repository (World Bank terms of use).
Download instructions are in the notebook (Section 1). The raw CSV file belongs in
`../../data/raw/` relative to this folder.

---

## Summary of Results

| Question | Finding |
|---|---|
| Q1: Fastest-growing economy | China grew GDP per capita (PPP) by **+429%** between 2000 and 2022 — from $4,066 to $21,499 |
| Q2: Investment vs. growth | Weak positive global correlation (r = 0.189); the link is strongest in Mongolia (r = 0.760), where capital investment tracks growth most consistently |
| Q3: Best livability | **Ireland** scores highest (0.904 out of 1.0) on a composite index of income, life expectancy, and income equality across 165 countries; Namibia scores lowest (0.169) |
| Q4: Crisis impact | COVID-19 (2020) caused a deeper contraction than 2008: world average GDP growth fell **8 percentage points** (from +2.8% to −5.3%) versus a 4-point drop in the financial crisis (to −0.3%); the 2021 recovery reached +5.7% |
| Q5: Life expectancy model | A Random Forest model predicts life expectancy with **R² = 0.922** and a mean error of 1.46 years; health expenditure per capita is the single strongest predictor |
| Prediction scenario | For a hypothetical middle-income country, increasing healthcare spending from $500 to $4,000 per capita predicts a **+7.5 year** gain in life expectancy |

---

## How to Run

1. Clone the repository and activate the virtual environment:

```bash
python -m venv .venv
.venv\Scripts\activate
pip install -r requirements.txt
```

2. Download the World Bank dataset (see notebook Section 1 for exact instructions)
   and save it as:
   ```
   data/raw/World Development Indicators [...] _Data.csv
   ```

3. Open and run the notebook:

```bash
jupyter notebook projects/blog-post-world-bank/analysis.ipynb
```

---

## Blog Post

Published on Medium:
[Where in the World Would You Want to Live? What 20 Years of Economic Data Reveals](https://medium.com/@mail_84883/where-in-the-world-would-you-want-to-live-what-20-years-of-economic-data-reveals-18664baa9bc0)

---

## Acknowledgments

- **Data source:** [World Bank — World Development Indicators](https://databank.worldbank.org/source/world-development-indicators),
  accessed September 2026. Data is made available under the
  [Creative Commons Attribution 4.0 International License](https://datacatalog.worldbank.org/public-licenses#cc-by).
- **Course:** Udacity Data Science Nanodegree
- **Sample blog post format inspired by:** Josh Bernhard,
  [How Do YOU Become a Developer?](https://medium.com/@josh_2774/how-do-you-become-a-developer-5ef1c1c68711)
