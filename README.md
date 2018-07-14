# Welcome to MovieRec4Parents!

## Executive Summary:
#### The goal of this project is to build a content-based movie recommender system for busy parents. The movie recommender can be utilized in two ways: the first is users answer a short series of questions about their family and standards regarding movie content and the second is users simply enter a movie name and receive a list of 5 recommended movies.

#### Data obtained from https://www.commonsensemedia.org/movie-reviews and associated individual movie pages. A system_test function was built to assess the quality of recommendations but has remained largely unutilized. Results of these and purely subjective analysis of recommendations shows about 80% accuracy.

### Below is a list of Jupyter notebooks with working code that you can visit if you so desire. Notebooks are located in the same folder as this README. Below each notebook name is a brief description of what the code in each notebook does.

MovieRec4Parents1_GetURL's.ipynb

    Scrape Common Sense Media's website for movie review pages for URL's.
MovieRec4Parents2_ScrapingMoviePages.ipynb

    Scrape individual movie pages for text and non-text data.
MovieRec4Parents3_Extracting_Features.ipynb

    Eliminate duplicate movies, extract features and preliminary data cleaning.
MovieRec4Parents4_Cleaning_and Organizing_Features.ipynb

    Data cleaned, organized, and separated into text and non-text features.
MovieRec4Parents5_NLP-Count_Vectorizer.ipynb

    Text features vectorized by word count and reduced by truncated SVD. Cosine similarity computed.
MovieRec4Parents5.1_NLP-TF-IDF_Vectorizer.ipynb

    Text features vectorized using TF-IDF (see notebook for more info) and reduced by truncated SVD. Cosine similarity computed.
MovieRec4Parents6_EDA_of_Non-text_Features.ipynb

    Exploratory Data Analysis of non-text features. Relationship between features characterized.
MovieRec4Parents7_Functions_for_Parents_Who_Have_More_Time.ipynb

    Functions for interface.py, a lib file to allow parents to interface with functions from clean notebook.
MovieRec4Parents8-User_Interface

    Notebook to allow parents to run simple commands without having to see the underlying code.

In the process of running the code in these notebooks, a number of data files were generated (located in the /data folder). Of these, two were larger than the 100MB file size limit to be transferred to GitHub, so some of the functions will not currently work--- notably, the movie recommenders themselves. However, if you wanted to run each notebook sequentially, the correct intermediary files will be created so that the project will work. Be forewarned:  the web scrape in the first notebook will take about 40 minutes and the scrape in the second will take about 3 hours to complete. Alternatively, the cosine similarity matrix was divided into 15 pieces. These matrix pieces can be recombined by running the function at the end of notebook 5.1.

### Non-standard packages and libraries:

In writing the above code, I used the modules pandas, numpy, sklearn, matplotlib, seaborn, scipy.stats, nltk, fuzzywuzzy. I also imported time, math, random, requests, copy, re, json, csv, pickle, and BeautifulSoup. I also made a non-standard library called interface that is located in the lib folder, without which the last notebook above will not work.

For a Technical Report, please click here.
> Written with [StackEdit](https://stackedit.io/).