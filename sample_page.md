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


### 2. Assess assumptions on which statistical inference will be based

```javascript
if (isAwesome){
  return true
}
```

### 3. Support the selection of appropriate statistical tools and techniques

<img src="images/dummy_thumbnail.jpg?raw=true"/>

### 4. Provide a basis for further data collection through surveys or experiments

Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium, totam rem aperiam, eaque ipsa quae ab illo inventore veritatis et quasi architecto beatae vitae dicta sunt explicabo. 

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).
