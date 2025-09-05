# TechStream Solutions - Unit Economics Analysis

## Project Overview

**Company:** TechStream Solutions  
**Product:** Streamline Pro (SaaS Platform)  
**Analysis Period:** March 2023  
**Objective:** Calculate and analyze unit economics to assess business profitability and growth sustainability

### About Streamline Pro
Streamline Pro is a comprehensive project management and collaboration tool designed to help businesses manage projects, track progress, and collaborate efficiently across teams of all sizes.

## Business Context

TechStream Solutions hired a new Data Analyst to evaluate the financial health of their SaaS platform. The analysis focuses on key unit economics metrics to:

- Identify profitability of customer acquisition and retention
- Assess efficiency of marketing and sales strategies  
- Make informed decisions on scaling operations
- Optimize resource allocation for sustainable growth

## Data Sources

**Dataset Location:** [Google Drive Folder](https://drive.google.com/drive/folders/1qhOW9Y2orRXuzbX-kXEmuJ7TMQiRs2Uv?usp=drive_link)

The analysis used multiple data sources from Google Sheets:

### 1. Monthly Expenses Dataset
**Google Sheet ID:** `10OGbaywwMIqKgnPGy8VDvpBVtjyqln47iYa2lFhI9Mw`
- `month`: Date of expense record
- `item`: Expense item name (e.g., Salesforce, AWS Hosting)
- `category`: Expense category (Software Licenses, Server Costs, etc.)
- `amount`: Expense amount in USD

### 2. Payroll Dataset
**Google Sheet ID:** `1c_WihqTZCQvNgxzmd-OwhR9i5diwtfxXVLyMn8R-Lp4`
- `month`: Payroll month
- `department`: Employee department (Sales, Marketing, Engineering)
- `paid`: Amount paid to employees in USD

### 3. Marketing Spending Dataset
**Google Sheet ID:** `1AZOIThOV4P-0eYDge53ZwumVkfkHoYPWxst3k3Bv87c`
- `date`: Date of marketing spend
- `spending`: Daily marketing expenditure in USD

### 4. Customer Receipts Dataset
**Google Sheet ID:** `1qayqML1zCKdmtzutkcy9LWvE6xFRm6TGBEVkHHJKIuE`
- `date`: Transaction date
- `customer_id`: Unique customer identifier
- `receipt_amount`: Transaction amount in USD
- `new_customer`: Binary flag (1 = new customer, 0 = existing)

### 5. Customer Lifespan Dataset
**Google Sheet ID:** `1by8tPHwOnq3uKYK2E7sA9VBUYoPM4p1Rnrm_Ss9cyHI`
- `customer_id`: Unique customer identifier
- `start_date`: Customer acquisition date
- `churn_date`: Date when customer stopped using service
- `lifespan_days`: Calculated customer lifetime in days

## Analysis Methodology

### Data Processing with Python & Pandas

The analysis was conducted using Python with the following approach:

1. **Data Collection:** Connected to Google Sheets APIs to extract real-time data
2. **Data Cleaning:** Processed and filtered data for March 2023
3. **Metric Calculations:** Computed key unit economics metrics
4. **Insight Generation:** Analyzed results against industry benchmarks

### Key Metrics Calculated

**Customer Acquisition Cost (CAC)**
```python
# Components: CRM costs + Sales/Marketing payroll + Marketing spending
CAC = total_sales_mrkt_expenses / number_of_new_customers
```

**Average Revenue Per User (ARPU)**
```python
ARPU = total_revenue / num_users
```

**Cost of Goods Sold (COGS)**
```python
# Components: Server costs + Software licenses + Engineering salaries
COGS = production_salaries + server_n_software_expense
```

**Gross Margin**
```python
gross_margin = (total_revenue - COGS) / total_revenue * 100
```

**Customer Lifetime Value (LTV)**
```python
LTV = avg_lifespan_months * ARPU * (gross_margin / 100)
```

## Key Findings & Business Health Assessment

### LTV/CAC Ratio Analysis
The LTV/CAC ratio shows if your business makes money from customers:
- Below 1.0x → Losing money (bad)
- 1.0x to 3.0x → Making some money (needs work)
- 3.0x to 5.0x → Good profit (healthy business)
- Above 5.0x → Excellent profit (very successful)

### Gross Margin Check
How much profit you keep after basic costs:
- 70%+ → Excellent performance
- 60-70% → Good performance  
- 40-60% → Okay (can improve)
- Below 40% → Poor (fix costs)

### Customer Metrics
- **ARPU**: How much money each customer pays you
- **CAC**: How much you spend to get one new customer
- **Customer Lifespan**: How long customers stay with you

## 🚀 Strategic Recommendations

### Quick Wins (Next 3 Months)

**Fix Customer Acquisition**  
If getting customers costs too much, check which marketing works best. Focus your money on channels that bring the most customers.

*Action items:* Look at each marketing channel's results. Test different website pages. Make sure you're targeting the right customers.

**Increase Revenue**  
If customers don't pay enough, consider raising prices or selling them more services.

*Action items:* Check competitor prices. Create different price levels. Help existing customers buy more.

**Cut Costs**  
If your profit margins are low, reduce unnecessary expenses.

*Action items:* Reduce server costs. Cancel unused software. Use automation to save time and money.

### Medium-Term Goals (3-12 Months)

**Keep Customers Longer**  
If customers leave too quickly, improve your product and customer service.

*Focus areas:* Better customer onboarding. Track customer health. Create upselling opportunities.

**Improve Your Product**  
Build features that make customers stay longer and pay more.

*Development focus:* Analyze which features customers use most. Create integrations. Build premium features.

### Long-Term Strategy (1+ Years)

**Scale Smart**  
Grow your business while keeping costs under control.

*Key areas:* Automate more processes. Find partners to help you grow. Build a platform others can use.

## Performance Tracking Framework

### Monthly Metrics to Watch
- **LTV/CAC Ratio**: Keep above 3.0x
- **Gross Margin**: Aim for 70%+
- **Customer Churn**: How many customers you lose each month
- **Revenue per Customer**: Track if this grows over time
- **Payback Time**: How long to recover customer acquisition costs

### Success Goals
Your business is healthy when you have:
- LTV/CAC ratio above 3.0x
- Gross margins above 60%
- Growing customer revenue
- Decreasing customer churn

## Key Takeaways

**Bottom Line:** Focus on the metric that needs the most improvement first, then build systems to track and improve all metrics over time.

The analysis provides TechStream Solutions with actionable insights to:
- Optimize customer acquisition strategies
- Improve operational efficiency
- Make data-driven decisions for sustainable growth
- Maximize long-term profitability
