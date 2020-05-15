# Bing search dataset for Coronavirus Intent  

## Data Source  
This dataset was curated from the Bing search logs (desktop users only) over the period of Jan 1st, 2020 – (Current Month - 1). Only searches that were issued many times by multiple users were included. The dataset includes queries from all over the world that had an intent related to the Coronavirus or Covid-19. In some cases this intent is explicit in the query itself (e.g., “Coronavirus updates Seattle”), in other cases it is implicit , e.g. “Shelter in place”. The implicit intent of search queries (e.g., “Toilet paper”) was extracted using random walks on the click graph as outlined in [this paper](https://www.microsoft.com/en-us/research/wp-content/uploads/2007/07/craswellszummer-random-walks-sigir07.pdf) by Microsoft Research. All personal data were removed.


## Contact Us
BingCoronaVirusTeam@microsoft.com


## Schema Description  

Inside the data folder there is a folder 2020 (for the year) which contains two kinds of files. 

* QueriesByCountry_DateRange.tsv : A tab separated text file that contains queries with Coronavirus intent by Country.   
* QueriesByState_DateRange.tsv	: A tab separated text file that contains queries with Coronavirus intent by State. 


### QueriesByCountry  

**Date** : string, Date on which the query was issued.  

**Query** : string, The actual search query issued by user(s).  

**IsImplicitIntent** : bool, True if query did not mention covid or coronavirus or sarsncov2 (e.g, “Shelter in place”). False otherwise.  

**Country** : string, Country from where the query was issued.  

**PopularityScore** : int, Value between 1 and 100 inclusive. 1 indicates least popular query on the day/Country with Coronavirus intent, and 100 indicates the most popular query for the same Country on the same day.  


### QueriesByState  

**Date** : string, Date on which the query was issued.  

**Query** : string, The actual search query issued by user(s).  

**IsImplicitIntent** : bool, True if query did not mention covid or coronavirus or sarsncov2 (e.g, “Shelter in place”). False otherwise.

**State** : string, State from where the query was issued. 

**Country** :string, Country from where the query was issued.  

**PopularityScore** : int, Value between 1 and 100 inclusive. 1 indicates least popular query on the day/State/Country with Coronavirus intent, and 100 indicates the most popular query for the same geogrpahy on the same day.  


## Data Update Frequency  
New data will be added once a month until coronavirus is no longer in the news.


## Terms of Use:  

Please see the LICENSE file for more details. If you choose to use the data, please attribute it to Microsoft as follows: "Data Source: Bing Coronavirus Query set (https://github.com/microsoft/BingCoronavirusQuerySet)".


## Contributing:  

This project is not open for contributions.  
This project has adopted the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/).
For more information see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/) or
contact [opencode@microsoft.com](mailto:opencode@microsoft.com) with any additional questions or comments.
