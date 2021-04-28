# ETL_MOVIES

To Run this project, just run the file "ETL_MOVIES-Final.ipynb"

This project takes data from three different sources to compile a database of top movies over the years in the US.

First, the top movies are taken from WIKI. The webscraping method was used to read the table of movie info. Rank, Movie Name, Director, Year, and Studio 

Second, what the movie is rated and the plot was extracted by using the OMDb API.

Third, the revenue of the movie was extracted from a CSV file (movies_metadata.csv) which was found from Kaggle. 

After the data was extracted, the data was cleaned and put into three different dataframes. The DFs were then merged into one and then pushed into MongoDb. 
