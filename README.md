## Authors:
Isaac Battles, Gabriele Furlan, Nawar Allabban, Louis-Alexandre Leger

## Abstract:

The star system has started in Hollywood in the 1920s with the goal of exploiting the image of actors to promote movies and generate publicity. The project aims at quantifying the impact of actors on movie success and how this varies along their career, through the definition of a 'star score' metric, associated with revenue and movie ratings. The success of movies may not only rely on the experience of actors and their star score, as it may also depend on the gender distribution in the cast. The coupling of these factors can express the benefit of choosing one actor over another one. By conducting a regression analysis on the dataset, we will quantify the contribution of different parameters and train a model to predict the success of a future movie depending on the actors starring in it. This would also be done in a similar manner to directors. 


Have you ever watched a movie because an actor was starring in it? Good actors lead to good movies. The star system has started in Hollywood in the 1920s with the goal of exploiting the image of actors to promote movies and generate publicity. The project aims at quantifying the impact of actors on the movie success and its variation along their career, through the definition of a 'star score' metric associated with profit and movie ratings. The success of the movie may not only rely on the experience of the actors and their score, but it may also depend on the gender distribution in the cast. The coupling of these factors can express the benefit of choosing one actor over another one, and which genre he/she is most suitable for. Through a regression model it will be possible to predict the success of a future movie depending on its actors. A further step will be to generate star scores for directors and writers and verify their influence on the movies' positive outcome.

## Research Questions:

- How much does the choice of actor impact movie success?
    - Is the 'star score' a significant metric to assess an actor influence of the success of a movie?
    - Are there any gender biases in the choice of actors?
    - How does the star score of an actor evolve over time?
    - What will be the success of future movies based on the selected actors?
    - Are there similarities between the actors' and directors' influence on movies?

## Additional Datasets:
1. [Inflation conversion factor dataset](https://liberalarts.oregonstate.edu/spp/polisci/faculty-staff/robert-sahr/inflation-conversion-factors-years-1774-estimated-2024-dollars-recent-years/individual-year-conversion-factor-table-0): dataset with the yearly inflation correction factor based on the average of inflation estimates by the Office of Management and Budget (OMB) and the Congressional Budget Office (CBO);
2. [IMDb dataset](https://datasets.imdbws.com/): dataset with IMDb movie ratings as an additional metric for the measurement of movie success. We use:
    - 'title.basics.tsv' and 'title.ratings.tsv'to obtain the ratings and the number of votes for the movies;
3. [Wikidata dataset](https://www.wikidata.org/): as we are also including the budgets of the movies to complement and make more sense of the revenues, the Wikidata dataset is used with the queries being carried out using SPARQL, the results of the query can be found in the Wikidata_query.json file.
4. [The Movies Dataset - Kaggle](https://www.kaggle.com/datasets/rounakbanik/the-movies-dataset): the dataset is used to import budgets for the movies. This allows to take into account the profits instead of the pure revenues for the evaluation of the star score.

## Methods:
1. **Data pre-processing**
    - The Data_Cleaning.ipynb file is used to clean up and merge the data sets mentioned above into a single working dataframe for the analysis. This is particularly relevant due to the large amount of NaN values for relevant variables in the movie metadata and character metadata files of the CMU database, and to reduce the size of the massive IMDb database. The output CSV file contains all the relevant information needed as can be seen in the following table:
2. **Preliminary analysis on the datasets**
    - A preliminary analysis is done on single actors to look into the viability and the completeness of the dataset for the purpose we intended to see and to investigate the correlation between different parameters.
<p align="center">
    <img width="380" alt="correlation" src="https://user-images.githubusercontent.com/114060781/202558137-0983da07-5662-44a3-ae2b-bacb93483c15.png">

    
3. **Definition of star score**
    - The star score will be built on revenues and IMDb scores of the actors. This will be done through using the average logarithm of the profits (Revenue-budget)SHOULD WE MAYBE USE RELATIVE PROFIT (rEVENUE-bUDGET)/BUDGET up to the actor's last appearance, and the average of the logarithm of the scores. This is done due to the heavy-tailed nature of both the revenues and the ratings. The IMDb scores are also normalized by the number of votes as that is an important potential confounder to take into account when using scores (This is done through a min-max scaling of the logarithem of the votes). This will in a similar manner be done to the directors as well.
4. **Utilizing the star score to assess the distribution over different actor experiences and genders**
 
5. **Prediction of future movies success based on regression model**
    - Once star scores are assigned to all actors (and similarly directors afterwards), a predictive model will be built around it based on the number of appearances of actors as well as their gender
8. **Investigation of movies success dependence on directors and writers and comparison with actors**.
    - Once the analysis is complete on actors, this can be done in a similar manner with directors, allowing for a more
## Proposed Timeline:

Week 9: Submission of milestone 2, and finishing the preliminary analysis of the data along with tests of the methods mentioned above on a small sample from the databases.

Week 10: Expansion of the analysis to the complete dataset of actors

Week 11: Building a predictive model involving actor gender and number of appearances

Week 12: Starting a draft of the data story, and the begining of the development of the web interface

Week 13: Applying prior assesment to directors, and completing the data story

Week 14: Submission of milestone 3

## Organization Within the Team:

Writing the text of the datastory

Formulation and Refinement of the Star Score

Building the website

Training and tuning the predictive model

Further dataset exploration

| Team Member | Task |
| --- | ----------- |
| Gabriele Furlan | Text |
| Isaac Battles | Text |
| Louise | Text |
| Nawar Allabban | Text |
