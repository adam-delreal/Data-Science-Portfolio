# Project 3 - Classifying Politics Based on Reddit Titles

This project showcases a political classifier, which predicts whether a news headline belongs to the European or Political subreddit.

--------------

## Motivation

The motivation behind this project was to create a classifier using 
qualitative data from subreddit headers/news-titles. 

----------

## Built with

This project was built with Jupyter Notebooks, using, but not limited to: Python, Pandas, Numpy, Scikit Learn, Natural Langauage Toolkit, Seaborn, and Motplotlib. Furthermore, the data scraped from Reddit using their API.

-------

## Overview

This project is broken down into three notebooks:

- 1) "Scrapping Reddit," which connects to reddit's api and scrapes the site for data.

- 2) "Exploratory Data Analysis," which analyzes, cleans, and engineers the data to prepare it for the models.

- 3) "Modeling," which trains & tests the data and showcases several models and their respective performance.

-------

## Dictionary 

The Variable definitions are below:

- `author` : The author of the post.
- `created_utc` : The time created.
- `domain` : The publication domain related to the post. 
- `downs` : The number of down-votes the post was given by users.
- `id` : The post identification key.
- `num_comments` : Number of posts belonging to the subreddit.
- `score` : Score is simply the number of up-votes (`ups`) minus the number of down-votes ('downs')
- `selftext` : A description of the post/title.
- `subreddit` : A sub-community belonging to the website.
- `subreddit_id` : The identification of the respective subreddit.
- `title` : The header of the post and what it's about.
- `ups` : The many up-votes the post was given by users.

------

## How to use?

If curious and this project is downloaded to be tested, the descriptions and interpretation should walk the user through the code and how to use it; please do not fret if coding, or anything in this notebook, is a new concept, the notebook is broken down with quick and simple interpretations! 

--------

## Credits

Special thanks to:

- Max Reinisch for the functions used to scrape the API and to convert the data into a dataframe.

- Wesley Bosse for interpreting what is going on behind-the-scenes in many scikit learn "black box" models.

- Douglas Strodtman for providing the structure and guidance to complete this project; his recommendations and work-flow were crucial for the completion of this project.

------- 

#### If interested in the subreddits:

<http://www.reddit.com/r/politics/>

<http://www.reddit.com/r/europe/>

