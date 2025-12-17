# Retail Product Performance Analysis by Category & Color (Power-BI)
***Download Power BI File***

You can download the full Power BI dashboard (.pbix) here: 
[![Download PBIX File](https://img.shields.io/badge/Download-.PBIX-orange?style=for-the-badge&logo=power-bi)]()

# I. Introduction
### 1. Project Overview
This Power BI project focuses on analyzing the sales performance and cost structure of products based on two key dimensions: Color and Category. Using the Adventure Works dataset, the report provides an in-depth overview of how different product categories contribute to total revenue and how product colors influence customer purchasing behavior.
### 2. Dataset Information
 - The ***Adventure Works dataset*** is a sample business dataset provided by Microsoft, representing the operations of Adventure Works Cycles, a global bicycle manufacturing and sales company. The dataset includes detailed information on products, customers, sales transactions, territories, and calendar, organized for the years 2016 and 2019.
 - Data resource: [*AdventureWorks*](https://docs.google.com/spreadsheets/d/1ugbRwkuouG5fW0Av-C4VkvOqncEjeoBY/edit?gid=494881559#gid=494881559)
 - Data dictionary:
   
   | Field | Data type | Type of column |
   | ----- | :---------: | :-----------: |
   | OrderDate | Date | `Dimension` |
   | OrderDate Key | Whole number | `Dimension` |
   | ProductKey | Whole number | `Dimension` |
   | CustomerKey | Whole number | `Dimension` |
   | SalesTerritoryKey | Whole number | `Dimension` |
   | SaleOrderNumber | Text | `Dimension` |
   | SalesOrderLineNumber | Whole number | `Dimension` |
   | OrderQuantity | Whole number | `Dimension` |
   | UnitPrice | Decimal number | `Dimension` |
   | ExtendedAmount | Decimal number | `Dimension` |
   | UnitPriceDiscountPct | Whole number | `Dimension` |
   | DiscountAmount | Whole number | `Dimension` |
   | ProductStandardCost | Decimal number | `Dimension` |
   | TotalProductCost | Decimal number | `Dimension` |
   | SalesAmount | Decimal number | `Dimension` |
   | TaxAmt | Decimal number | `Dimension` |
   | Freight | Decimal number | `Dimension` |
   | RegionMonthID | Text | `Dimension` |
   | Total_Sales | Decimal number | `Measure` |
   | Total_Cost | Decimal number | `Measure` |
   | Total_Profit | Decimal number | `Measure` |
   | Profit_Rank | Whole number | `Measure` |
   | PreviousYearSales | Decimal number | `Measure` |
   | Cost to Sales Ratio | Decimal number | `Measure` |
   | % Growth_Sales | Decimal number | `Measure` |
   | Territory Key | Whole number | `Dimension` |
### 3. Data Model
The data model for this project is built using the Adventure Works dataset, a well-structured sample database that simulates the operations of a global bicycle manufacturing company. The model follows a ***star-schema design***, separating transaction data into fact tables and descriptive attributes into dimension tables. This structure supports efficient querying, enables scalable analytics, and ensures clear relationships between sales, products, customers, calendar, and territory data. The goal of the data model is to provide a clean analytical foundation that supports ***accurate reporting***, ***DAX calculations***, and ***meaningful business insights***.

<img width="817" height="511" alt="Image" src="https://github.com/user-attachments/assets/fc775c9b-7495-45a1-8674-334b34734278" />

As you can see, there is one types of relationship in this Data Model: ***one-to-many***.

### 4. Business Questions
- Which product categories and colors drive the highest revenue?
-  How does sales performance evolve over time?
-  Which product categories are the most profitable?
- Are certain product colors or subcategories underperforming?
- How efficiently are we converting sales relative to cost?

## II. Data Analysis and Visualization
### 1. Overview of Financial Indicators

<img width="271" height="33" alt="Image" src="https://github.com/user-attachments/assets/6114a30f-c943-43c4-b04b-5bb8efa6feda" />
<img width="300" height="33" alt="Image" src="https://github.com/user-attachments/assets/1678b85b-9abe-43ef-aef2-47cf29774d95" />

**<img width="387" height="106" alt="Image" src="https://github.com/user-attachments/assets/d636e4bf-f54b-49aa-bb51-e6c3b7c56890" />**

- The total sales during the analysis period (July 2016 – June 2019) reached more than $29 million, with total costs exceeding $17 million.
- The cost ratio is approximately 58.6%, indicating a healthy profit margin and an overall positive business performance.

### 2. Sales by Color

<img width="239" height="250" alt="Image" src="https://github.com/user-attachments/assets/40964c4e-cb30-44d5-92b4-df0d24566606" />

- Black and Red are the top-performing colors, generating $8.8M and $7.7M respectively.
- Colors such as White, Multi, and several others contribute insignificantly to total revenue.

### 3. Sales by Category

<img width="347" height="253" alt="Image" src="https://github.com/user-attachments/assets/f9f4e2c4-cd72-4c2b-a8de-368a47cd181c" />

- Bikes dominate the business, contributing 96.46% of total revenue.
- Accessories and Clothing together account for less than 4%.

### 4. Sales, Costs, and Cost-to-Sales Ratio by Category

<img width="411" height="34" alt="Image" src="https://github.com/user-attachments/assets/5f0811de-8b5d-4f35-86ef-a984ef3e8a8a" />

**<img width="358" height="251" alt="Image" src="https://github.com/user-attachments/assets/47eb3d49-9944-4f82-9016-f5f6309d39f5" />**

- Bikes have high sales with moderate costs → Good cost ratio (0.59).
- Accessories and Clothing have low sales overall, but the cost-to-sales ratio differs significantly:
  - Accessories: 0.37 (good efficiency)
  - Clothing: 0.6 (high cost relative to sales)

### 5. Growth of Sales and Showing Total Categories and Colors by Year

<img width="469" height="67" alt="Image" src="https://github.com/user-attachments/assets/971e6af2-e9d2-42ff-988b-9051e6774e9c" />
<img width="556" height="34" alt="Image" src="https://github.com/user-attachments/assets/7122043e-3a8d-46d3-a3fb-a226efcd5c19" />

**<img width="603" height="210" alt="Image" src="https://github.com/user-attachments/assets/958837b2-96c2-4531-a47c-5cee2b183ce5" />**

***Sales and Growth % by Year and Month***
- Mid-2016 to Early 2018:
  - Sales remained stable between $300K–$600K per month.
  - Growth % showed no significant spikes → business operations were steady but not accelerating.
- Mid-2018 to Mid-2019:
  - Strong and clear upward trend, especially from late 2018 to mid-2019, peaked at nearly $2 million in June 2019.
  - % Growth_Sales exceeded 2.5%, indicating both absolute and relative growth.

  ➡️ Possible reason: The combined chart suggests that product color diversification may have contributed to this revenue increase.
- After June 2019:
  - Sales dropped sharply.
  - The dataset shows no updated data beyond this point.

***The Line Chart Showing Total Categories and Colors by Year***
- The dark blue dotted line shows product categories staying constant at 4 across all years → no expansion of product lines.
- The orange dotted line shows product colors increasing steadily → the company appears to adopt a strategy of expanding existing product lines (more colors) rather than creating new categories.

### 6. The Profit_Rank Table by Category and Top 3 Highest-Revenue Subcategories

<img width="324" height="33" alt="Image" src="https://github.com/user-attachments/assets/0b264497-9186-4dd4-8968-ed407c6345d2" />
<img width="457" height="33" alt="Image" src="https://github.com/user-attachments/assets/a3e95633-22de-4446-9ba7-8b61a83c6af4" />

**<img width="206" height="211" alt="Image" src="https://github.com/user-attachments/assets/f0bc4d52-a8e1-443f-b407-91679eb7153a" />**

- Bikes are clearly ranked first in profit contribution, other categories generate substantially lower sales: Accessories: ~40× lower than Bikes; Clothing: ~83× lower; Components: almost no sales at all.
- In the Bikes category, subcategories such as: Road Bikes, Mountain Bikes, Touring Bikes all exceed the one-million-dollar mark, other subcategories produce very low sales.

### *Business Performance Dashboard*

<img width="810" height="457" alt="Image" src="https://github.com/user-attachments/assets/217841ea-588d-4b3b-a39b-276dad861ab2" />

## III. Conclusion and Recommedations
- Bikes are the core product line that contribute over 96% of total revenue. Therefore, the company may consider further expanding this category. Accessories and Clothing require product improvement, repositioning, or strategic reconsideration.
- Black and Red are the best-selling product colors.
- Clothing has a high cost-to-sales ratio while generating limited revenue → reconsider pricing, design, or cost structure.
- The increasing variety of product colors through the years correlates with sales growth.
- Consider expanding high-performing colors and optimizing inventory for low-performing ones.
