# ada-2020-project-milestone-p3-p3_pia


**Title**<br>
---
**Analyzing plane travels and predicting people's home area based on their flight patterns**

**Abstract**<br>
---
The paper we worked on developed the process of building a model of human mobility. We propose to study other questions related to the same datasets. In particular, we would like to analyse the way people travel long distances and figure out whether we can characterize users' home areas by travel patterns. From the home location position derived from the paper, we can infer the country of residence of each user. Then we analyse checkins from a particular user over time and determine if checkins come from a long distance travel. Using a new added airport dataset, we can get better estimates of actual flown distances. This will allow us to understand trends of traveling per country by months. This can be used to predict user home areas based on their long-distance travels over time. Analysing human mobility patterns in 2010, could give insight about accessiblity to long distance travels across the globe.

**Research Questions**
---
We aim to:
- Find which countries travel the most.
- Detect patterns in global air traffic.
- Describe the network of airports.
- Find the most visited destinations by country.
- See if there is a conection between friends and visited countries.
- Check if it is possible to predict home areas based on travel patterns.

**Proposed dataset**<br>
---
- The datasets from [Gowalla](https://snap.stanford.edu/data/loc-Gowalla.html) and [Brightkite](https://snap.stanford.edu/data/loc-Brightkite.html) from the paper:
    - `loc-gowalla_totalCheckins.txt.gz`
    - `loc-brightkite_totalCheckins.txt.gz`
    - `loc-gowalla_edges.txt.gz`
    - `loc-brightkite_edges.txt.gz`
    
- A dataset with all airports worldwide. The dataset come from an [aviation website](https://ourairports.com/data/). We will use the `airports.csv` dataset which contains information about all airports, most importantly their position and the type of the airport. We will need this to better estimate the flown distances between airports. We can use this dataset to use only some airports (e.g large and medium and not small and private etc...). The dataset is a CSV file that can we can readily use and it contains the relevant features for our project.

- A dataset with all countries worldwide, `countries.csv`, which come from the same website as the one of the airports. We'll use it to get the full name of the countries given the its ISO code.

**Methods**<br>
---
We will reuse the methods from the paper to detect the homes for each user. The location of their home can be used to infer their country of residence. Once we have this information, we can go over the checkins by user sorted by time and detect when there is long-distance travel. For this we need to fix a threshold of minimum distance. This value would be used to detect when there is a big enough distance between two checkins, such that we can safely consider that the distance between the two checkins has been done by plane. After doing that we can have better estimates of the distance flown by using the airports dataset to find the closest airport to the last check-in before the travel and the first one after the travel. This should allow us to answer the first two and the fourth research questions. For the fifth one, we'll use the two friendships networks (datasets of edges) to what we'll add the countries by using the home of each user we already computed for milestone 2 as well as a method that will return the country based on some latitude and longitude coordinates. We can better analyse how the world is connected by studying the graph of the airports' network and answer the third question. For the last one, we could use different methods to predict user home areas based on travel patterns on a specific time frame. This is challenging because we may not have any differences between some countries or some countries may not have enough data, so it could be wiser to cluster into bigger groups such as continents. To do the predictions, we try different algorithms such as regressions, or a neural network.

**Proposed timeline / Organization within the team**<br>
---
Here is a timeline that will help us keep track of what have to be done and in how much time.<br>
<u>From 30/11 to 5/12:</u>
- Data Collection and preprocessing of the new dataset (airports): Maina
- Data Wrangling: Valentin & Maina
    - Modify datasets for visualization 
    - Analyse the airports' graph 
- Data Visualization - Checkins and homes: Alexander


<u>From 5/12 to 15/12:</u>
- Define the model for assigning a country to each home: Valentin
- Define a model to predict if a checkin represents a travel from home: Alexander
- Using airports to have a better precision: Alexander
- Define a model for assigning a country to each user of a friendship: Maina
- Data Visualization: 
    - plot the top ten visited countries:  Alexander
    - plot the top ten friendships between countries : Maina 
    - plot travel patterns over the world by months: Valentin
- Predictions using regression: Valentin 
- Predictions using a neural network: Alexander

<u>From 15/12 to 18/12:</u> (the three of us)
- Write the data story
- Submit the project
 
 **Repo structure**
 ---
 - extension_analysis.ipynb: Notebook with the extensive analysis
 - img/: folder with images representing plots runned on colab
 - `requirements.txt`: dependencies needed to run the notebook
 - data/: folder that needs to be created and where the data sets stated aboev need to be stored. It contains:
    - `loc-gowalla_totalCheckins.txt.gz`
    - `loc-brightkite_totalCheckins.txt.gz`
    - `loc-gowalla_edges.txt.gz`
    - `loc-brightkite_edges.txt.gz`
    - `countries.csv`
    - `airports.csv
