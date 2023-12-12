# Email-Marketing-analysis
# Shopee Financial Summary Report

## Background
The Shopee Financial Summary Report provides an analysis of Shopee's financial performance for the last two years (2018-2019). The report examines the total operating loss, revenue, and cost and expenses incurred by the company during this period. Additionally, the effectiveness of Shopee's email marketing campaign is evaluated based on the provided data. The aim is to identify the best strategy for the email marketing campaign that maximizes revenue while minimizing expenses.

## Problem Identification

### Problem Definition
Shopee has been experiencing continuous operational losses over the past two years. The total cost and expenses consistently exceed the revenue generated, indicating a need for analysis and improvement.

### Business Objectives
The main objectives of this report are:
1. Analyze Shopee's financial performance in terms of operating loss, revenue, and cost and expenses.
2. Evaluate the effectiveness of the email marketing campaign.
3. Identify the best strategy for the email marketing campaign to maximize revenue and minimize expenses.

### Data Requirements
The data for analysis is sourced from the following dataset: Shopee Code League - Marketing Analytics.
https://www.kaggle.com/competitions/open-shopee-code-league-marketing-analytics

### Analytic Approach
The analysis will involve the following steps:
1. Assess Shopee's financial performance by comparing operating loss, revenue, and cost and expenses.
2. Evaluate the email marketing campaign by analyzing the provided data on email sending, opening, and open rates.
3. Identify the top 6 features that correlate with user engagement in the email campaign.
4. Develop a strategy for the email marketing campaign based on the identified features and their correlation scores.
5. Analyze the impact of the proposed strategy on the email marketing budget, expenses, open rate, and potential revenue.

### Action and Value
The insights gained from this analysis will help Shopee's management make informed decisions regarding the email marketing campaign. By implementing the recommended strategy, Shopee can improve user engagement, increase open rates, and optimize the use of resources, leading to potential revenue growth and cost savings.

## Results and Evaluation

### Financial Performance Analysis
- Total Operating Loss: $2,025,260,000
- Total Revenue: $1,232,828,000
- Total Cost and Expenses: $3,258,088,000
- Total Sales and Marketing Expenses: $1,368,132,000

### Email Marketing Campaign Evaluation
- Date Range: 15 July 2019 - 1 September 2019
- Total Emails Sent: 50,285
- Total Emails Opened: 8,398
- Open Rate: 16.7%

### Top 6 Features
1. Open_count_last_10_days: The total number of emails opened in the last 10 days (correlation: 0.53).
2. country_code: An integer code for the user's country (correlation: 0.17).
3. isLast_open_more_360: Was the last time the user opened an email more than 12 months ago? (correlation: 0.12).
4. isLast_open_31_to_60: Was the last time the user opened an email more than 1-2 months ago? (correlation: 0.12).
5. isLast_open_61_to_90: Was the last time the user opened an email more than 2-3 months ago? (correlation: 0.11).
6. domain_gmail: Is the user's email domain Gmail? (correlation: 0.10).

### Strategy for Email Marketing Campaign
The best strategy for the email marketing campaign involves classifying users into two categories based on a threshold value (0.28). The strategy aims to maximize revenue and minimize expenses. The following assumptions and calculations are made:
- Ratio of income to expense: 1
- Email marketing expense: $1,000,000

### Analysis Results
#### BEFORE:
- Number of Emails Sent: 50,285
- Number of Emails Not Sent: 0
- Open Emails from Sent Group: 8,398
- Open Emails from Not-Sent Group: 0
- Expense Reduction: 0.0%
- Lost Customers: 0.0%
- Open Rate: 16.7%
- Email Marketing Budget: $1,000,000
- Expense: $1,000,000
- Saving: $0
- Income: $1,000,000
- Profit: $0
- Money in Hand (Profit + Saving): $0

#### AFTER:
- Number of Emails Sent: 8,784
- Number of Emails Not Sent: 41,501
- Open Emails from Sent Group: 5,075
- Open Emails from Not-Sent Group: 3,323
- Expense Reduction: 82.5%
- Lost Customers: 39.6%
- Open Rate: 57.8%
- Email Marketing Budget: $1,000,000
- Expense: $174,684
- Saving: $825,316
- Income: $604,311
- Profit: $429,626
- Money in Hand (Profit + Saving): $1,254,942

## Conclusion
Based on the analysis, Shopee's financial performance indicates operational losses. The email marketing campaign evaluation highlights a declining open rate. By implementing the recommended email marketing strategy, Shopee can significantly reduce expenses, improve the open rate, and potentially increase revenue. The following positive changes have been observed:

- Expense Reduction: The new email marketing strategy has led to a reduction in expenses. The expense reduction is approximately $825,316, representing a substantial decrease of 82.5% compared to the previous budget.

- Open Rate Improvement: The open rate of the email marketing campaign has shown a remarkable improvement. The open rate has increased to 57.8%, indicating a significant boost compared to the previous open rate of 16.7%.

- Profit and Savings: As a result of the expense reduction and improved open rate, Shopee has achieved a profit of $429,626. Additionally, the company has managed to save $825,316, leading to a combined total of $1,254,942 in money in hand.

These improvements demonstrate the effectiveness of the recommended email marketing strategy in enhancing Shopee's financial performance. By reducing expenses, improving the open rate, and increasing profits, Shopee is on track to achieve better financial outcomes and move closer to profitability. The significant percentage increases in expense reduction (82.5%) and open rate (246.7%) highlight the success of the implemented strategy.
