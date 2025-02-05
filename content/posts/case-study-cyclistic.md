---
title: How Does a Bike-Share Navigate Speedy Success?
date: 2025-02-04T12:00:00Z
draft: false
---
#### Understanding How Casual Riders Differ from Annual Members in Their Usage of Cyclistic Bikes

### **Executive Summary**

Cyclistic, a Chicago-based bike-share program, seeks to increase its annual memberships by understanding how casual riders differ from members in their usage of the service. Through an extensive analysis of historical bike trip data, key insights have emerged that can inform targeted marketing strategies.

- Casual riders exhibit significantly longer ride durations — 96% longer on average — compared to annual members.
- Peak usage times differ: Casual riders primarily ride late at night and in the afternoon, while members ride during commuting hours.
- Casual riders heavily favor electric scooters and high-traffic tourist locations, such as Shedd Aquarium and Buckingham Fountain.

**Key Recommendations**

Experience-Based Marketing Campaigns:

- Casual riders tend to use the bikes for leisure and recreational activities. Instead of just promoting membership, Cyclistic should highlight the experiences enabled by the bikes, such as exploring Chicago’s parks, waterfront paths, and late-night attractions.
- Create campaigns featuring popular destinations during peak casual user timeframes (afternoons, weekends, and nights), emphasizing how bikes and scooters provide convenient, cost-effective, and fun travel options.

Time-Sensitive & Location-Based Advertising:

- Physical advertising at key casual rider locations, such as billboards, transit stops, and docking stations near tourist hotspots.
- Use seasonal and time-based ad targeting — for instance, nighttime ads can highlight the convenience of 24-hour bike and scooter availability compared to late-night Uber wait times and surge pricing.
- Search-based ad buying: Bid for searches related to “Uber” and key docking locations at peak times, targeting casual users looking for transportation alternatives.

Electric Scooter & Multi-Modal Membership Promotion:

- Since casual riders are more likely to use electric scooters, Cyclistic ads should feature electric scooters.

By implementing these strategies, Cyclistic can effectively convert casual riders into long-term members, ensuring sustainable revenue growth and increased customer retention.

### Introduction & Business Task

Cyclistic is a Chicago-based bike-share program operating a fleet of over 5,800 bicycles across 600 docking stations. Unlike many bike-share services, Cyclistic offers a diverse range of bicycles, including reclining bikes, hand tricycles, and cargo bikes. This commitment to inclusivity, paired with flexible pricing options, has helped Cyclistic establish a strong presence in the city’s transportation network.

Despite its success, Cyclistic faces a critical business challenge: converting casual riders into long-term annual members. The company’s marketing strategy has historically focused on broad consumer awareness, but Director of Marketing Lily Moreno believes that sustainable growth hinges on expanding its base of committed members.

To address this, the business task is to analyze historical bike trip data to understand how casual riders differ from annual members. By identifying usage patterns, the goal is to develop data-driven marketing strategies that increase membership conversion rates, ensuring Cyclistic’s long-term financial sustainability and continued success.

**Key Stakeholders**

- Lily Moreno, Director of Marketing — Oversees campaigns promoting the bike-share program.
- Executive Team — Approves marketing strategies before implementation.
- Marketing Analytics Team — Collects, analyzes, and reports data to guide marketing efforts.

Insights from this analysis will shape marketing recommendations for the Executive Team, with the Marketing Analytics Team executing targeted strategies to drive membership growth.

### Description of Data Sources

Cyclistic’s historical trip data is sourced from the Divvy bike-sharing system, operated by Lyft Bikes and Scooters, LLC, in partnership with the City of Chicago. The dataset includes all recorded trips and is publicly available for research and analysis.

**Data Collection and Storage**

- Provider: Lyft Bikes and Scooters, LLC (Divvy system)
- Storage: Amazon S3 bucket (monthly CSV files)
- Timeframe: January 2024 to December 2024

**Key Dataset Columns**

- Ride ID
- Rideable Type (Classic Bike, Electric Bike, or Electric Scooter)
- Trip Start & End Timestamp
- Trip Start & End Station (ID & Name, Latitude/Longitude)
- User Type (Member or Casual)

**Data Credibility & Privacy Considerations**

The dataset adheres to the ROCCC framework:

- Reliable: Officially provided by Lyft Bikes & Scooters, LLC.
- Comprehensive: Covers all recorded rides in the timeframe.
- Current: Includes the latest available data.
- Cited: Properly referenced.

Privacy-Protected: Contains no personally identifiable information (PII).

Publicly Available: Divvy System Data Repository

### Data Cleaning and Processing

To ensure data integrity and usability, the dataset was processed using Excel, Bash, Python, PostgreSQL, and Azure Data Studio.

**Cleaning Steps**

- Checked for duplicates, nulls, typos, and abnormal values.
- Removed:
- Duplicate ride IDs (422 instances).
- Trips with end times before start times (277 instances).
- Outlier GPS values (50 instances outside the service area).
- Added Calculated Fields:
- Trip Duration (seconds)
- Day of the Week (1–7)

SQL Processing Pipeline

- 01_drop_duplicate_ride_id.sql
- 02_drop_invalid_trip_duration.sql
- 03_drop_outlier_gps.sql
- 04_add_trip_duration_seconds.sql
- 05_add_trip_day_of_week.sql

### Data Analysis Summary & Findings

**Key Findings**

- Ride Duration — Casual riders take 96% longer trips than members.
- Peak Usage Times — Casual riders peak 1 AM–3 AM and 2 PM, members peak during commuting hours.
- Seasonality — Casual ridership (relative to member ridership) peaks in July at 43%.
- Bike Type Preferences — Casual riders are more than twice as likely to select an electric scooter when compared to members.
- Popular Casual Rider Stations — Shedd Aquarium, DuSable Lake Shore, Dr & Monroe St, Streeter Dr & Grand Ave, Buckingham Fountain

### Visualizations & Key Insights

Figure 1 — Trip duration comparison by user type.

![](https://cdn-images-1.medium.com/max/1200/1*MIU83u0_iQrYJUi3WzVEBw.png)

Figure 2, 3, & 4 — Peak usage times by season, day of week, and hour of day.

![](https://cdn-images-1.medium.com/max/1200/1*qbuL5MWHKOlSScU8bpJFdQ.png)

![](https://cdn-images-1.medium.com/max/1200/1*G7I4tzKAc3JH8nBVkYA5eQ.png)

![](https://cdn-images-1.medium.com/max/1200/1*g4CBseSKfAvCu1tTPfzzDg.png)

Figure 5 — Bike type preference breakdown.

![](https://cdn-images-1.medium.com/max/1200/1*XYxkZGecE-e98yUdkcw_IA.png)

### Recommendations

**Experience-Based Marketing Campaigns**

- Casual riders tend to use the bikes for leisure and recreational activities. Instead of just promoting membership, Cyclistic should highlight the experiences enabled by the bikes, such as exploring Chicago’s parks, waterfront paths, and late-night attractions.
- Create campaigns featuring popular destinations during peak casual user timeframes (afternoons, weekends, and nights), emphasizing how bikes and scooters provide convenient, cost-effective, and fun travel options.

**Time-Sensitive & Location-Based Advertising**

- Physical advertising at key casual rider locations, such as billboards, transit stops, and docking stations near tourist hotspots.
- Use seasonal and time-based ad targeting — for instance, nighttime ads can highlight the convenience of 24-hour bike and scooter availability compared to late-night Uber wait times and surge pricing.
- Search-based ad buying: Bid for searches related to “Uber” and key docking locations at peak times, targeting casual users looking for transportation alternatives.

**Electric Scooter & Multi-Modal Membership Promotion**

- Since casual riders are more likely to use electric scooters, Cyclistic ads should feature electric scooters.

### Conclusion

By leveraging data-driven marketing, Cyclistic can effectively convert casual riders into annual members, ensuring long-term revenue growth and a more engaged user base.

### References & Appendix

- Data Source: Divvy System Data
- Full Dataset: [Download Here](https://divvy-tripdata.s3.amazonaws.com/index.html)

**Scripts**
```sql
--01_drop_duplicate_ride_id.sql  
WITH Duplicates AS (  
    SELECT *,  
           ROW_NUMBER() OVER (  
               PARTITION BY ride_id  
               ORDER BY started_at ASC  -- Keep the earliest ride if duplicates exist  
           ) AS row_num  
    FROM bike_rides  
)  
DELETE FROM bike_rides  
WHERE ride_id IN (  
    SELECT ride_id FROM Duplicates WHERE row_num > 1  
);  
ALTER TABLE bike_rides ADD PRIMARY KEY (ride_id);
```

```sql
-- 02_drop_invalid_trip_duration.sql  
WITH InvalidRides AS (  
    SELECT ride_id  
    FROM bike_rides  
    WHERE started_at > ended_at  
)  
DELETE FROM bike_rides  
WHERE ride_id IN (SELECT ride_id FROM InvalidRides);
```

```sql
-- 03_drop_outlier_gps.sql  
DELETE FROM bike_rides  
WHERE   
    start_lat NOT BETWEEN 41.4 AND 42.6   
    OR start_lng NOT BETWEEN -88.2 AND -87  
    OR end_lat NOT BETWEEN 41.4 AND 42.6  
    OR end_lng NOT BETWEEN -88.2 AND -87;
```

```sql
-- 04_add_trip_duration_seconds.sql  
ALTER TABLE bike_rides ADD COLUMN trip_duration_seconds BIGINT;  
UPDATE bike_rides   
SET trip_duration_seconds = EXTRACT(EPOCH FROM (ended_at - started_at));
```

```sql
-- 05_add_trip_day_of_week.sql  
ALTER TABLE bike_rides ADD COLUMN trip_day_of_week INT;  
  
UPDATE bike_rides   
SET trip_day_of_week = EXTRACT(DOW FROM started_at) + 1;
```