# Travel data of the yellow taxis in NY city 
## Table of Contents

 - [Project Overview](#project-overview)
 - [Data Sources](#data-sources)
 - [Recommendations](#recommendations)

### Project Overview
---
In this project we will analyze travel data of the yellow taxis in NY city from two different perspectives:

 - Vendor - Analyze taxi performance from a wider regional perspective
 - Employee (taxi drivers) - Analyze the data from an operational perspective, i.e., profitable operating hours and days of the week, etc.

### Data Sources
   - In NYC there are yellow taxis that pick up passengers and drive them to where they want to go. Taxi owners receive the calls for travel from various vendors, pick the passengers up in a suitable vehicle and drive them to the destination.
   - The yellow taxi trip records include fields capturing pick-up and drop-off dates/times, pick-up and drop-off locations, trip distances, itemized fares, rate types, payment types, and driver-reported passenger counts. The data used in the attached datasets were collected and provided to the NYC Taxi and Limousine Commission (TLC) by technology providers authorized under the Taxicab & Livery Passenger Enhancement Programs (TPEP/LPEP).
   - Analysis was made on May and June 2020. 
   - Data is obtained from [NYCTaxi & Limousine Commission website](https://www1.nyc.gov/site/tlc/about/tlc-trip-record-data.page).
   - [About Dataset](https://www.kaggle.com/datasets/microize/newyork-yellow-taxi-trip-data-2020-2019/data).
     
### Tools
Data was imported in PowerBI software and analyzed in three steps:
1. Data preparation
2. Data modeling
3. Data visualization


### Data Cleaning/Preparation
In the initial data preparation phase, we performed the following tasks: 
1. Data loading and inspection.
2. Handling missing values.
3. Data cleaning and formatting.

### Exploratory Data Analysis
EDA involved exploring the data to answer key questions, such as:

- Vendor Perspective
     - What is the distribution of vehicle types by day of the week? 
     - Which five hours a day, on average, have the most starting times for rides (tpep_pickup_datetime) ?
     - What borough has the most pickup rides ?
- Employee Perspective (taxi driver)
     - What are the two days a week when the average income per trip is the highest ?
     - What is the type of vehicle with the highest tip per mile ?

### Data Analysis
Include some interesting code/features worked with:
```
DayOfWeek = FORMAT(Trip_data[tpep_pickup_date], "dddd")
```
```
TipPerMile = IF( Trip_Data[trip_distance] > 0 && Trip_Data[tip_amount] > 0 ,(Trip_Data[tip_amount]/Trip_Data[trip_distance]), 0 )
```
 
### Results/Findings
1. Tuesday, Friday, and Monday are the most demanded days of the week for rides, and the preferred vehicle type during these peak days is predominantly private cars.
2. The data indicates that the most sought-after pickup times for rides are concentrated between 1:00 pm and 5:00 pm.
3. Among the boroughs analyzed, Manhattan stands out with the highest number of pickup rides.
4. Mondays and Sundays emerge as the days with the highest average income per trip, reaching $21.6 and $19.3, respectively.
5. Private cars exhibit the highest tip per mile ratio among all vehicle types, with an impressive $0.94 per mile. 
   
### Recommendations
1. Supply more vehicles or drivers for demanded days ( Monday, Tuesday, Friday). Ensure that there is a sufficient supply of private cars, as they appear to be the most demanded vehicle type.
2. Implement strategies to streamline pickups and improve overall service delivery during peak periods.
3. Tailor marketing campaigns to address the specific needs and preferences of customers in Manhattan.
4. Recognizing that Mondays and Sundays have the highest average income per trip, evaluate the possibility of adjusting pricing strategies on these days. This could include introducing promotions, discounts, or premium services tailored to the spending patterns observed on these high-income days.
5. Given that private cars have the highest tip per mile, consider encouraging the usage of private cars through targeted promotions or incentives. Highlight the benefits of choosing private cars and the positive tipping behavior associated with this vehicle type.




