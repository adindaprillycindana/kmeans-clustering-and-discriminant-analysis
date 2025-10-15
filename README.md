# Modeling Child Health Indicators Across Indonesian Provinces (2022)
### K-Means Clustering and Discriminant Analysis Approach

## Background
Child health is a key indicator in evaluating a nation’s development progress.  
This project analyzes **child health indicators** across 34 provinces in Indonesia using **K-Means clustering** and **Discriminant Analysis**.  
The study is based on data from the **Indonesian Ministry of Health publication "Profil Kesehatan Ibu dan Anak 2022"** (Mother and Child Health Profile 2022).  

The goal is to group provinces according to their child health performance and to identify which health indicators significantly differentiate these clusters.

---

## Research Questions
1. How can child health indicators in Indonesia be grouped into categories using the **K-Means algorithm**?  
2. Which health indicators significantly influence the clustering results across provinces?

---

## Objectives
- Identify **provincial groupings** in Indonesia based on child health indicators using **K-Means clustering**.  
- Determine **key indicators** that significantly contribute to the cluster formation using **Discriminant Analysis**.  
- Provide insights and recommendations for prioritizing public health interventions.

---

## Data Description
- **Source:** Badan Pusat Statistik (BPS) – *Profil Kesehatan Ibu dan Anak 2022*  
- **Scope:** 34 provinces in Indonesia (year 2022)  
- **Variables (7 indicators):**
  | Symbol | Variable Description | Scale |
  |:------:|:---------------------|:------:|
  | X1 | Percentage of children with health complaints (past month) | Ratio |
  | X2 | Percentage of children with health insurance | Ratio |
  | X3 | Percentage of children aged 5–17 who smoke | Ratio |
  | X4 | Percentage of children aged 12–23 months receiving full basic immunization | Ratio |
  | X5 | Percentage of children aged 0–23 months ever or currently breastfed | Ratio |
  | X6 | Percentage of children aged 0–5 months exclusively breastfed | Ratio |
  | X7 | Percentage of children aged 6–23 months consuming ≥5 of 8 food groups | Ratio |

---

## Methodology
The analytical workflow was implemented using **Python** (Google Colab) and SPSS.  

### Steps:
1. **Data Preparation** – cleaning, handling duplicates, and missing values.  
2. **Exploratory Data Analysis (EDA)** – descriptive statistics, density plots, and outlier detection (e.g., Aceh identified as an outlier for immunization).  
3. **Determining Optimal Clusters** – using the **Elbow Method** and `KneeLocator`, resulting in **k = 3** clusters.  
4. **K-Means Clustering** – grouping provinces based on child health indicators.  
5. **Profiling Clusters** – analyzing the average indicator values within each cluster.  
6. **Discriminant Analysis** – identifying significant indicators differentiating clusters.  
7. **Model Evaluation** – classification accuracy and interpretation.

---

## 🧮 Libraries Used
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-11557C?style=for-the-badge&logo=plotly&logoColor=white)
![Seaborn](https://img.shields.io/badge/Seaborn-4C8CBF?style=for-the-badge&logo=python&logoColor=white)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-F7931E?style=for-the-badge&logo=scikitlearn&logoColor=white)
![Kneed](https://img.shields.io/badge/Kneed-2C2D72?style=for-the-badge&logo=python&logoColor=white)
![Google Colab](https://img.shields.io/badge/Google%20Colab-F9AB00?style=for-the-badge&logo=googlecolab&logoColor=white)

---

## Key Findings

### Cluster Results (k = 3)
- **Cluster 0 – “High Child Health”**: 15 provinces with strong child health indicators (e.g., high breastfeeding and nutrition rates).  
- **Cluster 1 – “Moderate Child Health”**: 9 provinces with average performance but high insurance coverage.  
- **Cluster 2 – “Low Child Health”**: 10 provinces with lower health and nutrition indicators.

### Discriminant Analysis
- 3 significant variables contributing to cluster differentiation:  
  - **Children with health insurance (X2)**  
  - **Children aged 5–17 who smoke (X3)**  
  - **Children ever/currently breastfed (X5)**  

### Model Performance
- The discriminant model achieved a **classification accuracy of 94.1%**, indicating strong alignment between clusters and health indicator patterns.

---

## Insights & Recommendations
- Provinces in the **low health cluster** should be prioritized for government health interventions.  
- Increasing **exclusive breastfeeding** and **child health insurance coverage** can improve health outcomes.  
- Smoking prevention programs among children (ages 5–17) are essential in public health policy.

---
