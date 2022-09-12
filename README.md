# Surfsup_Challenge
## Overview
For this challenge we will be further analyzing weather data for Hawaii in order to determine if a Surf shop and ice cream business is sustainable all year round. Our initial analysis only accounted for the last 12 months, however we will be incorportating more than 10 years of historical weather data, in order to provide a more accurate analysis.

## Results 
![image](https://user-images.githubusercontent.com/106443196/189758763-e365ed84-9c49-4352-aa2c-93f68e02f369.png)
![image](https://user-images.githubusercontent.com/106443196/189758783-6b5b1791-05ce-4bf2-a349-290f01ecc5e8.png)

3 Key Differences in weather between June and December
* The minimum temperature in June is 64 and in December it's 56
* The standard deviation for June is 3.3 and in December it's 3.7
* The count for June is 1700 compared to 1517 in December

## Summary 
Based on our analysis we are able to conclude that December has a wider range of temperatures compared to June. Half of the days in December have temperatures 71 or below and a minimum temperature of 56. While in June, half of the days have temperatures of 75 or lower and minimum temperature of 64. These results show how generally the summer months are warmer than the winter months. Despite the differences in temperatures between June and December, the average temperature only varies by less than 4 degrees. In order to gather more information on weather data for the months of December and June, we should incorporate other measurements, such as precipitation. Performing 2 additional queries to the hawaii.sqlite database will allow us to generate some more detailed statistics to further support our business plan.

Precipitation Queries: 
* June_rain = session.query(Measurement.date,Measurement.prcp,).filter(extract('month', Measurement.date) == 6).all()
* Dec_rain = session.query(Measurement.date,Measurement.prcp,).filter(extract('month', Measurement.date) == 12).all()
