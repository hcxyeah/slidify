---
title       : My shiny application
subtitle    : 
author      : Ch
job         : 
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : []            # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides
---

## Profit and sales visualization

Hello, this is interactive data visualization of sales data. 

The application can be accessed on 
https://hcxyeah.shinyapps.io/data_product/
The raw scripts are on github:
https://github.com/hcxyeah/data_product


--- .class #id 

## Design

The application use googlevis and shiny to create interactive graph.
In this application, user select product categories and market to see the profit and sales in deifferent countries around the world, how the profit and sales change over time, and the comparison between different market. 

--- 

## Data

This dataset is the profit and sales data of a global company.


```r
data <- read.csv("../data.csv")
names(data)
```

```
##  [1] "X"              "Country"        "Row.ID"         "Order.ID"      
##  [5] "Order.Date"     "Ship.Date"      "Ship.Mode"      "Customer.ID"   
##  [9] "Customer.Name"  "Segment"        "City"           "State"         
## [13] "Postal.Code"    "Market"         "Region"         "Product.ID"    
## [17] "Category"       "Sub.Category"   "Product.Name"   "Sales"         
## [21] "Quantity"       "Discount"       "Profit"         "Shipping.Cost" 
## [25] "Order.Priority" "Code"
```

---

## Components

1. Map: show the sales and profit of each countries on the map and table.
2. Growth: show the profit and sales in different market change over time.
3. Bar chart: show the comparison of profit and sale on different markets.
4. Data: enable user to see the data and download it. 

---
