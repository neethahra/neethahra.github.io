## E-Commerce Business Analytics

**Project description:** Analyze raw transaction logs of an e-commerce company to understand how website is converting product page views into purchases by building a conversion funnel, perform cohort analysis and calculate retention rates for each of the cohorts.

### 1. Build a Conversion Funnel

- Created a table representation of raw data categorized by event type and number of unique users for each event type (view, shopping_cart and purchase).
- Conversion rates in percentage were calculated for two conversions, view to shopping_cart and shopping_cart to purchase by dividing the number of unique users for shopping_cart event type by number of unique users for view event type and diviiding number of unique users for purchase event type by number of unique users for shopping_cart event type respectively.

- User data of ecommerce website was analysed between the period 2020-09-24 and 2021-02-28 and the following observations were made.
1. Number of unique users that viewed the webiste were 10,453.
2. 29.04% of the unique users i.e. 3036 proceeded to the next step of adding items to their shopping cart.
3. 35.61% of users that added items to their shopping cart i.e. 1081 users made a purchase.

<img src="images/Conversion Funnel.png?raw=true"/>

### 2. Perform Cohort Analysis

Monthly cohorts (6) analysed based on cohort age (0 to 4 months) taking count of unique users.

<img src="images/Cohort Analysis.png?raw=true"/>

### 3. Calculate Retention Rate for each of the Cohorts

- Purchase activity data was extracted from raw data into purchase_activity sheet.
- New columns first_purchase_date, event_month, first_purchase_month and cohort_age were added.
- MIN event_date was calculated in first_purchase pivot table for each user_id.
- MIN value was then populated in purchase_activity sheet for first_purchase_date column using VLOOKUP.
- event_month and first_purchase_month values were extracted from first_purchase_date to columns event_month and first_purchase_month.
- cohort_age was calculated using datedif in months between event_date and first_purchase_date.

To calculate the retention rates, cohort_analysis was done using pivot table with first_purchase_month (2020-09, 2020-10, 2020-11, 2020-12, 2021-01 and 2021-02) as rows and cohort_age (0,1,2,3,4) as columns taking count of unique users as values. 
- Retention rates were calculated in a new table categorized based on monthly cohorts (first_purchase_month leaving the final month 2021-02) as rows and cohort ages of 1 to 4 (0 is not considered as cohort just started) months as columns.
- The values of retention rates for each row and column intersaction is calculated using formula "=IFERROR(cohort_analysis!C3/cohort_analysis!B3, "-")" i.e. dividing the current cohort_analysis value by the previous cohort's cohort_analysis value for the same first_purchase_month and representing in percentage.
- The error condition replaces any divide by zero error with a "-".

<img src="images/Retention Rate.png?raw=true"/>

It was observed that retention rates were the highest in 2nd cohort with 44% of 1st cohort returning for a purchase in October of 2020 and 50% in November of 2020 respectively.

[Back To Top](/Business_Analytics)                                                  

[Back](/index)

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

