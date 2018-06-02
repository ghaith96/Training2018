# Training Workshop 2018 

## Tawjihi
---
### Project Description

Tawjihi is a mobile application that can search tawjihi results with personalized statistics

### Step 1: Parsing
---
The first step is to find a data source, parse it and reformat as needed

Goals:
- getting familiar with a language
- getting familiar with IO
- string processing 
- getting familiar with hash tables
- getting familiar with data modeling

Todo: 
- download data set from [Github](https://github.com/Yousefjb/tawjihi-plain-data)
- convert xls files to csv files where needed
- read csv files with your language of choice

Notes:
- data set contains school, city, master, governorate and region names which used for aggregations
- data set for each year is not identical and sometimes separated across multiple files
- you are not required to write one parser for all data set files, you can write parser per file if needed
- this is a one time pass step and any hard coded / manual working is allowed
- one of the data set is missing names and can't be searched by name but still needed for statistics purpose 
- student name may include " char in their name and should be treated carefully



### Step 2: Database
---
Parsed result must be exported to a database

Goals:
- getting familiar with Db installation, connections and tools
- getting familiar with SQL aggregation functions 
- designing indices well suited for your queries
- getting familiar with full text search limitations

Todo:
- Create a new database of your choice [SQLite, MySQL, MSSQL, PostgreSQL or Oracle ] are allowed
- Create tables to hold your data
- You must create a table to hold each of school, city, master and governorate 
- Create indices and make sure they are used by the engine

Notes:
- this step is marked as step #2 but actually it can go along with step #1 where parsed data can be inserted immediately to database 
- SQLite database is preferred for portability


### Step 3: API
---
A public http api that will access database and provide statistics

Goals:
- how http server works
- how to handle get/post requests
- how to publish api behind a proxy
- hwo to host api for public

Todo: 
- The api can be written in your language of choice (JS, Java, C#, Go, Python ..)
- Search by full name
- Filter by year, school, city, master, governorate and region
- Order results
- Pagination
- Statistics endpoint which could serve a pre computed statistics or calculate them per request
- Statistics include but not limited to: 
    - Student count per year/city/school/master
    - Student score avg per year/city/school/master
    - Top all time schools by count/score
    - School count/score per year
- Statistics per student include but not limited to:
    - rank
    - rank /master /city /school
    - rank all time /school

Notes:
- more statistics could be added during the workshop 
- you can get creative with numbers and add your statistics

### Step 4: Mobile
---
Mobile application to present data provided by api

Goals: 
- how to make async network calls
- getting familiar with Drawer
- getting familiar with Toolbar
- getting familiar with Tabs
- getting familiar with Graphs
- getting familiar with Design Support Library
- getting familiar with Recyclerview
- getting familiar with Shared Preferences

Todo: 
- a suggested UI will be provided 
