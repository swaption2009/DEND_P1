# DEND Project 1

## Purpose

A startup called Sparkify wants to analyze the data they've been collecting on songs and user activity on their new music streaming app. The analytics team is particularly interested in understanding what songs users are listening to.

This data engineer project will create a Postgres database with tables designed to optimize queries on song play analysis. The tasks are twofold, ie. to create a database schema and ETL pipeline for this analysis. Final task is to test the database and ETL pipeline by running queries.

## Database Schema

#### Fact Table
`songplays`: records in log data associated with song plays i.e. records with page NextSong
* fields: `songplay_id`, `start_time`, `user_id`, `level`, `song_id`, `artist_id`, `session_id`, `location`, `user_agent`

####Dimension Tables
1. `users`: users in the app
   * fields: `user_id`, `first_name`, `last_name`, `gender`, `level`
2. `songs`: songs in music database
   * fields: `song_id`, `title`, `artist_id`, `year`, `duration`
3. `artists`: artists in music database
   * `artist_id`, `name`, `location`, `latitude`, `longitude`
4. `time`: timestamps of records in songplays broken down into specific units
   * fields: `start_time`, `hour`, `day`, `week`, `month`, `year`, `weekday`