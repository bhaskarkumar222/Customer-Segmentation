# Customer-Segmentation
## Goal of the project 
The goal is to help the business understand its customers better and create effective engagement strategies based on their behaviour, ultimately boosting sales revenue. By using RFM (Recency, Frequency, Monetary) analysis to segment customers into 11 groups based on their purchase history

## Analysis Approach
The first step towards generating useful insights from the data was the data preparation, quality assessment and data cleaning step. After the cleaning process exploratory data analysis on the dataset and identification customer purchasing behaviours to generate insights can be performed.

**Customer Demographics:**
-	**Irrelevant Columns:** Dropped 1 irrelevant column.
-	**Missing Values:** Addressed missing values in 5 columns by either dropping records or imputing values.
-	**Gender Standardization:** Standardized gender data to remove inconsistencies.
-	**Date of Birth:** Transformed into 'Age' and 'Age Group'; removed one outlier.
-	**Duplicates:** No duplicate records found.
  
**New Customer:**
-	**Irrelevant Columns:** Dropped 5 irrelevant columns.
-	**Missing Values:** Addressed missing values in 4 columns.
-	**Date of Birth:** Transformed into 'Age' and 'Age Group'.
-	**Duplicates:** No duplicate records found.
  
**Transaction Data:**
-	**Date Format:** Changed 'product_first_sold_date' to datetime format.
-	**Missing Values:** Addressed missing values in 7 columns.
-	**Profit Column:** Created a new 'Profit' column.
-	**Duplicates:** No duplicate records found.

**CustomerAddress:**
-	**State Standardization:** Standardized state data to remove inconsistencies.
-	**Customer IDs:** Some customer IDs from Customer Demographics were missing in the Address table.

## **Customer  segmentation Analysis:**
We use a method called RFM Analysis, which stands for Recency, Frequency, and Monetary. This approach groups customers based on their past purchase behavior:
-	**Recency:** How recently they made a purchase.
-	**Frequency:** How often they make purchases.
-	**Monetary:** How much money they spend.
  
**Process:**
Customers are segmented into 11 different groups based on their purchase history. This segmentation allows us to identify which groups are most valuable and should be targeted to boost sales revenue.
