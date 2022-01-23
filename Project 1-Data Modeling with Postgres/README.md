# Project 1 - Data Modeling with Postgres

## Project Introduction

#### Description
* Model user activity data (JSON) to create a database and ETL pipeline in Postgres for a music streaming app startup called Sparkify.
* Define Fact and Dimension tables for a STAR schema optimized for queries on song play analysis.  
* Insert data into new tables.

Sparkify's Analytics team will be able to query the newly designed relational database with ease to understand user behaviors such as what songs users are listening to.

#### Tools used
* PostgreSQL
* Python
* Jupyter Notebook


## Project Summary

### Project Structure 

```
|____data
| |____log_data                         # simulated app user activity logs
| |____song_data                        # metadata about a song and the artist of that song
|
|____notebook
| |____etl.ipnb                         # ETL processes to develop ETL builder 
| |____test.ipnb                        # to test ETL builder
|
|____script
| |____create_tables.py                 # script to create databases/tables
| |____etl.py                           # ETL builder
| |____sql_queries.py                   # DDL statements 
```

> ***NOTE:** You will not be able to run `test.ipynb`, `etl.ipynb`, or `etl.py` until you have run `create_tables.py` at least once to create the sparkifydb database, which these other files connect to.*




### Database Schema 

* #### Fact Table 


```
songplays 
          - songplay_id       PRIMARY KEY
          - start_time
          - user_id
          - level
          - song_id
          - artist_id
          - session_id
          - duration
          - user_agent
```

* #### Dimension Tables


```
users 
          - user_id           PRIMARY KEY
          - first_name
          - last_name
          - gender
          - level
```
```
songs 
          - song_id           PRIMARY KEY
          - title
          - artist_id
          - year
          - duration
```
```
artists 
          - artist_id         PRIMARY KEY
          - name
          - location
          - latitude
          - longitude
```
```
time 
          - start_time        PRIMARY KEY
          - hour
          - day
          - week
          - month
          - year
          - weekday
```
* #### Entity Relationship Diagram (ERD)

![](https://github.com/phphoebe/Udacity-Data-Engineering-Nanodegree/blob/master/Project%201-Data%20Modeling%20with%20Postgres/Sparkify%20ERD.png)
