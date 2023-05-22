# Eat Safe, Love
This repository contains scripts and data files for analyzing food establishments in the UK. The data is stored in a NoSQL database, and the analysis is performed using Python and Pandas.

## Set Up Database
* To set up the database, the NoSQL_setup.ipynb notebook provides instructions on importing the data and performing initial setup. The data from the establishments.json file is imported into the uk_food database and the establishments collection using the mongoimport command.

The notebook also includes instructions for updating the database. 
    
* Update the new restauarant with the correct BusineesTypeID. 

    
* Drop all establishments that has Dover as their Local Authority from the database. 

    
* Convert latitude and longitude to decimal numbers.

    
## Exploratory Analysis
* The NoSQL_analysis.ipynb notebook focuses on performing exploratory analysis on the data using Pandas DataFrames. Here are some of the analyses conducted:

Identifying establishments with a hygiene score equal to 20:
There are 41 establishments with a hygiene score of 20 in the uk_food dataset.

Finding establishments in London with a RatingValue greater than or equal to 4:
There are 34 establishments in London that have a RatingValue greater than or equal to 4.

Listing the top 5 establishments with a RatingValue rating of '5', sorted by lowest hygiene score and nearest to the new restaurant added, "Penang Flavours":
The top 5 establishments with a RatingValue of '5' sorted by lowest hygiene score and nearest to "Penang Flavours" are: "Volunteer", "Plumstead Manor Nursery", "Atlantic Fish Bar", "Iceland", and "Howe and Co Fish and Chips - Van 17".

Counting the number of establishments in each Local Authority area that have a hygiene score of 0:
There are 55 rows in the DataFrame with the count of establishments. The first 10 rows are as follows:

    | _id | count |
    |-----|-------|
    |Thanet|1130|
    |Greenwich|882|
    |Maidstone|713|
    |Newham|711|
    |Swale|686|
    |Chelmsford|680|
    |Medway|672|
    |Bexley|607|
    |Southend-On-Sea|586|
    |Tendring|542|

