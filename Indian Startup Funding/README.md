Indian Startup Funding Analysis 💰
This project analyzes funding details of Indian startups from a downloaded CSV file. It uses Pandas for data manipulation and Matplotlib for visualization. The analysis focuses on understanding funding trends, key investment types, and geographical distribution of startups.

Dataset Overview 📋
The dataset contains 3044 entries with details on Indian startups. The initial data exploration revealed the following:

Key Columns & Data Types
Amount in USD: The funding amount is stored as an object (string) and has 960 missing values. This column requires significant cleaning to be converted to a numeric type for calculations.

City Location: The city where the startup is located, with 180 missing values. The column name initially contained extra spaces, which were cleaned for consistency.

Date dd/mm/yyyy: The date of funding is an object and will need to be converted to a proper datetime format for time-series analysis.

Industry Vertical & SubVertical: These columns, describing the startup's sector, have 171 and 936 missing values respectively.

InvestmentnType: The type of funding round (e.g., Seed, Angel) has 4 missing values.

Data Cleaning Performed
Column Names: All column names were cleaned to remove leading/trailing whitespace and standardize spacing (e.g., 'City  Location' became 'City Location').

Categorical Data: Values in the City Location and InvestmentnType columns were standardized to fix inconsistencies and typos (e.g., 'Bangalore' to 'Bengaluru').

Missing Values: The number of missing values for each column was identified. These will be handled with appropriate methods in future analysis steps.

Initial Findings and Visualizations 📊
The initial analysis focused on the geographical distribution of startups. A bar chart was created to visualize the top 10 cities with the most funded startups, which is a great starting point for understanding where India's startup ecosystem is most concentrated.

Have Gemini write a document or code that you can edit
