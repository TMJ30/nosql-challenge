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
  * `Latitude` and `Longtiude` → float
  * `RatingValue` → integer

## Exploratory Analysis
Used the cleaned MongoDB data to answer key editorial questions:
* **Hygiene Score of 20**
  * Counted establishments with hygiene score = 20
  * Displayed sample document
* **London Establishments with High Ratings**
  * Located establishments with `RatingValue >= 4` using `$regex` for London Local Authorities
* **Top Rated Establishments Near "Penang Flavours"**:
  * Found top 5 establishments with `RatingValue = 5`
  * Sorted by lowest hygiene score
  * Filtered within ±0.01 degrees latitude/longitude of the new restaurant
* **Hygiene Score of 0 by Local Authority:**
  * Aggregated number of establishments with hygiene score = 0 per Local Authority
  * Sorted results to identify top 10 areas
