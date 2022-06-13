# Movies-ETL
## Overview
### Purpose
Clean and parse the extracted data with the ETL function.  Merge data sets and upload them into PostGreSQL. 

## Process 
### ETL_function_test
ETL function has to read the files from Kaggle metadata, MovieLens ratings CSV, and Wikipedia movie json as a Pandas DF. Created 3 variables to equal the file names.

  - Checking the wiki-movies dataframe. 
  - ![Check the wiki-movies DF](https://user-images.githubusercontent.com/101272613/173411886-c35be98c-7c91-452e-978b-472ae985549c.PNG)
  - Checking the kaggle dataframe. 
  - ![Check Kaggle DF](https://user-images.githubusercontent.com/101272613/173411955-79e64cec-cd30-4e64-8e46-8659a12ab174.PNG)
  - Checking the Ratings DF. 
  - ![Check the Ratings DF](https://user-images.githubusercontent.com/101272613/173415314-c18e0210-b10c-42a0-8999-fbcb74a8726e.PNG)

### ETL_clean_wiki_movies
Created the function to clean the movie list.  
Read the files from Kaggle metadata, MovieLens ratings CSV, and Wikipedia movie json as a Pandas DF.
Removed the null values from "Box office" column.  Cleaned the box office, budget column, release date, and running time column to set a standard format.  
Created 3 variables to equal the file names. 

  - Checking the wiki-movies dataframe after cleaning
![wiki movies DF](https://user-images.githubusercontent.com/101272613/173415552-b312cdf6-492e-4d02-bd78-559f1c49c67e.PNG)
  - Checking the wiki-movies dataframe count
![wiki movies count](https://user-images.githubusercontent.com/101272613/173417413-534ffe0b-46d2-4763-8772-5be3ea8deb88.PNG)

### ETL_clean_kaggle_data
Created variables to clean the Kaggle metadata.
Merging two data frames into the movies DF, dropped unnecessary columns from the merged DF, and fill in missing data by def function. 
Created 3 variables to equal the file names.

  - Checking the merged data count. 
![movies df count](https://user-images.githubusercontent.com/101272613/173417490-94765e24-3e1c-4183-a6e1-e277687e49ca.PNG)
  - Checking the merged data with ratings count.
![movies with ratings df count](https://user-images.githubusercontent.com/101272613/173417596-a7e6aba6-d3e0-46e4-b51c-6484e7eacc3d.PNG)

### ETL_clean_database
Using sqlachemy and psycopg2 to import the revised and cleaned data sets to the database.  

  - Loading the data to PostgreSQL
![PostgresSQL](https://user-images.githubusercontent.com/101272613/173417892-57176e9a-301b-4b64-a60b-89b36141349d.PNG)


## Results
### PostgreSQL
Using pgAdmin 4 to verify the correct count for both tables (movies, ratings).  
![movies in SQL](https://user-images.githubusercontent.com/101272613/173418806-7d079393-bf1f-45ab-8bd3-b0c78fe56051.PNG)
![ratings in SQL](https://user-images.githubusercontent.com/101272613/173418822-335953b9-be71-46bd-961c-13a87cb1af9a.PNG)



