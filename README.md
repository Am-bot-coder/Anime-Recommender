# Anime-Recommender
Anime Recommendation ML Model

# 🎌 Anime Recommendation System

This is a basic content-based anime recommendation system built using Python and scikit-learn. It analyzes metadata like genres, synopsis, studios, and more to recommend similar anime titles.

## 📌 Features

- Recommends anime using content-based filtering
- Combines genres, studios, synopsis, and more into a unified "tags" feature
- Uses cosine similarity for similarity calculation
- Easy to customize and expand

## 🧠 How It Works

1. **Data Preprocessing**:
   - Loads and cleans the dataset (`anime_dataset.csv`)
   - Combines multiple fields like `Genre`, `Type`, `Studio`, `Producers`, `Source`, and `Synopsis` into a single string field: `tags`.

2. **Feature Extraction**:
   - Uses `CountVectorizer` to tokenize and vectorize the `tags` field (max 5000 features, English stopwords removed).

3. **Similarity Calculation**:
   - Computes pairwise cosine similarity between anime using the tag vectors.

4. **Recommendation Function**:
   - Given a title, it finds the most similar anime using the similarity matrix.

## 🚀 Getting Started

### Prerequisites

Install the required Python libraries:

```bash
pip install pandas numpy scikit-learn

