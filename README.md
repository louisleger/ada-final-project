## Authors:
Isaac Battles, Gabriele Furlan, Nawar Allabban, Louis-Alexandre Leger

## Abstract:

Have you ever watched a movie because an actor was starring in it? Good actors lead to good movies. The star system has started in Hollywood in the 1920s with the goal of exploiting the image of actors to promote movies and generate publicity. The project aims at quantifying the impact of actors on the movie success and how this varies along their career, through the definition of a 'star score' metric, associated with profit and movie ratings. The success of the movie may not only rely on the experience of the actors and their star score, but it may also depend on the gender distribution in the cast. The coupling of these factors can express the benefit of choosing one actor over another one, and which genre he/she is most suitable for. By conducting a regression analysis on the dataset, we will quantify the contribution of the different parameters and train a model to predict the success of a future movie depending on the actors starring in it. A further step will be to generate star scores for directors and writers and verify their influence on the movies' positive outcome.


This project revolves around using the MCU database, as well as supporting information from the IMDb database and Wikidata, for determining the impact of actors on the success of a movie. This will be done through the creation of an impact score metric that links the movie profit, ratings, and actor experience. This would essentially allow for the understanding of how the impact of actors evolves over time as they gain experience, or how impacts vary across different genders or movie genres. From there a predictive model could even be built to understand the weights behind the different factors constituting this metric. For that purpose, actor information as well as their movie revenues will be taken from the MCU database, whereas movie ratings will be obtained from the IMDb database, and movie budgets from Wikidata.

## Research Questions:

- How much does the choice of actor impact movie success?
i) Is the 'star score' a significant metric to assess an actor influence of the success of a movie?
- Are there any gender biases in the choice of actors?
- How does the star score of an actor evolve over time?
- What will be the success of future movies based on the selected actors?
- Are there similarities between the actors' and directors' influence on movies?

## Additional Datasets:


With regards to the additional data sets used, we firstly needed to utilize IMDb movie scores as an additional metric for the measurement of movie success. For that we used title.basics.tsv and title.ratings.tsv from https://datasets.imdbws.com/ to obtain the ratings and the number of votes for the movies. As we also wanted to find the budgets of the movies to complement and make more sense of the revenues, the data was obtained from https://www.wikidata.org/ was used. Wikidata was also used to identify the ethnicities of the actors in the MCU dataset due to the fact that they were linked to Freebase IDs and Freebase is no longer in service.

## Methods: 

1. 

2. 

## Proposed Timeline:

Week 9: Submission of milestone 2: End the preliminary analysis of the data along with tests of the methods mentioned above on a small sample from the databases.

Week 10: Expansion of the analysis to the complete dataset

## Organization Within the Team:
