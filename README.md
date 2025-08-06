**Movie Recommendation System (TMDB 5000 Dataset)
**
Overview
**
This project is focused on building a content-based movie recommendation system using the TMDB 5000 Movies and Credits datasets. The goal is to process the data, clean and transform it, and implement a simple recommendation engine using Natural Language Processing (NLP) techniques.

**Data Sources
**tmdb_5000_movies.csv

tmdb_5000_credits.csv

These datasets are merged on the title column to create a unified structure for analysis.

Key Features
**Data Cleaning:
**
Handled missing values and duplicates

Selected relevant features: id, title, genres, overview, keywords, cast, crew

**Feature Engineering:
**
Extracted important fields from nested JSON-like columns using Python's ast.literal_eval

Created a new column to combine multiple features into a single text-based representation

**Natural Language Processing:
**
Applied stemming using NLTK’s PorterStemmer

Created a "tags" column combining all relevant text for vectorization

**Vectorization**:

Used CountVectorizer to convert text into numerical vectors

**Recommendation System:
**
Implemented cosine similarity to find and recommend similar movies based on input

**Functions Explained
**
convert(obj): Extracts names from JSON-like string fields (e.g., genres, keywords)

fetch_director(obj): Extracts the director's name from the crew column

collapse(L): Converts list of dictionaries into list of strings

stem(text): Applies stemming to a string of words using NLTK

recommend(movie): Takes a movie title and returns a list of similar movies using cosine similarity

**Technologies Used
**
Python

Pandas

NumPy

NLTK

Scikit-learn

**How to Use
**Load the notebook and run all cells sequentially.
use the dataset given in the repository.

Use the recommend('Movie Title') function to get a list of top 5 similar movies.

**Notes**
The stemming process used is basic and may affect the accuracy of matching in edge cases.

The similarity matrix is precomputed for efficiency but will consume memory depending on dataset size.

**Future Improvements
**
Integrate TF-IDF instead of CountVectorizer for better semantic matching

Add deployment as a web application

Incorporate user ratings and collaborative filtering
The stemming process used is basic and may affect the accuracy of matching in edge cases.

The similarity matrix is precomputed for efficiency but will consume memory depending on dataset size.

