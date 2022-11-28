# New York City Taxi Data EDA

This dataset contains 14,58,644 observations of New York City Taxi data. Each observation represents a Taxi ride that has been done in the New York City.

The Dataset is available at - https://drive.google.com/file/d/10tjPuNW4n6qTTTMyagmDGSbfDmxd0RBK/view?usp=sharing

## Description of the Columns

id - The id column shows us the unique id for each taxi ride.
vendor_id – Vendor Id is of 2 types based on the trip duration of the customer.
pickup_datetime – Time and date of which the customer has been picked up by the taxi driver. 
dropoff_datetime - Time and date of which the customer has been dropped by the taxi driver. 
passenger_count – Number of the passengers in a particular taxi trip. 
pickup_longitude – The longitude coordinates of the pickup location of the customer. 
pickup_latitude – The latitude coordinates of the pickup location of the customer. 
dropoff_longitude – The longitude coordinates of the drop off location of customer. 
dropoff_latitude – The longitude coordinates of the drop off location of the customer. 
store_and_fwd_flag – This depicts whether the customer would move forward with a extension of the trip or they get down at the same place.
trip_duration – Total trip duration of a particular taxi ride.


Out main objective is to perform EDA on the given dataset and draw useful conclusions about general trends in New York City and how different factors affecting taxi trips in New York City vary and are correlated. We can perform various analysis based on the interest shown in taxi rides booking in NYC.

## Questions for the Analysis
The insights that I want to forge out from the data by performing Exploratory Data Analysis are: 

1.	Which is most common way of taxi (long duration or short duration)? 
2.	Which location have a greater number of customers that take taxi?
3.	Which time in the day is the most preferred by customers to take taxi? 
4.	What is the percentage of the customers that take taxi in the evening out of all the taxi rides?
5.	What is the most common pickup point for the customers? 
6.	Which are the busiest months of taking taxis? 
7.	Which part of the city has the least number of taxi rides?
8.	How long does an average taxi trip take? 
9.	Which taxi vendor has the highest trip duration?
10.	Which taxi ride has a least lead time? 
11.	What is preferred distance in each ride of the taxi? 
12.	Bringing out the statistical insights of each numerical values of location.
13.	Which taxi has a high chance that its customer will return for another taxi ride?
14.	Which date in the year has most taxi rides in a single day? 
15.	How are the number of passengers and the trip duration correlated affecting the different parameters?
16.	What is the distribution of the plot that is drawn between trip duration and the pickup location?
17.	What is the range of the outliers for the data set based on the trip duration?
18.	Yearly and Monthly wise analysis of taxi trips and routes? 
19.	Average trip duration as per customer satisfaction.
20.	Analyse what is the trend of rides from different office buildings across New York City. (Using Plotly library)
21.	Average Daily Rate (ADR) for different types of locations and trip types? 
22.	Analyse which types of taxi riders are getting a greater number of rides? 



I chose this dataset to forge out the insights, as there is need of analysing of the taxi data day by day, as the need to predict the taxi riding density is much more needed as the surplus of the taxis must be maintained when the demand of the customers is being fluctuating throughout different seasons in a year.


# Statistical Analysis
•	The trip id id0053347 has the highest duration among all the other trips.
•	The average trip duration is 959.4922729603659
•	There are 4 instances where the trip duration exceeded 10,000 Minutes.
•	There are 2 Vendor Id’s:  2->780302 1->678342
•	The most number of times the passengers travelled solo.

# Data Cleaning Process
I have plotted a scatter plot to check the number of values that lie in different ranges. That showed us that there were some outliers that were affecting the whole data set. Some trips are as long as 2 days from east to west coast of United States. So, these trips don’t come under the regular taxi trips that are useful for analyzing the patterns in taxi data. We should remove the outliers using some statistical methods like considering the values within the 1.5 times the Interquartile Range (which is the statistically ideal range in which outliers are not present). To perform this task, we have calculated the Quartiles. Interquartile Range can be calculated by using the following formula: IQR = Q3 - Q1. The range without outlier is [1.5IQR+Q1, Q3+1.5IQR]. So, there are 13,84,424 values after removing the Outliers. So, we have plotted the box plot again to visualize whether the outliers have been removed or not. As we noticed in the 2nd Boxplot, majority of the outliers have been removed. Later we have plotted Scatter Plot to understand how the data has been distributed.


# Univariate Analysis
## Number of Passengers
 
The above is a histogram of the count of number of passengers.
•	There are 0.983 million instances where only a single passenger travelled.
•	There are 197,635 instances where 2 passengers travelled together.
•	There are 56,558 instances where 3 passengers travelled together.
•	There are 26,618 instances where 4 passengers travelled together.
•	There are 73,864 instances where 5 passengers travelled together.
•	There are 45,805 instances where 6 passengers travelled together.


## Trip Duration
 
The above hist plot shows how the trip duration is distributed among the number of trips.
•	The highest trip duration is between 365-367 minutes where there are 7705 instances.
•	The plot is taken as slots of nearly 4 minutes.

# Bivariate Analysis
Trip Duration related to Number of Passengers in a Ride
•	There are 1033540 customer bookings in which only one person travelled.
•	There are only 5 instances in which passenger count was 7 or above.
•	There are 60 instances where there was no passenger in the taxi.

As we can see, as the passenger count increases, the trip duration gradually increases.


## Conclusion (Until now)
First, we have taken the data set and performed some statistical methods to better understand the dataset. We have checked the shape and got to know that we have 50,000 rows of data. We got to know that there is a linearly proportional relation between the passenger count and the trip duration. That has been clearly depicted using the logarithmic histogram plotted previously. Later we have plotted a scatter plot to check the number of values that lie in different ranges. That showed us that there were some outliers that were affecting the whole data set. Some trips are if 2 days from east to west coast of United States. So, these trips don’t come under the regular taxi trips that are useful for analysing the patterns in taxi data. We should remove the outliers using some statistical methods like considering the values within the 1.5 times the Interquartile Range (which is the statistically ideal range in which outliers are not present). To perform this task, we have calculated the Quartiles. Interquartile Range can be calculated by using the following formula: IQR = Q3 - Q1. The range without outlier is [1.5IQR+Q1, Q3+1.5IQR]. So, there are 13,84,424 values after removing the Outliers. So, we have plotted the box plot again to visualize whether the outliers have been removed or not. As we noticed in the 2nd Boxplot, majority of the outliers have been removed. Later we have plotted Scatter Plot to understand how the data has been distributed.

