<div align="right">
  <a href="README.md">
    <img src="https://img.shields.io/badge/Language-Русский-blue?style=flat-square" alt="RU">
  </a>
</div>

# Alexander Kurilenko

**ML Engineer · machine learning and data pipelines**

I build ML systems end to end, from data loading and cleaning to model training, evaluation and the API. My main areas are recommendations, search and NLP. I work where ML meets data engineering: I prepare the data for my own models using Python, SQL and Airflow.

Currently a Research Engineer at the Quantum Computation Lab, MIPT, working on delivery logistics optimization.

### Tech Stack

| Area | Tools |
|---|---|
| **Languages** | Python, SQL |
| **ML / DL** | PyTorch, Transformers, Scikit-learn, OpenCV, YOLOv8 |
| **Recommendations & search** | next-item prediction, DPO, RAG, BM25, bi-encoders, FAISS, Qdrant |
| **Data** | PostgreSQL (full-text search, pgvector), Airflow, Pandas, NumPy, Parquet, asyncpg |
| **Engineering & MLOps** | FastAPI, Docker, Docker Compose, MLflow, pytest, Git, Linux |
| **Evaluation** | NDCG, MRR, Recall@K, bootstrap, statistical tests, A/B testing |

### Experience

**Quantum Computation Lab, MIPT** — Research Engineer · June 2026 – present

*   **Summer 2026, project with X5 Group** ([code](https://github.com/Yellow-Duck-Studio/VRP_and_Simulation_of_Retail_Delivery_Logistics)): wrote the first version of the evolutionary order-clustering algorithm, the data parser and a benchmark of five initialization methods. Converted the objective function to rubles, including SLA penalties.
*   **Since October 2026:** developing transport selection for a heterogeneous fleet with a Markov random field (Potts model), along with a five-component functional that scores route quality. Evaluating it on test problems and running ablations of its components.

### Projects: Recommendations and Search

**[Recommender system on Yambda-50M](https://github.com/sdwqwt2/music-recommender-system)** · PyTorch, Pandas, Parquet · [preprint](https://github.com/sdwqwt2/music-recommender-system/blob/main/reports/latex/main_en.pdf)

*   **Data:** built a reproducible pipeline for ~50M Yandex Music events: schema normalization, filtering, ID encoding and a leakage-free temporal split.
*   **Model:** trained a 43M-parameter GPT-2 from scratch to predict the next track; compared PPO and DPO fine-tuning with re-ranking by a user response model.
*   **Evaluation:** DPO improved NDCG@10 by 1.3% over the base model on the full catalog of 98.5K tracks. The gain is small: a one-sided bootstrap supports it (p = 0.037), the Wilcoxon test does not (p = 0.17).

**[Hybrid search over a 700K-product catalog](https://github.com/Kazualov/Furniture-RAG)** · PostgreSQL, Qdrant, FastAPI · lead of a team of 5

*   Wrote the search API that merges PostgreSQL full-text results with Qdrant vector results, and an asynchronous database client with connection pooling.
*   Fixed a failing catalog load from Parquet to PostgreSQL by normalizing types and missing values for batch inserts.
*   Implemented relevance labeling with an LLM judge (Llama 3.1) to evaluate search quality.

**[Candidate generation for Avito search](https://github.com/sdwqwt2/Basic-Search-Engine)** · FAISS, BM25, multilingual-e5

*   Profiled a corpus of 189K listings and built a category filter; adding a bi-encoder to BM25 raised Recall@50 from 0.28 to 0.35.

### Projects: Data Pipelines and ML Services

**[Airflow pipeline for used car prices](https://github.com/sdwqwt2/Used-Car-Price-Prediction)** · Airflow, MLflow, FastAPI, Docker Compose

*   Built a scheduled DAG (data cleaning → training → deployment) with retries on failure. Cleaning of 15K listings covers schema checks, missing values and outliers.
*   Metrics are logged to MLflow; the model is served through FastAPI and Streamlit in Docker Compose.

**[Long-term memory for an LLM assistant](https://github.com/Eeeee13/MTS_Router)** · PostgreSQL, pgvector, FastAPI · MTS True Tech Hack 2026 hackathon

*   Implemented dialogue history storage in PostgreSQL with embedding search (bge-m3, pgvector) and a context manager that adds relevant fragments of past dialogues to each request.

**[EndoAssist: endoscopy assistant](https://github.com/Kazualov/endoscopy_tool)** · YOLOv8, FastAPI · ML Engineer and Scrum Master

*   Prepared the dataset and trained a model for real-time polyp detection in video; developed API endpoints for patients, examinations and videos.
*   Ran sprints and turned doctors' needs into product requirements.

### Education

*   **Innopolis University** — Bachelor's degree in Data Science and Artificial Intelligence, 2024–2028. GPA 4.74 / 5.
*   **Deep Learning School, MIPT** — computer vision and NLP with PyTorch, 2026.

Languages: English (C1), German (B1).

### Contacts

*   **Email:** kurilenko.a.koivis@yandex.ru
*   **Telegram:** [@sdwqwt](https://t.me/sdwqwt)
