# Zillow Dashboard

- I used https://www.zillowdataexporter.com/ to download all current listings in Scottsdale, AZ.
- The Average Price column is color coded. Green means that the listing price is above the average price for like properties, red means below, and blue means there are no comps.

- I created two calculated fields to do this: 
-Average Prie = {FIXED [Property type], [Bedrooms], [Bathrooms] : AVG([Property price])}
-Price Comparison = IF [Property price] < [Average Price ] THEN 'Behind' ELSEIF [Property price] > [Average Price ] THEN 'Ahead' END
- Then drag Price Comparison to Color in the Marks box.
- You can click on a row in the table and the scatter plot will filter to all comps for the address in the row. Comps are properties that are the same property type, bedroom, and bathrooms size.
- Click on any data point in the scatter plot and the tooltip box will appear with a hyperlink(Zillow Listing) at the bottom of the tooltip. Click on the hyperlink and it will take you to the listing webpage on Zillow.com.

![zillow-dash](https://github.com/ChrisLaha/Tableau_Zillow_Dashboard/blob/main/zillow-dash.png?raw=true)
