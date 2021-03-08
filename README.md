# Data Engineering project 2 - Data Modelling with Cassandra

By Alessio Rea

==============================

You need to have Python 3.6.3 installed for this project

# General explanation

## 1. Purpose of the project

The purpose of the project is to build analyze data collecting on songs and user activity on a music streaming app. The analysis should enable stakeholders to understand what songs users are listening to. Currently, there is no easy way to query the data to generate the results, since the data reside in a directory of CSV files on user activity on the app.

The data engineer's job is to create an Apache Cassandra database which can create queries on song play data to answer the questions. 

The databes will be tested by running queries provided by the analytics team to create the results.


## 2. Database schema design and ETL pipeline

In this project, we will be working with one dataset: event_data. The directory of CSV files partitioned by date. Here are examples of filepaths to two files in the dataset:

```
event_data/2018-11-08-events.csv
event_data/2018-11-09-events.csv
```




Here is how the data is modelled according to a star schema :

- Fact table : table songplays containing the following features : songplay_id, start_time, user_id, level, song_id, artist_id, session_id, location, user_agent

- Dimension tables : 

    - users - users in the app. Features : user_id, first_name, last_name, gender, level
    - songs - songs in music database. Features : song_id, title, artist_id, year, duration
    - artists - artists in music database. Features : artist_id, name, location, latitude, longitude
    - time - timestamps of records in songplays broken down into specific units. Features : start_time, hour, day, week, month, year, weekday


## 3. Example queries and results for song play analysis

Once the data has been ETLed, you are free to take full benefit from the power of star modelling and make business driven queries like :

    - Which song has been played by user 'Lily' on a paid level?
    - When did user 'Lily' play song from artist 'Elena'?



# Project Organization 
----------------------

    ├── README.md                   <- The top-level README for users and developers using this project.
    ├── Project_Template.ipynb      <- Python script allowing to create database, create / drop tables with appropriate schema



# Getting started

## 1. Clone this repository

```
$ git clone <this_project>
$ cd <this_project>
```

## 2. Install requirements

```
$ pip install -r requirements.txt
```
--------

