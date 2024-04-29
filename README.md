# Crowdfunding_ETL_Mini_Project_KarunaKKothandath_BrentBeachtel

The entire project is divided into 4 sub parts:

* Create the Category and Subcategory DataFrames.
* Create the Campaign DataFrame.
* Create the Contacts DataFrame.
* Create the Crowdfunding Database.

## Create the Category and Subcategory DataFrames.

* First read the provided data 'crowdfunding.xlsx' into a Pandas DataFrame as 'crowdfunding_info_df'.
* Checked the data types of the columns using '.info()'.
* Retrieved all columns of the dataframe using '.columns'.
* Splited the 'category & sub-category' column into two seperate columns as 'category' and 'subcategory'.
* Retreived all unique values in the newly created columns using 'unique()'.
* Created numpy arrays from 1-9 for the categories and 1-24 for the subcategories.
* Used a list comprehension to add "cat" to each category_id and "subcat" to each subcategory_id. 
* Created a category DataFrame with the category_id,subcategory_id array as the category_id,subcategory_id and categories list,subcategories list as the category name  and subcategory name.
* Exported categories_df and subcategories_df as CSV files.

## Create the Campaign DataFrame.

* Created a copy of the crowdfunding_info_df DataFrame as campaign_df.
* Renamed the blurb, launched_at, and deadline columns as 'description','launched_date' and 'end_date'.
* Converted the goal and pledged columns to a `float` data type.
* Formated the launched_date and end_date columns to datetime format using 'pd.to_datetime'.
* Merged the campaign_df with the category_df on the "category" column and the subcategory_df on the "subcategory" column.
* Dropped 'staff_pick','spotlight','category & sub-category','category','subcategory' columns.
* Exported the DataFrame as a CSV file.


## Create the Contacts DataFrame.
* Read the provided 'contacts.xlsx'data into a Pandas DataFrame with `header=3` as 'contact_info_df'.
* Iterated through the 'contact_info_d'f and converted each row to a dictionary with the help of 'json'.
* Created a 'contact_info' dataFrame and added  'contact_id', 'name', 'email' columns and checked the datatypes of the columns.
* Splited the 'name' column into 'first_name' and 'last_name'.
* Re-ordered the columns and exported as a CSV file.

##  Create the Crowdfunding Database.
* In this part inspected the four CSV files created in the above part, and then sketched an ERD of the tables by using QuickDBD.
* Using the information from the ERD, created a table schema for each CSV file.
* Saved the database schema as a Postgres file named 'crowdfunding_db_schema.sql'.
* Created a new Postgres database, named 'crowdfunding_db'.
* Using the database schema, created the tables and imported each CSV file into its corresponding SQL table.
* Verified each table has the correct data by running a 'SELECT' statement.
* The same Contacts DataFrame is created using 'regex'. 



