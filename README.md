# DSA4060XA – PC Gaming Recommender System

**Course:** DSA 4060XA – Recommender Systems  
**Project type:** Five-week individual project  
**Domain:** PC gaming / Steam  
**Working dataset:** 5,000 Steam user-game interactions  
**Development:** Python in Google Colab; Streamlit application

## 1. Project overview
This project develops and evaluates a recommender system that suggests PC games to Steam users using historical user-game interaction data.

## 2. Planned models
1. Popularity-based recommendation (baseline)
2. Collaborative filtering (personalized model)
3. Singular Value Decomposition (advanced model)

## 3. Evaluation
- Precision@K
- Recall@K
- NDCG@K
- Catalog coverage
- Recommendation diversity

All metrics will be calculated on a held-out test set. The final report will document the split strategy, relevance definition, parameter choices and limitations.

## 4. Repository structure
```text
DSA4060XA-Recommender-Project/
├── README.md
├── data/
│   ├── raw/
│   └── cleaned/
├── notebooks/
│   ├── 01_data_understanding.ipynb
│   ├── 02_eda.ipynb
│   ├── 03_baseline.ipynb
│   ├── 04_personalized_model.ipynb
│   ├── 05_advanced_model.ipynb
│   └── 06_evaluation.ipynb
├── src/
│   └── recommender.py
├── app/
│   └── app.py
├── images/
├── requirements.txt
└── PROJECT_REPORT.pdf   # Add the final exported report here
```

## 5. Dataset
The planned source is the UCSD Steam dataset. The working file is `steam_gaming_5000.csv`, created by sampling 5,000 user-game interactions. The analysis table should contain:

- `user_id`
- `game_id`
- `game_name`
- `playtime_forever`
- `playtime_2weeks` (when available)

Keep original source files in `data/raw/` and processed files in `data/cleaned/`. Do not commit large raw datasets or files containing personal information without checking the dataset licence and GitHub limits.

## 6. Workflow
1. Understand and validate the dataset.
2. Explore user, game and playtime distributions.
3. Establish a popularity baseline.
4. Build personalized collaborative filtering.
5. Train and tune SVD.
6. Evaluate all models using the same test split and relevance rule.
7. Export the best model and connect it to the Streamlit app.
8. Complete and export the project report as `PROJECT_REPORT.pdf`.

## 7. Reproducibility
The notebooks should use a fixed random seed (42) where sampling or splitting is random. Record package versions, data source, sampling method and evaluation settings.

## 8. Current status
This is the initial repository scaffold. Replace TODO sections with executed analysis and verified results. Do not report model performance until the notebooks have been run.
