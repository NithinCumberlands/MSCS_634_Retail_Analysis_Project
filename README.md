# Retail_Transactions_Analysis

## Dataset Summary
For this project, I used a **Retail Transactions Dataset** which contains **1,000,000 entries** and **13 columns**. The dataset includes a variety of features such as:
- **Transaction_ID**: A unique identifier for each transaction.
- **Date**: The timestamp of when the transaction occurred.
- **Customer_Name**: Name of the customer making the purchase.
- **Product**: List of products purchased.
- **Total_Items**: The total number of items purchased in the transaction.
- **Total_Cost**: The total cost of the items purchased.
- **Payment_Method**: The method of payment used (e.g., Cash, Mobile Payment).
- **City**: City where the transaction took place.
- **Store_Type**: Type of store where the transaction occurred (e.g., Warehouse Club, Specialty Store).
- **Discount_Applied**: Whether a discount was applied to the transaction (True/False).
- **Customer_Category**: The category of the customer (e.g., Homemaker, Professional).
- **Season**: Season during which the transaction took place (e.g., Winter, Fall).
- **Promotion**: The promotion applied to the transaction (e.g., Buy One Get One, Discount on Selected Items).

I chose this dataset because it provides valuable insights into retail sales patterns, which can be useful for analyzing customer behavior, identifying popular products, and understanding sales trends.

## Key Insights from My Analysis
- **Most Popular Product Categories**: By analyzing the transaction data, I identified the most popular product categories based on total sales volume.
- **Time-Based Trends**: I observed peak sales times, such as holidays or weekends, that drive higher transaction volumes.
- **Price Distribution**: The **Price** distribution was right-skewed, indicating that most products have lower prices with a few higher-priced items.
- **Outliers**: After detecting outliers in **Quantity** and **Price** using boxplots, I removed extreme outliers to improve the quality of the analysis.

## Major Steps Taken in Data Cleaning and Exploration
1. **Missing Values**: I handled missing values by imputing the **Total_Cost** and **Total_Items** columns with the mean of each respective column.
2. **Duplicates**: I checked for duplicate rows and removed them to ensure no redundancy in the dataset.
3. **Outliers**: I identified and removed outliers in **Quantity** and **Price** using the **IQR method**, ensuring that extreme values do not distort the analysis.
4. **Date Parsing**: I converted the **Date** column into a proper datetime format to allow for more meaningful time-based analysis. I also extracted additional time features such as **Year**, **Month**, **Day**, and **Day of Week** to explore trends over time.

## Challenges Encountered and How They Were Addressed
- **Handling Missing Data**: Initially, I thought about removing rows with missing values, but this would have resulted in losing a large portion of the data. Instead, I chose to **impute** the missing values using the **mean** to retain data consistency.
- **Outliers**: Outliers in **Quantity** and **Price** posed a challenge because they could distort my findings. After visualizing the data using boxplots, I decided to **remove the extreme outliers** using the **IQR method**, which resulted in cleaner and more reliable data.
- **Date Format Issues**: The **Date** column initially had inconsistent formats, so I had to convert it into a **datetime** format to enable time-based analysis. This was crucial for exploring trends over time.

## Conclusion
This deliverable focused on the **data cleaning** and **exploratory data analysis (EDA)** of the retail transactions dataset. Through this process, I handled missing data, removed duplicates, and addressed outliers. I also derived key insights, such as identifying the most popular product categories and observing sales trends over time. The next steps in the project will involve building predictive models to analyze the factors that influence sales.

## Files Included
- **`Retail_Transactions_Dataset.csv`**: The raw dataset.
- **`cleaned_retail_transactions.csv`**: The cleaned version of the dataset after data preparation.
- **`Retail_Transactions_EDA.ipynb`**: Jupyter notebook containing all the code for data cleaning, analysis, and visualizations.
- **`Comprehensive_Report.pdf`**: The report summarizing the project steps, challenges, insights, and next steps.

