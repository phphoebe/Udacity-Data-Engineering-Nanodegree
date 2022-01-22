# Project 1 - Data Modeling with Postgres

## Project Introduction

#### Course Learning Outcomes
* Understand when to use a relational database
* Understand the difference between OLAP and OLTP databases
* Create normalized data tables
* Implement denormalized schemas (e.g. STAR, Snowflake)

#### Project Description: Data Modeling with Postgres
* Model user activity data to create a database and ETL pipeline in Postgres for a music streaming app called Sparkify.
* Define Fact and Dimension tables for a STAR schema optimized for queries on song play analysis.  
* Insert data into new tables.

Sparkify's Analytics team will be able to query the newly designed relational database with ease to understand user behaviors such as what songs users are listening to.

#### Tools used
* PostgreSQL
* Python
* Jupyter Notebook


## Project Summary

### Repository Structure 

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
