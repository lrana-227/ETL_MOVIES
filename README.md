# ETL_MOVIES

To Run this project, just run the file "ETL_MOVIES-Final.ipynb"

This project takes data from three different sources to compile a database of top movies over the years in the US.

## Extract

First, the top movies are taken from WIKI. The webscraping method was used to read the table of movie info. Rank, Movie Name, Director, Year, and Studio 

Second, what the movie is rated and the plot was extracted by using the OMDb API.

Third, the revenue of the movie was extracted from a CSV file (movies_metadata.csv) which was found from Kaggle. 

## Transform
WEBSCRAPING--> Columns which were not needed were moved, the column names chnaged so it could merge later, and the index was set to the Rank. Rank was also made into a string since the key cannot be an integer. 

OMDb API-->  A list was created from the Webscraping of the top movies and a for loop with a try catch was created. This way through API requests, the rating and plot could be collects, while disregarding any movies that weren't available. The column names were also renamed to help with merging. 

CSV--> The cvs files were read in and all the columns not needed were removed. The columns were also cleaned and renamed to help with merging.

All the dataframes were from the three sources were finally merged on Movie titles, finally into one Dataframe. Any title with no values, or duplicates were removed. 


## Load
After the data was cleaned,were pushed into MongoDb with the name movie_data2. 
