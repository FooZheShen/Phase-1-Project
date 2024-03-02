# Microsoft Movie Studio

**Author**: Foo ZheShen

## Overview

This repo helps to explore relationships between runtime, budget, genre, TMDB average vote score, and ROI. The best movies for optimizing ROI are short, low budget horror/thriller movies. These tend to have lower reviews however.The best movies for optimizing vote score and total profit are long, high budget, Action/SciFi or Action/Adventure movies. These still have ROI much higher than average movie, but may require expensive IP. Short, high budget, Animation/Adventure/Comedy movies also do very well according to all three metrics (ROI, total profit, and vote score)

## Business Problem

Microsoft sees all the big companies creating original video content, and they want to get in on the fun. They have decided to create a new movie studio, but the problem is they don’t know anything about creating movies. They have hired you to help them better understand the movie industry. Your team is charged with exploring what types of films are currently doing the best at the box office. You must then translate those findings into actionable insights that the head of Microsoft's new movie studio can use to help decide what type of films to create.

***
Questions to consider:
* Is making movies profitable? 
    few chart show result by number of moive, budget, gross.
* What type movie making more money? What's the genre, duration(how long), budget, studio, director and writer, actor. experienc, etc.
* What are the business's pain points related to this project? Total lack of direction
* How did you pick the data analysis question(s) that you did? Microsoft definitely has plenty of money to jump in on the big budget movies immediately, but without knowing the quality of their other investment opportunities and given they have an exisitng brand that is very valuable, I wanted to present a balanced approach that considers ROI, total profit, and also "quality".
* Why are these questions important from a business perspective? 
 * ROI is important to decide which movie making ventures make sense to fund vs. using the money in other Microsoft projects. 
 * Total profit is important in understanding the total amount of money that can be made making movies.
 * Vote average may be important to Microsoft's brand, depending on how clearly the movie studio is associated with the parent company. Being associated with cheap or low quality things may damage Microsoft overall, even if the movies make them more money.
***


## Data Exploration

In the folder zippedData in the associated GitHub repository are movie datasets from:

   * Box Office Mojo
   * IMDB
   * Rotten Tomatoes
   * TheMovieDB.org

***
Questions to consider:
* Where did the data come from, and how do they relate to the data analysis questions?
* What does the data represent? What is in the sample and what variables are included?
* What are the target variables? 
* What are the properties of the variables you intend to use?
***
## Data Preparation

After the initial exploration of the datasets, I have selected 3 datasets:

* imdb.title.basics.csv
* imdb.title.ratings.csv
* tn.movie_budgets.csv
***
Those datasets were selected based on:
* completeness.
* Relevance.
* Target variables: Average ratings, genres, movie budget, movie gross.
***


## Methods

Describe and justify the process for analyzing or modeling the data.

***
Questions to consider:
* How did you analyze or model the data?
 * Perform regressions on ROI vs genre, runtime, and budget, identify the optimal choices, and repeat using other metrics until we come to a full recommendation on what type of move to make.
* How did you iterate on your initial approach to make it better?
 * We examined many different slices of the data and visualizations until we found significant results. Discovering and fixing data cleaning and quality issues ended up changing our results significantly from the start to the end of the analysis process, so it's hard to say what modelling changes had a large impact.
* Why are these choices appropriate given the data and the business problem?
 * Microsoft has a lot of capital, but also lots of other expenses. We analyzed the data with multiple target variables in mind to enable them to make a good decision no matter how much capital they want to invest, how profitable their other investment opportunities are, or how much they think their movie studio's brand might influence the "Microsoft" brand (for better or worse).
***
***
## Analysis Findings
Is movie making profitable?:
* Short answer is yes, but other variables should be taken into consideration.
* There are huge risks to making movies, more than 47% of the movies analyzed are not profitable in a domestic setting.
* And 21.67% of movies listed flopped even after considering worldwide gross.
* Other variables such as marketing costs which were not included in this analysis, might change how profitable the movies we analyzed are.
  
Overall making movies can be profitable, but to ensure the continued success of our future movie studio,
we should consider how movies are rated.
* We find that most movies made were bad, less than 30% of movies made are rated "Average"
and only less than 2% are considered good movies.

To find out what makes a good movie, we analyzed the top 10 most successful movies in movie grossing.

* What type movie making more money? What's the genre, duration(how long), budget, studio, director and writer, actor. experienc, etc.
* What are the business's pain points related to this project? Total lack of direction
* How did you pick the data analysis question(s) that you did? Microsoft definitely has plenty of money to jump in on the big budget movies immediately, but without knowing the quality of their other investment opportunities and given they have an exisitng brand that is very valuable, I wanted to present a balanced approach that considers ROI, total profit, and also "quality".
* Why are these questions important from a business perspective? 
 * ROI is important to decide which movie making ventures make sense to fund vs. using the money in other Microsoft projects. 
 * Total profit is important in understanding the total amount of money that can be made making movies.
 * Vote average may be important to Microsoft's brand, depending on how clearly the movie studio is associated with the parent company. Being associated with cheap or low quality things may damage Microsoft overall, even if the movies make them more money.
***


## Evaluation
Evaluate how well your work solves the stated business problem.

***
Questions to consider:
* How do you interpret the results?
 * We identified movie types that vastly outperform average movies on all key metrics, which is a great result for shaping studio policy.
* How well does your model fit your data? How much better is this than your baseline model?
 * We don't have real "models" yet. Summary statistics indicate our recommendations should increase expected profit, ROI, and vote average beyond making generic movie.
* How confident are you that your results would generalize beyond the data you have?
 * Very confident.
* How confident are you that this model would benefit the business if put into use?
 * Very confident.
***


## Conclusions
Provide your conclusions about the work you've done, including any limitations or next steps.

***
Questions to consider:
*“Middle of the Road” movies are the worst across all metrics: 
** Make a low-budget (for best ROI) or high budget (for best profit, best ratings, good ROI) movie, not a middle budget movie
** Make a movie that is either long or short, not medium length
* Pick Genre that suits budget and length:
 * Horror/Thriller for Low Budget/Short Movies
 * Sci-Fi/Thriller for High Budget/Long Movies
* Intellectual Property seems important for successful High Budget/Long Movies
 * We did not fully explore this relationship due to limited data about IP costs; would recommend obtaining this data and re-analyzing
 * Acquire movie rights for comic book superheroes or popular books.
* Further Research
 * We can help analyze directors/writers/actors within a certain genre/budget/runtime once you make a decision!

***


## For More Information

Please review our full analysis in [our Jupyter Notebook](./dsc-phase1-project-MengyuJ.ipynb) or our [presentation](./Flatiron_DS_P1_Presentation_MengyuJ).

For any additional questions, please contact **Mengyu Jackson & mengyujackson121@gmail.com**

## Repository Structure

Describe the structure of your repository and its contents, for example:

```
├── __init__.py                               <- .py file that signals to python these folders contain packages
├── README.md                                 <- The top-level README for reviewers of this project
├── dsc-phase1-project-MengyuJ                <- Narrative documentation of analysis in Jupyter notebook
├── Flatiron_DS_P1_Presentation_MengyuJ.pdf   <- PDF version of project presentation
├── code
│   ├── __init__.py                           <- .py file that signals to python these folders contain packages
│   ├── visualizations.py                     <- .py script to create finalized versions of visuals for project
│   ├── data_preparation.py                   <- .py script used to pre-process and clean data
│   └── eda_notebook.ipynb                    <- Un-used
├── data                                      <- Both sourced externally and generated from code
└── images                                    <- Both sourced externally and generated from code
```
