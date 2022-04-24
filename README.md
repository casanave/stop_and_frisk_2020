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
3) comparing_zipcode_frequency_to_consent_asked.ipynb shows using pandas and sorting values to compare consent-asked rates to zipcode-frequency rates. I unpack some of the analysis here. My full table of findings is available as an excel file here in stop_and_frisk/data/2020_NYPD_Stop-and-Frisk_consent-asked_rate.xlsx

# CONCLUSION:

# High-Frequency Stop-and-Frisk Zip Codes

![east_harlem_stock_photo](https://user-images.githubusercontent.com/8728172/164987246-6a80f2ca-fcb1-4761-a909-74662e30eedc.jpg)

10029:

In East Harlem, the most common stop-and-frisk zip code, where 220 folks were reported stop-and-frisked in 2020, the consent-asked rate is around 11%, (in between the first and second quartile, so slightly less than the absolute average for this data set.)


![east_ny_stock_photo](https://user-images.githubusercontent.com/8728172/164987252-bc09b300-61a8-4d2a-bd0d-fefe28dac3a2.jpg)

11207:

East New York, the second most common stop-and-frisk zip code, percent-asked is around 20% (putting it in the 75 percentile of most consensual stop-and-frisks as well.) That's a big difference from East Harlem's 11% consent-asked rate, for those 169 folks stop-and-frisked. 


![bushwick_stock_photo](https://user-images.githubusercontent.com/8728172/164987266-e586b94c-5b30-410e-a5f3-cadcfb150034.jpg)

11206:

Bushwick, the seventh most common stop-and-frisk zip code, consent-asked is around 25%, (also putting it in the 75% percentile of most consensual stop-and-frisks.) This zip code has one of the highest consent-asked rates for high-frequency zipcodes. 


![mills_basin_stock_photo](https://user-images.githubusercontent.com/8728172/164987278-d23ffc1c-9c26-4022-8816-92457edbbe84.jpg)

11234:

Flatlands/Bergen Beach, the 14th most common stop-and-frisk zip code, the consent-asked rate is at about 23%, while just next door in Canarsie, zipcode 11236, the consent-asked rate is less than half of that at about 10.5%. 


![sunset_park_stock_photo](https://user-images.githubusercontent.com/8728172/164987289-57675efe-878e-4d00-8682-d7655dd8333a.jpg)

11220:

Sunset Park, the 15th most common stop-and-frisk zip code, consent-asked is the lowest% within the top 25 highest frequency zip codes, at just under 4% asked. This is a very interesting case since all the other zip codes in the top 25 most frequent zip codes have consent-asked rates much higher by about 3 times at least. The next most consent-asked zip code in the top 25 is 10002 (The Lower East Side) with a consent-asked rate of about 9%.

# Low-Frequency Consent-Asked Zip Codes:

![industry_city_stock_photo](https://user-images.githubusercontent.com/8728172/164987298-11b658cc-01de-4f29-8126-9e22acf60a34.jpg)

11232:

This is Bush Terminal/Greenwood/Sunset Park. Of the zip codes where consent was never asked for in 2020, this is the zip code where stop-and-frisks had the highest stop-and-frisk frequency of 40 people. 


![forrest_hills_stock_photo](https://user-images.githubusercontent.com/8728172/164987308-2f0aedbb-8c15-4345-b4dc-15449fe47800.jpg)

11375:

Forrest Hills had a low consent-asked rate too compared to its stop-and-frisk frequency of about 30 people, similar to sunset park.


![midland_beach_stock_photo](https://user-images.githubusercontent.com/8728172/164987320-d655f601-35a7-48af-983c-0834136e7b16.jpg)
10306:

This zip code is in Staten Island and includes Midland Beach. It had a surprising 0% consent-asked rate for the 31 people stop-and-frisked there, compared to just next door, in 10309 where 22 people were stop-and-frisked. But when we look to try to see what percentage of the folks in 10309 were asked for consent, we see a percent close to 20%.

![flatlands_stock_photo](https://user-images.githubusercontent.com/8728172/164987332-0216b01f-0fe0-4e91-8f8c-12d3527e61ce.jpg)

11210:

For the about 30 people who were stop-and-frisked in this part of the Flatlands in 2020, none were asked if they consented.
