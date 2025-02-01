# Customer-Segmentation with RFM Model

![image alt](https://github.com/bhaskarkumar222/Customer-Segmentation/blob/967b7f9118c80ad0cb5e80ed27a4f93b579bbd5e/Visualization/Customer%20Segmentation.png)

## Goal of the project 
The goal is to help the business understand its customers better and create effective engagement strategies based on their behaviour, ultimately boosting sales revenue. By using RFM (Recency, Frequency, Monetary) analysis to segment customers into 11 groups based on their purchase history

**Tools**: Jupyter Notebook (Python).

**Skills:** Python libraries (Numpy, Pandas, Matplotlib, Seaborn), for loop, def statement, data merging, nulls & duplicates handling, RFM analysis, quantile scoring, visualization.

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

## Exploratory Data Analysis on Customer Segments
### Wealth Segmentation by Age Group
  - The majority of customers across all age groups belong to the 'Mass Customer' segment, indicating that this category has the widest reach and customer base.
  - The 'High Net Worth' segment consistently holds the second-largest share of customers, highlighting a significant but more exclusive group with higher spending capacity.
  - Unlike other age groups, the 40-50 category sees the 'Affluent' segment surpass the 'High Net Worth' customers, suggesting a shift in financial standing or spending behavior within this demographic.



 <table>
  <tr>
    <td><b>New Customers by Age Distribution</b></td>
    <td><b>Old Customers by Age Distribution</b></td>
  </tr>
  <tr>
    <td><img src="https://github.com/bhaskarkumar222/Customer-Segmentation/blob/b522906c4e52857ad9263298b71ccda80c713875/Visualization/New%20Customers%20-%20Wealth%20Segmentation%20by%20Age%20Group.jpg" height="400" align="middle" ></td>
    <td><img src="https://github.com/bhaskarkumar222/Customer-Segmentation/blob/b522906c4e52857ad9263298b71ccda80c713875/Visualization/old%20Customers%20-%20Wealth%20Segmentation%20by%20Age%20Group.jpg" height="400" align="middle"></td>
  </tr>
  </table>

  ## **RFM Analysis and Customer Segmentation:**
We use a method called RFM Analysis, which stands for Recency, Frequency, and Monetary. This approach groups customers based on their past purchase behavior:
-	**Recency:** How recently they made a purchase.
-	**Frequency:** How often they make purchases.
-	**Monetary:** How much money they spend.
  
**Process:**
Customers are segmented into 11 different groups based on their purchase history. This segmentation allows us to identify which groups are most valuable and should be targeted to boost sales revenue.

  - Platinum Customers
  - Very Loyal Customers
  - Recent Customers
  - Potential Customers
  - Lost Customers
  - Losing Customers
  - Late Bloomer
  - High Risk Customers
  - Evasive Customers
  - Becoming Loyal
  - Almost lost Customers
    
### Number of Customers by Customer Segment :
*Some key insights from the "Number of Customers by Customer Segment"*:

  - **"Losing Customer" Segment is the Largest** – This category has the highest number of customers, which could indicate retention issues or disengagement from the brand. Businesses should focus on retention strategies such as personalized offers or loyalty programs.
  - **High Engagement in "Very Loyal" and "Potential Customer" Segments** – A significant number of customers fall into these segments, showing strong engagement and possible future high-value customers. Nurturing these customers with exclusive benefits can help convert them into long-term loyal clients.
  - **At-Risk Segments ("Almost Lost" & "Lost Customers") Need Attention** – The presence of a notable number of customers in these segments signals a need for re-engagement efforts. Businesses should analyse the reasons behind customer churn and implement targeted reactivation campaigns.

<img src="https://github.com/bhaskarkumar222/Customer-Segmentation/blob/00caaf4106c568fefe660104410119aa1b8e4279/Visualization/Number%20of%20Customers%20by%20Customer%20Segment.jpg" height="400" align="middle">

### Recency vs Monetary :
*Here are some key insights from the "Recency vs Monetary" scatter plot:*
-	**Negative Correlation Between Recency and Monetary** – Customers who made recent purchases tend to have higher monetary values, indicating that frequent shoppers contribute more revenue.
-	**High-Value Customers Are More Active** – The highest monetary transactions are concentrated in the low recency range between 0-50 days  suggesting that engaged customers tend to spend more.
-	**Inactive Customers Spend Less** – As recency increases monetary values generally decrease, indicating potential churn and the need for re-engagement strategies.

<img src="https://github.com/bhaskarkumar222/Customer-Segmentation/blob/00caaf4106c568fefe660104410119aa1b8e4279/Visualization/Recency%20vs%20Monetary.jpg" height="400" align="middle">

### Frequency vs Monetary :
*Here are some key insights from the "Frequency vs Monetary" scatter plot:*

  - **Positive Correlation Between Frequency and Monetary** – Customers who purchase more frequently tend to have higher total spending, indicating that loyal customers contribute significantly to revenue.
  
  - **High-Spending Customers Have Higher Frequency** – The highest monetary values are observed among customers with purchase frequencies above 8, reinforcing the importance of repeat buyers.
  
  - **Potential for Upselling and Loyalty Programs** – Encouraging customers with lower frequencies (1-5 purchases) to buy more could boost overall revenue. Loyalty programs, personalized offers, and targeted marketing can help achieve this.

<img src="https://github.com/bhaskarkumar222/Customer-Segmentation/blob/00caaf4106c568fefe660104410119aa1b8e4279/Visualization/Frequency%20vs%20Monetary.jpg" height="400" align="middle">

### Customer Distribution by RFM Label
*The bar chart represents the Customer Distribution by RFM Label, which categorizes customers into four segments: Bronze, Silver, Gold, and Platinum. Here are some insights:*

  - **Platinum Segment Leads** – The highest number of customers fall under the Platinum category, indicating a strong base of high-value customers.
  - **Gold and Silver are Well-Represented** – Both Gold and Silver categories have significant customer numbers, suggesting a stable mid-tier customer base.
  -- **Bronze Category is the Smallest** – The Bronze category has the least number of customers, which could indicate a lower engagement or recent acquisition of these customers.
  - **Potential for Upgrading Customers** – There might be an opportunity to convert Silver and Gold customers into Platinum through better engagement, loyalty programs, or incentives.

<img src="https://github.com/bhaskarkumar222/Customer-Segmentation/blob/00caaf4106c568fefe660104410119aa1b8e4279/Visualization/Customer%20Distribution%20by%20RFM%20Label.jpg" height="400" align="middle">

### Comparision of RFM Segments by Average Quartile
*Here are some key insights from the Comparison of RFM Segments by Average Quartile chart:*

  - **"Very Loyal" Customers Score Highest** – They have the highest quartile scores across all metrics, indicating frequent, recent, and high-value transactions.
  - **Variation Across Segments** – Some customer groups, such as "Late Bloomers," show lower frequency or monetary quartiles, suggesting potential for engagement strategies.
  - **Balanced Segments** – Several customer segments have a mix of mid-range quartile scores, showing room for improvement in retention and value growth.

<img src="https://github.com/bhaskarkumar222/Customer-Segmentation/blob/00caaf4106c568fefe660104410119aa1b8e4279/Visualization/Comparision%20of%20RFM%20Segments%20by%20Average%20Quartile.jpg" height="400" align="middle">

# Insights and Findings from the RFM Analysis Project
## Conclusions of the Project
  1. **Customer Segmentation & Behavior**: RFM analysis successfully segmented customers into different groups based on purchasing behavior, enabling targeted marketing strategies.
  2. **Loyalty Insights**: A significant portion of customers are in the “Very Loyal” and “Platinum” segments, indicating a strong repeat customer base. However, "Lost" and "Almost Lost" segments highlight areas for customer re-engagement.
  3. **Revenue Correlation**: High-frequency customers tend to contribute more to revenue, as shown in the Frequency vs. Monetary analysis.
  4. **Recency Impact**: Customers who made recent purchases have a higher monetary value, suggesting that timely engagement is crucial for revenue growth.
  5. **Marketing Optimization**: Personalized retention strategies can be applied to at-risk customers, while exclusive offers can be targeted toward high-value customers to maximize revenue.

## Key Insights & Findings
  - The Platinum and Very Loyal customers contribute the most to the business, warranting special retention strategies.
  - The Lost and Almost Lost customers form a notable segment, highlighting a need for reactivation campaigns.
  - Recency and Monetary values show an inverse relationship, meaning customers who haven't purchased in a long time contribute less revenue.
  - Frequent shoppers tend to spend more, justifying loyalty programs to retain these customers.
  - Strategic focus should be on improving retention and re-engagement efforts for at-risk customers while maintaining strong relationships with high-value ones.












