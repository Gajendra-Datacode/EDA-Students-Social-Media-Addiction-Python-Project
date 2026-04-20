# 📱 Students' Social Media Addiction Analysis

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![Pandas](https://img.shields.io/badge/Pandas-Data_Cleaning-green)
![Matplotlib](https://img.shields.io/badge/Matplotlib-Visualization-orange)
![Seaborn](https://img.shields.io/badge/Seaborn-Statistical_EDA-red)

## 🧐 Project Overview
This project focuses on the critical issue of social media addiction among students globally. It involves processing raw survey data, cleaning it for analysis, and generating behavioral insights. The ultimate goal is to understand how digital consumption impacts academic performance, mental health, and sleep patterns.

### Key Objectives:
* **Data Preparation:** Convert raw CSV data into a clean, normalized format.
* **Methodology Documentation:** Provide transparent, reproducible code for data cleaning.
* **Analysis & Reporting:** Present statistical summaries and findings in a polished format.

---

## 📊 Dataset Profile
The dataset contains information on **705 students** across **110 countries**.

| Feature | Description |
| :--- | :--- |
| **Student_ID** | Unique identifier for each student. |
| **Age** | Age range (18–32). |
| **Gender** | Male (M) or Female (F). |
| **Academic_Level** | High School, Undergraduate, or Graduate. |
| **Avg_Daily_Usage_Hours** | Self-reported daily hours on social media. |
| **Most_Used_Platform** | Instagram, TikTok, Twitter, YouTube, etc. |
| **Mental_Health_Score** | Well-being score (Range: 40–99). |
| **Addicted_Score** | Calculated addiction metric (Range: 2–9). |
| **Academic_Performance** | Subjective rating (Excellent, Good, Average, Poor). |

---

## 🛠️ Technical Workflow

### 1. Data Cleaning & Preprocessing
Real-world data often contains gaps. This project implements the following imputation techniques:
* **Mental Health Score:** Filled missing values using the **Mean** ($\approx 69.36$).
* **Daily Usage Hours:** Missing values filled using the **Mode**.
* **Sleep Hours:** Handled via **Median** ($\approx 6.6$) to reduce outlier impact.
* **Academic Performance:** Utilized **Forward Fill (ffill)** for categorical consistency.
* **Feature Engineering:** Created a `High_Usage` boolean column to categorize students exceeding usage thresholds.

### 2. Exploratory Data Analysis (EDA)
We utilized **Matplotlib** and **Seaborn** to visualize:
* **Demographics:** Age distribution showing concentration in late teens and early 20s.
* **Platform Popularity:** Identifying Instagram and TikTok as dominant platforms.
* **Behavioral Correlation:** Analyzing the direct link between usage hours and addiction scores.

---

## 💡 Key Insights
* **The 5-Hour Threshold:** Students spending >5 hours daily report significantly lower academic performance.
* **Mental Health Impact:** Higher addiction scores correlate strongly with reduced sleep quality and lower mental well-being scores.
* **Academic Correlation:** Approximately **41.7%** (294 students) are classified as "High Usage" users, often coinciding with "Average" or "Poor" academic ratings.
* **Social Conflict:** Increased usage leads to a higher frequency of conflicts with family and friends (measured on a 0–5 scale).

---

## 📂 Project Structure
```bash
├── Data/
│   ├── Students_Social_Media_Addiction.csv       # Raw Dataset
│   └── Clean_Students_Social_Media_Addiction.csv # Processed Dataset
├── Notebooks/
│   └── Project_code.ipynb                        # Data Cleaning & EDA Code
├── Reports/
│   └── Project_report.pdf                        # Final Analysis Report
└── README.md
