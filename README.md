# Market-Analysis-Report-for-a-National-Clothing-Chain
# Project Description
An online national clothing chain needs your help creating a targeted marketing campaign. Sales have been flat and they want to lure lost customers back. They want to advertise specific products to specific customers in specific locations, but they don’t know who to target. They need you to conduct an analysis to determine the best product to advertise to each customer. They have identified three key products for this campaign. The products are:
- Shirt: $25
- Sweater: $100
- Leather Bag: $1,000
# Project Analysis Questions:
- Which customer do you predict has the highest income?
- Which product will be advertised the most?
- What is the correlation (R2 value) between sales and income?
- What is the correlation (R2 value) between customer ratings and product return rate?
- What are the linear regression formulas to predict customer income from customer sales?
# Data Sources:
The data sources used for this market analysis are:
### Business Dataset
- Product Inventory
- Product Prices
- Customer Rating
### US Census Bureau Dataset
- Average Income
- Location
- Population
- Industry
### Customer Dataset
- Customer ID
- Names
- Location
- Date of Birth
- Purchase History
### Additional Dataset
- Weather
- Demographics (Industry Salary Data)
# Tools used
- Power BI
- Power Query
- DAX (Data Analysis Expression)
# Data Cleaning and Transformation
- Data loading and inspection
- Data cleaning and formatting
- Data transformation process such as splitting and unpivoting columns
- Handling missing, null and misspelt values
- Eliminate redundant rows
# Data Analysis and Visualizations
The seven tables were imported into power BI and connected into a table relationship. The data model is shown below:

![Model diagram](https://github.com/DannyRukks/Market-Analysis-Report-for-a-National-Clothing-Chain/assets/97890440/817f5d54-0e0e-4c1a-8359-d82c7f42a974)

Measures were created using DAX expressions to gain better understanding of the dataset. Some of the key measures are:
```
Customer with Max Income = 
LOOKUPVALUE('Customer List'[Customer ID],
'Customer List'[Predicted Income],
MAX('Customer List'[Predicted Income]))
```
```
Lowest Predicted Income = MIN('Customer List'[Predicted Income])
```
```
Max Predicted Income = MAX('Customer List'[Predicted Income])
```
```
Regression Formula = "AVG Sales = " & ROUND('Income Sales Measures'[m], 2) & "*AVG Income " & ROUND('Income Sales Measures'[b], 2)
```
Several visualizations were created for the market analysis.
- **Linear regression plot** was created to establish the relationship between sales and income and also to establish the relationship between customer ratings and product return rate.
- **Linear regression formula** was generated and used to predict customer income from customer sales.
- **Histogram plot** was created to show the predicted income distribution.
- **Heat map** was created to show household Income by location.
- **Other visuals** created for the market analysis were **line chart** to show the trend of customer’s sales with time, **tree map** to show top ten states by population, **clustered column** and **bar charts** to show top customers with high predicted income, **matrix** and **tables** to show customers based on their income and their location and **donut chart** to show the percentage of the categories of customer’s income and product recommendation.

The dashoard showing detailed analysis of the products is shown below:

![Product Insights](https://github.com/DannyRukks/Market-Analysis-Report-for-a-National-Clothing-Chain/assets/97890440/681d4a32-6f18-4edb-a0db-ef03fdb6dbfa)

The dashoard showing detailed analysis of the customers is shown below:

![customer insights](https://github.com/DannyRukks/Market-Analysis-Report-for-a-National-Clothing-Chain/assets/97890440/68fa5781-5117-40d7-9a5b-39d5b3ed3d35)

The dashoard showing detailed analysis of the customer's income is shown below:

![new income insight](https://github.com/DannyRukks/Market-Analysis-Report-for-a-National-Clothing-Chain/assets/97890440/34051994-bf0e-48ea-b47d-8d971cd2a1b6)

# Insights
- The linear regression formula between sales and income was given as:
```
AVG Sales = 0.01 × AVG Income - 722.14
```
- The correlation (R2 value) between sales and income was 0.78. This shows that there is a strong positive correlation between sales and income. 
- The correlation (R2 value) between customer rating and product return rate was 0.69. This shows a strong negative relationship between product return rate and customer ratings. The customer with the highest predicted income has a customer id of JLit30836 with an income of $597,214. 
- There are 1000 customers. 45.3% of these customers are located in California, Florida, Texas, New York and Illinois. 
- High income customers are located in Illinois, New Jersey, District of Columbia, Hawaii, California, Texas and Nevada. 81.9% are low-income customers, 15% are medium income customers and 3.1% are high income customers. 
# Recommendations
There are 1000 customers of which 81.9% are low-income customers. Therefore, the low price products should be advertised the most. However, the medium price products should
also be advertised in areas where the medium income customers are situated while the high price product can also be advertised in areas where the high income customers are located
as shown in the power BI reports.

On a final note, click [here](https://app.powerbi.com/links/2oS20Stt9G?ctid=96c3451c-0db8-4f19-88af-5cb06c0a43fe&pbi_source=linkShare) to access the dashboards for interactivity.

### Thank you 🤝



