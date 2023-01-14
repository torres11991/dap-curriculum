# Sprint Planning Points

## Create a new SQL database

1. Using the tool of your choice create a new sqlite database

## Import data from csv files

1. Pull the sample data from the repo
1. Copy the files to the directory where your
1. Import the following tables:
    1. plan information sample.txt
    1. beneficiary cost file sample.txt
    1. basic drugs formulary file.txt
    1. product package ndc.csv
    1. plan information zip.csv

## Use SQL to create key column and map relationships

1. Our sample data uses a three column primary key let's simplify that by creating a new primary key in the plan information table.
1. The plan information table can be normalized
    1. Write a select statement for each part of the table that represents a normalized recordset
    1. Use your select statements to populate two new tables
1. Translate the three part key to the new id column for:
    1. beneficiary cost
