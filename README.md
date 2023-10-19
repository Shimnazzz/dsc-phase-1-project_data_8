# Phase 1 Project
Welcome to the Project Repository of Shimnaz Fathima! You will find a brief overview of the project, the findings and the recommendations derived after the completion of this project here. Please feel free to browse through the files to know more about the analysis done in this project.

![Title Picture](https://github.com/Shimnazzz/dsc-phase-1-project_data_8/assets/147800579/5cc5a12e-0043-4773-b67c-65ed34cbbbbe)


### Project Overview

This project involves using various avaiable movie related databases to perform data analysis and derive meaningful insights and recommendations for Microsoft for their new venture to create a new movie studio.

### Business Problem

Microsoft as a new entrant in the movie production space, requires expert recommendation in this area. This project looks into catering to this problem and doing analysis of the different movie related attributes and develop findings related to these. These findings will be converted into actionable insights that the head of Microsoft's new movie studio can use to help decide what type of films to create.

### The Data

In the folder `zippedData` are movie datasets from:

* [Box Office Mojo](https://www.boxofficemojo.com/)
* [IMDB](https://www.imdb.com/)
* [Rotten Tomatoes](https://www.rottentomatoes.com/)
* [TheMovieDB](https://www.themoviedb.org/)
* [The Numbers](https://www.the-numbers.com/)

This project will be looking into the following datasets from the above listed ones:

* imdb.title.basics
* imdb.title.ratings
* imdb.title.principals
* mdb.name.basics
* bom.movie_gross

### Methodology

The above mentioned datasets were used in the analysis done in Jupyter notebook. The datsets were used to understand any correlation between movie related parameters and also to find the best available solutions to create the movie with for Microsoft.

* Firstly, using the datsets, imdb.title.ratings and imdb.title.basics, the attributes of runtime of movies (in minutes) and number of votes by audience were analysed using a scatter plot. The resulting scattter plot was similiar to a normal distrubution. In order to further understand the relationship between movie runtime and movie ratings, a categorised data involving both the parameters were created. This means the movie runtime was distributed into bins of 10 minute intervals and the mean of the votes received for movies with runtime in that particular bin was found out. 

  After this the 25th percentile, 50th percentile and the 75th percentile of the audience votes was found out by considering the cumilative sum of the audience ratings. These percentiles were obtained from the following formula:

  Xth percentile of the data= X/100 × Sum of the average ratings

  After obtaining the 25th percentile, 50th percentile and 75th percentile of the audience votes, it was compared with the cumilative audience votes and the corresponding movie runtime was found out.

* Secondly, from the datsets, bom.movie_gross and imdb.title.ratings, the attributes of movie studio and movie ratings were obtained respectively. In order to merge the two datasets, a thrid dataset, imdb.title.basics had to be used. This is because bom.movie_gross had the title of the movie in the dataset however imdb.title.ratings showed the ratings and number of votes for each IMDB movie ID. In order to find the corresponding movie title from the movie ID, this third dataset was used which had both IMDB movie ID and movie title. 

  Once the datasets were merged the top 10 studios based on the average rating of all their movies were found.

* Thirdly, from the datasets, bom.movie_gross and tn.movie_budgets, the worldwide gross, domestic gross and foreign gross were obtained. These were merged based on the movie titles. From imdb.name.basics and imdb.title.principals, the actors who played in the movies were obtained. After making necessary adjustments, the above mentioned datasets were merged.

  Further to this, the top 10 actors were found based on the highest average worldwide gross for the movies and also in order to recommend actors that were appealing to the domestic audience, the top 10 actors based on the highest domestic gross for their movies were also learned.

### Results

* **Movie Run Time recommendation based on the number of votes received for movies:**
  
![Img1](https://github.com/Shimnazzz/dsc-phase-1-project_data_8/assets/147800579/7e5f98e6-4335-48d0-bf27-bf0373867d04)

  The runtime corresponding to the 25th percentile 50th percentile and 75th percentile of the votes were found to be 130 minutes, 160 minutes and 190 minutes.

* **Top 10 Studios based on the average rating of their movies**

![Img2](https://github.com/Shimnazzz/dsc-phase-1-project_data_8/assets/147800579/eb70f9e1-f28f-475f-bd7c-97f87b1846a3)

* **Top 10 actors based on the highest worldwide and domestic gross**
  Following is the plot showing the top 10 actors beased on the highest average worldwide gross of their movies:
![Img3](https://github.com/Shimnazzz/dsc-phase-1-project_data_8/assets/147800579/850b77ab-a190-45be-8f2b-2128a6f42d0f)
  Following is the plot showing the top 10 actors beased on the highest average domestic gross of their movies:
![Img4](https://github.com/Shimnazzz/dsc-phase-1-project_data_8/assets/147800579/a70ff1a6-e5c0-4e6b-90f5-8ecc883df7ef)


## Conclusion and Recommendation

The following conclusions and recommendations can be derived from the results:

* The movies with higher number of votes had a run time between 130 minutes and 190 minutes. Microsoft would be recommended to create a movie within this timeframe in order to attain the satisfaction of the audience.

* The top ten studios that created movies with highest ratings were found out and these included studios like Trafalgar, NAV and GrtIndia. The client could look into the production style of these studios or associate with them for the first movie.

* The top ten actors that acted in movies that bagged high revenue from across the world was found out and these included actors like Rafe Spall, Yiu-Wing Chan and Aarif Rahman.

* For good revenue collection in the domestic market, the top ten actors that could be associated with were found out and they included actors like Craig T Nelson, Huck Milner and Diego Luna. Microsoft may considering associating with these actors based on the market segment they are interested in.
