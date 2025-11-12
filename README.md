# Project Overview

1. This project aims to segment customers into distinct groups based on their demographic characteristics and spending behavior using clustering techniques. By analyzing features such as Age, Gender, Profession, and Spending Score, the study identifies meaningful customer segments that reveal shopping patterns and preferences. 
2. The insights from these clusters can help businesses tailor marketing strategies, campaigns, enhance customer engagement and improve overall customer satisfaction through personalized experiences. Ultimately, this project demonstrates how clustering can transform raw customer data into actionable intelligence that supports data-driven business decision-making.


# Business Context:

Retail companies rely on understanding customer behavior to optimize marketing strategies, campaigns, enhance product recommendations, and improve overall customer satisfaction. However, treating all customers as a single group often results in inefficient marketing efforts and missed revenue opportunities. 

But, by identifying distinct customer segments based on demographic and behavioral characteristics, businesses can deliver more personalized experiences, allocate resources more effectively, and ultimately drive higher customer loyalty and profitability.


# Project Objective:

This project aims to apply data-driven segmentation techniques (Clustering) to group customers into distinct clusters based on their demographic characteristics - Age, Gender, Profession and their Spending Score. The resulting clusters will reveal unique customer profiles, such as high-value spenders, budget-conscious shoppers, or mid-range professionals. These insights will help retailers design and  develop targeted marketing strategies, personalized offers and make more informed business decisions that enhance customer engagement and profitability.


# Business Value:

By identifying clear customer segments, this project provides several strategic benefits to the organization:
    1. Targeted Marketing: The marketing team can tailor promotions that align with customer preferences and needs.
    2. Improved Customer Retention: The company can improve customer retention by offering personalized experiences and offers can strengthen customer relationships and encourage long term loyalty.
    3. Efficient Resource Allocation: Management can allocate marketing and operational resources more effectively by focusing on high-value customer segments and their behaviors.


# Project Goals

The main goal of this project is to segment customers into meaningful groups based on their demographic and behavioral attributes to enable data-driven marketing decisions

    1. Identify distinct customer segments using clustering algorithms (e.g., K-Means).

    2. Analyze the key characteristics of each segment, including factors like income level, spending behavior, age group, and profession.

    3. Generate actionable business insights that supports a retail company design targeted marketing campaigns and personalized engagement strategies.

    4. Demonstrate the practical application of data science techniques, which includes data cleaning, exploratory analysis, feature engineering, and unsupervised learning, to solve a real-world business problem.

# Technical Stack:
Programming Language: Python
Prerequisites
    1. Python 3.9+
    2. Jupyter Notebook

Libraries Used:
    1. Numpy: matrix operations
    2. Pandas: data analysis
    3. Matplotlib: creating graphs and plots
    4. Seaborn: enhancing matplotlib plots
    5. SKLearn: regression analysis

# Methodology
To address our business question “Can we cluster customers into different segments based on their Spending Score and demographic features such as Age, Gender, and Profession?” we followed a structured data science workflow. This ensures that our analysis is transparent, reproducible, and delivers actionable business insights.

## 3.1) Data Collection

Dataset Description

The dataset used in this project is titled Shop Customer Data (Customers.csv). It contains information about customers’ demographic characteristics, professional background, and spending behavior. Each row represents a unique customer record, which includes details that can help identify different customer groups.

### Key Features

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

### Dataset Source
This dataset originates from Kaggle’s Shop Customer Data repository, designed for learning and analysis in retail marketing and customer segmentation.
It can be accessed here: [Shop Customer Data on Kaggle](https://www.kaggle.com/datasets/datascientistanna/customers-dataset)

### Relevance to the Business Problem
This dataset contains both demographic (Age, Gender, Profession, Family Size) and behavioral (Spending Score, Income) variables, making it ideal for customer segmentation analysis.

By applying clustering algorithms, we can uncover groups of customers with similar characteristics and spending habits. These insights help businesses:
- Design targeted marketing campaigns
- Create personalized offers based on customer profiles
- Improve customer satisfaction and retention

## 3.2) Data Preprocessing - Emilia 

Imported the dataset (Customers.csv) and reviewed column names, data types, and missing values.
Handled missing or inconsistent entries through imputation or removal where necessary.
Encoded categorical features such as Gender and Profession into numerical format for analysis.
Standardized numerical features (Age, Annual Income ($), Spending Score (1-100), Work Experience, Family Size) to ensure equal weight in clustering.

## 3.3) Exploratory Data Analysis (EDA) - Emilia & Harris

Conducted descriptive statistics and visualized distributions for all numeric features (histograms, boxplots).
Used pairplots and correlation heatmaps to identify relationships between variables.
Examined potential patterns in spending behavior across demographic groups (e.g., income vs. spending score by gender or profession).
Detected and addressed potential outliers that could distort clustering results.

## 3.4) Feature Selection - Preethi

Selected key features for clustering based on business relevance and statistical patterns:
Demographic: Age, Gender, Profession, Family Size
Behavioral: Annual Income ($), Spending Score (1-100), Work Experience
Applied feature scaling (StandardScaler) to normalize feature ranges.

## 3.5) Clustering Analysis - Emilia, Miguel, Sanyam

Applied K-Means clustering to group customers into distinct segments.
Determine the optimal number of clusters (k) using the Elbow Method and Silhouette Score.
Compared cluster characteristics to interpret their business meaning (e.g., high-value vs. budget-conscious customers).
Optionally tested Hierarchical Clustering to validate cluster stability and interpret similarity between groups.


## 3.6) Visualization - Olena 

Created 2D and 3D scatterplots to visualize clusters using combinations such as:
Annual Income ($) vs. Spending Score (1-100)
Age vs. Spending Score (1-100)
Used Principal Component Analysis (PCA) to reduce dimensionality and visualize clusters more effectively.
Developed summary charts (e.g., average income, spending, family size per cluster) to highlight key differences.

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
5.	Open Customer_Purchasing_Behaviour.ipynb and run all cells.



# Insights and Recommendations - Team

Based on the clustering results, several insights were derived, such as:

    1. Identification of high-value customer segments that contribute significantly to revenue based on demographic and behavioral characteristics (e.g., income, spending habits, age groups).
    2. Recognition of potential customer segments for targeted marketing campaigns.
    3. Understanding of customer preferences and behaviors to improve product offerings, thereby  improving customer engagement.


# Conclusion - Team

The Customer Segmentation Analysis project provides a comprehensive approach to understand and categorize customers. By leveraging clustering techniques and visualizations, businesses can gain valuable insights into their customer base and make informed decisions to enhance their marketing strategies and overall performance.
