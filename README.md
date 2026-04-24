# Movie Recommender System

A content-based movie recommendation engine built using **Python**, **Pandas**, and **Scikit-Learn**. This system suggests movies similar to a user's favorite based on genres, keywords, cast, and crew metadata.

---

## 🛠️ How it Works

The recommendation engine follows these primary steps:

1.  **Data Preprocessing**: Merges the TMDB 5000 Movies and Credits datasets.
2.  **Feature Engineering**: Extracts the top 3 actors, the director, genres, and keywords from JSON-formatted strings.
3.  **Data Cleaning**: Removes spaces from names to ensure the vectorizer treats unique names as single entities.
4.  **Vectorization**: Uses `CountVectorizer` to convert the combined "tags" (overview + genres + keywords + cast + crew) into 5,000-dimensional vectors.
5.  **Similarity Calculation**: Calculates the **Cosine Similarity** between all movie vectors to find the closest matches in a multidimensional space.

---

## 🏗️ Tech Stack

*   **Language:** Python 3.x
*   **Libraries:** 
    *   `pandas` & `numpy` (Data Manipulation)
    *   `ast` (Abstract Syntax Trees)
    *   `sklearn` (Machine Learning & Vectorization)
    *   `pickle` (Model Deployment)

---

## 📁 Project Structure

| File | Description |
| :--- | :--- |
| `tmdb_5000_movies.csv` | Dataset containing movie details. |
| `tmdb_5000_credits.csv` | Dataset containing cast and crew details. |
| `movie_recommender.ipynb` | Main logic and data cleaning script. |
| `movie_list.pkl` | Pickled DataFrame for use in web apps. |
| `similarity.pkl` | Pickled similarity matrix. |

---
