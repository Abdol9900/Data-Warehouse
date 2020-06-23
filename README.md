# Data Warehouse


### This is the third project for the Udacity Data Engineering Nanodegree Program and is undertaken to assess the knowledge of data warehousing concepts. Some of the tasks involved in the project include facilitating Sparkify startup, which helps create a data warehouse useful for storing the data of songs and from which users can listen. The process allows Sparkify to analyze the activities of the user. In this project, amazon s3 is used to store files while Amazon Redshift is used for data warehouse purposes and database storage. The project is written in python. 


## Source Data

### Source data is found in both the log data and songs data. The log data are contained in the Amazon s3 bucket file found at s3://udacity-dend/log_data and contains user’s song play history in json format. Songs data includes lists of songs and details and is given in Amazon s3 bucket accessible through the path s3://udacity-dend/song_data. 

# Data Schema

### The fact and dimension table for this project are presented below. 

#### Dimension Tables:
##### •	users
##### •	columns: user_id, first_name, last_name, gender, level
##### •	songs
##### •	columns: song_id, title, artist_id, year, duration
##### •	artists
##### •	columns: artist_id, name, location, lattitude, longitude
##### •	time
##### •	columns: start_time, hour, day, week, month, year, weekday

#### Fact Table:

##### •	songplays
##### •	columns: songplay_id, start_time, user_id, level, song_id, artist_id, session_id, location, user_agent

## To run the project:

#### The following steps are followed to run the project: 
##### •	Run the command to install the requirements pip install.
##### •	Use Amazon Redshift cluster credentials and the IAM role to update the dwh.cfg file. 
##### •	Run python create_tables.py. to create the database and other tables needed. 
##### •	Run python etl.py. to start the pipeline that reads data from files and populate the tables. 
