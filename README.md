# Modeling Child Health Indicators Across Indonesian Provinces (2022)
### K-Means Clustering and Discriminant Analysis Approach

## Background
Child health is a key indicator in evaluating a nation’s development progress.  
This project analyzes **child health indicators** across 34 provinces in Indonesia using **K-Means clustering** (Python) and **Discriminant Analysis** (SPSS).  
The study is based on data from the **Indonesian Ministry of Health publication "Profil Kesehatan Ibu dan Anak 2022"** (Mother and Child Health Profile 2022).  

The goal is to group provinces according to their child health performance and to identify which health indicators significantly differentiate these clusters.

---

## Research Questions
1. How can child health indicators in Indonesia be grouped into categories using the **K-Means algorithm**?  
2. Which health indicators significantly influence the clustering results across provinces?

---

## Objectives
- Identify **provincial groupings** in Indonesia based on child health indicators using **K-Means clustering**.  
- Determine **key indicators** that significantly contribute to the cluster formation using **Discriminant Analysis (via SPSS)**.  
- Provide insights and recommendations for prioritizing public health interventions.

---

## Data Description
- **Source:** Badan Pusat Statistik (BPS) – *Profil Kesehatan Ibu dan Anak 2022*  
- **Scope:** 34 provinces in Indonesia (year 2022)  
- **Variables (7 indicators):**
  | Symbol | Variable Description | Scale |
  |:------:|:---------------------|:------:|
  | X1 | % of children with health complaints (past month) | Ratio |
  | X2 | % of children with health insurance | Ratio |
  | X3 | % of children aged 5–17 who smoke | Ratio |
  | X4 | % of children aged 12–23 months receiving complete immunization | Ratio |
  | X5 | % of children aged 0–23 months ever/currently breastfed | Ratio |
  | X6 | % of children aged 0–5 months exclusively breastfed | Ratio |
  | X7 | % of children aged 6–23 months consuming ≥5 of 8 food groups | Ratio |

---

## Methodology
The analytical workflow combined **Python** (for data preprocessing, EDA, and K-Means clustering) and **SPSS** (for discriminant analysis and validation).  

### Steps:
1. **Data Preparation** – cleaning and checking for missing values.  
2. **Exploratory Data Analysis (EDA)** – descriptive statistics, distribution plots, and outlier detection.  
3. **Optimal Cluster Selection** – used the **Elbow Method** and `KneeLocator` in Python, resulting in **k = 3** clusters.  
4. **K-Means Clustering** – implemented in Python (`scikit-learn`) to classify provinces based on child health indicators.  
5. **Cluster Profiling** – interpreted the characteristics of each cluster.  
6. **Discriminant Analysis (SPSS)** – identified significant health indicators contributing to provincial grouping.  
7. **Model Evaluation** – assessed classification accuracy and interpretability (94.1%).

---

## Tools & Libraries
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-11557C?style=for-the-badge&logo=plotly&logoColor=white)
![Seaborn](https://img.shields.io/badge/Seaborn-4C8CBF?style=for-the-badge&logo=python&logoColor=white)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-F7931E?style=for-the-badge&logo=scikitlearn&logoColor=white)
![Kneed](https://img.shields.io/badge/Kneed-2C2D72?style=for-the-badge&logo=python&logoColor=white)
![SPSS](https://img.shields.io/badge/SPSS-0536D6?style=for-the-badge&logo=ibm&logoColor=white)
![Google Colab](https://img.shields.io/badge/Google%20Colab-F9AB00?style=for-the-badge&logo=googlecolab&logoColor=white)

---

## Key Findings

### Cluster Results (k = 3)
- **Cluster 0 – “High Child Health”**: 15 provinces with strong health outcomes (high breastfeeding & nutrition indicators).  
- **Cluster 1 – “Moderate Child Health”**: 9 provinces with average performance but high insurance coverage.  
- **Cluster 2 – “Low Child Health”**: 10 provinces with weaker health and nutrition performance.

### Discriminant Analysis (via SPSS)
- 3 variables significantly differentiate clusters:  
  - **X2:** % of children with health insurance  
  - **X3:** % of children aged 5–17 who smoke  
  - **X5:** % of children aged 0–23 months ever/currently breastfed  
- The discriminant model achieved **94.1% classification accuracy**, showing high validity.

---

## Insights & Recommendations
- Prioritize interventions for provinces in the **Low Child Health** cluster.  
- Improve **exclusive breastfeeding** and **health insurance coverage** access.  
- Implement **smoking prevention programs** for children and teens.  
- Focus resources on regional disparities in healthcare and nutrition.

---

## 📁 Repository Structure
