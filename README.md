# Project_2_Bangkok_House_pricing_Win


# Problem Statement

“..AP Thai CMO is thinking of launching new project in 2024, aiming to found accommodation in Bangkok and suburban areas with data-driven pricing strategy. What he needs are 

(1) To see which factors are significant to real estates price? 
(2) An acceptably accurate price prediction model. 

So, he requests his Data Science team to deliver the result within 2 weeks..”


# Data dictionary

|Feature|Type|Description|Dataset|
|---|---|---|---|
id|int|ID of selling item|train|
province|string|province name: this dataset only includes Bangkok,Samut Prakan and Nonthaburi|train|
district|string|district name|train|
subdistrict|string|subdtistrict name|train|
address|string|address e.g. street name, area name, soi number|train|
property_type|string|type of the house: Condo, Townhouse or Detached House|train|
total_units|float|the number of rooms/houses that the condo/village has|train|
bedrooms|int|the number of bedrooms|train|
baths|int|the number of baths|train|
floor_area|float|total area of inside floor [㎡]|train|
floor_level|int|floor level of the room|train|
land_area|float|total area of the land [㎡]|train|
latitude|float|latitude of the house|train|
longitude|float|longitude of the house|train|
nearby_stations|int|the number of nearby stations (within 1km)|train|
nearby_station_distance|list|list of (station name, distance[m]). Each station name consists of station ID, station name, and Line such as "E4 Asok BTS"|train|
nearby_bus_stops|int|the number of nearby bus stops|train|
nearby_supermarkets|int|the number of nearby supermarkets|train|
nearby_shops|int|the number of nearby shops|train|
year_built|int|year built|train|
month_built|string|month built: January-December|train|
price|float|selling price|train|



# Summary and Recomendation

For Condo, the lassoCV model 3 is the best model with highest R2-Score and the overall average predicted price error is around 1,056,890 THB. The total area of the condo is the most positive factor when it increases by 1 meter square, the predicted price will increase around +933,445 THB while the distance from the closest railway station is the most negative factor when it increases by 1 meter, the predicted price will decrease around -876,662 THB

For Non-condo, Detached house and Townhouse, the lassoCV model 6 is the best model with highest R2-Score and the overall average predicted price error is around 1,259,870 THB.The number of baths is the most positive factor when it increases by 1 unit, the predicted price will increase around +636,543 THB while the ‘townhouse’ property type is the most negative factor which give the sales price cheaper than that of detached house around -802,908 THB in the same environment.
