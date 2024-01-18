## NYC Airbnb Data Analysis

**Project description:** Analyze data collected on current Airbnb listings to identify targeted properties, calculate occupancy & estimate revenue for an investment property.

### 1. Identify Targeted Properties

- Added neighborhood_clean column displaying neighborhood text trimmed and capitalized using = TRIM(PROPER(AB4))
- Created a pivot table to focus on 10 most popular vacation rental neighborhoods in New York City. Pivot table has one row
neighborhood_clean in descending order sorted by COUNT of number_of_reviews_ltm. Values of pivot table are number_of_reviews_ltm 
with defalt view and summarized by SUM.
- Added bedrooms_clean column next to bedrooms

- Created a pivot table for property sizes most popular in rentals with reference to number of bedrooms.
- An assumption here is studio apartments have no bedrooms , so the count of bedrooms is 0
- Pivot table is created with following: row as neighborhood_clean (ordered descending sorted by SUM of number_of_reviews_ltm and Grandtotal), column as bedrooms_clean ordered by ascending, sorted by SUM of number_of_reviews_ltm and Grandtotal and value as number_of_reviews_ltm summartized by SUM with % row view.

<img src="images/Targeted Properties.png?raw=true"/>

### 2. Calculate Occupancy

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

### 3. Estimate Revenue for an Investment Property

Estimated annual income for the property recommended in Lower East Side neighborhood would be 365&#42;509&#42;0.8 = $148,628
- Although there were other properties in the same neighborhood that seemed lucrative my recommendation above is based on factors like the 
consistency which is determined by the occupancy rate, host being a super host and having high number of reviews over the last twelve months
- The number of bedrooms for the property recommended is 2 as that has been the most popular property size consistently being occupied with 
higher number of reviews over the last twelve months

An updated estimated annual income for a 2 bedroom property recommended in Lower East Side neighborhood is 365&#42;451.92&#42;88.99 = $146,786.
- The above recommendation is based on factors like high occupancy rate, high number of reviews over the last twelve months and host being super host.



For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

