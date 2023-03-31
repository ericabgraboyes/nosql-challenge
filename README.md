##### Source Code: The code in this repo uses the base starter code provided. The remaining part of the code reflects individual contributions

## Project Overview
The UK Food Standards Agency evaluates various establishments across the United Kingdom, and gives them a food hygiene rating. <br> <br>
The ask is to evaluate some of the rating data in order to help identify where to focus future articles <br>
<br> There are three parts of the project: <ol><li>Database and Jupyter Notebook Set Up <li> Update the Database <li> Exploratory Analysis </ol>
### Part One Database and Jupyter Notebook Set Up <br>
<ol>
  <li> From the terminal import the data provided in the establishments.json file
  <li> Copy the text used to import the file and display in a markdown file within the notebook<br>
  <li> Import both the PyMongo and Pretty Print libraries and create an instance of Mongo Client (mongo)
  <li> Confirm that the database is created and data loaded properly
  <ol> <li> List the databases in mongoDB. Confirm "uk_food" exists
       <li> List the collection(s) in the database, confirm that "establishments" exists
       <li> Find and display one document in the establishments collection. Display with pprint </ol>
  <li> Assign the database and collection to variables </ol>
    
### Part Two Update the Database
Before running any queries we need to make changes to the database per the requests below<br>
#### Requested Changes
<ol>
  <li> Add a new halal restaurant to the database, which just opened (the code to add has been copied to the jupyter notebook)
  <li> Find the BusinessTypeID for "Restaurant/Cafe/Canteen" and return only the BusinessTypeID and BusinessType fields
  <li> Update the new restaurant with the BusinessTypeID you found associated with #2
  <li> Query the database to determine how many documents contain "Dover" as the Local Authority. Remove all documents with Dover Local Authority from the database  
  <li> Update the datatype from string to decimal for latitude and longitude. Update using the update_many syntax </ol>
  
### Part Three Exploratory Analysis
The last aspect of the project was to conduct analysis on specific questions <br><br>
Items to note before conducting the analyis<br>
<ul><li> RatingValue refers to the overall rating decided by the Food Authority and ranges from 1-5. The higher the value, the better the rating
  <li> This field also includes non-numeric values such as 'Pass', where 'Pass' means that the establishment passed their inspection but isn't given a number rating.
  <li> The scores for Hygiene, Structural, and ConfidenceInManagement work in reverse. This means, the higher the value, the worse the establishment is in these areas.
  <li> Unless otherwise stated, for each question: 
    <ol><li> display number of documents using count_documents
      <li> Display the first document in the results using pprint
        <li> Convert the result to a Pandas DataFrame, print the number of rows in the DataFrame, and display the first 10 rows</ol></ul>

##### Analysis to Conduct
<ol>
  <li> Determine establishments with a hygiene score equal to 20
  <li> Determine which establishments in London have a RatingValue greater than or equal to 4
  <li> Determine the top 5 establishments with a RatingValue of '5', sorted by hygiene score (lowest to highest) that are closet to the new restaurant.  Search within 0.01 degree of the new restaurant added in Part 2  
  <li> Determine how many establishments in each Local Authority area have a hygiene score of 0. Sort from highest to lowest based on count of documents, and print the top 10 areas. </ol>
