## Authors:
Isaac Battles, Gabriele Furlan, Nawar Allabban, Louis-Alexandre Leger

## Abstract:

Have you ever watched a movie because an actor was starring in it? Good actors lead to good movies. The star system has started in Hollywood in the 1920s with the goal of exploiting the image of actors to promote movies and generate publicity. The project aims at quantifying the impact of actors on the movie success and how this varies along their career, through the definition of a 'star score' metric, associated with profit and movie ratings. The success of the movie may not only rely on the experience of the actors and their star score, but it may also depend on the gender distribution in the cast. The coupling of these factors can express the benefit of choosing one actor over another one, and which genre he/she is most suitable for. By conducting a regression analysis on the dataset, we will quantify the contribution of the different parameters and train a model to predict the success of a future movie depending on the actors starring in it. A further step will be to generate star scores for directors and writers and verify their influence on the movies' positive outcome.


This project revolves around using the MCU database, as well as supporting information from the IMDb database and Wikidata, for determining the impact of actors on the success of a movie. This will be done through the creation of an impact score metric that links the movie profit, ratings, and actor experience. This would essentially allow for the understanding of how the impact of actors evolves over time as they gain experience, or how impacts vary across different genders or movie genres. From there a predictive model could even be built to understand the weights behind the different factors constituting this metric. For that purpose, actor information as well as their movie revenues will be taken from the MCU database, whereas movie ratings will be obtained from the IMDb database, and movie budgets from Wikidata.

## Research Questions:

- How much does the choice of actor impact movie success?
    - Is the 'star score' a significant metric to assess an actor influence of the success of a movie?
    - Are there any gender biases in the choice of actors?
    - How does the star score of an actor evolve over time?
    - What will be the success of future movies based on the selected actors?
    - Are there similarities between the actors' and directors' influence on movies?

## Additional Datasets:

- Inflation conversion factor dataset (https://liberalarts.oregonstate.edu/spp/polisci/faculty-staff/robert-sahr/inflation-conversion-factors-years-1774-estimated-2024-dollars-recent-years/individual-year-conversion-factor-table-0);
- IMDb dataset (https://datasets.imdbws.com/);
- Wikidata dataset (https://www.wikidata.org/);

With regards to the additional data sets used, we include a dataset with the yearly inflation correction factor based on the average of inflation estimates by the Office of Management and Budget (OMB) and the Congressional Budget Office (CBO). Then, we utilize IMDb movie ratings as an additional metric for the measurement of movie success. For that we use 'title.basics.tsv' and 'title.ratings.tsv'to obtain the ratings and the number of votes for the movies. As we are also including the budgets of the movies to complement and make more sense of the revenues, the Wikidata dataset is used.

## Methods: 

1. 

2. 

## Proposed Timeline:

Week 9: Submission of milestone 2: End the preliminary analysis of the data along with tests of the methods mentioned above on a small sample from the databases.

Week 10: Expansion of the analysis to the complete dataset

## Organization Within the Team:
