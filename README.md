# Introduction
In this project I have decided to conduct an analysis on the behavioral change of customer carts and purchases before and during a major global event. The major event that takes place during this data's time frame is the Covid-19 Pandemic alongside it's lockdowns and regulations. I have taken two different sets of data one from October 2019, which is the Pre-Pandemic and then another from April 2020 which is During the Time period that the Covid-19 regulations (lockdowns/SOPs/social distancing) were in full effect at a global scale. 

To summarize the overall goal of this analysis is to look beyond just the raw numbers and uncover the intent behind user actions—specifically. The focus is on Cart Abandonment, Average Order Value (AOV), and Most Purchased Products at the time, in order to understand pandemic-induced panic buying and economic hesitation.

When it comes to the original RAW dataset I am using for this project it can be viewed & downloaded from this link: https://www.kaggle.com/datasets/mkechinov/ecommerce-behavior-data-from-multi-category-store. Regarding the particular source dataset, it is a large quantity of data that is openly shared but still details about the store itself are protected by NDAs. 


# 🎯 Method to Conduct the Analysis:
Initially I had planned to use MySQL Workbench, a software I am familiar with, to do data cleaning but turns out that utilizing Kaggle's own Python (pandas) and SQL (duckdb) made the cleaning process a lot smoother. The source datasets had over 70 million rows of data that had large amounts of *NULL* values, potential *duplicate data*, *negative prices* and *jumbled category_codes & brands*, this meant the data had to be properly cleaned before use. Views, an extremely common *event_type* in the data set, had to also be removed, as it would've caused it to lag or overload Power BI and would make the data set have too much useless data. After cleaning in order to visualize the data, I chose Power BI Desktop, a tool that can provide clean visuals and filters for the different parts of the data that needed to be analyzed. 

- **Data Cleaning and Sampling**: Python (pandas) using Kaggle Notebook platform
- **Data Querying**: SQL (DuckDB) for efficient extraction of data.
- **Visualization & Interactivity** is created using Microsoft Power BI Desktop.

## 🧹 Data Cleaning Process:
- The 2 raw data sets combined contain over 70 million rows total.
- Filtered out the "View" events completely to focus predominantly on the bottom-of-funnel behavior ("carts" and "purchases")
- Handled missing data: Filled any missing *brand* and *category_code* with "Unknown" to preserve revenue rows, but dropped any rows with missing *user_session* IDs.
- Removed any negative prices and exact duplicate event logs.
- Individually clean each different dataset first, then combine both of the cleaned data sets in order to have a smooth, lag-free performance when ported to Power BI Desktop.

# 💡 Key Business Insights:
- **Surge in Cart Abandonment**: Cart abandonment rates jumped significantly from 54.74% in Oct '19 to 76.53% in Apr '20. While users were browsing and adding items to their carts at high rates, hesitation or supply chain issues prevented them from checking out.
  
- **Proof of Panic Buying**: Despite the higher Cart abandonment in April 2020, purchases managed to reach $244 million, with the average order value being at least $50 less than October's. Average Order Value (AOV) decreased from $309.56 in October 2019 to a $252.93, proving that customers were bulk-buying essential items and home improvement tools rather than highly expensive products.
  
- **Shift in Product Demand**: In October 2019 the product demand was more towards new smartphones and other high end electronic devices. When the pandemic hit and lockdowns were brought into effect, the demand for electronic items dropped in priority and was instead replaced with home improvement tools and leisure.

To fully interact with this Power BI dashboard and use the slicers please download the *eCommerce Online Store Project.pbix* file in this repository.

Main Dashboard Layout:

Unfiltered data visuals (not using Slicers):

<img width="1671" height="1111" alt="Screenshot (2623)" src="https://github.com/user-attachments/assets/479ba0e3-ee99-467b-accd-9f62de2f1703" />


Total Purchases, AOV & Cart Abandonment KPIs per month:

October 2019:

<img width="213" height="470" alt="Oct 2019" src="https://github.com/user-attachments/assets/3491f367-5c03-49b9-b3f3-0f06390bc75f" />

<img width="280" height="245" alt="OctAR2019" src="https://github.com/user-attachments/assets/48e5225e-1359-4f74-8a81-780f3fd13382" />



April 2020:

<img width="210" height="477" alt="Apr 2020" src="https://github.com/user-attachments/assets/98520211-0ff2-4795-9e02-1aa233a6eccd" />

<img width="284" height="250" alt="AprAR2020" src="https://github.com/user-attachments/assets/1f339b24-92a5-40a7-a38b-73dfeeed448c" />



# Repository Files:
- eCommerce Online Store Project.pbix - the Interactive Power BI dashboard file.
- Cleaning process notebook on Kaggle - https://www.kaggle.com/code/mgregj/data-cleaning-process-for-ecommerce-behavior-data. The Python/Pandas & SQL (DuckDB) Notebook with its code that is used to clean, sample, and merge the raw datasets can be accessed here. 
