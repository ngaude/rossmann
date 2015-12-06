# rossmann kaggle

Beyond stores to state association, I really wanted to go the hard way and put stores on map with latitude and longitude. For this, I went to the [Google Places API][1] and referenced all german drugstores with ad-hoc [Radar Search][2] requests :  

As a first result, I got 6754 geolocated german drugstores, with an insight on the company owner e.g. Rossmann (2020) , DM (2178), other (2556). I have attached these results in the **german_drogerice_geo.csv** file.



Then I dwell into finding some local information about the 2020 Rossmann stores found. The most important feature for this Kaggle, because of its time-series nature, is the store opening-hours that I retreived using [Place Details][3] request. The attached **rossmann_opening_hours.csv** file contains the open and  close hours for all Rossmann stores and day of week. For instance, we saw that only 147 Rossmann Stores seems to be opened on sunday.

Last, I found also useful to enrich the 2020 rossmann stores with some public local information I grabbed from the [geonames.org][4] platform such as : city, near local population, city elevation, distance to the nearest hotel,  distance to the nearest rail station and, of course, the Bundesland they belong to. All these enrichments of Rossmann stores are available in the **rossmann_store_geo.csv** file attached.

So here is all the raw material needed to proceed to Rossmann store mapping. 
From these data, one can find its own so-far-so-good association between the 2020 physical stores and the 1115 stores in dataset. But that's [another story][5].

  [1]: https://developers.google.com/places/ "Google Place API"
  [2]: https://developers.google.com/places/web-service/search
  [3]: https://developers.google.com/places/web-service/details
  [4]: http://download.geonames.org/export/dump/DE.zip
  [5]: https://en.wikipedia.org/wiki/Stable_marriage_problem
