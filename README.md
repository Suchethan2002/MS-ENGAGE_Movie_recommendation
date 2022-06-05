# MS-ENGAGE_Movie_recommendation
An application where users can login into his/her account, pick his/her favourite movie and can get the similar movies related to that movie.
# Recommendation System
A recommendation engine is a type of machine learning that provides customers with relevant ideas. Before the recommendation system, the most common method of purchasing was to rely on the advice of friends. However, based on your search history, watch history, or buy history, Google now knows what news you will read and YouTube knows what type of videos you will watch. A recommendation system aids a firm in gaining loyal clients and establishing confidence by providing them with the items and services for which they come to your website. Today's recommendation systems are so sophisticated that they can manage even new customers who are visiting the site for the first time. They can also recommend things that are currently trending or highly rated. For this project I used content-based filtering.
# Content-Based Filtering
The algorithm suggests a product that is similar to those that were previously viewed. To put it another way, we're trying to locate items that seem alike in this algorithm. If a person enjoys watching Sachin Tendulkar's shots, he might also enjoy watching Ricky Ponting's shots because the two videos have comparable tags and categories. Only the material appears to be identical, and it does not place a greater emphasis on the viewer. Only the product with the greatest score based on previous preferences is recommended.
# Dataset
The dataset is taken from Kaggle.
Movies Dataset Link: - https://www.kaggle.com/datasets/tmdb/tmdb-movie-metadata?select=tmdb_5000_movies.csv
It consists of two csv files one contains movies data while other contains credits related to that movie.
# Tech Stack
- Python
- pandas
- streamlit
- NLTK
- Pickle
- Requests
# Data COllection
-> The data comes from Kaggle, which is based on the TMDB 5000 Movie Dataset.
# Data Processing
->We will remove any missing values and duplicate values from the dataset.
# Feature Selection
-> We are not going to use all of the feature columns. We will only select those that we believe will assist us in making recommendations.
# Feature extractions:
->We'll extract tags from some of the selected features to use in our recommendation system.
# Stemming
-> Porter Stemming is used to perform stemming operations on a tag's column. Python's nltk package is used for this. The process of reducing a word to its word stem, which affixes to suffixes and prefixes or to the roots of words known as a lemma, is called stemming. A stemming algorithm, for example, converts the words "chocolates," "chocolatey," and "Choco" to the root word "chocolate," and "retrieval," "retrieved," and "retrieves" to the stem "retrieve."
# Creating Vectors
->I created vectors for corresponding movies based on the tags column and then calculated the cosine distance, i.e. utilising Cosine-similarity. Cosine similarity is a metric for determining how similar documents are regardless of size. It calculates the cosine of the angle formed by two vectors projected in three dimensions. Because of the cosine similarity, even if two comparable texts are far apart by the Euclidean distance (due to the size of the document), they are likely to be oriented closer together. The greater the cosine similarity, the smaller the angle.
# Recommendations:
-> Based on the top five closest vectors by cosine-similarity we recommend the five movies for the corresponding selected movie.
