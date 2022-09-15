# Zillow Dashboard

- I used https://www.zillowdataexporter.com/ to download all current listings in Scottsdale, AZ.
- The Average Price column is color coded. Green means that the listing price is above the average price for like properties, red means below, and blue means there are no comps.
- I created two calculated fields to do this: 
Average Prie = {FIXED [Property type], [Bedrooms], [Bathrooms] : AVG([Property price])}
Price Comparison = IF [Property price] < [Average Price ] THEN 'Behind' ELSEIF [Property price] > [Average Price ] THEN 'Ahead' END

- You can filter the dual axis line chart by selecting a state in the dropdown selector or by clicking on a state in the map. 

![zillow-dash](https://github.com/ChrisLaha/realtor.com_dashboard/blob/main/images/Dashboard%20Screenshot.png?raw=true)
