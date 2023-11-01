# Project_2_Bangkok_House_pricing_Win


# Problem Statement

“..AP Thai CMO is thinking of launching new project in 2024, aiming to found accommodation in Bangkok and suburban areas with data-driven pricing strategy. What he needs are 

(1) To see which factors are significant to real estates price? 
(2) An acceptably accurate price prediction model. 

So, he requests his Data Science team to deliver the result within 2 weeks..”


# Data dictionary

|Feature|Type|Dataset|Description|
|---|---|---|---|
|month|string|rainfall-monthly-number-of-rain-days|Datetime (Month) "YYYY-MM"| 
|no_of_rainy_days|int|rainfall-monthly-number-of-rain-days|Number of Rain Days in the Month| 
|total_rainfall|float|rainfall-monthly-total|Monthly Total Rainfall(Millimetre)|
|maximum_rainfall_in_a_day|float|RainfallMonthlyHighestDailyTotal|Highest Daily Rainfall in the Month(Millimetre)| 
|mean_rh|float|RelativeHumidityMonthlyMean|Monthly mean relative humidity(%)| 
|mean_sunshine_hrs|float|SunshineDurationMonthlyMeanDailyDuration|Monthly Mean Daily Sunshine Duration(Hours)| 
|mean_temp|float|SurfaceAirTemperatureMonthlyMean|Surface Air Temperature - Monthly Mean(Degree Celsius)| 
|temp_mean_daily_min|float|SurfaceAirTemperatureMonthlyMeanDailyMinimum|Monthly Mean Daily Minimum Temperature(Degree Celsius)| 
|temp_mean_daily_max|float|SurfaceAirTemperatureMonthlyMeanDailyMaximum|Monthly Mean Daily Maxumum Temperature(Degree Celsius)|
|month_name|string|Added column|Name of the month e.g. Jan, Feb|
|year|int|Added column|Year ( B.C.) | 
|moonsoon_type|string|Added column|To distinguish the type of moonsoon season by month ( NE,SW,None) | 


# Summary and Recomendation

For Condo, the lassoCV model 3 is the best model with highest R2-Score and the overall average predicted price error is around 1,056,890 THB. The total area of the condo is the most positive factor when it increases by 1 meter square, the predicted price will increase around +933,445 THB while the distance from the closest railway station is the most negative factor when it increases by 1 meter, the predicted price will decrease around -876,662 THB

For Non-condo, Detached house and Townhouse, the lassoCV model 6 is the best model with highest R2-Score and the overall average predicted price error is around 1,259,870 THB.The number of baths is the most positive factor when it increases by 1 unit, the predicted price will increase around +636,543 THB while the ‘townhouse’ property type is the most negative factor which give the sales price cheaper than that of detached house around -802,908 THB in the same environment.
