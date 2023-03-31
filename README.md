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
    
### Part Two Update the Database <br>
Before running any queries we need to make changes to the database per the requests below<br>
#### Requested Changes
<ol>
  <li> Add a new halal restaurant to the database, which just opened (the code to add has been copied to the jupyter notebook)
  <li> Find the BusinessTypeID for "Restaurant/Cafe/Canteen" and return only the BusinessTypeID and BusinessType fields
  <li> Update the new restaurant with the BusinessTypeID you found
  <li> List or display both the database and the collection to confirm "uk_food" and "establishments" are present. Return 1 document
  <li> Assign the database and collection to variables <br>
