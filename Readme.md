#### Capstone Project : Immigration analysis using data lakes 

#### Outline:  

##### Introduction

In this project, A data lake will be prepared for immigration analysis and functionalities. Immigration is an ongoing daily activity, hence data is always increasing. The reason behind choosing a data lake was that they can be accessed and updated easily. 
<br>
The Project will prepare the data model & data lake for Immigration analytics. The notebook ***Capstone Project.ipynb*** details all the steps of importing and exploring data , data cleaning/wrangling, data lake preparation and writing parquet files and data quality checks. The notebook also includes various example queries run using parquet files which include reading parquet, creating views and running SQL's to extract data from views. 



##### Scripts and files included

There are 2 main scripts

- common_functions.py = reusable code that carries out different operations on data e.g. data cleaning, data loading, data writing and data quality checks.
- etl.py = This script provides the etl pipeline. It uses the functions in common_functions.py script and runs them step by step to complete the pipeline. various variables are also used to control where data is read from and where its written. 

Capstone Project.ipynb = notebook with execution, output and details of each step within the etl.py and common_functions.py. Also included are the actual analytic sample queries executed on data lake by loading data from parquet files for executing SQL queries.



##### Usage 

- execute script via **python etl.py create** to create the initial data lake
- execute script via **python etl.py update** to update data into the existing parquet files. Currently only update for immigration data is built. 



##### Data-Lake Architecture

The data lakes are built upon dimensional and fact tables which are then used by business applications. These are stored as Parquet files into local directory. To ensure that queries are run with optimum performance, the data lakes are partitioned. The exact partitioning and distribution for each table is defined in step 3 of the notebook. 



##### Example queries included  

Below we present a few examples of analytical queries and their results for immigration data analysis.

- Which where the top 5 busiest ports in month 04 / 2016  
  - Which months have the highest immigration inflow.
  - Which US Port/States have the highest number of immigrants, what is their visa type (i.e. Student, Business, Pleasure)
  - Which airline has the maximum number of passengers
  - Which residence country has the highest number of students


