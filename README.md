# NoSQL Challenge 

Part 1: Setting up the Database

Import Data**: Import the data provided in the `establishments.json` file from your Terminal. Name the database `uk_food` and the collection `establishments`. Copy the text you used to import your data from your Terminal to a markdown cell in your notebook.

2. **Import Libraries**: Within your notebook, import the libraries you need: PyMongo and Pretty Print (pprint).

3. **Create Mongo Client**: Create an instance of the Mongo Client.

4. **Confirm Database Setup**:
   - List the databases you have in MongoDB. Confirm that `uk_food` is listed.
   - List the collection(s) in the database to ensure that `establishments` is there.
   - Find and display one document in the `establishments` collection using `find_one` and display with `pprint`.
   - Assign the `establishments` collection to a variable to prepare the collection for use.

## Part 2: Updating the Database

5. **Add New Restaurant**: The magazine wants you to include a new halal restaurant in Greenwich, which hasn't been rated yet. Add the provided information to the database.

6. **Find BusinessTypeID**: Find the `BusinessTypeID` for "Restaurant/Cafe/Canteen" and return only the `BusinessTypeID` and `BusinessType` fields.

7. **Update New Restaurant**: Update the new restaurant with the `BusinessTypeID` you found.

8. **Remove Dover Establishments**: The magazine is not interested in any establishments in Dover. Check how many documents contain the Dover Local Authority, remove them from the database, and check the number of documents to ensure they were deleted.

9. **Data Type Conversion**: Some number values are stored as strings when they should be stored as numbers. Use `update_many` to convert latitude and longitude to decimal numbers. Use `update_many` to convert `RatingValue` to integer numbers.

## Part 3: Exploratory Analysis

10. **Explore Dataset**: Use the provided notebook `NoSQL_analysis_starter.ipynb` for this section. Here are the specific questions to answer:

   - **Question 1**: Which establishments have a hygiene score equal to 20?
   - **Question 2**: Which establishments in London have a `RatingValue` greater than or equal to 4? (Hint: Use `$regex` for London)
   - **Question 3**: What are the top 5 establishments with a `RatingValue` of 5, sorted by the lowest hygiene score, nearest to the new restaurant "Penang Flavours"?
   - **Question 4**: How many establishments in each Local Authority area have a hygiene score of 0? Sort the results from highest to lowest and print out the top ten local authority areas.

