# Movie Recommendation System
#Demo

https://drive.google.com/file/d/1DwccGL1kxRLQs1BNo2vJXSOKCoIUThf5/preview



## Overview

This project is a content-based Movie Recommendation System that suggests movies to users based on the similarity of movies' metadata such as genres, keywords, cast, and crew. By analyzing the features of movies, the system can provide personalized movie suggestions. The recommendation is made using Natural Language Processing (NLP) techniques and cosine similarity to calculate the distance between feature vectors.

## Features

- Personalized movie recommendations based on content similarity.
- Feature extraction from movie metadata including genres, keywords, cast, and crew.
- Real-time recommendation engine using cosine similarity.
- Efficient handling and processing of large datasets.
- Easy integration and scalability for further improvement and deployment.

## Tools & Technologies Used

- **Python**: The core programming language used for the implementation.
- **Pandas**: For data manipulation and preprocessing.
- **Scikit-Learn**: Used for the `CountVectorizer` feature extraction and cosine similarity calculations.
- **Natural Language Processing (NLP)**: To process textual data.
- **CountVectorizer**: To convert text data into a vectorized form for machine learning algorithms.
- **Cosine Similarity**: The algorithm used to measure the similarity between movies.

## Methodology

1. **Data Collection**: The project utilizes the TMDB 5000 Movie Dataset which contains movie metadata such as titles, genres, keywords, cast, crew, and more.

2. **Data Preprocessing**: Using `Pandas`, the datasets are merged and cleaned to remove missing values. Features like genres, keywords, cast, and crew are extracted from JSON-like strings using Python’s `ast` module.

3. **Feature Engineering**: 
   - **CountVectorizer**: Converts the movie metadata into a matrix of token counts.
   - **Cosine Similarity**: Calculates the similarity between the feature vectors of different movies.

4. **Recommendation Engine**: By using cosine similarity, the system calculates the closeness of movies based on their feature vectors. It ranks the movies based on similarity scores to recommend movies that are most similar to a given movie.

5. **Model Persistence**: The final model is saved using the `pickle` library, allowing it to be loaded and used for real-time recommendations without needing to retrain or process data again.

## Setup Instructions

### Prerequisites

- Python 3.x
- Pip (Python package installer)

### Installation

1. Clone this repository to your local machine:
    ```bash
    git clone https://github.com/yourusername/movie-recommendation-system.git
    cd movie-recommendation-system
    ```

2. Create a virtual environment (recommended) and activate it:
    ```bash
    python -m venv env
    source env/bin/activate  # On Windows use `env\Scripts\activate`
    ```

3. Install the required packages:
    ```bash
    pip install -r requirements.txt
    ```

### Usage

1. **Prepare the Data**: Ensure that the TMDB movie dataset files (`tmdb_5000_movies.csv` and `tmdb_5000_credits.csv`) are placed in the `data/` directory.
   
2. **Run the Script**: Execute the main Python script to generate recommendations:
    ```bash
    python movie_recommendation.py
    ```

3. **Get Recommendations**: Use the defined functions to get movie recommendations by inputting a movie name:
    ```python
    recommend('Movie Name')
    ```

### Example

To get recommendations for the movie "Gandhi", run:

```python
recommend('Gandhi')
