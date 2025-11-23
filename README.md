# Anime-Recommendation-System
The "Anime Recommendation System" project implements a simple yet effective Content-Based Filtering recommendation system designed to suggest anime titles similar to a user's favorite. It analyzes the features (such as genre, description, or tags) of a given anime and uses vector similarity to find the most relevant recommendations.
<img width="1536" height="1024" alt="ChatGPT Image Nov 23, 2025, 04_54_56 PM" src="https://github.com/user-attachments/assets/1f00fa6b-2798-4464-93d5-2dbecc7ab445" />
-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
# Project File

1 ) Anime-Recommendation-System.ipynb: The main Jupyter Notebook containing the data loading, preprocessing, model implementation, and demonstration.

2) Methodology: Content-Based Filtering

The core of this recommender is built using the following steps:

Data Preprocessing: The system reads the anime dataset, cleans up necessary columns (e.g., handling missing values, converting text to lowercase).

Feature Extraction: Textual features (like genres, synopses, or tags) are converted into a numerical matrix using techniques like TF-IDF (Term Frequency-Inverse Document Frequency) Vectorizer. This creates a vector representation for each anime.

Similarity Calculation: Cosine Similarity is used to calculate the similarity score between the feature vector of the target anime (the one the user inputs) and all other anime in the dataset. Cosine Similarity measures the angle between two vectors, indicating how closely related they are.

Recommendation Generation: The system retrieves the top N anime titles with the highest similarity scores, excluding the input anime itself.

---------------------------------------------------------------------------------------------------------------------------------------------------------

 # Requirements

To run this notebook, you will need the following Python libraries:

pandas

numpy

scikit-learn (specifically TfidfVectorizer and cosine_similarity)

You can install the necessary dependencies using pip:

pip install pandas numpy scikit-learn
-------------------------------------------------------------------------------------------------------------------------------------------------------------

# Usage

Run the Notebook: Open the Anime-Recommendation-System.ipynb file in a Jupyter environment (Jupyter Lab, VS Code, Google Colab, etc.) and run all cells sequentially.

Ensure Data is Available: The notebook assumes the presence of a CSV file containing the anime data. Make sure the data file is placed in the expected path (as defined in the notebook's initial cells).

Get Recommendations: Use the main function, typically named recommend_content or similar, to get recommendations for an anime by name (e.g., using the exact name as it appears in the dataset).

Example Code from Notebook:

# Example of getting recommendations for the anime "Naruto"
recommend_content("Naruto")
---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
📈 Workflow Details
1. Dataset
The dataset includes:

anime.csv: Contains anime_id, name, genre, type, episodes, rating, and members.
rating.csv: Contains user_id, anime_id, and rating.

2. Data Processing
Cleaned missing data in genres and ratings.
Split and analyzed multi-label genres.
Counted and visualized genre frequency.

3. Recommendation Logic
Used TF-IDF vectorization on anime genres.
Computed cosine similarity between TF-IDF vectors.
Built a function to fetch top-N similar anime based on genre similarity.



🛠 Technologies Used

Languages: Python

Libraries:
Machine Learning: Scikit-learn

Data Handling: Pandas, NumPy

Visualization: Seaborn, Matplotlib

App Framework: Streamlit

Tools: Jupyter Notebook, Git


--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

🧠 How It Works

1️⃣ Data Preprocessing

Clean missing values

Process genres, type, synopsis

Create user–anime rating matrix

2️⃣ Content-Based Filtering

Apply TF–IDF vectorization on synopsis/genres

Compute cosine similarity between anime features

3️⃣ Collaborative Filtering (ALS)

Build sparse user–anime matrix

Train ALS using the implicit library

Predict unseen anime ratings

4️⃣  Streamlit Web App

Search anime by title

Displays recommended anime + scores

Simple, fast, and interactive UI


The output will be a list of suggested anime titles sorted by their similarity score.


🙋 Author

Sushant Balkrishna Jadhav
GitHub: https://github.com/sushantj01

LinkedIn: https://www.linkedin.com/in/sushant-jadhav-9ab2b5213/
