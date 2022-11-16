## Authors:
Isaac Battles, Gabriele Furlan, Nawar Allabban, Louis-Alexandre Leger

## Abstract:
Have you ever watched a movie because an actor was starring in it? Good actors lead to good movies. The star system has started in Hollywood in the 1920s with the goal of exploiting the image of actors to promote movies and generate publicity. The project aims at quantifying the impact of actors on the movie success and how this varies along their career, through the definition of a 'star score' metric, associated with profit and movie ratings. The success of the movie may not only rely on the experience of the actors and their star score, but it may also depend on the gender distribution in the cast. The coupling of these factors can express the benefit of choosing one actor over another one, and which genre he/she is most suitable for. By conducting a regression analysis on the dataset, we will quantify the contribution of the different parameters and train a model to predict the success of a future movie depending on the actors starring in it. A further step will be to generate star scores for directors and writers and verify their influence on the movies' positive outcome.

## Research Questions:

- How much does the choice of actor impact movie success?
    - Is the 'star score' a significant metric to assess an actor influence of the success of a movie?
    - Are there any gender biases in the choice of actors?
    - How does the star score of an actor evolve over time?
    - What will be the success of future movies based on the selected actors?
    - Are there similarities between the actors' and directors' influence on movies?

## Additional Datasets:
- [Inflation conversion factor dataset](https://liberalarts.oregonstate.edu/spp/polisci/faculty-staff/robert-sahr/inflation-conversion-factors-years-1774-estimated-2024-dollars-recent-years/individual-year-conversion-factor-table-0): dataset with the yearly inflation correction factor based on the average of inflation estimates by the Office of Management and Budget (OMB) and the Congressional Budget Office (CBO);
- [IMDb dataset](https://datasets.imdbws.com/): dataset with IMDb movie ratings as an additional metric for the measurement of movie success. We use:
    - 'title.basics.tsv' and 'title.ratings.tsv'to obtain the ratings and the number of votes for the movies;
- [Wikidata dataset](https://www.wikidata.org/): as we are also including the budgets of the movies to complement and make more sense of the revenues, the Wikidata dataset is used.

## Methods:
1. Data pre-processing;
2. Preliminary analysis on the datasets;
3. Definition of star score;
4. Investigation of movies success dependence on actors trough regression analysis;
5. Prediction of future movies success based on regression model;
6. Investigation of movies success dependence on directors and writers and comparison with actors.

## Proposed Timeline:

Week 9: Submission of milestone 2: End the preliminary analysis of the data along with tests of the methods mentioned above on a small sample from the databases.

Week 10: Expansion of the analysis to the complete dataset

## Organization Within the Team:
