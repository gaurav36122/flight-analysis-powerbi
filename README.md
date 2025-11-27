# Flight Data Analysis -- Power BI Project

## Project Overview

This repository contains a professionally designed Power BI dashboard
developed to analyze key aspects of flight operations.\
The analysis includes metrics such as delay behavior, cancellation
trends, airline performance, and route-level insights.\
The project aims to support data-driven evaluation of operational
efficiency and improve understanding of flight traffic patterns.

## Dashboard Preview

![Dashboard](https://github.com/gaurav36122/flight-analysis-powerbi/blob/main/Flight_Dashboard.png?raw=true)

## Dashboard Features

### 1. Overview

-   Total flights
-   Total delayed flights
-   Total cancellations
-   Average delay time
-   On-time performance percentage

### 2. Delay Analysis

-   Delay breakdown by airline
-   Delay analysis by reason (weather, technical, crew, ATC, etc.)
-   Monthly and daily delay trends
-   Delay severity segmentation

### 3. Route Analysis

-   Top busiest routes
-   Airport-to-airport traffic movement
-   Route-wise delay comparison
-   Passenger/traffic patterns

### 4. Airline Performance

-   Airline punctuality scoring
-   Delay contribution percentage by airline
-   Total flights handled by each airline

## Dataset Information

The dataset includes key fields used for modeling: - Flight number -
Airline - Source airport - Destination airport - Scheduled time - Actual
time - Delay minutes - Cancellation reason - Date and month

## Data Cleaning & Transformation

Data preparation was conducted using Power Query, involving: - Removing
duplicates - Handling null and inconsistent values - Standardizing date
and time formats - Adding custom calculated columns - Creating KPI
measures using DAX

## DAX Measures Used (Examples)

    Ave_flight_delay_by_departures =
    CALCULATE(AVERAGE('power bi flight'[Departure Delay (Minutes)]))

    Avg_flight_delay_by_arrivals =
    CALCULATE(AVERAGEA('power bi flight'[Arrival Delay (Minutes)]))

    cancelled =
    CALCULATE(
        COUNTROWS('power bi flight'),
        FILTER('power bi flight','power bi flight'[Flight Status] = "Cancelled")
    )

    distribution_flights_by_airline =
    CALCULATE(DISTINCTCOUNT('power bi flight'[Airline]))

    Flight_delay_by_arrival =
    CALCULATE(AVERAGE('power bi flight'[Arrival Delay (Minutes)]))

    flights_handled_by_the_airport_authority =
    CALCULATE(COUNTA('power bi flight'[Arrival Airport]))

    total_flight_delayed =
    CALCULATE(
        COUNTROWS('power bi flight'),
        FILTER('power bi flight','power bi flight'[Flight Status] = "Delayed")
    )

## Tools Used

-   Power BI Desktop\
-   Power Query\
-   DAX\
-   Excel / CSV datasets

## Project Structure

    Flight-Dashboard/
    │
    ├── flight.pbix
    ├── datasets/
    └── README.md

## Conclusion

This project delivers a comprehensive analysis of flight operations,
identifying critical performance insights such as delays, cancellations,
and airline efficiency.\
The dashboard equips stakeholders with actionable intelligence to
enhance service quality and operational planning.

## Author

**Gaurav Singh**\
📧 Email: gaurav36122@gmail.com\
💼 LinkedIn: www.linkedin.com/in/gaurav-singh-692b24273

⭐ If you found this project valuable, please consider starring the
repository!
