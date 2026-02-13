## 🎯 Business Context

Recommendation systems are critical for streaming platforms to increase:
- User engagement
- Watch time
- Retention
- Content discovery

This project simulates a production-ready movie recommendation pipeline,
focusing on scalable similarity computation and hybrid ranking strategies.


## 🧠 Modeling Decisions

### Why TF-IDF?
TF-IDF was chosen because:
- It is efficient for large sparse datasets.
- It emphasizes rare but informative keywords.
- It provides interpretable similarity signals.

### Why N-Grams?
Using (1,2)-grams captures phrases like "science fiction" and improves semantic grouping.

### Why Sparse Matrix Multiplication?
Instead of computing a full similarity matrix (45k × 45k),
similarity is computed on-demand using sparse matrix multiplication,
reducing memory usage significantly.



## ⚠️ Limitations

- The model is content-based and does not include user personalization.
- TF-IDF captures lexical similarity but not deep semantic meaning.
- No collaborative filtering is implemented.
- External TMDB API calls may introduce latency.

These limitations provide opportunities for future improvement.

## 🏗 System Architecture

User (Streamlit UI)
        ↓
FastAPI Backend
        ↓
TF-IDF Recommender
        ↓
TMDB API (Metadata Enrichment)
        ↓
Response


## 💼 Key Highlights

- Built an end-to-end NLP-based recommendation system for 45k+ movies.
- Implemented efficient sparse similarity computation.
- Designed hybrid ranking strategy combining similarity and ratings.
- Integrated third-party API for real-time metadata enrichment.
- Deployed full-stack ML application to cloud.
