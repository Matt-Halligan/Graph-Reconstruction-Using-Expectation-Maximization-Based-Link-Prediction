# IMDb Graph Reconstruction using Expectation Maximization (EM)

Relational databases are noisy, vulnerable to data entry errors and likely to have missing data. This is a reproducible project that uses an Expectation-Maximization model to infer actor-genre preferences from the IMDb relational dataset, then uses those preferences to predict i.e., reconstruct likely actor/movie links. 

The pipeline includes:

•	Dataset exploration and statistics.

•	EM to learn P(genre | actor), P(genre | director), P(genre | movie).

•	Scoring function that combines those probabilities to score (actor, movie | director).

•	Batched storage of predicted scores.

•	Graph generation actor, genre bipartite graph using GraphML and sampling for visualization

•	Link-prediction evaluation vs ground-truth roles

## Project Overview (Slides)

![Slide 6](media/slide6.PNG)

![Slide 8](media/slide8.PNG)

![Slide 9](media/slide9.PNG)

## Full Presentation Recording

You can download the full presentation recording here:

![Halligan-IMDb Expectation Maximization Algorithm.pptx](Halligan-IMDb Expectation Maximization Algorithm.pptx)

![Halligan-IMDb Expectation Maximization Algorithm.mp4](media/Halligan-IMDb-EM-Graph-Analytics-Final.mp4)

## Files included
•	EM_Analysis.ipynb — Jupyter notebook that performs the pipeline of data exploration to EM to scoring to evaluation.

•	data/ — generated files:

	•	actor_genre_probs.csv, director_genre_probs.csv, movie_genre_probs.csv

	•	actor_to_idx.pkl, genre_to_idx.pkl

	•	actor_in_movie_score.sql (SQLite DB of predicted scores)

	•	GraphML files: e.g. actor_genre_probs_0.5.graphml, sampled subgraph files

•	media/ — plots and images used in presentations / README

•	Halligan-IMDb Expectation Maximization Algorithm.pptx — final presentation (uploaded)