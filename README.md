# Retail_Transactions_Analysis

## Dataset Summary
For this project, I used a **Retail Transactions Dataset** containing **541,909 entries** and **8 columns**. The dataset includes the following features:

- **InvoiceNo**: A unique invoice number for each transaction.
- **StockCode**: Product (item) code.
- **Description**: Product (item) name.
- **Quantity**: The number of items purchased for each transaction line.
- **InvoiceDate**: The date and time when each transaction was generated.
- **UnitPrice**: Unit price of the product in sterling.
- **CustomerID**: Unique identifier for each customer (may contain missing values).
- **Country**: Country of the customer.

## Key Insights from My Analysis
- **Top-Selling Items**: I identified products with the highest total quantities sold by aggregating `Quantity`.
- **Seasonal Trends**: By parsing `InvoiceDate`, I observed peak transaction volumes during holiday seasons (e.g., December).
- **Revenue Distribution**: Calculated revenue per line (`Quantity × UnitPrice`) and found a right-skewed distribution, indicating most orders are low-value with occasional high-value transactions.
- **Geographic Distribution**: The majority of transactions occurred in the United Kingdom, with smaller volumes in other European countries and beyond.

## Major Steps Taken in Data Cleaning and Exploration
1. **Handling Missing Values**: Imputed missing `CustomerID` entries where needed, and dropped any rows with critical missing fields.
2. **Removing Duplicates**: Detected and removed exact duplicate rows to avoid redundancy.
3. **Outlier Detection**: Used the **IQR method** on `Quantity` and derived `Total_Cost` to filter out extreme values that could distort analysis.
4. **Feature Engineering**:  
   - Created `Total_Cost` as `Quantity × UnitPrice`.  
   - Parsed `InvoiceDate` into datetime and extracted `Year`, `Month`, `Day`, and `DayOfWeek` for time-series analysis.

## Challenges Encountered and How They Were Addressed
- **Inconsistent Date Formats**: Converted the `InvoiceDate` column into a unified datetime format to enable chronological analyses.
- **Missing Customer IDs**: Since many transactions lacked `CustomerID`, I decided to retain these rows but excluded them from any customer-specific segmentation analyses.
- **Skewed Distributions**: Addressed right-skewness in revenue by using log-transformations where appropriate for visualization and summary statistics.

## Conclusion
The focus of this deliverable was on **cleaning** and **exploratory data analysis (EDA)** of real-world retail transaction data. I handled missing and duplicate data, engineered new features, and extracted actionable insights such as top-selling products and seasonality effects. Future work will involve building forecasting models to predict sales volume and customer behavior.  


