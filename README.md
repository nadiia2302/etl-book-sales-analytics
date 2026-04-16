# Book Sales Analytics Project
This project focuses on building a robust data pipeline and a professional BI dashboard to analyze book sales from multiple sources. The core challenge involved data reconciliation, entity resolution (handling aliases), and delivering actionable business insights.
## 🔗 Project Links
Live Dashboard: https://app.powerbi.com/view?r=eyJrIjoiNmNiZGZkNWMtMDQxOS00MmVjLTlhYzQtNDNkYzcwMDNhMWQ3IiwidCI6ImRmODY3OWNkLWE4MGUtNDVkOC05OWFjLWM4M2VkN2ZmOTVhMCJ9 

Source Code: All_datas.ipynb, data1_in_details.ipynb
## 🛠️ Engineering Process (ETL)
The input data was provided in three separate datasets (DATA1, DATA2, DATA3), each containing "noisy" records. My engineering workflow included:

- Data Reconciliation: Implementing a matching algorithm to identify unique users across different IDs using email and phone normalization.

- Deduplication: Removing redundant records while preserving transaction integrity.

- Entity Resolution (Aliases): Identifying that a single customer could have multiple system IDs. These are grouped and reported as an array of IDs.

Relational Modeling: Creating a Star Schema in Power BI, connecting Users, Books, and Orders for efficient querying.
## 📊 Business Insights (Dashboard)
The final BI Dashboard consists of three independent views (one for each dataset) and tracks the following key performance indicators:

- Financials: Daily revenue trends and Top 5 high-income days (Format: YYYY-MM-dd).

- Audience: Total count of unique users after deduplication.

- Inventory: Identification of unique author sets and the most popular authors based on sales volume.

- VIP Customers: Identification of the "Best Buyer" including all their known aliases (array of IDs).
## Dashboard Preview
<img width="962" height="539" alt="image" src="https://github.com/user-attachments/assets/6b122ed1-8b41-492d-8dd8-472b535ab7cc"/>

## 🚀 Technologies Used
Python (Pandas): For heavy data lifting and cleaning, preprocessing.

Power BI: For professional data modeling and visualization.

