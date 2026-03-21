## Project Overview

Introduction

Cyclistic is a bicycle-sharing company operating in Chicago, with more than 5,800 bicycles and 600 docking stations. For the company's continued growth, the stakeholders are interested in understanding customer behavior. The purpose is to provide a detailed analysis to identify patterns in both Casual and Member riders to increase the number of memberships. 

The goal of this project is to answer the question:

The goal of this project is to answer the question:
**How do annual members and casual riders use Cyclistic bikes differently?**

Before continuing, let's define each type of rider.

- **Member:** a person who uses the bikes frequently. This type of rider pays an annual membership fee to have access to the bikes at any time.
- **Casual:** a person who uses the bikes for a specific period. Generally, these people are tourists or occasional users who don't use the bikes often. They pay for short periods, such as a single ride or a day pass.

---

## Data source:

https://divvy-tripdata.s3.amazonaws.com/index.html

For this analysis, I selected the previous 12 months of data (April 2019 to March 2020). The data analyzed covers the same period. I explored the data to understand all variables and the overall structure, making sure everything was accurate and consistent. The project is based on four quarters:

- Q2 2019 (April–June)  
- Q3 2019 (July–August)  
- Q4 2019 (October–December)  
- Q1 2020 (January–March)

### Observations
- In Q2 2019, the last recorded date is June 27th (three days are missing)  
- There is no data available for September  
- A total of 3,228,091 trips were analyzed  

---

## Data Cleaning & Processing

The first step was cleaning the data in Excel.

- Removed latitude and longitude since they were only available for one quarter  
- Removed the `rideable_type` field because there was only one bike type  
- Standardized values:
  - “Subscriber” → “Member”
  - “Customer” → “Casual”
- Renamed columns:
  - “from” → “Start”
  - “to” → “End”
- Sorted dates in Q1 2020 to match the other datasets  

After cleaning, I combined all datasets using **Power Query** due to Excel row limitations.

Finally, I used **Power BI** to create DAX measures and build the interactive dashboard.

## Dashboard

![cyclistic_bike_project_dashboard](https://github.com/user-attachments/assets/b0b8660f-831d-42f0-ac11-7c1c43a588cb)
![cyclistic_bike_project_dashboard_casual](https://github.com/user-attachments/assets/80706f54-91b8-4294-854a-0d4708b00f78)
![cyclistic_bike_project_dashboard_member](https://github.com/user-attachments/assets/cc9edf57-ffdf-4b53-b05c-526bdc888366)

---

## Key Findings

- Summer is the busiest season, especially July and August  
- Members are more active from Monday to Friday  
- Casual riders are more active on weekends  
- Members ride more often, but for shorter periods  
- Casual riders take fewer trips, but ride longer  
- The afternoon (12 PM–6 PM) is the busiest time for both groups  

---

## Conclusion

There is a clear difference between casual and member riders.

Members ride more often from Monday to Friday and for shorter periods of time, with an average of 14 minutes per ride, generally for daily routines such as going to work or the gym. However, casual riders use the bikes more often on weekends, with an average of 1 hour per ride, which looks more like leisure or tourism activities. Increasing memberships has a positive impact on the company. With more members, there is less maintenance required for the bikes and more availability for future users.


