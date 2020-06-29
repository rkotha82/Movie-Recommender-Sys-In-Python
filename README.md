# MovieRecommenderSysInPython
This is a Hollywood Movie recommender system built in Python. IMDB 5000 Movie dataset was used to build this. 

Link to dataset: https://www.kaggle.com/carolzhangdc/imdb-5000-movie-dataset

Link to the Web application: 

## What is a Recommendation System? ##
As it is clear by name, Recommender System is a piece of software that recommends us the relevant products or services. Recommender systems are everywhere. There can’t be a day when you don’t come through a recommender system on web.

Recommender system is the most basic application of machine learning. Some real life examples of recommender system:

Amazon recommends us products based on the products we checked out in the past. Netflix recommends us movies based on our watch history. Google gives us suggestions when we type something in the search box based on our search history.

###  Types of Recommender System
There are basically two main components of any recommendation system, Users and Items. Items are the entities that are recommended by the recommender system to the users. Let’s understand by taking some examples:

__Platform--User--Item__
Netflix--	People--Movies
Facebook--People--People
Amazon--People--Product
Linkedin--People--Jobs

Netflix recommends movies to the people, hence movies are items and people are users, while Facebook recommends the people you may know to the people, here people are users and people are items too.

___What is a Recommendation System?___
There are three types of recommender systems that are mostly used:

* Popularity Based Recommender System

Popularity based recommender system recommends the most popular items to the users. Most popular items is the item that is used by most number of users. For example, youtube trending list recommends the most popular videos of the day.

* Content Based Recommender System
Content based recommender systems recommends similar items used by the user in the past.

For example, Netflix recommends us the similar movies to the movie we recently watched.

Similarly, Youtube also recommends us similar videos to the videos in our watch history.

* Collaborative Filtering based Recommender System
Collaborative Filtering based recommender system creates profiles of users based on the items the user likes. Then it recommends the items liked by a user to the user with similar profile.

For example, Google creates our profile based on our browsing history and then shows us the relevant ads

Now we’ll be building a Content Based Hollywood movie recommender system in Python programming language. First we’ll dive deeper into the working of Content Based Recommender System.

## Content Based Recommender System Working
Content Based Recommender System recommends items similar to the items user likes. How does it decide which item is most similar to the item user likes. Here we use the similarity scores.

* Similarity Score :It is a numerical value ranges between zero to one which helps to determine how much two items are similar to each other on a scale of zero to one. This similarity score is obtained measuring the similarity between the text details of both of the items. So, similarity score is the measure of similarity between given text details of two items.

Here we’ll use cosine similarity between text details of items. In the example below it is shown how to get cosine similarity:

Step 1 : Count the number of unique words in both texts.
Step 2 : Count the frequency of each word in each text.
Step 3 : Plot it by taking each word as an axis and frequency as measure.
Step 4 : Find the points of both texts and get the value of cosine distance between them.
Example : Text 1 = “Money All Money”
Text 2 = “All Money All”
Step 1 : There are only two unique words between both texts. ‘Money’ and ‘All’
Step 2 : Counting the frequency.

------Text 1---Text2 </ br>
Money---2--------1 </ br>
All-----1--------2 </ br>

Step 3 and Step 4 : There are only two unique words, hence we’re making a 2D graph.

Now we need to find the cosine of angle ‘a’, which is the value of angle between both vectors. Here is the formula used for doing this:

** Angle Between Two Vectors **
For Finding Angle between two vectors, check out the link: https://www.youtube.com/watch?v=dYPRYO8QhxU

In our case, cos(a) = 0.8 . Hence similarity score between Text 1 and Text 2 is 0.8, so we can say that both the texts are 80% similar.

This was all the Math behind cosine similarity, which is used by Content Based Recommender System. Now let’s see how to make a Content Based Recommender System in Python.
