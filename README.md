# UK Food Hygiene Analysis
## Overview
This project analyzes UK food hygiene data from the Food Standards Agency to help the magazine _Eat Safe, Love_ identify establishments that warrant coverage in their articles.

The project involves three key stages:
1. Setting up a MongoDB database and importing data
2. Updating and cleaning the database
3. Performing exploratory analysis to answer specific questions about food establishments

## Database Setup
* Imported `establishments.json` into MongoDB
* Created database `uk_food` and collection `establishments`
* Connected to MongoDB using PyMongo
* Verified data import:
  * Listed databases and collections
  * Viewed a sample document using `find_one()` and `pprint`
 
## Database Updates
* Added a new halal restaurant in Greenwich (`Penang Flavors`)
* Updated the restaurant with the correct `BusinessTypeID`
* Removed all establishments in Dover Local Authority
* Converted numeric fields stored as strings to proper data types
  * `Latitude` and `Longtiude` -> float
