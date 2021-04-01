# Project: Data Modeling with Postgres

A startup named Sparkify wants to analyze user activities using their song and user data. 
The data given is in JSON files. Because of the complexity, we decided to create an ETL Pipeline and load user and song data to a Postgres database. 
We decided to run with a star schema for simplicity.

## Datasets

The data is currently already collected for song and user activities, in the following directories:
`data/log_data` and `data/song_data`, using JSON files.

![](sparkify_erd.png?raw=true)


# Fact Table

songplays - records in log data associated with song plays i.e. records with page NextSong
songplay_id, start_time, user_id, level, song_id, artist_id, session_id, location, user_agent


# Dimension Tables

users - users in the app
user_id, first_name, last_name, gender, level
songs - songs in music database
song_id, title, artist_id, year, duration
artists - artists in music database
artist_id, name, location, latitude, longitude
time - timestamps of records in songplays broken down into specific units
start_time, hour, day, week, month, year, weekday