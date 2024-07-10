## download the pbip file along with Report and semantic_model otherwise an error will occur





CRM Data Analysis Project
Introduction
Customer Relationship Management (CRM) data is critical for effective sales and marketing strategies. By capturing and organizing detailed information about customers, prospects, and sales interactions, CRM systems provide invaluable insights into consumer behavior, preferences, and purchasing patterns.

Effective utilization of CRM data allows companies to enhance customer engagement through personalized marketing campaigns and optimize sales strategies by identifying high-value prospects, tracking ongoing deals, and refining sales tactics. This strategic advantage is essential for sustaining growth and maintaining competitiveness in any industry.

Project Scenario
A B2B company selling computer hardware has collected sales pipeline data for a year but lacks the expertise to extract valuable insights. As data consultants, we are tasked with analyzing the CRM data, highlighting sales process trends, establishing metrics and benchmarks, and collaborating with sales and marketing leaders to optimize their strategies.

Data Overview
The CRM database includes the following tables:

Accounts: Information about the companies that have purchased products.
Products: Details about the products sold.
Sales Team: Information about the sales team members.
Sales Pipeline: Information about sales opportunities and deals.
Focus is on the United States, as other countries in the dataset have only one account each. The merged dataset includes additional columns:

Engage Month: Month of last account engagement.
Close Month: Month the deal was closed.
Employee Size: Size of the company.
Time to Close: Days from engage_date to close_date.
Time to Close Bin: Categorical variable for time to close (0–30 days, 31–60 days, 61–90 days, >90 days).
Analysis Limitations
Several limitations may influence the accuracy of our findings:

Lack of supplementary data fields such as customer interactions and touchpoints, limiting nuanced analysis.
Limited contextual information on external market conditions, competitor actions, or macroeconomic factors.
Customer Segmentation
Segmentation Features
For this dataset, Sector, Regional Office, and Employee Size are selected as segmentation features:

Sector: Understand industry-specific needs and tailor products accordingly.
Regional Office: Recognize geographical trends and local market dynamics.
Employee Size: Customize approach based on the organizational scale of potential clients.
Segmentation Analysis
By Sector
Retail: Largest share of accounts and deals, average annual revenue of $1.5 billion.
Software: 10% of accounts, 12% of deals, average annual revenue of $4.4 billion.
Retail, Medical, and Software: Constitute 44% of all deals, significant for prioritizing sales and marketing strategies.
By Employee Size
0–1000 and 2051–5000 employees: Represent 50% of total accounts and deals.
10000+ employees: Likely software companies, contributing high revenue.
By Regional Office
East Office: Lower percentage of deals (28.20%).
Central and West Offices: Generate 36.11% and 35.69% of deals, respectively.
Key Metrics
Relevant metrics to track and analyze for measuring and improving sales performance:

Deal Close Rate: Percentage of successfully closed deals.
Average Deal Value (ASP): Average revenue from each closed deal.
Average Deal Event Value: Expected value of a deal before closure.
Average Time to Close: Average days to close a deal from initiation.
Metrics Analysis
Average Time to Close
Overall: 48 days, median of 45 days.
By Regional Office: East - 47 days, Central and West - 48 days.
By Employee Size: Larger companies (10000+ employees) - 46 days, smaller companies (7501-10000 employees) - 49 days.
By Sector: Technology - 45 days, Software - 49 days.
Deal Close Rate, Average Deal Value & Deal Event Value
By Sector:

Marketing: Highest close rate (60%), lowest Average Deal Value ($2,123) and Deal Event Value ($1,266).
Entertainment: Highest Average Deal Value ($2,650) and Deal Event Value ($1,528).
By Employee Size:

10000+ and 5001-7500 employees: Highest close rates (58.6% and 59.7%) and Average Deal Values ($2,640 and $2,492).
By Regional Office:

Central Office: Lowest close rates, Average Deal Values, and Deal Event Values.
Trend Analysis of Key Metrics
Deal Close Rates Trend (Overall Company)
Seasonal/Cyclical Trends: Peak deal activity in July, decline in November and December.
Efficiency Increase: Sharp increase in close rate from August to October.
Strategy Adjustments: Review sales strategies during lower efficiency periods.
Deal Close Rates (By Sector & Employee Size)
By Sector: Retail and Medical generate the highest number of deals.
By Employee Size: Similar trend across all sizes, with 5001-7500 employee size showing a slight dip in close rate in the last month.
Average Deal Value (By Sector, Employee Size & Regional Office)
By Sector:

Upward Trend: Finance, Telecommunications, and Entertainment.
Downward Trend: Medical, Services, and Employment.
By Employee Size:

10000+ employees: Breaking $2,000 mark from September.
By Regional Office:

East Office: Consistent upward trend, 200% increase from January to December.
Deal Event Value (By Sector, Employee Size & Regional Office)
By Sector: Volatility in Average Deal Value.
By Employee Size: 10000+ employee size shows upward trend.
By Regional Office: East Office shows the most pronounced upward trend
