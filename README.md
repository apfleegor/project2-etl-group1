# Project-2-etl-group-1

## Background

For this project, we were tasked with looking at 2 data sources and performing the ETL processes on them. In the below sections, we explain how we extracted our data, made necessary transformations to them, and loaded it into a databases.


## Extract

First, we explored kaggle.com to find an interesting data sources to work with. We found data sources that look at gun violence data and automobile data.

### Sources of Data:

* Complete vehicle technical database:  https://www.car-engineer.com/complete-vehicle-technical-database/ 
    
* United States Gun Violence Data 2014-2022: https://www.kaggle.com/datasets/jasonmobley/united-states-gun-violence-data-20142022? resource=download



## Transform

* Both of our data sources were formatted in excel files and we loaded them into our Jupyter Notebooks and used Pandas to turn them into csv files.

* For each source, selected variables of interest for the analysis and renamed the columns to make them compatible with Postgres.

* We used Python functions to clean and group relevant data.

* We dropped some extra columns that we deemed unusable for future analysis because the dataframe contained NaN values and did not provide       valuable information. 

* All of our data were in a CSV format, so we went with SQL to store the data.


## Load


* After we were satisfied with our cleaned data transformations, we used the following procedure to load our dataframes into our relational Postgres Databases:

    * We created a python file to hold our passwords. Using the password file, we created an engine to connect to our Postgres database and confirmed a successful connection by checking for existing tables.


    * We then added each of our transformed dataframes to Postgres. To validate the data was inserted correctly, we ran simple SQL queries.


## Findings 

* Car Queries:
    * Maxiumum Average Fuel Consumption
        * Top car overall: Volkswagon Toureg with _ mpg
        * 2WD: Renault Grand Espace with 12.2 mpg
    * 
    
* Gun Violence Queries: 
    * Number of incidents by city
        * Philadelphia has the 2nd most incidents in the US
    * 20 most dealy gun incidents of 2022
        * Not surprisingly, Uvalde with 22 confirmed deaths
