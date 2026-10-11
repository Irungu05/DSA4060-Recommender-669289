
# DSA 4060 Personalized Movie Recommender

## Student Details
- **Student Name:** Angela Irungu
- **Student ID:** 669289
- **Assigned User ID:** 10

---

## Project Objective
This project builds a personalized content-based movie recommender system for an assigned streaming platform user. By analyzing historical user ratings and movie genre vectorization, the system identifies the user's specific preferences and generates five sensible, unrated movie recommendations.

---

## Datasets
The project uses two primary datasets:
- `movies.csv`: Catalogue containing `movieId`, `title`, and pipe-separated `genres`.
- `ratings.csv`: Historical rating interactions containing `userId`, `movieId`, `rating`, and `timestamp`.

---

## Method / Approach
1. **User Profiling:** Filtered interactions for **User ID 10** to list rated movies, identify top-rated titles, and analyze genre frequency and average ratings.
2. **Preference Identification:** Isolated positively rated movies with a threshold rating of $\ge 4.0$ as evidence of user preference.
3. **Genre Vectorization & Similarity:** Processed movie genres using `TfidfVectorizer` to create numerical feature vectors. Computed pairwise `cosine_similarity` across all catalogue items against the user's liked movies.
4. **Filtering & Ranking:** Excluded movies already rated by User 10, calculated mean similarity scores for unseen movies, and selected the top 5 highest-ranked titles.

---


## Limitation and Suggested Improvement

* **Limitation:** The current content-based model relies exclusively on genre tags. It cannot account for movie quality, release year, director, or cast, leading to potential over-specialization and recommendation of low-rated titles sharing similar tags.


* **Suggested Improvement:** Implement a hybrid recommender model that combines collaborative filtering (analyzing behavioral rating patterns across all users) with richer metadata features (actors, directors, keywords) to enhance diversity and personalization.



```

```
