# Credit Card Customer Segmentation

## Project Overview

This project focuses on performing customer market segmentation using unsupervised machine learning techniques on a credit card usage dataset. The goal is to identify distinct groups of customers based on their spending and behavior patterns to enable targeted marketing strategies and enhance customer relationship management.

## Dataset

The project utilizes a dataset containing information about credit card customers, including various features related to their balance, purchase behavior (one-off, installments), cash advances, payments, credit limit, and tenure.

## Methodology

1.  **Data Loading and Initial Exploration:** The dataset was loaded and initial checks for missing values and duplicates were performed.
2.  **Data Preprocessing:**
    *   Irrelevant features ('CUST\_ID') were removed.
    *   Missing values in 'MINIMUM\_PAYMENTS' and 'CREDIT\_LIMIT' were imputed with the mean.
    *   Outliers were identified using the Interquartile Range (IQR) method and capped to the upper and lower bounds.
    *   The data was scaled using `StandardScaler` to prepare it for clustering.
3.  **Exploratory Data Analysis (EDA):**
    *   Distribution plots were generated to visualize the distribution of each feature.
    *   A heatmap was created to show the correlation between features.
4.  **K-Means Clustering:**
    *   The optimal number of clusters was determined using the Elbow Method, visualized with `KElbowVisualizer` from the yellowbrick library.
    *   K-Means clustering was applied with the optimal number of clusters (4 in this case).
    *   Cluster centers were inverse transformed to understand the characteristics of each segment in the original scale.
5.  **Cluster Analysis and Interpretation:** The characteristics of each identified cluster were analyzed based on their centroid values, providing insights into different customer segments.

## Identified Customer Segments

Based on the K-Means clustering, four distinct customer segments were identified:

*   **Cluster 0:** Moderate balance, high balance frequency, high purchases (especially one-off), low cash advance, high purchase frequency, moderate credit limit and payments. Likely represents engaged purchasers with a preference for one-off transactions.
*   **Cluster 1:** Higher balance, very high balance frequency, very high overall purchases (mix of one-off and installment), moderate cash advance, very high purchase and installment frequency, highest credit limit and payments. Represents high-value, high-spending customers.
*   **Cluster 2:** Highest balance, high balance frequency, low purchases, highest cash advance usage and transactions, low purchase frequency, moderate credit limit, high minimum payments. Likely represents customers primarily using credit for cash advances.
*   **Cluster 3:** Lowest balance, lowest balance frequency, low overall purchases, low cash advance usage, low purchase frequency, lowest credit limit, payments, and minimum payments. Represents customers with low credit card activity.

## Potential Applications

The insights gained from this segmentation can be used for:

*   Developing targeted marketing campaigns for each customer segment.
*   Improving customer relationship management by offering personalized services.
*   Informing product development and service offerings based on segment needs.
*   Assessing credit risk associated with different customer groups.
*   Optimizing resource allocation by focusing on valuable segments.

This project demonstrates the application of unsupervised machine learning for practical business insights.
