## Authors:
Isaac Battles, Gabriele Furlan, Nawar Allabban, Louis-Alexandre Leger

## Project Description:

This project revolves around using the MCU database, as well as supporting information from the IMDb database and Wikidata, for determining the impact of actors on the success of a movie. This will be done through the creation of an impact score metric that links the movie profit, ratings, and actor experience. This would essentially allow for the understanding of how the impact of actors evolves over time as they gain experience, or how impacts vary across different genders or movie genres. From there a predictive model could even be built to understand the weights behind the different factors constituting this metric. For that purpose, actor information as well as their movie revenues will be taken from the MCU database, whereas movie ratings will be obtained from the IMDb database, and movie budgets from Wikidata.

## Research Questions:

- How much does the choice of actor impact movie success?
- What metric can be used to quantitavily assess how much an actor influenced the success of a movie?
- Is there an asymmetry in the degree of impact male and female actors have?
- How are the impact scores distrbuted over different ethnicities?
- How does the impact score of an actor evolve over time

## Additional Datasets:


With regards to the additional data sets used, we firstly needed to utilize IMDb movie scores as an additional metric for the measurement of movie success. For that we used title.basics.tsv and title.ratings.tsv from https://datasets.imdbws.com/ to obtain the ratings and the number of votes for the movies. As we also wanted to find the budgets of the movies to complement and make more sense of the revenues, the data was obtained from https://www.wikidata.org/ was used. Wikidata was also used to identify the ethnicities of the actors in the MCU dataset due to the fact that they were linked to Freebase IDs and Freebase is no longer in service.

## Methods: 

1. 

2. 

## Proposed Timeline:

Week 9: Submission of milestone 2: End the preliminary analysis of the data along with tests of the methods mentioned above on a small sample from the databases.

Week 10: Expansion of the analysis to the complete dataset

## Organization Within the Team:
