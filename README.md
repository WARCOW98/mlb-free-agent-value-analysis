# MLB Free Agent Value Analysis: Descriptive & Predictive Insights

This repository explores how MLB free agent salaries can be better understood and predicted using data analytics. The project is divided into two phases: **descriptive analytics** to uncover salary trends and drivers, and **predictive modeling** using machine learning to identify under- and overvalued players.

---

## 📁 Project Overview

**Author:** Akshay Prabu  
**Scope:** 1998–2013 MLB Free Agents  
**Phases:**  
1. Descriptive analysis of salary distributions and key statistical drivers  
2. Predictive modeling using Linear Regression and Random Forest

---

## 🧾 Dataset

The dataset includes MLB player statistics, contract years, inflation-adjusted salaries, and various performance indicators (WAR, HRs, RBI, OBP, SLG, etc.).

⚠️ **Note**: *The dataset is proprietary and cannot be shared publicly due to academic copyright restrictions.*

---

## 📊 Descriptive Analytics Highlights

### Salary Distribution:
- **Highly right-skewed**, with most players earning below $1M and few stars earning $30M+
- **Log transformation** normalized the distribution and enabled effective modeling across salary ranges.

### Trends Over Time:
- **Mean and median salaries** increased steadily from 1998 to 2013.
- **Salary inequality grew**, with superstar contracts pulling the mean higher relative to the median.

### Salary Drivers:
- Strongest correlation with next year’s salary:
  - **avgRBI, avgTB, RC, avgHR**
  - Power metrics and offensive production are highly predictive of higher salaries.

### Star Power & Outliers:
- Players with high HRs generally earn more, but exceptions exist.
- **Kevin Brown** was the most cost-effective HR producer.
- **Jason Kendall** was the most expensive per HR.

---

## 🔮 Predictive Modeling Highlights

### Modeling Techniques:
- Applied **log transformation** to the target salary variable for improved stability.
- Compared **Linear Regression** and **Random Forest** models.

### Model Performance:

| Model            | R² (Eval) | MAE (Eval) |
|------------------|-----------|------------|
| Linear Regression | 0.2816    | 0.6116     |
| Random Forest     | 0.6744 ✅ | 0.1822 ✅   |

- **Random Forest** outperformed significantly, capturing nonlinear salary structures and reducing errors.

### Top Predictors:
- **WAR**, **HRs**, **BA**, **OBP**, **SLG**, and **Plate Appearances**
- WAR stood out as the strongest and most consistent salary predictor.

---

## 🧩 Value Insights (2013)

### Undervalued Players:
- **Travis Hafner (CLE)** – Power stats with below-market pay
- **Mike Napoli (BOS)** – Strong slugging undervalued
- **Jason Castro (HOU)** – Catcher metrics exceeded expectations
- **Jed Lowrie (OAK)** – Solid infield WAR, underpaid
- **Carlos Gomez (MIL)** – High SB and WAR with modest salary

### Overvalued Players:
- **Andruw Jones (TEX)** – High pay despite poor OBP
- **Alex Rodriguez (NYY)** – Declining production vs contract
- **Albert Pujols (STL)** – Stat regression not reflected in salary
- **David Ortiz (BOS)** – Aging metrics with legacy pricing
- **Derek Jeter (NYY)** – Brand premium outpaced output

---

## 📈 Residual Analysis

- Most predictions were tightly clustered around zero residuals (on log scale)
- Random spread indicates **no strong model bias**
- Outliers were few but instructive, especially among lower-salary players with unpredictable performance

---

## 🧠 Negotiation Strategy Recommendations

- **Agents** of undervalued players should leverage WAR and OBP metrics in negotiations.
- **Teams** should:
  - Prioritize undervalued players for high ROI.
  - Avoid overpaying based on legacy reputation alone.
  - Use predictive models in **contract renewal strategy**.

---

## 🛠️ Tools Used

- Python 3.x
- Pandas, NumPy
- Scikit-learn
- Seaborn, Matplotlib
- Jupyter Notebook

---
