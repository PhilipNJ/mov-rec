# Movie Recommendation System

This is a content based rec system.

Data Source: https://www.kaggle.com/tmdb/tmdb-movie-metadata?select=tmdb_5000_movies.csv

The following steps are performed:

-      Movies and Credit data sets are merged and filtered

-      Data is cleaned for null and duplicate rows

-      Columns in the format of dictionary are converted to string or list

-      Select Director from crew and top 3 artists from the fields

-      Natural Language Processing:

o   Spaces removed in between names to make them unique (eg. James Cameron to JamesCameron)

o   New column "Tags" created by concatenating "Overview", "Genres", "Keywords", "Cast" and "Crew"

o   All words are made lowercase

o   Using "nltk" we stem the words in "tags"

o   We remove stopwords from "tags"

o   Using a count vectorizer, we get the feature names 

o   Cosine Similarity Algorithim is applied

-      Function is created to extracted movies with 5 closest similarity indices.
