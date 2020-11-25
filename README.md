# ada-2020-project-milestone-p3-p3_pia

Should contains:

1) Title: Some ideas:  
    - Who's the worst?  
    - Polution and mobility  

2) Abstract: A 150 word description of the project idea, goals, datasets used. What's the motivation behind your project? How do you propose to extend the analysis from the paper? What story would you like to tell, and why? 
  - project idea: analyse the long distance/plane mobility per country, understand their trends of traveling 
  - goals: Find which nationality polute the most
  - datasets used: loc-gowalla_totalCheckins.txt.gz and loc-brightkite_totalCheckins.txt.gz
  - motivation: could use our analyse to give personalize advices on who should reduce travelling depending of the country
  - how do we want to extend? Not our case
  - story: ?

3) Research Questions: A list of research questions you would like to address during the project.
Which nationalities travel the most(number of large travel)? the furthest? Where, like the first 3 countries (depending on the season/month)? How much (mean) g/CO2 per nationality? Could use <=500km for cars and >500 for plane..should we add the trains? J'sais pas si ca revient a faire pleins de calcul un peu chiant pour rien de rajouter l'analyse de quantité moyenne de CO2

4) Proposed dataset: List the dataset(s) you want to use, and some ideas on how you expect to get, manage, process, and enrich it/them. Show us that you've read the docs and some examples, and that you have a clear idea on what to expect. Discuss data size and format if relevant. It is your responsibility to check that what you propose is feasible given the datasets at hand.
- The datasets from [Gowalla](https://snap.stanford.edu/data/loc-Gowalla.html) and [Brightkite](https://snap.stanford.edu/data/loc-Brightkite.html) from the paper. We will use only the dataset with the checkins.
- A dataset with all airports worldwide. The dataset come from an [aviation website](https://ourairports.com/data/). We will use the `airports.csv` datset which contains information about all airports, most importantly their position and the type of the airport. We will need this to better estimate the flown distances between airports. We can use this datset to use only some airports (e.g large and medium and not small and private etc...). The dataset is a CSV file that can we can readily use and it contains the relevent features for our project.

5) Methods:

6) Proposed timeline:
  P3: 27/11: ne pas oublier le form;
  Timeline:
    avoir fini sa figure 3B?
    avoir fini le notebook?
    avoir fini la data story?
    avoir updaté le replication report?;
  P4: 18/12: data story, notebook & updates replication report;
  P5: 23/12: No poster but video of presentation?;

7) Organization within the team: A list of internal milestones up until project milestone P4. Add here a sketch of your planning for the next project milestone.
  
8) Questions for TAs (optional): Add here any questions you have for us related to the proposed project.
  
