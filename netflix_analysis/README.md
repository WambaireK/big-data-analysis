# Netflix-Style Recommendation System Analysis

This folder contains the code and visualisations for the Netflix case study (Task 3) of the Big Data Applications assignment.

## Files

- `netflix_recommender_stable.py`: Memory-optimised Python script implementing a content-based recommendation system using the MovieLens 100k dataset.
- `netflix_chart_1_top_movies.png`: Visualisation showing the top 10 most rated movies in the dataset.
- `netflix_chart_2_rating_distribution.png`: Visualisation showing the distribution of movie ratings.

## Dataset

The script uses the **MovieLens 100k dataset** (`ml-100k.zip`), which contains:
- 100,000 ratings from 943 users
- 1,682 movies
- Available at: https://files.grouplens.org/datasets/movielens/ml-100k.zip

## Key Features

- **Memory Optimisation**: Processes only 100 movies at a time to prevent memory crashes in Colab
- **Content-Based Filtering**: Uses TF-IDF and cosine similarity to find similar movies
- **Visual Output**: Generates 2 charts showing rating patterns and popular movies
- **Recommendation Engine**: Provides movie recommendations based on title similarity

## Running the Script

1. Download the MovieLens 100k dataset and extract `u.data` and `u.item`
2. Place them in the same directory as the script
3. Install dependencies: `pip install pandas numpy matplotlib scikit-learn`
4. Run: `python netflix_recommender_stable.py`

## Generated Outputs

| File | Description |
|------|-------------|
| `netflix_chart_1_top_movies.png` | Top 10 most rated movies |
| `netflix_chart_2_rating_distribution.png` | Distribution of movie ratings |

## Dependencies

- Python 3.x
- pandas
- numpy
- matplotlib
- scikit-learn

## Notes

This script is designed to run in Google Colab's free tier without memory crashes by limiting the dataset to 100 movies for similarity calculations.
