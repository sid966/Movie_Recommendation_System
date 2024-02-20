# Overview:
In this project I have prepared a movie recommendation system with the help of python and its various libraries on 5000 movies data file that is available in the repository.
# Description:
The dataset used is tmdb_5000_movies.csv that has 4803 entries with 20 columns/features.
Out of which 3 are float64, 4 are int64 and  13 are object data types.
Out of these features, the usable features for our use purpose are: title,tagline,overview and popularity.
Then we created an extra feature by combining tagline and overview features.
# Step 1:Text pre-processing
In this step I have performed pre-processing of the test data present in our description feature which is going to be used for recommending purpose.
Here I have used various libraries like NLTK,re,Contractions,numpy,...
Here I have performed basic text pre-processing by replacing everything except word characters and white space character with ".
Changed all text into lower case,removed leading or trailing spaces,fixing contractions,tokenized text,removed stop words
and lastly returned the pre-processed text for feature engineering.
# Step 2:Feature Engineering
Here I have used traditional text representation model:TF-IDF which normalizes counts using the inverse document frequency to downplay the effects of frequently occuring words.
And considered unigram as well as bigram and considered only those with the minm count =2.
Now we have got our TF-IDF matrix which we will use in the next step for finding similarity between documents.
# tep 3:Document Similarity Computation
Here based on this tf_idf matrix , we have calculated similarity matrix that shows how such similar a certain document is with the rest of documents by using cosine_similarity.
This Cosine_similarity assigns score to each document based on how similar it is to other documents.
# Step 4:Find top similar movies
Now to find the movies similar to a certain movie.We have taken the index of the movie of which we want to find similar movies then taken the index of top 5 movies based on the similarity matrix and printed the names.

