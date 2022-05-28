# MS-ENGAGE_Movie_recommendation
An application where users can login into his/her account, pick his/her favourite movie and can get the similar movies related to that movie.
# Recommendation System
A recommendation engine is a class of machine learning which offers relevant suggestions to the customer. Before the recommendation system, the major tendency to buy was to take a suggestion from friends. But Now Google knows what news you will read, YouTube knows what type of videos you will watch based on your search history, watch history, or purchase history. A recommendation system helps an organization to create loyal customers and build trust by them desired products and services for which they came on your site. The recommendation system today is so powerful that they can handle the new customer too who has visited the site for the first time. They recommend the products which are currently trending or highly rated and they can also recommend the products which bring maximum profit to the company. For this project I used content-based filtering.
# Content-Based Filtering
The algorithm recommends a product that is like those which used as watched. In simple words, in this algorithm, we try to find finding item look alike. For example, a person likes to watch Sachin Tendulkar shots, so he may like watching Ricky Ponting shots too because the two videos have similar tags and similar categories. Only it looks similar between the content and does not focus more on the person who is watching this. Only it recommends the product which has the highest score based on past preferences.
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
-> Data is taken from Kaggle which is a TMDB 5000 Movie Dataset.
# Data Processing
-> Dataset may consist of some missing values and duplicate values so we will remove these impurities.
# Feature Selection
-> We will not take all the feature columns. We will only choose which we think can help us to make recommendations.
# Feature extractions:
-> For recommendation system we require some tags which we are going to extract from some of the selected features.
# Stemming
-> Performing stemming operations on the tag’s column using Porter Stemming. For that we use python's nltk module. Stemming is the process of reducing a word to its word stem that affixes to suffixes and prefixes or to the roots of words known as a lemma. For example, a stemming algorithm reduces the words “chocolates”, “chocolatey”, “Choco” to the root word, “chocolate” and “retrieval”, “retrieved”, “retrieves” reduce to the stem “retrieve”.
# Creating Vectors
-> Based on the tags column we formed the vectors for corresponding movies and then calculate the cosine distance i.e., using Cosine-similarity. Cosine similarity is a metric used to measure how similar the documents are irrespective of their size. Mathematically, it measures the cosine of the angle between two vectors projected in a multi-dimensional space. The cosine similarity is advantageous because even if the two similar documents are far apart by the Euclidean distance (due to the size of the document), chances are they may still be oriented closer together. The smaller the angle, higher the cosine similarity.
# Recommendations:
-> Based on the top five closest vectors by cosine-similarity we recommend the five movies for the corresponding selected movie.
