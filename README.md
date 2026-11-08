# DCS402 — Data Analytics & Visualization

[![Python](https://img.shields.io/badge/Python-3.10%2B-blue.svg)](https://www.python.org/)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange.svg)](https://jupyter.org/)
[![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-150458.svg)](https://pandas.pydata.org/)
[![Seaborn](https://img.shields.io/badge/Seaborn-Visualization-4c72b0.svg)](https://seaborn.pydata.org/)

This repository contains coursework, data cleaning pipelines, and visual analytics assignments analyzing how different chart types impact audience interpretation.

---

## 📁 Repository Structure

```text
DCS402/
├── .gitignore
├── README.md
└── pandas/
    ├── cleaning.ipynb              # NFL play-by-play data cleaning & missing value handling
    ├── pandas.ipynb                # Core Pandas series, dataframes, indexing & wrangling
    └── assig/
        ├── assig.ipynb             # Assignment notebook with comparative code & charts
        ├── kaggle_titanic.csv      # Dataset 1: Categorical / survival data
        ├── kaggle_sales_trends.csv # Dataset 2: 24-Month continuous time-series
        ├── kaggle_house_prices.csv # Dataset 3: Continuous bivariate property data
        ├── chart1_titanic_comparison.png
        ├── chart2_sales_trend_comparison.png
        └── chart3_housing_comparison.png
```

---

## 🚀 Getting Started & Execution

1. **Clone the repository:**
   ```bash
   git clone git@github.com:saaloni7/DCS402.git
   cd DCS402
   ```

2. **Install dependencies:**
   ```bash
   pip install pandas numpy matplotlib seaborn jupyter
   ```

3. **Launch Jupyter Notebook:**
   ```bash
   jupyter notebook
   ```
   Navigate to `pandas/assig/assig.ipynb` to run the comparative visualization code.

---

## 📊 Assignment: Impact of Chart Types on Audience Interpretation

### 1. Introduction
Data visualization translates complex quantitative data into intuitive visual patterns. Human perception decodes spatial position and length along a common baseline with far greater speed and precision than angles, areas, or disconnected categories. Selecting the right chart ensures audiences grasp key trends immediately without cognitive fatigue or distorted interpretations.

### 2. Kaggle Datasets Used
* **Dataset 1 (Titanic):** [Kaggle Titanic Competition](https://www.kaggle.com/competitions/titanic) *(Categorical proportions)*
* **Dataset 2 (Superstore):** [Kaggle Sales Forecasting](https://www.kaggle.com/datasets/rohitsahoo/sales-forecasting) *(Continuous time-series)*
* **Dataset 3 (Ames Housing):** [Kaggle House Prices Competition](https://www.kaggle.com/competitions/house-prices-advanced-regression-techniques) *(Continuous bivariate correlation)*

---

### Chart 1: Titanic Survival by Passenger Class

![Chart 1: Titanic Comparison](pandas/assig/chart1_titanic_comparison.png)

* **Best Chart:** **Grouped Bar Chart** (versus a Pie Chart)
* **Explanation:** A grouped bar chart aligns survival counts along a shared horizontal baseline ($y = 0$). This allows viewers to instantly judge differences in bar heights and see that 3rd Class passengers suffered disproportionately high casualties. In contrast, a multi-slice pie chart encodes values into circular angles and 2D wedge areas, which human eyes frequently misjudge, obscuring relative class comparisons.

---

### Chart 2: Monthly Sales Trends Over Time

![Chart 2: Sales Trend Comparison](pandas/assig/chart2_sales_trend_comparison.png)

* **Best Chart:** **Continuous Line Chart with Markers** (versus a Discrete Bar Chart)
* **Explanation:** Time is continuous, and a line chart relies on connected slopes to intuitively display velocity, direction of change, and cyclical Q4 holiday spikes. Plotting 24 separate monthly vertical bars introduces heavy visual clutter ("chartjunk") and creates artificial barriers between months, obscuring the overarching long-term revenue momentum.

---

### Chart 3: Living Area vs. Sale Price

![Chart 3: Housing Price Comparison](pandas/assig/chart3_housing_comparison.png)

* **Best Chart:** **Bivariate Scatter Plot with Trendline** (versus an Aggregated Bar Chart)
* **Explanation:** A scatter plot maps each property as an individual coordinate pair, preserving critical pricing dispersion, density, and outliers (such as oversized homes sold at steep discounts). An aggregated bar chart averages data into broad bins, concealing price variance and misleading audiences into believing home values follow a rigid, uniform stair-step pattern.

---

### 3. Conclusion & Selection Justification
Matching visual encodings to the data's mathematical structure is essential for accurate audience interpretation: a **grouped bar chart** was selected for the Titanic dataset because linear lengths on a common axis are easier to compare than circular angles; a **line chart** was chosen for sales trends because continuous slopes intuitively convey rate of change without bar clutter; and a **scatter plot** was selected for housing prices because it preserves correlation density, variance, and outliers that summary bar averages hide.
