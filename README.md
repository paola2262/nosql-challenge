# Challenge - Module 12 - nosql-challenge
### Student Paola Moreno

![images.jpeg](images.jpeg)

## NoSQL_setup_starter.ipynb

### Data Import

Initially, I imported the data stored in establishments.json using my Terminal. The database was named "uk_food", and the collection was named "establishments".

mongoimport --type json -d uk_food -c establishments --drop --jsonArray establishments.json

* Imported the necessary libraries and modules, such as pymongo for interacting with MongoDB and pprint for pretty printing.
* Created an instance of MongoClient to connect to your MongoDB database running on port 27017.
* Verified that the new database uk_food was created by listing the available databases.
* Reviewed the collections in the newly created database to ensure it was successfully set up.
* Used the find_one() method to retrieve and display a document from the establishments collection to examine its structure.
* Created a dictionary containing the data for a new restaurant named "Penang Flavours".
* Inserted the new restaurant data into the establishments collection using the insert_one() method.
* Confirmed that the new restaurant data was successfully inserted by querying the database again and checking for the presence of the new document.
* Retrieved the BusinessTypeID for "Restaurant/Cafe/Canteen" using a query, and then updated the new restaurant document with this BusinessTypeID using the $set operator in an update operation.
* Verified that the new restaurant document was updated correctly by querying the database and checking its contents.


## NoSQL_analysis_starter.ipynb

* Identified establishments with a hygiene score of 20 by using the count_documents method to find the count of establishments with this specific score. It then displays the first document in the
  results using pprint for further examination.
* Converted the result into a Pandas DataFrame, printing out the number of rows in the DataFrame and displaying the first 10 rows. Utilized $regex to search for establishments within London.
  Similarly, count_documents is employed to determine the count of establishments meeting the criteria. The first document in the results is displayed using pprint, and the result is converted to a
  Pandas DataFrame, showcasing the number of rows and displaying the first 10 rows.
* Identified the top 5 establishments with a RatingValue of 5. The notebook searches for establishments with this specific rating, sorting the results by hygiene score in ascending order.
  It then narrows down the search to establishments within a certain distance of the coordinates of "Penang Flavours." Similar to previous steps, it displays the first document using pprint,
  converts the result to a Pandas DataFrame, and showcases the number of rows along with the first 10 rows.
* Employed groupby to count the number of establishments in each area with a hygiene score of 0. The results are sorted from highest to lowest, and the top ten Local Authority areas with the
  highest count are printed out.


