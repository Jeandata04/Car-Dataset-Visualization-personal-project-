# Car-Dataset-Visualization-personal-project-

## Overview
This project analyzes a car dataset to explore the relationship between horsepower, pricing, and brand performance. The goal is to identify top-performing car models and understand pricing trends across manufacturers.

The dashboard was built in Power BI using DAX measures and interactive visualizations.

## Tools Used
- Power BI 
- DAX
- Excel

## Key Insights
- Visualize for easy understanding of the data
- The Veneno Roadster emerged as the most purchased car model
- Ferari leads in total purchases
- High-performance vehicles (600+ HP) fall into a premium pricing tier

## DAX Measures used
1. Total Sold = COUNTROWS('Cars')

Most Bought Car = 
2. VAR SummaryTable =
    ADDCOLUMNS(
        VALUES('Cars'[Car Name]),
        "TotalSold", CALCULATE(COUNTROWS('Cars'))
    )
RETURN
    MAXX(
        TOPN(1, SummaryTable, [TotalSold], DESC),
        'Cars'[Car Name]
    )

## Dataset sourced from Kaggle: [Car Datasets 2025]
(https://www.kaggle.com/datasets/abdulmalik1518/cars-datasets-2025)

## Dashboard Preview
![Car Visualization Full insight](https://github.com/user-attachments/assets/19071bff-7fa6-4977-86bc-8f380e467189)

