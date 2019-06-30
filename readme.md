# (Dataset Exploration Title)
## by Dirk Henrichmoeller


## Dataset

#### Preliminary Wrangling

The raw data set can be downloaded [here](https://www.lyft.com/bikes/bay-wheels/system-data). The individual channels contain the following 16 data columns:

* Trip Duration (seconds)
* Start Time and Date
* End Time and Date
* Start Station ID
* Start Station Name
* Start Station Latitude
* Start Station Longitude
* End Station ID
* End Station Name
* End Station Latitude
* End Station Longitude
* Bike ID
* User Type (Subscriber or Customer – “Subscriber” = Member or “Customer” = Casual)
* Member Year of Birth
* Member Gender

Since the data comes with one csv-file per month, 12 individual csv-files were downloaded and concatenated (after the structures similarity was validated).  
The final data set includes all observations from year 2018. It includes 1741556 observations with 14 features. Most features are categorical (some of the date interpretations should be seen as ordinal data). There is only one real numeric type (duration_sec): the duration of the bike rent in seconds.

## Summary of Findings

* About 3/4 of all customers are male.
* Almost 90 % of all customers use this service as subsribed regular users while only about 10 % are casual users.
* Most rentals start at "SF Caltrain Station 2".
* Most rentals end at "SF Caltrain Station 2".
* The distribution of the rental duration is unimodally distributed in a logarithmic representation with its mean at 773 seconds. There are many outliers which are caused by very long rental durations (possible reason: customer didnt return the bike or the system falsly didn't detect the return of the bike).
* Most rentals take place on working days with its maximum on mid-week (Tuesday, Wednesday, Thursday). On the weekends the rental frequency drops by around 50%.
* Most rentals start at 08:00h (start of work) and 17:00h (end of work). It could be interesting to further observe the hour of bike return and correlatte the rental duration in this matter.
* Most rentals take place in and around the sommer time.
* The customers mean age is 1983. The age distribution is left skewed.
* The most driven route starts at "SF Ferry Building" and ends at "The Embarcadero". We can assume that this route brings commuters from the ferry harbour to the next public transportation hub. Another observation is, that the Matrix is not symmetric. That means that end and start locations are not interchangeble. This means that customers dont always use the same route for their return trip.
* The mean rental duration increases over the weekend. This might indicate that customers use this service primarely to commute on work days, while on weekend days more leisure rides might be planned.
* When looking at the mean duration of rental, female customers seems to take a little bit more time. If we focus on the most used commuter route, this difference appear to shrink.
* Frequent customers use their rental bikes for a shorter amount of time than casual customers.
* The increase of rental duration from working days to weekend days is almost twice as high for female customers as for male customers.
* Customers who rent their bike at 03:00h in the morning will keep their bikes longer then others (party returners who keep the bike overnight?).


## Key Insights for Presentation

The increase of rental duration from working days to weekend days is almost twice as high for female customers as for male customers.  
__Female customers seem to focus more on leisure at weekends.__