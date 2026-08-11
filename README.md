# Customer Segmentation using K-Means

## Project Overview

This project focuses on customer segmentation using the K-Means clustering algorithm.

The goal is to identify groups of customers with similar characteristics based on their age, annual income, and spending score.

The project follows a complete unsupervised learning workflow, including data understanding, exploratory data analysis, preprocessing, feature scaling, cluster selection, clustering, evaluation, dimensionality reduction, and business interpretation.

---

## Business Problem

Businesses often have customers with different characteristics, income levels, and spending behaviors.

Treating all customers in the same way may lead to ineffective marketing strategies.

Customer segmentation can help businesses:

- Identify different customer groups.
- Understand customer behavior.
- Design targeted marketing campaigns.
- Improve customer retention.
- Develop personalized offers.

---

## Dataset

The project uses the Mall Customers dataset.

The dataset contains information about 200 customers, including:

- Customer ID
- Gender
- Age
- Annual Income (k$)
- Spending Score (1-100)

For clustering, the following numerical features were selected:

- Age
- Annual Income (k$)
- Spending Score (1-100)

Customer ID was excluded because it is only an identifier.

Gender was not used in the clustering model because the analysis focuses on numerical customer characteristics and spending behavior.

---

## Technologies and Libraries

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook / Google Colab

---

## Methodology

The project follows these main steps:

1. Data Loading
2. Data Understanding
3. Data Cleaning
4. Exploratory Data Analysis (EDA)
5. Feature Selection
6. Feature Scaling
7. Elbow Method
8. Silhouette Score
9. K-Means Clustering
10. Cluster Analysis
11. PCA Visualization
12. Business Insights

---

## Data Preprocessing

The dataset was inspected for:

- Missing values
- Duplicate rows
- Data types
- Statistical characteristics

The selected numerical features were standardized using `StandardScaler`.

This step ensures that features with different numerical ranges contribute more fairly to the clustering algorithm.

---

## Choosing the Number of Clusters

Two evaluation techniques were used to select an appropriate number of clusters.

### Elbow Method

The Elbow Method was used to analyze the decrease in inertia as the number of clusters increased.

### Silhouette Score

The Silhouette Score was used to evaluate how well-separated the clusters were.

The highest Silhouette Score was obtained at:

**K = 6**

with a score of approximately:

**0.43**

Therefore, six clusters were selected for the final K-Means model.

---

## K-Means Clustering

The final K-Means model was trained using:

- Number of clusters: 6
- Random state: 42
- Number of initializations: 10

The resulting customer segments were analyzed using their average age, annual income, and spending score.

---

## Customer Segments

The final segmentation identified six customer groups.

| Cluster | Customers | Avg Age | Avg Income (k$) | Avg Spending |
|--------:|----------:|--------:|----------------:|-------------:|
| 0 | 45 | 56.33 | 54.27 | 49.07 |
| 1 | 39 | 26.79 | 57.10 | 48.13 |
| 2 | 33 | 41.94 | 88.94 | 16.97 |
| 3 | 39 | 32.69 | 86.54 | 82.13 |
| 4 | 23 | 25.00 | 25.26 | 77.61 |
| 5 | 21 | 45.52 | 26.29 | 19.38 |

---

## Business Insights

### Cluster 3 — High-Value Customers

Customers in this cluster have high annual income and high spending scores.

They represent high-value customers and may be suitable for premium offers, loyalty programs, and personalized marketing campaigns.

### Cluster 2 — High Income / Low Spending

Customers in this cluster have high annual income but relatively low spending scores.

They represent an important business opportunity because they have purchasing capacity but are not spending heavily.

Targeted campaigns and personalized offers could be used to increase engagement.

### Cluster 4 — Low Income / High Spending

Customers in this cluster have relatively low annual income but high spending scores.

Affordable promotions, loyalty rewards, and value-oriented offers could help maintain their engagement.

### Cluster 5 — Low Income / Low Spending

Customers in this cluster have both low annual income and low spending scores.

Low-cost promotional strategies could be considered while evaluating the cost-effectiveness of targeting this segment.

### Cluster 0 — Older Customers with Moderate Spending

This segment contains relatively older customers with moderate income and spending levels.

Marketing strategies could focus on customer retention, relevant products, and personalized communication.

### Cluster 1 — Younger Customers with Moderate Spending

This segment contains younger customers with moderate income and spending levels.

Digital campaigns, personalized recommendations, and engagement-focused promotions could be effective for this group.

---

## PCA Visualization

PCA was applied to reduce the three-dimensional feature space into two principal components for visualization.

The first two principal components explain approximately:

**77.57% of the total variance**

This provides a useful two-dimensional representation of the customer segments.

---

## Model Evaluation

The final K-Means model achieved a Silhouette Score of approximately:

**0.428**

This indicates reasonably separated customer groups and supports the selected six-cluster solution.

---

## Project Structure

## How to Run

1. Clone the repository
git clone https://github.com/EngSaraGamal/customer-segmentation-kmeans.git

2. Install dependencies
pip install -r requirements.txt

3. Open the notebook
Mall_customer_segmentation.ipynb
The notebook can be executed using Jupyter Notebook or Google Colab.

## Conclusion

This project demonstrates a complete unsupervised learning workflow for customer segmentation using K-Means clustering.

The analysis combines data preprocessing, exploratory analysis, feature scaling, cluster selection, model evaluation, PCA visualization, and business interpretation.

The resulting customer segments can help businesses understand customer behavior and develop more targeted marketing strategies.

```text
customer-segmentation-kmeans/
│
├── Mall_customer_segmentation.ipynb
├── requirements.txt
└── README.md
