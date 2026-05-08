# 🛒 SmartCart Customer Clustering System

## 📌 Project Overview
SmartCart is a growing e-commerce platform that previously used generic marketing strategies for all customers.This approach resulted in inefficient marketing, delayed identification of churn-prone users, and missed opportunities to retain high-value customers. 

This project implements an intelligent customer segmentation system using unsupervised machine learning. [cite_start]By analyzing historical transaction data, the system groups customers into meaningful clusters based on their purchasing behavior, engagement levels, and loyalty indicators.

## 📊 Dataset Description
[cite_start]The dataset contains **2,240 customer records** with **22 attributes**[cite: 4]. The features are divided into several categories:
* [cite_start]**Demographics:** Year of birth, Education, Marital Status, Income, and household details[cite: 13, 14].
* [cite_start]**Purchase Behavior (Amount Spent):** Spending over the last 2 years on categories like Wines, Fruits, Meat, Fish, Sweets, and Gold[cite: 15, 16].
* [cite_start]**Purchase Behavior (Frequency):** Number of purchases made via discounts, website, catalog, and physical stores, as well as monthly web visits[cite: 17, 18].
* [cite_start]**Customer Feedback:** Recency (days since last purchase) and recent complaints[cite: 19, 21].

## 🛠️ Tech Stack
* **Language:** Python
* **Libraries:** Pandas, NumPy, Scikit-Learn, Matplotlib, Seaborn
* **Algorithms:** kMeans Cluctering , Agglomorative algo  

## 🚀 Project Steps & Methodology

### 1. Data Preprocessing & Cleaning
* Handled missing values (e.g., in the `Income` column).
* Engineered new features (e.g., calculating customer `Age` from `Year_Birth`, or `Total_Spent` from individual product categories).
* [cite_start]Encoded categorical variables like `Education` and `Marital_Status`[cite: 14].

### 2. Exploratory Data Analysis (EDA)
* Analyzed the distribution of spending habits and income.
* [cite_start]Visualized correlations between features (e.g., Income vs. Amount spent on Wines)[cite: 14, 16].
* Handled outliers to ensure they didn't skew the clustering models.

### 3. Feature Scaling & Dimensionality Reduction
* [cite_start]Standardized the dataset using `StandardScaler` so that high-value features (like `Income`) didn't dominate low-value features (like `NumWebVisitsMonth`)[cite: 14, 18].
* Applied Principal Component Analysis (PCA) to reduce the 22 dimensions and visualize the clusters in 2D/3D space.

### 4. Clustering Algorithm Implementation
* [cite_start]Utilized Unsupervised Machine Learning Agglomorative algorithms to discover hidden patterns[cite: 7, 9].
* Used the **Elbow Method**  to determine the optimal number of clusters (K).
* [cite_start]Trained the final clustering model and assigned labels to all 2,240 records[cite: 4].

### 5. Cluster Profiling & Business Insights

* **Cluster 0 ("Budget-Conscious Couples"):** Partners with lower household incomes (~$39k) and lower total spending. They visit the website frequently but rely heavily on discount deals (`NumDealsPurchases`) when making purchases.
* **Cluster 1 ("Premium Families"):** High-income (~$72k) partners with massive total spending. They are heavy, high-value shoppers across all channels (physical stores, catalogs, and web) and rarely rely on discounts.
* **Cluster 2 ("Single Parents on a Budget"):** Customers living alone with the highest average number of children at home. They have the lowest income (~$36k) and total spending, hunting for deals and visiting the website frequently.
* **Cluster 3 ("Affluent Singles"):** High-income (~$70k) individuals living alone with high spending levels. They rarely use discounts but have an exceptional **32% response rate** to marketing campaigns, making them highly reactive to premium product launches.

## 💡 Business Recommendations
Based on the clusters identified, SmartCart can now:
1. Target high-income clusters with premium catalog offers.
2. Send discount-heavy email campaigns specifically to the "Deal Hunter" segment.
3. [cite_start]Re-engage at-risk customers (high `Recency` score) with personalized retention campaigns[cite: 21].

## 💻 How to Run This Project
1. Clone the repository: `git clone https://github.com/yourusername/SmartCart-Clustering.git`
2. Install dependencies: `pip install -r requirements.txt`
3. Run the Jupyter Notebook: `jupyter notebook SmartCart_Clustering.ipynb`


 
