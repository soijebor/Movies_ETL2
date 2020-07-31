# Movies_ETL

## Project Overview
* Create an ETL pipeline from raw data to a SQL database.
* Extract data from disparate sources using Python.
* Clean and transform data using Pandas.
* Use regular expressions to parse data and to transform text into numbers.
* Load data with PostgreSQL.


## Resources
* Data Source: wikipedia-movies.json, movies_metadata.csv, ratings.csv
* Software: Python 3.7.6, Anaconda 4.8.3, Jupyter Notebook 6.0.3, PostgreSQL 11.8 (pgAdmin 4.23)

## Challenge Overview
* Create a function that takes in three arguments:
  * Wikipedia data
  * Kaggle metadata
  * MovieLens rating data (from Kaggle)
* Use the code from your Jupyter Notebook so that the function performs all of the transformation steps. Remove any exploratory data analysis and redundant code.
* Add the load steps from the Jupyter Notebook to the function. You’ll need to remove the existing data from SQL, but keep the empty tables.
* Check that the function works correctly on the current Wikipedia and Kaggle data.
* Document any assumptions that are being made. Use try-except blocks to account for unforeseen problems that may arise with new data.


## Assumptions
* There is a lot of assumptions made because the challenge file is missing a lot of the explanatory data that you will need to easily understand the code.
* Majority of budget entries are entered as one of the following formats
  * $123.4 million/billion
  * $123,456,789
* Runtime does not include seconds. It only includes hours, hour & minutes, or minutes.
* We dropped the Wikipedia data because Wikipedia data is missing release dates for 11 movies, but the Kaggle data isn’t missing any release dates.
* It is legitimate to replace NaN with zero's to better utilize dataset.
* We decided to drop the Wikipedia data because the Kaggle data is much more consistent, and it would be difficult, to translate the Wikipedia data into the same format.
