# ada-2020-project-milestone-p3-p3_pia


**1) Title**<br>
**Analyzing long distance plane travel geographically and seasonally**

**2) Abstract**<br>
The paper we worked on developed the process of building a model of human mobility dynamics. We propose to study other questions related to the same datasets. In particular, we would like to analyse the way people travel from their home and figuring out which countries see their population polluting the most by using planes (at least in 2010). To do so, we propose to add another dataset consisting of airport positions and from the home location found in the first replication, we can infer the nationality of each user. Then we analyze checkins from a particular user over time and determine if the checkin comes from a long distance travel, using the airport dataset. This will allow us to understand trends of traveling per nationality, in a world where means of traveling are becoming more accessible. Our analysis could be used to give personalized advices on which country should reduce travelling.

**3) Research Questions**<br>
A list of research questions you would like to address during the project.
   1. Which nationalities travel the most long distance by plane?
   2. Where do people from different countries travel to the most?
   3. Are there seasonal variations?
   3. Can we estimate the environmental effect? 

**4) Proposed dataset**<br>
List the dataset(s) you want to use, and some ideas on how you expect to get, manage, process, and enrich it/them. Show us that you've read the docs and some examples, and that you have a clear idea on what to expect. Discuss data size and format if relevant. It is your responsibility to check that what you propose is feasible given the datasets at hand.
- The datasets from [Gowalla](https://snap.stanford.edu/data/loc-Gowalla.html) and [Brightkite](https://snap.stanford.edu/data/loc-Brightkite.html) from the paper. We will use only the dataset with the checkins:
    - `loc-gowalla_totalCheckins.txt.gz`
    - `loc-brightkite_totalCheckins.txt.gz`
    
- A dataset with all airports worldwide. The dataset come from an [aviation website](https://ourairports.com/data/). We will use the `airports.csv` datset which contains information about all airports, most importantly their position and the type of the airport. We will need this to better estimate the flown distances between airports. We can use this datset to use only some airports (e.g large and medium and not small and private etc...). The dataset is a CSV file that can we can readily use and it contains the relevent features for our project.

**5) Methods**<br>
We will reuse the methods from the paper to detect the homes for each user. The location of their home can be used to infer their nationality. Once we have this information, we can go over the checkins by user sorted by time and detect when there is long-distance travel. For this we need to fix a threshold of minimum distance. This value would be used to detect when there is a big enough distance between two checkins, such that we can safely consider that the distance between the two checkins has been done by plane. After doing that we can have better estimates of the distance flown by using the airports dataset to find the closest airport to the last check-in before the travel and the first one after the travel. We can then analyze trends based on the nationality and season of travels.

**6) Proposed timeline**<br>
Here is a timeline that will help us keep track of what have to be done and in how much time.<br>
From 30/11 to 10/12:
- Data Collection and preprocessing of new datasets. : Qui fait ca

- Data Visualisation - Checkins and airports - Seasonal visualization?

- Data Wrangling - Modify datasets for visualization: Qui fait ca

From 10/12 to 17/12: 
- Define the model for assigning a country to each homes
- Define a model to predict if a checkin represents a travel from home

18/12:
- Submit the milestone

**7) Organization within the team**<br>
A list of internal milestones up until project milestone P4. Add here a sketch of your planning for the next project milestone.
  
**8) Questions for TAs (optional)**<br>
Add here any questions you have for us related to the proposed project. What do you think about that idea of extending the use of the given datasets? How feasible it is for you?
  
