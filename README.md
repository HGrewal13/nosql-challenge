# nosql-challenge - UK Food Standards Agency Analysis for the magazine <i>Eat Safe, Love</i>

Description
-----------
The UK Food Standards Agency evaluates various establishments across the United Kingdom, and gives them a food hygiene rating. You've been contracted by the editors of a food magazine, <i>Eat Safe, Love</i>, to evaluate some of the ratings data in order to help their journalists and food critics decide where to focus future articles.

Perform data cleaning, reading, updating and deleting (CRUD) using MongoDB to analyze the data provided in the establishments.json file. Then provide analysis findings to help <i>Eat Safe, Love</i> gain a better understanding of the listed UK restaurants and their hygiene standards.

Technologies Used
------------------
- MongoDB
- Pandas
- PyMongo
- pprint
- Jupyter Notebook

Part 1: Database and Jupyter Notebook Set Up
--------------------------------------------
1. import data from establishments.json by typing the following command in the command prompt:
  ``` mongoimport --type json -d uk_foods -c establishments --drop --jsonArray establishments.json ```

2. import the following libraries:
- pyMongo
- pprint

3. create an instance of the Mongo Client

4. confirm the following:
- database ```uk_food``` was created
- collection ```establishments``` was created
- find and pprint function were able to locate a document within the ```establishments``` collection

Part 2: Update the Database
---------------------------
1. Inserted new entry to the collection: A new halal restaurant named <strong>Penang Flavours</strong> (Details found in <a href="https://github.com/HGrewal13/nosql-challenge/blob/main/Final_Code/NoSQL_analysis_starter.ipynb">NoSQL Analysis Starter</a>)

2. Found the BusinessTypeID for all BusinessType of "Restaurant/Cafe/Canteen"

3. Updated Penang Flavours' BusinessTypeID to match "Restaurant/Cafe/Canteen" restaurants

4. Found and deleted 994 documents which were establishments located in Dover (undesirable field for the magazine)

5. Performed data cleaning to update the latitude, longitude, and rating values which were stored as strings and converted them to decimals

Part 3: Exploratory Analysis
----------------------------
1. Which establishments have a hygiene score equal to 20?
Ans: 41 establishments
   
2. Which establishments in London have a RatingValue greater than or equal to 4?
Ans: 33 establishments

3. What are the top 5 establishments with a RatingValue of 5, sorted by lowest hygiene score, nearest to the new restaurant added, "Penang Flavours"?
Ans:
- BusinessName: Volunteer
- BusinessName: Plumstead Manor Nursery
- BusinessName: Lumbini Grocery Ltd T/A Al-Iman
- BusinessName: Iceland
- BusinessName: Howe and Co Fish and Chips - Van 17

4. How many establishments in each Local Authority area have a hygiene score of 0? Sort the results from highest to lowest, and print out the top ten local authority areas.
Ans: 55 establishments


<strong>Note: Please refer to <a href="https://github.com/HGrewal13/nosql-challenge/blob/main/Final_Code/NoSQL_analysis_starter.ipynb">NoSQL Analysis Starter</a> for detailed dataframes that include the businesses and comprehensive data, along with the work performed to answer these questions. These were not included in this portion to avoid clutter in the readme.</strong>