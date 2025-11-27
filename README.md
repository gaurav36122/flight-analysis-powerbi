# Flight Data Analysis -- Power BI Project

## Project Overview

This project contains a Power BI dashboard built for analyzing flight
operations, delays, airline performance, and route insights.\
The goal of this dashboard is to understand flight behavior, delay
reasons, traffic patterns, and operational efficiency.

## 📸 Dashboard Previews
![Dashboard](https://github.com/gaurav36122/flight-analysis-powerbi/blob/main/Flight_Dashboard.png?raw=true)

## Dashboard Features

### 1. Overview

-   Total flights\
-   Total delayed flights\
-   Total cancellations\
-   Average delay time\
-   On-time percentage

### 2. Delay Analysis

-   Delay by airline\
-   Delay by reason (weather, technical, crew, ATC, etc.)\
-   Daily and monthly delay trends\
-   Severity of delays

### 3. Route Analysis

-   Busiest routes\
-   Airport-to-airport flight movement\
-   Route-wise delay comparison\
-   Passenger or traffic patterns

### 4. Airline Performance

-   Airline punctuality\
-   Airline delay contribution\
-   Total flights per airline

## Dataset Information

-   Flight number\
-   Airline\
-   Source airport\
-   Destination airport\
-   Scheduled time\
-   Actual time\
-   Delay minutes\
-   Cancellation reason\
-   Date and month

## Data Cleaning & Transformation

Performed using Power Query: - Removed duplicates\
- Handled null values\
- Standardized time formats\
- Added calculated columns\
- Created KPIs using DAX measures

## DAX Measures Used (Example)
Ave_flight_delay_by_departures =
CALCULATE(AVERAGE('power bi flight'[Departure Delay (Minutes)]))

Avg_flight_delay_by_arrivals =CALCULATE(AVERAGEA('power bi flight'[Arrival Delay (Minutes)]))

cancelled =CALCULATE(COUNTROWS('power bi flight'),FILTER('power bi flight', 'power bi flight'[Flight Status] = "Cancelled"))

distribution_flights_by_airline =CALCULATE(DISTINCTCOUNT('power bi flight'[Airline]))

Flight_delay_by_arrival =CALCULATE(AVERAGE('power bi flight'[Arrival Delay (Minutes)]))

flights_handled_by_the_airport_authority =CALCULATE(COUNTA('power bi flight'[Arrival Airport]))

total_flight_delayed =CALCULATE(COUNTROWS('power bi flight'),FILTER('power bi flight', 'power bi flight'[Flight Status] = "Delayed"))

  

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

This Power BI dashboard provides insights into flight operations,
delays, airline performance, and route traffic.

👤 **Author**
**Gaurav Singh**  
📧 Email: [gaurav36122@gmail.com]  
💼 LinkedIn: [www.linkedin.com/in/gaurav-singh-692b24273]  
⭐ *If you found this project insightful, please consider starring the repository!* ⭐
