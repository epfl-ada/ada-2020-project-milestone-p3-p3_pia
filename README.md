# ada-2020-project-milestone-p3-p3_pia


**1) Title**<br>
**Analyzing plane travels and predicting people's home area based on their flight patterns**

**2) Abstract**<br>
The paper we worked on developed the process of building a model of human mobility. We propose to study other questions related to the same datasets. In particular, we would like to analyse the way people travel long distances and figure out whether we can characterize continents of residence by travel patterns. From the home location position derived from the paper, we can infer the country of residence of each user. Then we analyze checkins from a particular user over time and determine if checkins come from a long distance travel. Using a new added airport dataset, we can get better estimates of actual flown distances. This will allow us to understand trends of traveling per country by months. This could be used to predict user home areas based on their long-distance travels over time. Analyzing human mobility patterns in 2010, could give insight about accessiblity to long distance travels across the globe.

**3) Research Questions**
   1. Which countries travel the most long distance by plane?
   2. Where do people from different countries travel to the most?
   3. Where users' friends are based?
   4. Check if it is possible to predict user home areas based on their travel patterns? 

**4) Proposed dataset**<br>
- The datasets from [Gowalla](https://snap.stanford.edu/data/loc-Gowalla.html) and [Brightkite](https://snap.stanford.edu/data/loc-Brightkite.html) from the paper:
    - `loc-gowalla_totalCheckins.txt.gz`
    - `loc-brightkite_totalCheckins.txt.gz`
    - `loc-gowalla_edges.txt.gz`
    - `loc-brightkite_edges.txt.gz`
    
- A dataset with all airports worldwide. The dataset come from an [aviation website](https://ourairports.com/data/). We will use the `airports.csv` dataset which contains information about all airports, most importantly their position and the type of the airport. We will need this to better estimate the flown distances between airports. We can use this dataset to use only some airports (e.g large and medium and not small and private etc...). The dataset is a CSV file that can we can readily use and it contains the relevant features for our project.

- A dataset with all countries worldwide, `countries.csv`, which come from the same website as the one of the airports. We'll use it to get the full name of the countries given the its ISO code.

**5) Methods**<br>
We will reuse the methods from the paper to detect the homes for each user. The location of their home can be used to infer their country of residence. Once we have this information, we can go over the checkins by user sorted by time and detect when there is long-distance travel. For this we need to fix a threshold of minimum distance. This value would be used to detect when there is a big enough distance between two checkins, such that we can safely consider that the distance between the two checkins has been done by plane. After doing that we can have better estimates of the distance flown by using the airports dataset to find the closest airport to the last check-in before the travel and the first one after the travel. This should allow us to answer the first two research questions. For the third one, we'll use the two friendships networks (datasets of edges) to what we'll add the countries by using the home of each user we already computed for milestone 2 as well as a method that will return the country based on some latitude and longitude coordinates. We can better analyse how the world is connected by studying the graph of the airports' network. For the last one, we could use different methods to predict user home areas based on travel patterns on a specific time frame. This is challenging because we may not have any differences between some countries or some countries may not have enough data, so it could be wiser to cluster into bigger groups such as continents. To do the predictions, we can apply different algorithms such as regressions, or a neural network.

**6) Proposed timeline / Organization within the team**<br>
Here is a timeline that will help us keep track of what have to be done and in how much time.<br>
From 30/11 to 5/12:
- Data Collection and preprocessing of the new dataset (airports): Maina
- Data Wrangling - Modify datasets for visualization : Valentin & Maina
                 - Analyse the airports' graph 
- Data Visualization - Checkins and homes: Alexander


From 5/12 to 15/12: 
- Define the model for assigning a country to each home: Valentin
- Define a model to predict if a checkin represents a travel from home: Alexander
- Using airports to have a better precision: Alexander
- Define a model for assigning a country to each user of a friendship: Maina
- Data Visualization: - plot the top ten visited countries:  Alexander
                      - plot the top ten friendships between countries : Maina 
                      - plot travel patterns over the world by months: Valentin
- Predictions using regression: Valentin 
- Predictions using a neural network: Alexander

From 15/12 to 18/12: (the three of us)
- Write the data story
- Submit

**7) Questions for TAs (optional)**<br>
What do you think about that idea of extending the use of the given datasets? <br>
How feasible it is for you?
  
