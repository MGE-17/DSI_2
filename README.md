# Project Overview

1. This project aims to segment customers into distinct groups based on their demographic characteristics and spending behavior using clustering techniques. By analyzing features such as Age, Gender, Profession, and Spending Score, the study identifies meaningful customer segments that reveal shopping patterns and preferences. 
2. The insights from these clusters can help businesses tailor marketing strategies, campaigns, enhance customer engagement and improve overall customer satisfaction through personalized experiences. Ultimately, this project demonstrates how clustering can transform raw customer data into actionable intelligence that supports data-driven business decision-making.


# Business Context:

Retail companies rely on understanding customer behavior to optimize marketing strategies, campaigns, enhance product recommendations, and improve overall customer satisfaction. However, treating all customers as a single group often results in inefficient marketing efforts and missed revenue opportunities. 

But, by identifying distinct customer segments based on demographic and behavioral characteristics, businesses can deliver more personalized experiences, allocate resources more effectively, and ultimately drive higher customer loyalty and profitability.


# Project Objective:

This project aims to apply data-driven segmentation techniques (Clustering) to group customers into distinct clusters based on their demographic characteristics - Age, Gender, Profession and their Spending Score. 

The resulting clusters will reveal unique customer profiles, such as high-value spenders, budget-conscious shoppers, or mid-range professionals. 

These insights will help retailers design and  develop targeted marketing strategies, personalized offers and make more informed business decisions that enhance customer engagement and profitability.


# Business Value:

By identifying clear customer segments, this project provides several strategic benefits:
1. **Targeted Marketing:** The marketing team can tailor promotions that align with customer preferences and needs.
2. **Improved Customer Retention:** The company can improve customer retention by offering personalized experiences and offers can strengthen customer relationships and encourage long term loyalty.
3. **Efficient Resource Allocation:** Management can allocate marketing and operational resources more effectively by focusing on high-value customer segments and their behaviors.


# Project Goals

The main goal of this project is to segment customers into meaningful groups based on their demographic and behavioral attributes to enable data-driven marketing decisions

1. Identify distinct customer segments using clustering algorithms (e.g., K-Means).

2. Analyze the key characteristics of each segment, including factors like income level, spending behavior, age group, and profession.

3. Generate actionable business insights that supports a retail company design targeted marketing campaigns and personalized engagement strategies.

4. Demonstrate the practical application of data science techniques, which includes data cleaning, exploratory analysis, feature engineering, and unsupervised learning, to solve a real-world business problem.


# Technical Stack:
**Programming Language:** Python

**Environment:** Jupyter Notebook 

**Libraries Used:**
1. Numpy: matrix operations
2. Pandas: data analysis
3. Matplotlib: creating graphs and plots
4. Seaborn: enhancing matplotlib plots
5. SKLearn: regression analysis


# Methodology
To address our business question **“Can we cluster customers into different segments based on their Spending Score and demographic features such as Age, Gender, and Profession?”** we followed a structured data science workflow. This ensures that our analysis is transparent, reproducible, and delivers actionable business insights.

## Data Collection

### Dataset Description

The dataset used in this project is titled Shop Customer Data (Customers.csv). It contains information about customers’ demographic characteristics, professional background, and spending behavior. Each row represents a unique customer record, which includes details that can help identify different customer groups.


### Dataset Source
This dataset originates from Kaggle’s Shop Customer Data repository, designed for learning and analysis in retail marketing and customer segmentation.
It can be accessed here: [Shop Customer Data on Kaggle](https://www.kaggle.com/datasets/datascientistanna/customers-dataset)

### Relevance to the Business Problem
This dataset contains both demographic (Age, Gender, Profession, Family Size) and behavioral (Spending Score, Income) variables, making it ideal for customer segmentation analysis.

By applying clustering algorithms, we can uncover groups of customers with similar characteristics and spending habits. These insights help businesses:
- Design targeted marketing campaigns
- Create personalized offers based on customer profiles
- Improve customer satisfaction and retention

## Data Preprocessing - Emilia 

- Imported the dataset (Customers.csv) and reviewed column names, data types, and missing values.
- Handled missing or inconsistent entries through imputation or removal where necessary.
- Encoded categorical features such as Gender and Profession into numerical format for analysis.
- Standardized numerical features (Age, Annual Income ($), Spending Score (1-100), Work Experience, Family Size) to ensure equal weight in clustering.

## Exploratory Data Analysis (EDA) - Emilia & Harris

- Conducted descriptive statistics and visualized distributions for all numeric features (histograms, boxplots).
- Used pairplots and correlation heatmaps to identify relationships between variables.
- Examined potential patterns in spending behavior across demographic groups (e.g., income vs. spending score by gender or profession).
- Detected and addressed potential outliers that could distort clustering results.

![alt text](image.png)

## Feature Selection - Preethi

- Selected key features for clustering based on business relevance and statistical patterns:
    - Demographic: Age, Gender, Profession, Family Size
    - Behavioral: Annual Income ($), Spending Score (1-100), Work Experience
- Applied feature scaling (StandardScaler) to normalize feature ranges.

## Clustering Analysis - Emilia, Miguel, Sanyam

- Applied K-Means clustering to group customers into distinct segments.
- Determine the optimal number of clusters (k) using the Elbow Method and Silhouette Score.
- Compared cluster characteristics to interpret their business meaning (e.g., high-value vs. budget-conscious customers).
- Optionally tested Hierarchical Clustering to validate cluster stability and interpret similarity between groups.

## Visualization - Olena 

- Created 2D and 3D scatterplots to visualize clusters using combinations such as:
    - Annual Income ($) vs. Spending Score (1-100)
    - Age vs. Spending Score (1-100)
- Used Principal Component Analysis (PCA) to reduce dimensionality and visualize clusters more effectively.
- Developed summary charts (average Age, Income, Spending per cluster) to highlight key differences.


## Key Features

| **Feature** | **Description** | **Type** |
|--------------|-----------------|-----------|
| **CustomerID** | Unique identifier assigned to each customer | Numerical |
| **Gender** | Gender of the customer (e.g., Male, Female) | Categorical |
| **Age** | Age of the customer in years | Numerical |
| **Annual Income ($)** | Customer’s annual income in U.S. dollars | Numerical |
| **Spending Score (1-100)** | A score assigned by the business based on customer spending patterns and purchasing behavior | Numerical |
| **Profession** | Customer’s occupation category (e.g., Engineer, Doctor, Artist, etc.) | Categorical |
| **Work Experience** | Number of years of professional experience | Numerical |
| **Family Size** | Number of family members in the customer’s household | Numerical |


## Insights and Recommendations — Team

Based on the clustering analysis, several meaningful insights emerged that reveal how different demographic and behavioral factors influence customer spending patterns. These insights can directly support marketing, sales, and customer engagement strategies.

### Key Insights

- **Cluster 0 — Young, High-Income, High-Spending Customers**  
  These customers have strong purchasing power and high engagement, making them ideal targets for premium offers, loyalty programs, and early-access campaigns.

- **Cluster 1 — Older, High-Income, Low-Spending Customers**  
  Despite high income levels, this segment demonstrates conservative spending behavior. They are more likely to respond to trust-based communication, value-driven promotions, and senior-friendly benefits.

- **Cluster 2 — Middle-Aged, Moderate-Income, Moderate-Spending Customers**  
  This group represents a stable but price-sensitive customer base. Bundled offers, promotions, and personalized discounts can help increase spending and retention.

### Additional Observations

- **Income and age** play a significant role in predicting customer spending. Younger individuals with higher incomes tend to spend the most.  
- **PCA and 3D visualizations** indicate strong cluster separation, validating the quality of the segmentation.  
- High-value segments (especially Cluster 0) can significantly impact revenue when targeted effectively.

### Recommendations

1. **Develop targeted marketing campaigns** tailored to each cluster’s preferences and spending behaviors.  
2. **Enhance customer retention** by offering personalized experiences—particularly for high-value customers in Cluster 0.  
3. **Introduce value-focused offerings** for Cluster 1 to encourage engagement without aggressive promotion.  
4. **Promote bundled and discount-based campaigns** for Cluster 2 to increase purchase frequency.  
5. **Consider adding more behavioral features** (e.g., purchase frequency, recency, product categories) in future analyses to strengthen segmentation accuracy.


## Visualization Summary
| **Visualization** | **Purpose** | **Key Takeaway** |
|--------------------|-------------|------------------|
| **Annual Income vs. Spending Score** | 2D scatterplot showing spending by income level. | Identifies premium and budget-conscious groups. |
| **Age vs. Spending Score** | Compares spending patterns by age. | Younger customers spend more frequently. |
| **PCA Projection** | Reduces features into 2 components. | Confirms clear cluster separation. |
| **3D Cluster View** | Combines Age, Income, and Spending. | Shows complete cluster separation. |
| **Average Metrics per Cluster** | Bar charts for mean Age, Income, and Spending. | Highlights differences among groups. |
| **Customer Count per Cluster** | Cluster size distribution. | Cluster 1 largest; Cluster 0 smallest but most profitable. |


## Project Assumptions and Limitations
- **Spending Score Assumption:**  
  The dataset doesn’t specify how the *Spending Score (1-100)* is calculated (frequency, amount, loyalty, etc.). We assumed it represents general purchasing behavior, but verification with business context is needed.  

- **Dataset Representativeness:**  
  The dataset is open-sourced and may not reflect a specific company’s real customer base. It may be biased toward certain demographics or regions.  

- **Cluster Selection (k):**  
  We chose `k=3` based on the Elbow Method. However, different evaluation metrics (e.g., Silhouette Score) might suggest other valid choices.  

- **Model Constraints:**  
  K-Means assumes equal variance and spherical clusters, which may not fully represent complex real-world behavior.  

**Next Steps:**  
- Validate the *Spending Score* definition with stakeholders.  
- Test different cluster counts (`k=4`, `k=5`).  
- Compare results with **Hierarchical** or **DBSCAN** clustering.  
- Incorporate new behavioral variables for richer segmentation.


# Project Reproducibility

1.	Clone this repository:
git clone https://github.com/MGE-17/DSI_2
2.	Navigate to the project directory:
cd DSI_2
3.	Install dependencies:
pip install kagglehub
pip install pypalettes
4.	Launch the notebook:
jupyter notebook


# Conclusion - Team

In this project, customer data was analysed using K-Means clustering to group customers based
on Age, Annual Income and Spending Score. After comparing the overall averages with each cluster's averages, CLUSTER 0 emerged as the most valuable segment because it showed the highest spending score, making it the ideal target for marketing efforts.
Targeting this high-spending cluster enables the business to allocate resources more efficiently and design personalized offers that match customer behaviour. This data-driven approach helps increase customer engagement, improve conversion rates and ultimately boost overall profitability.



# Video links
| **Name** | **Link** |
| Chung Ho Lee | |
| Emilia Lubanska Oledzka | |
| Miguel Gomez Escobar | |
| Olena Oliinyk | |
| Preethi Sivakumar | |
| Sanyam Arora | |