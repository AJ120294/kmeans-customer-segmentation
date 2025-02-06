# Customer Segmentation Project

## **Overview**
Customer segmentation is the process of dividing customers into groups based on their characteristics, behaviors, or spending patterns. In this project, we used clustering techniques to analyze customer data from a retail mall dataset. The objective was to identify distinct customer groups to help businesses tailor marketing strategies and improve customer engagement.

---

## **Dataset**
### **Description**
The dataset contains 200 observations of customers with the following features:
- **Customer ID**: Unique identifier for each customer (dropped during clustering).
- **Gender**: Male or Female.
- **Age**: Age of the customer.
- **Annual Income (k$)**: Customer's annual income in thousands of dollars.
- **Spending Score (1-100)**: A score assigned to customers based on their spending habits and purchasing behavior.
### **Acknowledgment**
The dataset used in this project is publicly available on Kaggle, titled "Mall Customer Segmentation Data". I thank the original contributors for providing this valuable resource for analysis and learning purposes.

---

## **Objective**
- To identify distinct customer segments using clustering.
- To analyze the characteristics of each segment.
- To provide actionable business insights based on the segmentation.

---

## **Methodology**

### **1. Data Preprocessing**
- Removed irrelevant columns (e.g., `Customer ID`).
- Selected key features for clustering: `Age`, `Annual Income (k$)`, and `Spending Score (1-100)`.
- Standardized the data using **StandardScaler** to ensure fair distance calculation.

### **2. Clustering Technique**
- Applied **K-Means Clustering** to segment customers.
- Determined the optimal number of clusters (K) using:
  - **Elbow Method**: K=6 showed diminishing returns in Within-Cluster Sum of Squares (WCSS).
  - **Silhouette Score**: K=6 provided the highest silhouette score (~0.42), indicating well-separated clusters.

### **3. Visualization**
- Created 2D and 3D scatter plots to visualize clusters across features.
- Used pairwise scatter plots to explore feature relationships and cluster distribution.

---

## **Results**

### **Cluster Characteristics**
| Cluster | Age  | Annual Income (k$) | Spending Score | Description                       |
|---------|------|---------------------|----------------|-----------------------------------|
| 0       | 56   | 54                 | 49             | Older, moderate income/spending  |
| 1       | 27   | 57                 | 48             | Younger, moderate income/spending|
| 2       | 42   | 89                 | 17             | Middle-aged, high-income, low spenders |
| 3       | 33   | 87                 | 82             | Younger, high-income, high spenders |
| 4       | 25   | 25                 | 78             | Younger, low-income, high spenders |
| 5       | 46   | 26                 | 19             | Older, low-income, low spenders   |

---

### **Cluster Analysis and Business Insights**
#### **Cluster 3 (High-Income High Spenders)**
- **Characteristics**: Younger customers with high income and high spending.
- **Recommendations**: Focus on loyalty programs, premium product offerings, and personalized marketing.

#### **Cluster 4 (Low-Income High Spenders)**
- **Characteristics**: Younger customers with low income but high spending.
- **Recommendations**: Provide discounts or budget-friendly premium options.

#### **Cluster 2 (High-Income Low Spenders)**
- **Characteristics**: Middle-aged customers with high income but low spending.
- **Recommendations**: Upsell or cross-sell products that match their preferences.

#### **Cluster 0 (Moderate Income Moderate Spenders)**
- **Characteristics**: Older customers with moderate income and moderate spending.
- **Recommendations**: Use personalized offers to encourage more frequent purchases.

#### **Cluster 1 (Younger Moderate Spenders)**
- **Characteristics**: Younger customers with moderate income and spending behavior.
- **Recommendations**: Engage through dynamic, youth-focused marketing campaigns.

#### **Cluster 5 (Low-Income Low Spenders)**
- **Characteristics**: Older customers with low income and low spending.
- **Recommendations**: Offer discounts or incentives to encourage spending.

---

## **Visualizations**
- **Pairwise Scatter Plots**: Visualize feature relationships across clusters.
- **2D Scatter Plots**:
  - Age vs. Spending Score
  - Annual Income vs. Spending Score
  - Age vs. Annual Income
- **3D Scatter Plot**: Visualize clusters in three dimensions (`Age`, `Annual Income`, and `Spending Score`).
- **Cluster Size Bar Chart**: Show the number of customers in each cluster.

---

## **Conclusion**
The clustering analysis successfully segmented customers into six distinct groups based on their age, income, and spending behavior. These clusters provide actionable insights for businesses to design targeted marketing strategies, optimize resource allocation, and improve customer satisfaction.

This segmentation framework can be further enhanced by including additional features such as purchase history, geographic location, or product preferences.

---

## **Future Scope**
- Experiment with hierarchical clustering or DBSCAN to compare results.
- Include additional features like product categories or geographic data.
- Test clustering results using real-world marketing data to measure business impact.
