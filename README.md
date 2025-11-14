# Movie-Recommendation-System-using-Deep-Learning
This project builds a hybrid neural recommendation system using TensorFlow Recommenders. It creates a two-tower model that combines collaborative filtering (user/movie IDs) with content-based filtering (movie titles) for personalized movie suggestions.

# Key Features
Hybrid Model Architecture: Leverages both user and movie features (collaborative filtering) alongside contextual information from text features (content-based filtering).
Deep Learning for Representation: Uses embedding layers to create dense vector representations for user IDs, movie IDs, and other categorical features.
Text Feature Integration: Employs a text embedding model to process and utilize movie title information, enhancing the model's understanding of content.
Multi-Task Learning: The model is trained to optimize for two key objectives simultaneously:
Retrieval Task: Efficiently sifting through the entire movie catalog to generate a shortlist of candidate movies.
Ranking Task: Precisely ranking the candidate list to present the most relevant movies at the top.
Built with TFRS: Utilizes the high-level TFRS library to simplify the implementation of complex recommendation system components and best practices.

# Model Architecture
The system is built as a two-tower model:
Query Tower: Encodes user information (user ID, etc.) into a query embedding.
Candidate Tower: Encodes movie information (movie ID, title text, etc.) into a candidate embedding.
The model is trained to make the inner product of the query and candidate embeddings high for positive (user, movie) pairs and low for negative ones.
