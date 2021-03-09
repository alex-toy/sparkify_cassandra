# Data Engineering project 2 - Data Modelling with Cassandra

By Alessio Rea

==============================

You need to have Python 3.6.3 installed for this project

# General explanation

## 1. Principle of Cassandra

When you design a Cassandra based data model, you need to take into account the following principles :

- In Cassandra, there is no JOIN, which means that you need to denormalize your tables thereby creating redundancy
- Cassandra is fast-write
- When designing your model, you need to take into account the most common queries you will be performing on your database and create a table specifically to satisfy that query.

## 2. Purpose of the project

The purpose of the project is to build analyze data collecting on songs and user activity on a music streaming app. The analysis should enable stakeholders to understand what songs users are listening to. Currently, there is no easy way to query the data to generate the results, since the data reside in a directory of CSV files on user activity on the app.

The data engineer's job is to create an Apache Cassandra database which can create queries on song play data to answer the questions. 

The database will be tested by running queries provided by the analytics team to create the results.



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

