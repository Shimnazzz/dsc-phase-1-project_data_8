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

**Firstly,** using the datsets, imdb.title.ratings and imdb.title.basics, the attributes of runtime of movies (in minutes) and number of votes by audience were analysed using a scatter plot. The resulting scattter plot was similiar to a normal distrubution. In order to further understand the relationship between movie runtime and movie ratings, a categorised data involving both the parameters were created. This means the movie runtime was distributed into bins of 10 minute intervals and the mean of the votes received for movies with runtime in that particular bin was found out. 

After this the 25th percentile, 50th percentile and the 75th percentile of the audience votes was found out by considering the cumilative sum of the audience ratings. These percentiles were obtained from the following formula:

Xth percentile of the data= X/100 × Sum of the average ratings

After obtaining the 25th percentile, 50th percentile and 75th percentile of the audience votes, it was compared with the cumilative audience votes and the corresponding movie runtime was found out.

**Secondly,** from the datsets, bom.movie_gross and imdb.title.ratings, the attributes of movie studio and movie ratings were obtained respectively. In order to merge the two datasets, a thrid dataset, imdb.title.basics had to be used. This is because bom.movie_gross had the title of the movie in the dataset however imdb.title.ratings showed the ratings and number of votes for each IMDB movie ID. In order to find the corresponding movie title from the movie ID, this third dataset was used which had both IMDB movie ID and movie title. 

Once the datasets were merged the top 10 studios based on the average rating of all their movies were found.

**Thirdly,** from the datasets, bom.movie_gross and tn.movie_budgets, the worldwide gross, domestic gross and foreign gross were obtained. These were merged based on the movie titles. From imdb.name.basics and imdb.title.principals, the actors who played in the movies were obtained. After making necessary adjustments, the above mentioned datasets were merged.

Further to this, the top 10 actors were found based on the highest average worldwide gross for the movies and also in order to recommend actors that were appealing to the domestic audience, the top 10 actors based on the highest domestic gross for their movies were also learned.

### Results

* **Movie Run Time recommendation based on the number of votes received for movies:** 

* **Top 10 Studios based on the average rating of their movies** 

* **Top 10 actors based on the highest worldwide and domestic gross** 

## Getting Started

Please start by reviewing this assignment, the rubric at the bottom of it, and the "Project Submission & Review" page. If you have any questions, please ask your instructor ASAP.

Next, we recommend you check out [the Phase 1 Project Templates and Examples repo](https://github.com/learn-co-curriculum/dsc-project-template) and use the MVP template for your project.

Alternatively, you can fork [the Phase 1 Project Repository](https://github.com/learn-co-curriculum/dsc-phase-1-project), clone it locally, and work in the `student.ipynb` file. Make sure to also add and commit a PDF of your presentation to your repository with a file name of `presentation.pdf`.

## Project Submission and Review

Review the "Project Submission & Review" page in the "Milestones Instructions" topic to learn how to submit your project and how it will be reviewed. Your project must pass review for you to progress to the next Phase.

## Summary

This project will give you a valuable opportunity to develop your data science skills using real-world data. The end-of-phase projects are a critical part of the program because they give you a chance to bring together all the skills you've learned, apply them to realistic projects for a business stakeholder, practice communication skills, and get feedback to help you improve. You've got this!
