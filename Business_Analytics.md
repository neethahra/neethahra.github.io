## E-Commerce Business Analytics

**Project description:** Analyze raw transaction logs of an e-commerce company to understand how website is converting product page views into purchases by building a conversion funnel, perform cohort analysis and calculate retention rates for each of the cohorts.

### 1. Build a Conversion Funnel

- Created a table representation of raw data categorized by event type and number of unique users for each event type (view, shopping_cart and purchase).
- Conversion rates in percentage were calculated for two conversions, view to shopping_cart and shopping_cart to purchase by dividing the number of unique users for shopping_cart event type by number of unique users for view event type and diviiding number of unique users for purchase event type by number of unique users for shopping_cart event type respectively.

- User data of ecommerce website was analysed between the period 2020-09-24 and 2021-02-28 and the following observations were made.
1. Number of unique users that viewed the webiste were 10,453.
2. 29.04% of the unique users i.e. 3036 proceeded to the next step of adding items to their shopping cart.
3. 35.61% of users that added items to their shopping cart i.e. 1081 users made a purchase.

<img src="images/Targeted Properties.png?raw=true"/>

### 2. Perform Cohort Analysis

- Created occupied column using the function =IF((D2="f"),1,0)
- Created day_of_week column using function =WEEKDAY(B2)
- Applied custom date and time format on day_of_week column to display the day of the week in short 
form, Mon, Tue, Wed, Thu, Fri, Sat or Sun"

- Created Pivot Table for average occupancy for any listing using listing_id for row sorted by listing id in 
ascending order and occupied for values showing average with default view

- Created another Pivot Table for highest occupancy based on day of the week by updating the above Pivot Table
- Added day_of_week row sorted by average of occupied in descending order, Show totals
- Created a bar chart for day_of_week and occupied columns with Y-axis showing aggregated view of day of week 
and Series of Average of Occupied as SUM and Listing id as COUNT

<img src="images/Average Price:Occupancy Rate.png?raw=true"/>

<img src="images/Occupancy by DayOfWeek.png?raw=true"/>

<img src="images/Average Occupancy per DayOfWeek.png?raw=true"/>

### 3. Calculate Retention Rate for each of the Cohorts

Estimated annual income for the property recommended in Lower East Side neighborhood would be 365&#42;509&#42;0.8 = $148,628
- Although there were other properties in the same neighborhood that seemed lucrative my recommendation above is based on factors like the 
consistency which is determined by the occupancy rate, host being a super host and having high number of reviews over the last twelve months
- The number of bedrooms for the property recommended is 2 as that has been the most popular property size consistently being occupied with 
higher number of reviews over the last twelve months

An updated estimated annual income for a 2 bedroom property recommended in Lower East Side neighborhood is 365&#42;451.92&#42;88.99 = $146,786.
- The above recommendation is based on factors like high occupancy rate, high number of reviews over the last twelve months and host being super host.



For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

