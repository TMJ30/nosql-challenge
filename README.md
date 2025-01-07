# nosql-challenge

**Instructions**

The UK Food Standards Agency evaluates various establishments across the United Kingdom, and gives them a food hygiene rating. You've been contracted by the editors of a food magazine, Eat Safe, Love, to evaluate some of the ratings data in order to help their journalists and food critics decide where to focus future articles.

**Part 1: Create Database in Jupyter Notebook**

**Part 2: Update the Database with the given information below**
        
        {
                "BusinessName":"Penang Flavours",
                "BusinessType":"Restaurant/Cafe/Canteen",
                "BusinessTypeID":"",
                "AddressLine1":"Penang Flavours",
                "AddressLine2":"146A Plumstead Rd",
                "AddressLine3":"London",
                "AddressLine4":"",
                "PostCode":"SE18 7DY",
                "Phone":"",
                "LocalAuthorityCode":"511",
                "LocalAuthorityName":"Greenwich",
                "LocalAuthorityWebSite":"http://www.royalgreenwich.gov.uk",
                "LocalAuthorityEmailAddress":"health@royalgreenwich.gov.uk",
                "scores":{
                    "Hygiene":"",
                    "Structural":"",
                    "ConfidenceInManagement":""
                },
                "SchemeType":"FHRS",
                "geocode":{
                    "longitude":"0.08384000",
                    "latitude":"51.49014200"
                },
                "RightToReply":"",
                "Distance":4623.9723280747176,
                "NewRatingPending":True
            }
**Part 3: Exploratory Analysis**

Eat Safe, Love has specific questions they want you to answer, which will help them find the locations they wish to visit and avoid.

        Which establishments have a hygiene score equal to 20?
        
        Which establishments in London have a RatingValue greater than or equal to 4?
        
        Hint: The London Local Authority has a longer name than "London" so you will need to use $regex as part of your search.
        
        What are the top 5 establishments with a RatingValue of 5, sorted by lowest hygiene score, nearest to the new restaurant added, "Penang Flavours"?
        
        Hint: You will need to compare the geocode to find the nearest locations. Search within 0.01 degree on either side of the latitude and longitude.

How many establishments in each Local Authority area have a hygiene score of 0? Sort the results from highest to lowest, and print out the top ten local authority areas.
