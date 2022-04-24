# stop_and_frisk
 
This short project is to visualize the frequency of stop and frisk reports in NYC in 2020 using 
folium to make two cloropleth maps. The first map shows frequency of stop-and-frisks by zipcode. 
The second map shows consent-asked rates, color coded by quantile. They will appear on my blog. 
https://medium.com/@ls.casanave
 
Primary Data source: https://www1.nyc.gov/site/nypd/stats/reports-analysis/stopfrisk.page
 
GeoJason file source: https://github.com/fedhere/PUI2015_EC/blob/master/mam1612_EC/nyc-zip-code-tabulation-areas-polygons.geojson


Zipcode Frequency Map: 

<img width="823" alt="stop_and_frisk_2020" src="https://user-images.githubusercontent.com/8728172/164055225-1f9febe6-f40a-46e6-8a08-b3dcc94b7d7c.png">


Consent-Asked Map: 

<img width="824" alt="consent_asked_w_thresh" src="https://user-images.githubusercontent.com/8728172/164986742-298a3cd1-a685-42a4-a1bf-b09fd31c232c.png">

The three notebooks work together in the following order:
1) zipcode_frequency.ipynb shows how to make the first map by dropping null values and aggregating the data to show the frequency of stop-and-frisks by zipcode in 2020 NYC. 
2) consent_asked.ipynb shows how to make the second map using similar methods, but also introduces how to use the "threshold" parameter in folium. It shows the consent-asked rates by zipcode for stop-and-frisks in 2020 NYC. 
3) comparing_zipcode_frequency_to_consent_asked.ipynb shows using pandas and sorting values to compare consent-asked rates to zipcode-frequency rates. I unpack some of the analysis here. 
