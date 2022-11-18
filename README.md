## Authors:
Isaac Battles, Gabriele Furlan, Nawar Allabban, Louis-Alexandre Leger

## Abstract:

Have you ever watched a movie because an actor was starring in it? Good actors lead to good movies. The star system has started in Hollywood in the 1920s with the goal of exploiting the image of actors to promote movies and generate publicity. The project aims at quantifying the impact of actors on the movie success and its variation along their career, through the definition of a 'star score' metric associated with profit and movie ratings. The success of the movie may not only rely on the experience of the actors and their score, but it may also depend on the gender distribution in the cast. The coupling of these factors can express the benefit of choosing one actor over another one, and which genre he/she is most suitable for. Through a regression model it will be possible to predict the success of a future movie depending on its actors. A further step will be to generate star scores for directors and writers and verify their influence on the movies' positive outcome.

## Research Questions:

- How much does the choice of actor impact movie success?
    - Is the 'star score' a significant metric to assess an actor influence of the success of a movie?
    - Are there any gender biases in the choice of actors?
    - How does the star score of an actor evolve over time?
    - What will be the success of future movies based on the selected actors?
    - Are there similarities between the actors' and directors' influence on movies?

## Additional Datasets:
1. [Inflation conversion factor dataset](https://liberalarts.oregonstate.edu/spp/polisci/faculty-staff/robert-sahr/inflation-conversion-factors-years-1774-estimated-2024-dollars-recent-years/individual-year-conversion-factor-table-0): dataset with the yearly inflation correction factor based on the average of inflation estimates by the Office of Management and Budget (OMB) and the Congressional Budget Office (CBO). This can be found in inflation_correction.csv;
2. [IMDb dataset](https://datasets.imdbws.com/): dataset with IMDb movie ratings as an additional metric for the measurement of movie success. We use:
    - 'title.basics.tsv' and 'title.ratings.tsv'to obtain the ratings and the number of votes for the movies;
3. [The Movies Dataset - Kaggle](https://www.kaggle.com/datasets/rounakbanik/the-movies-dataset): the dataset is used to import budgets for the movies. This allows us to take into account the profits instead of pure revenues for the evaluate the star score, cutting out a potential confounder. This can be found in kaggle_movies_metadata.csv in the data directory;

## Methods:

1. **Data pre-processing:**
The 'Data_Cleaning.ipynb' file is used to clean up and merge the data sets mentioned above into a single working dataframe for the analysis. This is particularly relevant due to the large amount of NaN values in the movie metadata and character metadata files of the CMU database, and to reduce the size of the massive IMDb database. The output CSV files 'profit_data.csv' and 'rating_no_budget_data.csv' differ by the movie budget column, which allows to profits. A sample of 'profit_data.csv' can be seen in the following table:
    
    'profit_data.csv'
||Actor_name|Actor_gender|Actor_date_of_birth|Movie_name|budget|Movie_release_date|Movie_box_office_revenue|averageRating|numVotes|
| --- | ----------- | ----------- |----------- |----------- |----------- |----------- |----------- |----------- |----------- |
|0|Wanda De Jesus|F|1958-08-26|Ghosts of Mars|28000000|2001-08-24|14010832.0|6.4|55259|
|1|Natasha Henstridge|F|1974-08-15|Ghosts of Mars|28000000|2001-08-24|14010832.0|6.4|55259|
|:|:|:|:|:|:|:|:|:|:|

2. **Preliminary analysis on the datasets:**
A preliminary analysis in the 'Data_Exploration.ipynb' file is done on single actors to look into the completeness of the dataset and to investigate the correlation between different parameters to assess the viability of the idea we had in mind. As an example, the revenues and experience (measured in terms of number of appearances) of Leonardo DiCaprio show a positive linear correlation:
<p align="center">
    <img width="380" alt="correlation" src="https://user-images.githubusercontent.com/114060781/202558137-0983da07-5662-44a3-ae2b-bacb93483c15.png">

3. **Definition of star score:**
The star score is built on revenues and IMDb scores of the actors. This is done by using the average logarithm of the revenues up to the actor's last appearance, and the average of the logarithm of the scores. This is done due to the heavy-tailed nature of both the revenues and the ratings. The IMDb scores are also normalized by the number of votes as that is an important potential confounder to take into account when using scores (done through a min-max scaling of the logarithm of the votes). Further detail on this star score can be found in the 'star_score.ipynb' file.
    
This is done on the all the actors remaining from the filtered datasets. An interesting finding shows that the star score follow a skew normal distribution, with parameters= TO BE ADDED as can be seen below:
 <p align="center">   
    <img width="431" alt="Capture" src="https://user-images.githubusercontent.com/114060536/202744875-e3de5fc9-cf41-4c24-a6fb-189c5ebf4777.PNG">
    
    This will in a similar manner be done to the directors as well.

4. **Utilizing the star score to assess the distribution over different actor experiences and genders:**
The star score distribution over different genre's can also be found as shown in the box plot below, showing that the gender of an actor could potentialy influence their impact on a movie even in modern times. Branching out from this point, one could look at the same statistic after discritizing the data into decades for example, to assess its evolution over time. 
    
5. **Prediction of future movies success based on regression model:**
Ultimately, once star scores are assigned to all actors (and similarly directors afterwards), a predictive model will be built around it based on the number of appearances of actors as well as their gender, and the potential genres they appeared in. Such a tool would be extremely powerful as it would give production companies an initial prediction on what actors and directors to go for based on how much impact the model outputs.

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
