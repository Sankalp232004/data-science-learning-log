Retail Store Sales: Data Cleaning & Customer Segmentation
📜 Project Overview
This project demonstrates a complete data science workflow, starting with a messy, real-world retail sales dataset and ending with actionable customer insights. The primary goals were to perform a thorough data cleaning process, conduct an exploratory data analysis (EDA) to uncover sales trends, and apply a K-Means clustering model to segment customers based on their purchasing behavior.

📊 Dataset
The project uses the "Dirty Retail Store Sales Dataset" from Kaggle. This dataset is designed to contain common issues found in real-world data, such as inconsistent column names, incorrect data types, missing values, and invalid entries.

📋 Data Cleaning Process
The raw dataset required several cleaning steps to prepare it for analysis. The final, clean dataset consists of 11,362 valid transactions.

Standardized Column Names: All column headers were stripped of leading/trailing whitespace, converted to lowercase, and spaces were replaced with underscores (e.g., transaction date became transaction_date).

Corrected Data Types: The transaction_date column was converted from object to a proper datetime64 format. The customer_id was converted to a string type to handle alphanumeric IDs.

Handled Missing Values: Rows with missing customer_id or transaction_date were dropped.

Removed Invalid Data: Transactions with a negative or zero quantity (likely returns) or a unit_price of zero were removed.

Dropped Duplicates: All duplicate rows were removed to ensure each transaction is unique.

💡 Exploratory Data Analysis (EDA) & Key Insights
After cleaning the data, several key business insights were uncovered through visualization:

Sales Distribution: The vast majority of transactions are of lower value, with a long tail of higher-value purchases.

Top Categories: Electronics and clothing are consistently the highest-selling product categories.

Sales Trends: A clear seasonal trend was observed, with sales peaking significantly in the end-of-year holiday months.

🤖 Customer Segmentation Model
A K-Means clustering algorithm was used to segment customers into three distinct groups based on their purchasing habits.

Features Used: The model was trained on two key metrics for each customer:

Monetary Value: The total amount of money spent by the customer.

Frequency: The total number of transactions made by the customer.

Segments Identified: The analysis revealed three customer clusters with the following average characteristics:

Cluster	Avg. Total Spent (Monetary)	Avg. # of Transactions (Frequency)	Customer Segment
2	~63,044	~484	High-Value, Frequent Customers
0	~58,544	~454	Mid-Value, Regular Customers
1	~56,343	~433	Low-Value, Occasional Customers

Export to Sheets
These segments can be used for targeted marketing campaigns, loyalty programs, and personalized customer service strategies.

🛠️ Tools & Libraries
Language: Python

Libraries:

Pandas & NumPy (Data Cleaning and Manipulation)

Seaborn & Matplotlib (Data Visualization)

Scikit-learn (K-Means Clustering Model)

Environment: Jupyter Notebook
