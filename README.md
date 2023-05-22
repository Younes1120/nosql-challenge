### UK Food Standards Agency Database Analysis
This repository contains code and instructions to analyze the food hygiene ratings data from the UK Food Standards Agency. The analysis aims to help the editors of Eat Safe, Love magazine identify establishments to focus on for future articles. The analysis includes setting up the database, updating the data, and performing exploratory analysis.

# Prerequisites
Before running the analysis, ensure that you have the following software installed:

* Python 3
* Jupyter Notebook
* MongoDB
* PyMongo

 ## Part 1: Database and Jupyter Notebook Set Up
* Start by importing the data provided in the establishments.json file into the MongoDB database.

* Open the terminal and navigate to the directory where the establishments.json file is located.
* Use the following command to import the data into the MongoDB database:
css
Copy code
mongoimport --db uk_food --collection establishments --file establishments.json
Note: Replace <path_to_file> with the actual file path.
Open the Jupyter Notebook and import the necessary libraries: PyMongo and Pretty Print (pprint).

* Create an instance of the Mongo Client in your Jupyter Notebook.

* Confirm that the database and data are loaded properly:

* List the databases using the following code:
python
Copy code
client.list_database_names()
* Confirm that uk_food is listed.
* List the collections in the uk_food database using the following code:
python
Copy code
db.list_collection_names()
Confirm that establishments is listed.
Find and display one document in the establishments collection using find_one and display with pprint.
Assign the establishments collection to a variable to prepare the collection for use.
## Part 2: Update the Database
* Add a new restaurant, "Penang Flavours," to the database with the given information. The restaurant has not been rated yet.

* Use the insert_one method to add the document to the establishments collection.
Find the BusinessTypeID for "Restaurant/Cafe/Canteen" and return only the BusinessTypeID and BusinessType fields.

* Use the find_one method with a query for the given BusinessType.
Update the new restaurant document with the BusinessTypeID found.

* Use the update_one method with a query for the new restaurant's name and an update to set the BusinessTypeID field.
Check the number of documents that contain the Dover Local Authority.

* Use the count_documents method with a query for the Dover Local Authority.
Remove any establishments within the Dover Local Authority from the database.

* Use the delete_many method with a query for the Dover Local Authority to remove the documents.
Convert specific fields to their appropriate data types:

* Use the update_many method to convert latitude and longitude to decimal numbers.
* Use the update_many method to convert RatingValue to integer numbers.
## Part 3: Exploratory Analysis
Answer the following questions and present the results:

* Which establishments have a hygiene score equal to 20?
* Which establishments in London have a RatingValue greater than or equal to 4?
* What are the top 5 establishments with a RatingValue of 5, sorted by the lowest hygiene score, nearest to the new restaurant added, "Penang Flavours"?
* How many establishments in each Local Authority area have a hygiene score of 0? Sort the results from highest to lowest and print out the top ten local authority areas.
* For each question:

* Use count_documents to display the number of documents contained in the result.
* Display the first document in the results using pprint.
* Convert the result to a Pandas DataFrame, print the number of rows in the DataFrame, and display the first 10 rows.
## Conclusion
This analysis provides insights into the food hygiene ratings data from the UK Food Standards Agency. The results can be used by Eat Safe, Love magazine to focus their future articles on specific establishments. For more details, refer to the Jupyter Notebook file.

