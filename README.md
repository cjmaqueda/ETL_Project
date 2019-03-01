# ETL_Project
Data Sources
  Source #1 - CSV file from Argus with timeseries data on a specific tanker route (TD9)
  Source #2 – US Energy Information Administration (EIA) API 
Detailing the process of the extraction, transformation, and loading steps
  Source #1 - Used python and pandas to convert CSV file into data frame
  Source #2 
    Queried EIA API to retrieve: 1) monthly Brent crude price, 2) monthly Colombian landed Brent Crude price
    Created a column to calculate the difference between the two
    Combined the two sources, indexed on date, with a left join
Explication why you have performed the types of transformations you did
  I performed the transformations to create a list of timeseries data for potential relationship examination
Why you chose the type of the final database
  A relational database allows one to link information from different (future) tables through the use of foreign keys
Schema of the tables/collections in the final database
  `oil_db` > `brent_vs_landed`
Hypothetical use cases for your database
  Examination of how freight price fluctuation influences the overall cost of crude oil imports. Moreover, if the difference in cost         between landed bbls vs original purchase price is different than the freight cost, one may be able to identify other significant factors   impacting landed cost.


