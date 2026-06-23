# Data Analytics — Project 2

> Regression and probability analysis of Instacart grocery reorder data

![Python](https://img.shields.io/badge/Python-0a7?style=flat-square) ![Jupyter Notebook](https://img.shields.io/badge/Jupyter_Notebook-0a7?style=flat-square) ![pandas](https://img.shields.io/badge/pandas-0a7?style=flat-square) ![numpy](https://img.shields.io/badge/numpy-0a7?style=flat-square) ![seaborn](https://img.shields.io/badge/seaborn-0a7?style=flat-square) ![matplotlib](https://img.shields.io/badge/matplotlib-0a7?style=flat-square) ![statsmodels](https://img.shields.io/badge/statsmodels-0a7?style=flat-square) ![scipy](https://img.shields.io/badge/scipy-0a7?style=flat-square) ![scikit-learn](https://img.shields.io/badge/scikit--learn-0a7?style=flat-square) 

### 🌐 Live project page → **https://selsaady1.github.io/dat301-data-analytics-project-2/**

## Overview
A DAT301 data analytics project analyzing the Instacart Market Basket dataset in a single Jupyter notebook. It explores how order quantity, purchase frequency, and days between orders relate to product reorders using data merging, visualization, OLS regression, and a binomial probability model. The work covers data cleaning, exploratory plots, regression diagnostics, and a probability mass function for cart checkout behavior.

**Highlight:** R-squared = 0.742 for reorders-vs-products regression

## Key Achievements
- Merged multiple Instacart CSV files (orders, prior order-products, products, departments, aisles) and built grouped tables of product counts and reorder sums by product ID
- Fit a multivariate OLS regression of reorders on products and days_since_prior_order, plus a single-variable OLS of products on reorders reporting R-squared of 0.742
- Produced histograms, a boxplot, residual density plot, QQ plot, and fitted-regression-line scatter to diagnose a right-skewed distribution
- Built a binomial probability model (n=5, p=0.65) computing mean 3.25, variance 1.1375, and a full probability mass function table for items checked out

## Approach
Working in Python (pandas, numpy, seaborn/matplotlib), the notebook reads and merges the Instacart file collection, then cleans and visualizes the data to expose relationships between reorders, products per order, and time between orders. It applies OLS regression via statsmodels for both a three-variable and a two-variable model, evaluates fit with residual, QQ, and fitted-line plots, and closes with a hand-derived binomial distribution implemented with scipy to model checkout cart behavior.

## Tools & Technologies
- Python
- Jupyter Notebook
- pandas
- numpy
- seaborn
- matplotlib
- statsmodels
- scipy
- scikit-learn

## Repository Structure
```
.gitignore
LICENSE
README.md
src/DAT301Project2.ipynb
```

## Results
The two-variable regression of products on reorders reached an R-squared of 0.742, indicating a strong linear relationship, while the three-variable model showed weak correlation; distributions were found to be right-skewed and the binomial model gave a mean of 3.25 items per 5-item cart.

## Deliverable
See [`src/DAT301Project2.ipynb`](src/DAT301Project2.ipynb).

## License
MIT — see [`LICENSE`](LICENSE).

---
_Part of [Saif Elsaady's engineering portfolio](https://selsaady1.github.io/portfolio/). Deliverables only — routine homework/quizzes/exams excluded._