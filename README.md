# Movie Recommender 

A beginner-friendly movie recommendation system built in Google Colab using Python, pandas, scikit-learn, and the MovieLens dataset.

The goal of this project is to understand how recommendation systems work step by step instead of only relying on generated code. The notebook starts from basic data loading, explores movie and rating data, builds a simple personal taste profile, and then recommends movies based on similarity, public ratings, and popularity.

---

## Project Overview

This project recommends movies based on a user's personal ratings.

The user provides a few movies they have watched and rates them from 1 to 5. The system then studies the genres of those movies, builds a taste profile, compares that profile against all movies in the dataset, and returns the most relevant recommendations.

The first version uses content-based filtering, meaning it recommends movies similar to the ones the user already likes.

---

## What This Project Does

- Downloads the MovieLens dataset directly inside Google Colab
- Loads movie and rating data using pandas
- Allows the user to search for movies by title
- Lets the user create personal movie ratings
- Converts movie genres into numeric features using TF-IDF
- Builds a personal taste profile from the user's ratings
- Uses cosine similarity to compare the user's taste with all movies
- Improves recommendations using:
  - Personal similarity score
  - Average public rating
  - Rating count / popularity
- Saves final recommendations into a CSV file

---

## Tech Stack

- Python
- Google Colab
- pandas
- NumPy
- scikit-learn
- MovieLens dataset

---

## How the Recommendation Works

The recommendation system follows this flow:

```mermaid
flowchart TD
    A[Start in Google Colab] --> B[Download MovieLens Dataset]
    B --> C[Load Movies and Ratings CSV Files]
    C --> D[Explore Movies and Ratings Data]
    D --> E[User Searches for Movies]
    E --> F[User Adds Personal Ratings]
    F --> G[Clean Movie Genres]
    G --> H[Convert Genres to Numbers using TF-IDF]
    H --> I[Build User Taste Profile]
    I --> J[Compare User Profile with All Movies]
    J --> K[Calculate Similarity Scores]
    K --> L[Add Public Rating and Popularity Scores]
    L --> M[Calculate Final Recommendation Score]
    M --> N[Remove Already Rated Movies]
    N --> O[Show Final Movie Recommendations]
    O --> P[Export Recommendations to CSV]
