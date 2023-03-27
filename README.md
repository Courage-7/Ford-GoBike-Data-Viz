# (2019 Ford GoBike System Exploration)
## by (Courage Siameh


## Dataset

   The dataset includes:
   
The ('201902-fordgobike-tripdata.csv') data contains 63377 entries of trip records with 16 data columns which can then be split into 4 major categories for easy exploration ,analysis and visualization:

trip duration : With columns [
duration_sec, 
start_time, 
end_time ]

station info: With columns [
start_station_id, 
start_station_name, 
start_station_latitude, 
start_station_longitude, 
end_station_id, 
end_station_name, 
end_station_latitude, 
end_station_longitude ]

member's information:With the columns [
bike_id, 
user_type, 
member_birth_year, 
member_gender,
member_age, 
bike_share_for_all_trip]

trip info: With columns [
duration_minute, 
start_date, 
start_hourofday, 
start_dayofweek, 
start_month

There was some cleaning needed to the dataset. This included:
   - fixing the issue of wrong data types for the columns [ 'start_date', 'start_time','start_station_id', 'end_station_id',
   'bike_id','user_type','member_gender'] 
   
   - adding new columns for trip duration in minute,trip start date in yyyy-mm-dd format, trip start hour of the day, day of week and month
   
   - The member_birth_year can be used to find the current age of bikers. With 2019 as the current year in the dataset, a new 
   column can be created from subtracting the current year from each year value in the ['member_birth_age'] column displaying 
   the current age of bikers or riders.
   
   - filter out outlier ages from ['member_age'] column, thus occurance of ages > 70 years. This is only logical in its rarity of seeing
   a 90 year old person biking.
   
   - Changing the dtypes of the columns, 'member_birth_year' and 'member_age' to integer instead of float dtype.
   
   - the longitude and latitude start and end points are enough to create a new column for distance in kilometers


## Summary of Findings

   The relationship between the various variables plotted is seen collectively, and information is displayed simultaneously, strengthening some of the patterns identified in the preceding bivariate investigation as well as the univariate study. Subscribers' efficient or short periods of consumption are consistent with their high concentration during Monday through Friday rush hours, showing that the use is mostly for commuting to work. Customers clearly utilize the bike sharing system considerably differently than subscribers, frequently on weekends and in the afternoons, likely for leisure or city tours, as seen by the more flexible and lax pattern of their usage.


## Key Insights for Presentation
Insight #1
More bikers seem to cover or take short distance trips from 0 to 2km whereas an even lesser number of riders embark on long distant bike trips within the distances of 3 to 5km. time of day, day of the week, and gender amongst others are underlying factors with come correlation to our histogram data plot.

Insight #2
Much more subscriber usage is seen as compared to the overallcasual customers. Theere's quite a drop in volume on weekends for subscribers indicating that they ride bikes for work commute during work days in the case of traffic congestion.The significant increase of use by customers on weekends can be related to leisure, touring and relaxing or workout purposes.

Insight #3
It is seen that the other gender has the greatest fluctuation, especially in the ages of40 years and beyond. 
The male gender appears to have a steady movement along the line plot from the age 18 to 59 , with a massive fall within the ages of 69. 
        The ages of female at 57 years recorded a peak distance of 2.2 km
        The ages of other at 60 years recored a peak distance of about 2.7 km
        The ages of males at 18 years recored a peak distance of about 2.3 km
