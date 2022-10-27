# Section 4 Story Cards and Tasks

## Create a new database
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

## Use Lucid Chart to Draw a database diagram
1. Create a free Lucid Chart Account
1. Run the Lucid Chart ERD query against your database
1. Import your database schema to Lucid Chart
1. Connect the tables
1. Export your ERD as a PDF and sumbit it as your assignment

## Create mapping tables to describe your data
1. Some of our data is represented with ids only. Let's create mapping tables to translate the ids to labels.
1. There will be a task here for each table - TBD

## Export cleaned data to csv for use in a reporting tool.
1. Describe what fact you have learned that you find most interesting
1. Translate your finding into a SQL select statment that creates a table you can use to build a report
1. Export your data as a csv file
1. Re-import your file to a new table to test for any issues that may make your new dataset difficult to work with. 