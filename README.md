# Customer Segmentation using PCA, MCA, FAMD & KMeans

This project performs a complete **unsupervised learning analysis** on the **Bank Marketing dataset**, combining **PCA**, **MCA**, and **FAMD** to understand and visualize customer behavior and campaign performance patterns.

---

## Project Overview

The goal is to identify **customer segments** with similar behaviors and assess which groups are most likely to subscribe to a term deposit.  
The project integrates both **numerical** and **categorical** variables to ensure a holistic understanding of client profiles.

---
## 🗂 Dataset

- **Name**: UCI Bank Marketing Dataset
- **Source**: [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/Bank+Marketing)
- **Size**: 41,188 records × 21 features
- **Target variable**: `y` (whether the client subscribed to a term deposit)
- **Features**: Mix of numerical and categorical attributes (age, job, marital status, campaign info, economic indicators, etc.)

---

## Methods & Techniques

| Step | Description |
|------|--------------|
| **PCA (Principal Component Analysis)** | Reduced numerical variable dimensionality and identified the most influential features. |
| **MCA (Multiple Correspondence Analysis)** | Explored relationships between categorical variables such as job, education, and outcome. |
| **FAMD (Factor Analysis of Mixed Data)** | Combined both variable types to capture the full data structure. |
| **KMeans Clustering** | Applied on FAMD components to group clients with similar profiles. |
| **Evaluation** | Used Elbow and Silhouette methods to determine the optimal number of clusters. |
| **Visualization** | Plotted FAMD dimensions and cluster distributions for interpretability. |

---
## Key Insights from Dimensionality Reduction Techniques

- Economic factors (employment rate, interest rates) strongly influence client subscription
- Campaign engagement metrics (previous contacts, call duration) are significant predictors
- Client profiles (job, education, loans) moderate subscription likelihood
- Dimensionality reduction can help summarize high-dimensional datasets into interpretable components for modeling and visualization

## Key Findings

- **Optimal number of clusters:** 4  
- **Cluster 1** shows the **highest success rate (≈60%)** and corresponds mainly to clients contacted in **August**, with **successful past outcomes** and **shorter campaign durations**.  
- **Clusters 0, 2, and 3** have mostly **"no" responses**, associated with **longer call durations**, **old contacts**, or **less favorable economic conditions**.  
- The **most influential variables** in customer separation were:
  - `duration`, `campaign`, `pdays` (numerical)
  - `job`,`month`, `poutcome`, `education`, `contact` (categorical)

These insights suggest that **timing, previous contact success, and call duration** are the main drivers of client conversion.

---

## Visualizations

- PCA, MCA, and FAMD component plots  
- Correlation circle for variable contributions  
- Elbow & Silhouette method graph  
- FAMD 2D cluster visualization  
- Cluster profiling tables (numerical and categorical summaries)

---

## Tools & Libraries

- **Python**: pandas, numpy, scikit-learn  
- **Statistical analysis**: prince (PCA, MCA, FAMD)  
- **Visualization**: matplotlib, seaborn, plotly  
- **Clustering**: KMeans

---

## Conclusion

The combination of **dimensionality reduction** (FAMD) and **clustering** enabled the discovery of clear customer segments.  
These insights can support **targeted marketing strategies**, improving efficiency by focusing on segments with the highest likelihood of success.

---

## Future Work

- Test **Hierarchical Clustering** or **DBSCAN** for comparison.  
- Develop a **supervised model** (Logistic Regression / XGBoost) using the identified clusters as input features.  
- Explore **temporal effects** by including year or seasonality trends.

---
## How to Run

1. **Clone the repository**:
   ```bash
   git clone https://github.com/yourusername/uci-bank-multivariate-analysis.git
   cd uci-bank-multivariate-analysis
2.**Install Dependencies**:
    pip install -r requirements.txt

3.**Run the notebooks**:
eda_notebook.ipynb → Explore and clean data
pca_mca_famd_analysis.ipynb → Apply PCA, MCA, FAMD, and visualize results
    
