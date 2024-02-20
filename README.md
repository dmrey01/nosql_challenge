# nosql_challenge
Module 12 Challenge 

Part 1  Database and Jupyter Notebook Set Up
    Import the data provided in the establishments.json file from your Terminal. Name the database uk_food and the collection establishments.
    Import the dataset with `mongoimport --type json -d uk_food -c establishments --drop --jsonArray establishments.json'
  Started with the imports : pymongo and pprint. 
     Created instance of Mongo client then confimed the data bases worked.  Then we reviewed the collections  called establishments 
  
  Part 2: Update the Database
    An exciting new halal restaurant just opened in Greenwich, but hasn't been rated yet. The magazine has asked you to include it in your analysis. Add the following restaurant "Penang Flavours" to the database.

    Created a dictionary for the new restaurant data. Penang Flavours, by inserting the Business Name, then Business Type. 


The magazine is not interested in any establishments in Dover, so check how many documents contain the Dover Local Authority. Then, remove any establishments within the Dover Local Authority from the database, and check the number of documents to ensure they were deleted.
    Found  994 documents with 'Dover'
    then deleted all the docuements.  
    This one i had issues with, as I had to restart the Kernals when I re-ran everything it kept telling me that I had zero docuement found.  
      This is when I discovered that something possibly happen to my notebook.  So I started it again and by deleting the notebook and restarting.  It worked and the problem corrected itself , along with reloading the Json file .  (which I did try first).

    # Change the data type from String to Decimal for longitude and latitude
      This section I had issues with and had to call for help to the TA.  something in the code was not transfering the longitue andlatitude over to strings.  After TA looked at code there was a small typo that we both found. 

      finished out the setup for the started code. 

    Eat Safe, Love
Notebook Set Up
    imported the dependencies of pymongo, pprint and pandas 
     Created instance of Mongo client then confimed the data bases worked.  Then we reviewed the collections  called establishments 

  Part 3: Exploratory Analysis

Which establishments have a hygiene score equal to 20?
    query for the scores.Hygiene :20 
    found 41 docuements with a Hygiene score of 20 and pprinted the first docuement. 

Created a Pandas DF called hygiene_df  and printed out the DF .  

2. Which establishments in London have a RatingValue greater than or equal to 4?
    query the LocalAuthority Name using the $regex command. 
    this one was a little more tricky as the outline just called the Local Authority but the proper name was Local Authority Name. 
    Once results were found convereted into pandas DF. 

    What are the top 5 establishments with a RatingValue rating value of 5, sorted by lowest hygiene score, nearest to the new restaurant added, "Penang Flavours"?

    again had to call the TA for help as there were a couple coding issues with my set up. The TA was very helpful and again steered me on the right path. 
    finshed this section and put into a pandas DF
        DF would only do 1 row.  tried several times to fix and gave up.  


    4. How many establishments in each Local Authority area have a hygiene score of 0?
establishements
# Create a pipeline that: 

Used the match, group, sort and pipeline methods here then printed out the results.  Results again put into Pandas DF. 

