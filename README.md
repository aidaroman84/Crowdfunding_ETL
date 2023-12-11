# Crowdfunding ETL 

## Team Pretzels
- Magdalena Olczak

- Aida Roman

## Purpose
The purpose of this ETL (Extract, Transform, Load) mini project is to build an ETL pipeline that processes crowdfunding campaign data. We used Python, Pandas, and data transformation techniques to extract data from Excel files, perform necessary transformations, create CSV files, design a relational database schema, and load the data into a Postgres database.

## Tools Used

- __Python and Pandas:__ Python programming language is used along with Pandas library to manipulate and transform the data extracted from Excel files.

- __Jupyter Notebook:__ Used a Jupyter Notebook to execute code, visualize data, and create structured documentation.

- __Postgres Database:__ We created a Postgres database to store the cleaned and transformed data.


## Steps

### Data Extraction and Transformation
The ETL process has multiple steps of data extraction and transformation:

#### Category and Subcategory DataFrames
- We extracted data from the "crowdfunding.xlsx" Excel file to create a category DataFrame.
- The category DataFrame contained category IDs and titles.
- We performed similar extraction and transformation to create a subcategory DataFrame.
- The subcategory DataFrame contained subcategory IDs and titles.
- Both DataFrames were exported to "category.csv" and "subcategory.csv" respectively.

#### Campaign DataFrame
- We extracted campaign data from the "crowdfunding.xlsx" Excel file.
- The campaign DataFrame underwent various transformations, including data type conversions and renaming of columns.
- UTC times were converted to datetime format for "launch_date" and "end_date".
- Category and subcategory IDs were added to link with the respective DataFrames.
- The transformed campaign DataFrame was exported to "campaign.csv".

#### Contacts DataFrame
- We used two methods to extract and transform data from the "contacts.xlsx" Excel file: Python dictionary methods and regular expressions.
- For both methods, we extracted contact IDs, names, and email addresses.
- In the dictionary method, we iterated through the DataFrame and created dictionaries for each row.
- In the regular expressions method, we used regex patterns to extract specific information.
- The transformed contacts DataFrame was exported to "contacts.csv".

### Database Schema and Loading
- We sketched an Entity-Relationship Diagram (ERD) based on the extracted and transformed data.
- Using the ERD, we designed a table schema for each CSV file, specifying data types, primary keys, and foreign keys.
- The table schema was saved in "crowdfunding_db_schema.sql".
- We created a Postgres database named "crowdfunding_db".
- Tables were created in the correct order, considering foreign keys.
- CSV files were imported into corresponding SQL tables.
- The loaded data was verified using SELECT statements.

## Conclusion
This ETL mini project involved extracting, transforming, and loading data from Excel files into a Postgres database. Using Python and Pandas we processed crowdfunding campaign data and designed a relational database schema. This project demonstrates the application of ETL processes in real-world data manipulation and storage scenarios.
