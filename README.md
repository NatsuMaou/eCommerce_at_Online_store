# 📌 eCommerce_at_Online_store
Data Analytics file created using Power BI tools and Kaggle SQL, will have the .pbix version provided for this repository.

This project analyzes a massive multi-category e-commerce dataset to understand drastic shifts in consumer behavior between a "normal" period (October 2019) and the first month of the COVID-19 lockdowns (April 2020).
The goal of this analysis is to look beyond raw numbers and uncover the intent behind user actions—specifically focusing on Cart Abandonment, Average Order Value (AOV), and Most Purchased Products at the time, in order to understand pandemic-induced panic buying vs. economic hesitation.

Tools used:
- **Data Cleaning and Sampling**: Python (pandas) using Kaggle Notebook platform
- **Data Querying**: SQL (DuckDB) for efficient extraction of data.
- Visualization & Interactivity is created using Microsoft Power BI Desktop.

# 💡 Key Business Insights:
- **Surge in Cart Abandonment**: Cart abandonment rates jumped significantly from 54.74% in Oct '19 to 76.53% in Apr '20. While users were browsing and adding items to their carts at high rates, hesitation or supply chain issues prevented them from checking out.
  
- **Proof of Panic Buying**: Despite the higher Cart abandonment in April 2020, purchases managed to reach $244 million, with the average order value being at least $50 less than October's. Average Order Value (AOV) decreased from $309.56 in October 2019 to a $252.93, proving that customers were bulk-buying essential items and home improvement tools rather than highly expensive products.
  
- **Shift in Product Demand**: In October 2019 the product demand was more towards new smartphones and other high end electronic devices. When the pandemic hit and lockdowns were brought into effect, the demand for electronic items dropped in priority and was instead replaced with home improvement tools and leisure.

To fully interact with this dashboard please download the *eCommerce Online Store Project.pbix* file.

Main Dashboard Layout:
<img width="1926" height="1103" alt="Screenshot (2610)" src="https://github.com/user-attachments/assets/c45ba773-d0f9-405b-a072-ac2d7f829fca" />


AOV & Cart Abandonment KPIs:
October 2019:
<img width="502" height="474" alt="Oct 2019" src="https://github.com/user-attachments/assets/56247fde-150b-4c2f-a564-3945794d9f67" />

April 2020:
<img width="500" height="465" alt="April 2020" src="https://github.com/user-attachments/assets/a279d815-8fa8-437c-a743-c744224ca4a0" />


# Data Cleaning Process:
- The raw data sets combined contain over 80 million rows total.
- Filtered out the "View" events completely to focus predominantly on the bottom-of-funnel behavior ("carts" and "purchases")
- Handled missing data: Filled any missing *brand* and *category_code* with "Unknown" to preserve revenue rows, but dropped any rows with missing *user_session* IDs.
- Removed any negative prices and exact duplicate event logs.
- Individually cleaned each different dataset first, then combined both of the cleaned data sets to have a smooth, lag-free performance on Power BI Desktop.

# Repository Files:
- eCommerce Online Store Project.pbix - the Interactive Power BI dashboard file.
- Cleaning process notebook on Kaggle - The Python/Pandas & SQL (DuckDB) code used to clean, sample, and merge the raw datasets.
