### Executive Summary:
#### The goal of this project is to build a content-based movie recommender system for busy parents.

### Problem Statement:
#### Parents are busy. Sometimes they need a break. Parking the kids in front of a screen for a few hours is often very tempting--- yet, how is a busy parent to evaluate the myriad video entertainment options?

### Summary of MovieRec4Parents:
#### MovieRec4Parents will give you the titles of five movies that are the most closely related to a movie you name by cosine similarity of text associated with the movies. Text data was scraped from movie review pages at  https://www.commonsensemedia.org/movie-reviews. Text was extracted, combined, cleaned, and subjected to TF-IDF (text frequency-inverse document frequency) vectorization. Text was also sent through Count Vectorization for more straightforward analysis according to simple word count (see notebook 5). TF-IDF vectorized text yielded more accurate subjective results.

#### TF-IDF Vectorized text was then sent through truncated SVD to yield orthogonal components. This was done both to reduce the number of features and to get rid of excess noise. Non-text data was also scraped and analyzed separately to better characterize the data (see notebook 6) and to allow users to specify the parameters of their children's movie entertainment choices more precisely (see notebook 7 and below).
 
#### The movie recommender can be utilized in two ways. The first has users answer a short series of questions about their family and familial standards regarding the movie content parents are willing to allow their children to see. After parents give the name of a single movie their childen have enjoyed in the past, the recommender will get a list of similar movies and filter them according to the standards they entered. The top five results will then be returned. The second way the recommender can be used is users simply enter a movie name and receive a list of the top 5 most closely related movies.

#### To facilitate user experience and to allow functions developed in different notebooks to be used together, a non-standard library called interface was created. It is located in the folder called lib in the base capstone directory. This library contains all of the functions needed to run the movie recommender functions, provided the similarity matrix could be recreated (see the end of notebook5.1).

### Data Analysis:
#### Non-text data included the MPAA rating (G, PG, PG-13, R, NR, and NC-17), the minimum recommended age of viewership according to Common Sense Media, the movie genre, and a group of ratings from 0 to 5 of various movie characteristics of  parental concern such as the amount of violence or sex in movies targeted at teens or the amount of 'violence and scariness' or 'sexy stuff' in movies targeted at younger kids. Graphs of exploratory data analysis can be found in notebook 6. Generally, there appear to be two sets of movies, those recommended for children younger than 9 and those recommended for tweens/teens and older. Consequently, two separate sets of questions were created depending upon the age of the children in the family. 80% of the movies had no rating for 'educational value.' These movies were deemed to be different from those that had a zero for 'educational value,' so a boolean was created called is_educational to allow parents to restrict themselves to just a list of ostensively educational movies.

### 


> Written with [StackEdit](https://stackedit.io/).