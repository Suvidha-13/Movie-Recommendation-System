# Movie-Recommendation-System 🍿 🎥📷🎬📽🎞
It is a Content-Based Recommender System that recommends movies similar to the movie user chooses.

Content-based filtering is one of the popular technique of recommendation or recommender systems.

Here, the system uses your features and likes in order to recommend you with things that you might like. It uses the information provided by you over the internet and the ones they are able to gather and then they curate recommendations according to that. 

The details of the movies(title, genre, runtime, rating, poster, etc) are fetched using an API by TMDB, https://www.themoviedb.org/documentation/api.

## Link to the Application
Check out the Application by clicking over here 👉 https://the-movie-magic.herokuapp.com/

### The Movie Magic 🃏
I've developed a web application called "The Movie Magic" which supports all language movies. I've used the TMDB's recommendation engine in "The Movie Magic". 
The recommendation part that I first in this application doesn't support for multi-language movies as it consumes more of RAM (even after deploying it to Heroku) for generating Count Vectorizer matrix for all the 700,000+ movies in the TMDB.

## How to get the API key?
Create an account in https://www.themoviedb.org/, click on the `API` link from the left hand sidebar in your account settings and fill all the details to apply for API key. If you are asked for the website URL, just give "NA" if you don't have one. You will see the API key in your `API` sidebar once your request is approved.

## How to run the project?
1. Clone this repository in your local system.
2. Install all the libraries mentioned in the [requirements.txt](https://github.com/Suvidha-13/Movie-Recommendation-System/files/8793551/requirements.txt) file with the command `pip install -r requirements.txt`.
3. Replace YOUR_API_KEY in both the places (line no. 24 and 44) of `static/recommend.js` file.
4. Open your terminal/command prompt from your project directory and run the `main.py` file by executing the command `python main.py`.
5. Go to your browser and type  http://127.0.0.1:5000 in the address bar.

Hurray! That's it.

## Architecture
![Architecture](https://user-images.githubusercontent.com/90213576/170879759-04a78cbf-23ef-4aa0-9074-215a4b805c23.PNG)

## Cosine Similarity
How does it decide which item is most similar to the item user likes? Here come the similarity scores.

It is a numerical value ranges between zero to one which helps to determine how much two items are similar to each other. This similarity score is obtained measuring the similarity between the text details of both of the items. So, similarity score is the measure of similarity between given text details of two items. This can be done by cosine-similarity.

## How Cosine Similarity works?
Cosine similarity is a metric used to measure how similar the documents are irrespective of their size. Mathematically, it measures the cosine of the angle between two vectors projected in a multi-dimensional space. The cosine similarity is advantageous because even if the two similar documents are far apart by the Euclidean distance (due to the size of the document), chances are they may still be oriented closer together. The smaller the angle, higher the cosine similarity.

![cosine similarity](https://user-images.githubusercontent.com/90213576/170880047-7906dfc3-ed45-4563-9757-7b105575f91e.PNG)

#### To know more about cosine similarity:
https://www.machinelearningplus.com/nlp/cosine-similarity/

https://towardsdatascience.com/understanding-cosine-similarity-and-its-application-fd42f585296a


## Sources of the datasets
1. [movie_metadata.csv](https://www.kaggle.com/datasets/carolzhangdc/imdb-5000-movie-dataset?select=movie_metadata.csv)
2. [movies_metadata.csv](https://www.kaggle.com/datasets/rounakbanik/the-movies-dataset?select=movies_metadata.csv)
3. [credits.csv](https://www.kaggle.com/datasets/rounakbanik/the-movies-dataset?select=credits.csv)
4. [List of movies in 2018](https://en.wikipedia.org/wiki/List_of_American_films_of_2018)
