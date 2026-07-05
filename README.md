# movie-recommendation-system
Content-based movie recommender using TMDB dataset

#  Movie Recommendation System

A content-based movie recommender that suggests similar movies using
metadata such as genres, keywords, cast, and director, combined with
cosine similarity.

##  Dataset
[TMDB 5000 Movie Dataset](https://www.kaggle.com/datasets/tmdb/tmdb-movie-metadata)
— 5000 movies with metadata (genres, cast, crew, keywords, overview).

##  Tech Stack
- Python
- Pandas, NumPy
- Scikit-learn (CountVectorizer, Cosine Similarity)
- Kagglehub (dataset loading)

##  Approach
1. **EDA & Cleaning** — merged movies + credits data, handled nulls,
   explored ratings and popularity distributions.
2. **Feature Engineering** — extracted genres, keywords, top 3 cast
   members, and director from nested JSON fields; combined with
   overview text into a single `tags` feature.
3. **Vectorization** — converted tags into count vectors
   (`CountVectorizer`, 5000 features, English stopwords removed).
4. **Similarity** — computed pairwise **cosine similarity** across
   all movie vectors.
5. **Recommendation** — for a given movie, returns the top-N most
   similar movies based on similarity score.

##  Sample Output
