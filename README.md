# Classifying Climate Zones 
Classifciation of weather stations into evapotranspiration based climate zones 

## Objective 
Create a classification model that can classify Southern California weather data into a climate zones. Identify climate analogues using climate zone classifications. 

## How to Run
```
gh repo clone cbotts/climate_zones 
jupyter notebook Botts_Project3 1.ipynb
```

## Data
Data was collected from the California Irrigation Management Information System website: 
https://cimis.water.ca.gov/WSNReportCriteria.aspx

Data from 01/01/2013 to 01/01/2023 was downloaded by station to sample data across eight California counties to represent Southern California. Data was compiled into one dataframe and CIMIS zones were mapped to stations as an new feature. 

Data Dictionary 

- Jul	: The day of the year 

- ETo :	Reference evapotranspiration using a standardized surface of cool season turf, measured in inches 

- Precip :	The number of inches of rain received in a day 

- Sol Rad :	The amount of energy delivered by the sun measured in units of Langly per day.  

- Avg Vap Pres (mBars) :	A component of atmospheric pressure that is derived from molecular concentration of water in the air

- Max Air Temp (F) : The temperature high for the day measured in degrees Fahrenheit 

- Min Air Temp (F) : The temperature low for the day measured in degrees Fahrenheit

- Avg Air Temp (F) : The temperature average high for the day measured in degrees Fahrenheit

- Max Rel Hum (%) : The maximum amount of water vapor in the air for the day provided as a percentage 

- Min Rel Hum (%) : The minimum amount of water vapor in the air for the day provided as a percentage

- Avg Rel Hum (%) : The average amount of water vapor in the air for the day provided as a percentage

- Dew Point (F) : The temperature to which the air must be cooled to be saturated with water vapor. 

- Avg Wind Speed (mph) : The average speed of wind for the day, given in miles per hour 

- Wind Run (miles) : The amount of wind that passed in a day, given in miles 

- Avg Soil Temp (F) : A measurement of the warmth of the soil, given in Fahrenheit. 

- CIMIS Zone : Zone number designated by the CIMIS system 

## Methods 
Data was downsampled to create balanced class sizes. Three models were built: 

Decision Tree

Random Forest

Gradient Boosting

Hyperparameters were tuned with GridSeracg and accuracy was used to measure model performance. 

## Conclusion
CIMIS zones successfully take into account several climatic factors when delineating climate zones, but some zones may require revision. 

XGB models most accurately predict CIMIS zones. 

Future models should consider including soil characteristics. 
