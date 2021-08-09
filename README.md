# Citi Bike Analysis

As the new lead analyst for the [New York Citi Bike Program](https://en.wikipedia.org/wiki/Citi_Bike), you are now responsible for overseeing the largest bike sharing program in the United States. In your new role, you will be expected to generate regular reports for city officials looking to publicize and improve the city program.  
Since 2013, the Citi Bike Program has implemented a robust infrastructure for collecting data on the program's utilization. Through the team's efforts, each month bike data is collected, organized, and made public on the [Citi Bike Data](https://www.citibikenyc.com/system-data) webpage.  
However, while the data has been regularly updated, the team has yet to implement a dashboard or sophisticated reporting process. City officials have a number of questions on the program, so your first task on the job is to build a set of data reports to provide the answers.


## Assignment structure
```
citi-bike-analysis 
| 
|__ images/                              # contains images of graphs created
|
|__ resources/                           # contains raw datasets and combined data
| 
|
|__ citi_bike_analysis_2020.twbx         # tableau file containing analysis
|
|__ data_cleanup.ipynb                   # notebook used to combine and clean datasets
|
|__ README.md                            # readme file
```

## Usage

Dependencies and Setup
```
import pandas as pd
import glob
import os
```
Tableau: https://www.tableau.com/


## Visual Analysis
### Analysing Data from 01/2020 - 12/2020
1. Short-Term Customers vs Annual Subscribers
- Majority of users are males
- There is double amount of annual subscribers to short-term customers
- Annual subscribers and short-term customers rise at around the same rate throughout 2020
- The largest group of users are aged 31-40
- Most age groups have more annual subscribers, however, the 51-60 age group has more short-term customers
  - This phenomenon may be due to people aged 50 and below using bikes frequently to go to work, while those 51+ may be retired from work and use the bikes in a more leisurely manner  

![customers_vs_subscribers](images/customers_vs_subscribers.jpg)
  
  

2. CitiBike Use
- Bike use peaks around 7-8 AM and 5-6 PM
  - This is most likely due to people using bikes to travel to/from work
- Bikes are used more in the summer season than winter season
- During 2020, there was a decline in bike trip totals during the first third of the year, followed by a rise in the middle months and finally, another dip near the end of the year
  - This phenomenon likely coincides with the COVID-19 situation; (source: https://en.wikipedia.org/wiki/COVID-19_pandemic_in_New_York_City)
    - Lockdown was announced in New York between March and April 2020
    - Restrictions were eased in May 2020
    - COVID cases begin to rise again during November 2020 and restrictions were introduced again  
- Most rides start/end in the postal code 07302, which seems to be the city center in New York
![citi_bike_use](images/citi_bike_use.jpg)


3. Most/Least Popular Stations
- Of the top 8 most popular stations, 7 of the 8 are shared between the most popular journey starting locations and ending locations
- The top 4 most popular stations are:
  1. Grove St PATH
  2. Newport Pkwy
  3. Liberty Light Rail
  4. Hamilton Park
![station_popularity](images/station_popularity.jpg)