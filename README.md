#  Students' Social Media Addiction Analysis

##  Project Overview
This project focuses on the critical issue of social media addiction in the student population. It involves taking raw, uncleaned survey or usage data, processing it into a usable format, and preparing it for meaningful analysis. The ultimate goal is to generate insights that can be summarized in a comprehensive report.

### Key Objectives:
* **Data Preparation:** Convert raw CSV data into a clean, normalized format suitable for analysis.
* **Methodology Documentation:** Provide transparent, reproducible code that details the exact steps taken to clean the data.
* **Analysis & Reporting:** Present the final findings, statistical summaries, and conclusions in a polished PDF report.

## 🔗 Project Resources

-  Source Code: [Open Notebook](https://drive.google.com/drive/folders/1-cAeiWcxfTJWtX5uV10UMMT4Okbvjr3u?usp=drive_link)

---

##  Students' Social Media Addiction Dataset

### Overview
This dataset contains information on 705 students globally, exploring the relationship between social media usage, academic performance, and mental well-being. It captures demographic details alongside usage patterns across various platforms like Instagram, TikTok, and Twitter.

* [View Raw CSV Data](./Students_Social_Media_Addiction.csv.csv)

### Dataset Structure
* **Total Records:** 705
* **Total Features:** 17
* **Key Missing Data:** Approximately 10% (70 rows) of data is missing for `Mental_Health_Score`, `Daily_Usage_Hours`, `Sleep_Hours`, and `Academic_Performance`.

### Feature Descriptions
| Column | Description |
| :--- | :--- |
| **Student_ID** | Unique identifier for each student. |
| **Age** | Age of the student (Range: 18–32). |
| **Gender** | Male (M) or Female (F). |
| **Academic_Level** | High School, Undergraduate, or Graduate. |
| **Country** | Country of residence (110 unique countries). |
| **Avg_Daily_Usage_Hours** | Self-reported average daily hours spent on social media. |
| **Most_Used_Platform** | Primary platform (Instagram, Twitter, TikTok, YouTube, etc.). |
| **Affects_Academic_Performance** | Binary (Yes/No) indicating if social media impacts grades. |
| **Sleep_Hours_Per_Night** | Hours of sleep obtained on average. |
| **Mental_Health_Score** | A score representing mental well-being (Range: 40–99). |
| **Relationship_Status** | Single, In Relationship, or Complicated. |
| **Conflicts_Over_Social_Media** | Frequency of conflicts due to usage (0–5 scale). |
| **Addicted_Score** | A calculated addiction metric (Range: 2–9). |
| **Academic_Performance** | Subjective performance rating (Excellent, Good, Average, Poor). |
| **Weekend_Usage_Hours** | Social media usage specifically during weekends. |

---

##  Data Analysis & Technical Summary
This project involves a comprehensive data cleaning and exploratory data analysis (EDA) pipeline.

* [View Data Cleaning Code](./Project_code.ipynb)

### 1. Data Cleaning & Preprocessing
* **Mental Health Score:** Missing values filled using the **Mean**.
* **Daily Usage Hours:** Missing values filled using the **Mode**.
* **Sleep Hours:** Missing values filled using the **Median**.
* **Academic Performance:** Utilized the **Forward Fill (ffill)** method.
* **Duplicate Check:** Verification performed on `Student_ID`.

### 2. Exploratory Data Analysis (EDA)
* **Demographic Insights:** Histogram used to visualize age concentration.
* **Platform Popularity:** Count plot identifies dominant platforms (Instagram, TikTok, Facebook).
* **Correlation Analysis:** Scatter plots exploring relationship between usage hours and `Addicted_Score`, using `Academic_Performance` as a hue.

### 3. Libraries Used
* **Pandas & NumPy:** For data manipulation.
* **Matplotlib & Seaborn:** For statistical visualizations.

---

##  Cleaned Dataset Summary
* [Download Cleaned CSV File](./Clean_Students_Social_Media_Addiction_File.csv)

### 1. Data Integrity & Cleaning
* **Numerical Imputation:** `Mental_Health_Score` ($\approx 69.36$) and `Sleep_Hours` ($\approx 6.6$).
* **Feature Engineering:** Added **High_Usage** (Boolean) to categorize consumption levels.

### 2. Dataset Profile
* **Total Columns:** 18 (1 additional feature).
* **Data Types:** Numerical, Categorical, and Boolean.

### 3. Key Observations
* **Academic Performance:** Most frequent rating is "Good" (257 students).
* **Addiction Levels:** Average `Addicted_Score` is 6.44 (Std Dev: 1.58).
* **Usage Classification:** 41.7% (294 students) fall into the high-usage category.

---

##  Report

### Core Objectives
The study analyzes how usage patterns correlate with:
* **Mental Health:** Screen time vs. well-being scores.
* **Physical Health:** Impact on sleep duration.
* **Academic Performance:** Identifying negative productivity thresholds.
* **Social Behavior:** Evaluating conflict and addiction levels.

### Key Insights & Findings
* **The 5-Hour Threshold:** Usage above 5 hours daily shows a higher negative impact on grades.
* **Addiction Correlation:** Direct positive correlation between daily hours and addiction scores.
* **Health Deterioration:** High addiction is associated with reduced sleep quality.
* **Demographic Variations:** Scores vary across academic levels, genders, and platforms.

### Technical Workflow
1.  **Data Cleaning:** Systematic handling of missing values and inconsistencies.
2.  **EDA:** Identifying patterns and distributions.
3.  **Visualization:** Pinpointing high-risk platforms and trends.

---

##  Conclusion
Social media addiction is a complex issue influenced by various factors. This project emphasizes the necessity of balanced digital usage and demonstrates the power of data analytics in understanding modern social challenges.
