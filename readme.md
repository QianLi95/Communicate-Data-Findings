# (Dataset Exploration Title)
## by (your name here)


## Dataset

> The data comes originally from RITA (https://d17h27t6h515a5.cloudfront.net/topher/2017/August/599fd2ad_image-predictions/image-predictions.tsv). The dataset reports United States domestic flights from the US Department of Transportation including carriers, arrival and departure delays, and reasons for delays ect., from 1987 to 2020. Due to the dataset size, In this report, I will gather & analyze flights of 2019 from July to December. 5196 rows with no tail number have been removed and nine data columns were removed from the analysis due to inconsistencies or missing information. There are 3782503 flights' informations with 21 columns in the dataset will be used.


>  After cleaning the original dataset, I will use the following variables:

              Name                        Description
              Year                        1987-2008
              Month                       1-12
              DayOfWeek                   1 (Monday) - 7 (Sunday)
              DepTime                     actual departure time (local, hhmm)
              ArrTime                     actual arrival time (local, hhmm)
              UniqueCarrier               unique carrier code
              TailNum                     plane tail number
              AirTime                     flight Time, in Minutes
              ArrDelay                    arrival delay, in minutes
              DepDelay                    departure delay, in minutes
              Origin                      origin Airport
              Dest                        destination Airport
              Distance                    distance between airports (miles)
              Cancelled                   cancelled Flight Indicator (1=Yes)
              CancellationCode            reason for cancellation (A = carrier,B = weather,C = NAS,D = security)
              CarrierDelay                carrier Delay, in Minutes
              WeatherDelay                weather Delay, in Minutes
              NASDelay                    national Air System Delay, in Minutes
              SecurityDelay               security Delay, in Minutes
              LateAircraftDelay           late Aircraft Delay, in Minutes
              


## Summary of Findings

### From Univariate Exploration

WN(Southwest Airlines Co.), DL(Delta Air Lines Inc.), AA(American Airlines Inc.) and OO(Skywest Airlines Inc.) have most airlines
The top 20 airports for depart and arrive are same, first five are ATL(William B Hartsfield-Atlanta Intl) ,ORD(Chicago O'Hare International), DFW(Dallas-Fort Worth International) , DEN(Denver Intl), CLT(Charlotte/Douglas International)
There is no big difference of the number of flights between the weekdays.
There is no big difference of the number of flights between months.
Most flights' flight time are around 50 to 150 minutes.
Many flights distance are around 600 miles, there are not that many flights distance above 1500 miles.
There are 44457 flights(1.2%) were cancelled.
There are 1225183 flights (32.4%) were delayed.
There are 324914 (45.37%) flights delayed due to carrier, there are 35987 (5.03%) flights delayed due to weather, 355183 (49.6%) flights delayed due to nas, 344653 (48.13%) flights delayed due to late aircraft, and 2184 (0.305%) flights due to security.
There are 2512863 (66.4%) flights can depart on time, 1225183 (32.4%) flights are delayed, 44457 (1.2%) flights are cancelled.
Most airplanes' flights time are around 50 minutes to 150 minutes.
Most airplanes' flights time are within 2 hours are 65.8% of all flights, 27.3% airplanes' flights time are between 2 - 4 hours, 6.5% are within 6-8 hours.
None of the features were there any unusual
No transformation was needed

### From Bivariate Exploration

WN (Southwest Airlines Co) have the highest on-time rate, also have highest Delayed rate and cancelled rate, next is DL,AA,OO and UA. That may because these company carried the most airplanes everyday.

There is no big difference of flight depart on time between months. Generally, the more flight in month, the delayed rate they have. However, the delayed rate in December are unusual. This might because of the weather, the low temperature might frozen the door of cabin. The cancelled rate have no relationship between the frequency of the flights, since the highest cancelled rate of flights are July and August, after is September,December and October. The least cancelled rate is in November.

There is no big difference of flight depart on time between weekdays. The more flight in each day of week, the delayed rate they have. There is no relationship between the number of flights each day of week and the cancelled rate. The highest cancelled rate of flights is on Thursday, and least is on Sunday.

Company WN have most flights in July, and least in September. Company DL have most flight in June and least in November. Company AA have most flights in June and least in September. Most company carry lowest flights in September.

The flights have flight time within 2 hours are more easier to be delayed. There are almost no flights will be delayed when the flight time over 6 hours.

### From Multivariate Exploration

I extended my investigation of flight status in this section by looking at the impact of the carrier, week and month. The multivariate exploration of heatmaps shows clearly very different flights situation between the two type of flight status. Dealyed flights happened heavily in Monday of December and Thursday of June. The flight on Saturday of September have lowest number of delayed flights. Cancelled flights happened heavily on Thursday of July, and least flights cancelled on Thursday and Sunday of Noverber. There are more flights delayed in the June and July, which is same for cancelled flights.

Delayed flights happened heavily in WN (Southwest Airlines Co) in December and least number of delayed flights in September. Cancelled flights happened heavily in WN(Southwest Airlines Co) in June and least number of cancelled in November. Delayed flights happened heavily in AA(American Airlines Inc.) in June and least number of delayed flights in September. Cancelled flights happened heavily in AA(American Airlines Inc.) in June and least number of cancelled in December. HA runs the fewest airlines and it has the least number of delayed flights and does not have cancelled flight. If people want to buy flight tickets from Southwest Airlines Co, try to avoid buying June and December tickets. For American Airlines Inc, avoid buying the tickets for June, it has large probability that the flights would be cancelled.

The flight tickets in June, July and December have large probability to be cancelled or delayed than other months, however, people more prefer to travel beacuse of nice weather and hoilday. If you want to reduce the opportunities that flight cancelled or delayed, avoid buying the ticket on Monday of December, Thursday of June and Thursday of July.

### Summary 
The flight tickets in June, July and December have large probability to be cancelled or delayed than other months, however, people more prefer to travel beacuse of nice weather and hoilday. If you want to reduce the opportunities that flight cancelled or delayed, avoid buying the ticket on Monday of December, Thursday of June and Thursday of July.


## Key Insights for Presentation

For the presentation, first I will introduce the pencetage of Delay Reason

Next is the percentage of flights status - cancelled, delayed and normal

Afterwards, I introduce the relationship between status for each Company, month and flight status, weekday and flight status, month and OP UNIQUE CARRIER, flight status and airtime

Finally, I will show graph of the flights status vary weekdays during month and Each carriers' flight status in each month 

## Resources 

https://docs.google.com/document/d/e/2PACX-1vQmkX4iOT6Rcrin42vslquX2_wQCjIa_hbwD0xmxrERPSOJYDtpNc_3wwK_p9_KpOsfA6QVyEHdxxq7/pub?embedded=True

https://www.transtats.bts.gov/Fields.asp?Table_ID=236
    
https://stackoverflow.com/questions/58274401/importing-multiple-csv-files-into-pandas-and-merge-them-into-one-dataframe

https://stackoverflow.com/questions/43983622/remove-unnamed-columns-in-pandas-dataframe

https://stackoverflow.com/questions/47097447/convert-string-to-hhmm-time-in-python

https://datatofish.com/check-nan-pandas-dataframe/

https://mode.com/python-tutorial/pandas-groupby-and-python-lambda-functions/
    
https://mode.com/python-tutorial/defining-python-functions/

https://www.kite.com/python/answers/how-to-display-the-value-of-each-bar-in-a-bar-chart-using-matplotlib-in-python
    
https://stackoverflow.com/questions/19913659/pandas-conditional-creation-of-a-series-dataframe-column
    
    

