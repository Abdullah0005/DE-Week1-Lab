# Week 1 Data Engineering Lab

## Scenario
A small online shop sends daily order data as a CSV file. A manager wants a reliable summary of valid orders by city.

## Pipeline plan
- Source: `orders.csv` (daily batch file)
- Raw destination: BigQuery table `de_intro.raw_orders`
- Curated output: query results after checking and filtering the data
- User of the output: shop manager

## Local data check
Before reporting, record at least two issues you found in the CSV and what you recommend doing with each.

1. Issue and recommendation:Repeated row O-1006, we should drop one of them.
2. Issue and recommendation:Missing customer city in order O-1004,we should handle missing values.

## What the pipeline does
Complete after the lab: In one sentence, describe how the data moves from the source to a useful output.
