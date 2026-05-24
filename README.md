# 🏦 Banking Client Analytics — Exploratory Data Analysis


> A full exploratory data analysis of a banking client dataset with **3,000 records** and **25 features**, uncovering financial behaviour patterns, client segmentation insights, and risk profiles — visualised through Python and an interactive Power BI dashboard.

---

## 📌 Table of Contents

- [Project Overview](#-project-overview)
- [Business Problem Statement](#-business-problem-statement)
- [Dataset](#-dataset)
- [Project Structure](#-project-structure)
- [Tools & Technologies](#-tools--technologies)
- [Analytical Workflow](#-analytical-workflow)
- [Key Findings](#-key-findings)
- [Dashboard](#-dashboard)
- [How to Run](#-how-to-run)
- [Report](#-report)

---

## 🔍 Project Overview

This project was built as a data analytics portfolio piece to demonstrate end-to-end EDA skills — from raw data ingestion and feature engineering through statistical analysis, visualisation, and business insight generation.

The dataset simulates a real-world retail banking environment, containing client demographics, financial product holdings, loyalty classifications, fee structures, and risk weightings.

---

## 💼 Business Problem Statement

> *"How can the bank leverage client demographic, financial, and behavioural data to segment its customer base, identify high-value client groups, assess financial risk exposure, and develop data-driven strategies that improve client retention, cross-sell financial products, and optimise fee and loyalty structures?"*

### Objectives
- Understand the demographic composition of the client base (age, gender, nationality, occupation)
- Analyse income distribution and financial product holdings across client segments
- Identify loyalty tier patterns and their relationship with financial behaviour
- Examine fee structure allocation and surface upsell/upgrade opportunities
- Quantify correlations between financial variables to find cross-sell potential
- Profile clients by risk weighting to support risk management decisions

---

## 📊 Dataset

| Attribute | Details |
|---|---|
| **Records** | 3,000 client entries |
| **Features** | 25 columns |
| **Missing Values** | None |
| **Data Types** | Numerical (int, float) + Categorical (string) |
| **File** | `Banking.csv` |

### Feature Highlights

| Feature | Type | Description |
|---|---|---|
| `Client ID` | Categorical | Unique client identifier |
| `Age` | Numerical | Client age (17–85 years) |
| `Nationality` | Categorical | 5 nationalities (European, Asian, American, Australian, African) |
| `Estimated Income` | Numerical | Annual income ($15K–$522K) |
| `Loyalty Classification` | Categorical | Platinum / Gold / Silver / Jade |
| `Fee Structure` | Categorical | High / Mid / Low |
| `Risk Weighting` | Ordinal | 1 (Very Low) to 5 (Very High) |
| `Bank Deposits` | Numerical | Total deposit balance |
| `Bank Loans` | Numerical | Total loan amount |
| `Saving Accounts` | Numerical | Savings account balance |
| `Business Lending` | Numerical | Business lending balance |
| `Credit Card Balance` | Numerical | Total credit card balance |
| `Superannuation Savings` | Numerical | Retirement savings balance |

---

## 📁 Project Structure

```
banking-eda/
│
├── Banking.csv                    # Raw dataset
├── BANKING_CASE_CODE.ipynb        # Jupyter Notebook — full EDA code
├── Banking_Dashboard__.pbix       # Power BI interactive dashboard
├── Banking_Analytics_Report.docx  # Detailed business report
└── README.md                      # Project documentation
```

---

## 🛠 Tools & Technologies

| Tool | Purpose |
|---|---|
| **Python 3.x** | Core programming language |
| **Pandas** | Data loading, cleaning, manipulation |
| **NumPy** | Numerical computations |
| **Seaborn** | Statistical visualisations (countplots, histplots, heatmaps) |
| **Matplotlib** | Custom chart rendering and layout |
| **Jupyter Notebook** | Interactive analysis environment |
| **Power BI** | Interactive business dashboard |

---

## 🔄 Analytical Workflow

```
1. Data Loading & Inspection
   └── df.info(), df.describe(), df.isnull().sum(), df.shape

2. Feature Engineering
   └── Income Band (Low / Mid / High) via pd.cut()

3. Univariate Analysis
   └── Value counts + count plots for all categorical/ordinal features

4. Bivariate Analysis
   └── Categorical features cross-tabulated by Nationality (hue)

5. Numerical Distribution Analysis
   └── KDE histograms for Age, Income, Savings, Loans, Deposits, etc.

6. Correlation Heatmap
   └── Pearson correlation matrix across 8 numerical features

7. Power BI Dashboard
   └── Interactive segmentation, income band, loyalty & risk visuals
```

---

## 📈 Key Findings

### Client Demographics
- **Age:** Ranges 17–85 years | Mean age ~51 years
- **Gender:** Near-equal split — 50.4% Female, 49.6% Male
- **Nationality:** Europeans dominate at 43.6%, followed by Asians (25.1%) and Americans (16.9%)

### Financial Segmentation

| Metric | Value |
|---|---|
| Avg. Estimated Income | $171,305 |
| Avg. Bank Deposits | $671,560 |
| Avg. Bank Loans | $591,386 |
| Avg. Credit Card Balance | $3,176 |
| Avg. Superannuation Savings | $25,532 |

### Loyalty Tier Distribution

| Tier | Count | Share |
|---|---|---|
| Jade (Entry) | 1,331 | 44.4% |
| Silver | 767 | 25.6% |
| Gold | 585 | 19.5% |
| Platinum | 317 | 10.6% |

### Fee Structure

| Structure | Count | Share |
|---|---|---|
| High | 1,476 | 49.2% |
| Mid | 962 | 32.1% |
| Low | 562 | 18.7% |

### Correlation Highlights

| Variable Pair | r | Interpretation |
|---|---|---|
| Bank Deposits ↔ Saving Accounts | **0.75** | Strongest — savers hold larger deposits |
| Business Lending ↔ Bank Deposits | 0.44 | Borrowers also maintain high deposits |
| Business Lending ↔ Bank Loans | 0.42 | Active business borrowers also carry bank loans |
| Income ↔ Superannuation Savings | 0.37 | Higher earners save more for retirement |
| Income ↔ Business Lending | 0.33 | Income drives business credit uptake |
| Income ↔ Credit Card Balance | 0.30 | Higher income correlates with card spend |

---

## 📊 Dashboard

The Power BI dashboard (`Banking_Dashboard__.pbix`) includes interactive panels for:
- Client segmentation by nationality, loyalty tier, and fee structure
- Income band distribution across demographic groups
- Risk weighting profile across the client base
- Financial product overview (deposits, loans, savings, credit)

> Open with **Power BI Desktop** (free download at [powerbi.microsoft.com](https://powerbi.microsoft.com))

---

## ▶️ How to Run

### Prerequisites
```bash
pip install pandas numpy seaborn matplotlib jupyter
```

### Steps
```bash
# 1. Clone the repository
git clone https://github.com/your-username/banking-eda.git
cd banking-eda

# 2. Launch Jupyter Notebook
jupyter notebook BANKING_CASE_CODE.ipynb

# 3. Run all cells in order
# The notebook reads Banking.csv from the same directory
```

---

## 📄 Report

A full business report (`Banking_Analytics_Report.docx`) is included covering:
- Executive Summary with key metrics
- Business Problem Statement & Objectives
- Dataset Feature Catalogue
- Detailed EDA Findings
- Business Insights & Recommendations

---

*Built as part of a Data Analytics Portfolio — May 2026*
