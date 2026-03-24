# Movie-Recommender-with-Sentiment-Intelligence

The **Movie Recommendation with Sentiment Analysis System** is an innovative project that combines the power of content-based movie recommendation with sentiment analysis of reviews. The system enhances the movie exploration process by analyzing reviews related to the selected movie. It employs a pre-trained machine learning model to determine whether the reviews are positive or negative in nature, providing users with rapid insights into the overall reception of the movie.

## Dataset
* The dataset was downloaded from Kaggle: *[TMDB 5000 Movie Dataset](https://www.kaggle.com/datasets/tmdb/tmdb-movie-metadata)*
* Movie posters and reviews are fetched dynamically via the TMDB API.

## Features
- **Content-based Movie Recommendations:** Get top 10 similar movies based on your selection.
- **Detailed Movie Information:** View essential details including cast, director, genre, and release date.
- **Sentiment Analysis:** Analyzes live movie reviews to determine and highlight positive/negative sentiments.
- **User-friendly Interface:** Features a clean, responsive web interface built with Streamlit.

## Getting Started

1. **Clone this repository:**
   ```bash
   git clone https://github.com/your_username/movie-recommendation-system.git
   cd movie-recommendation-system
   ```

2. **Install required dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

3. **API Key Setup:**
   Ensure your TMDB API Key is configured in the code.

## Usage

1. **Run the Streamlit app:**
   ```bash
   streamlit run WebApp.py
   # or
   python -m streamlit run WebApp.py
   ```

2. **Select a Movie:** Choose your preferred movie title from the searchable dropdown menu.
3. **Get Recommendations:** Click the **Recommend** button to fetch movie details, posters, top reviews (with sentiment analysis), and similar movie recommendations.

## How it Works

### Text Preprocessing
Review text is cleaned and normalized before sentiment analysis. The pipeline includes:
- Converting text to lowercase.
- Removing links, HTML tags, punctuation, and numbers.
- Removing extra spaces.

### Sentiment Analysis
A pre-trained model vectorizes the preprocessed review text using TF-IDF and predicts whether the overall sentiment is Positive (👍) or Negative (👎).

### Cosine Similarity
Cosine similarity measures the similarity between movies based on their feature vectors (genres, cast, crew, overview). It mathematically determines which movies are closest to the user's selection in the vector space.

## Dependencies
- [Streamlit](https://streamlit.io/)
- [scikit-learn](https://scikit-learn.org/)
- [pandas](https://pandas.pydata.org/)
- [joblib](https://joblib.readthedocs.io/)
- [requests](https://docs.python-requests.org/en/latest/)
