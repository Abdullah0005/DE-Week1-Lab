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

## BigQuery Lab Results
Raw table: DE_Intro.orders
- Rows loaded: 8
- Rows with a missing city: 1
- Rows with a non-positive quantity: 1
- Rows returned by the filtered query: 5

## What the pipeline does
Complete after the lab: In one sentence, describe how the data moves from the source to a useful output.
The pipeline ingests raw order data from a CSV file into BigQuery, filters out data quality anomalies, and produces a clean, reliable dataset for the shop manager.