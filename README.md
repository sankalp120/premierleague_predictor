# premierleague_predictor

Premier League Match Result Prediction
Overview

This project focuses on predicting match outcomes (Win, Draw, or Loss) in the English Premier League using real match statistics.
The workflow includes data preprocessing, exploratory data analysis (EDA), feature engineering, and predictive modeling using Logistic Regression, Random Forest, and XGBoost classifiers.

Dataset
Source: Kaggle - Premier League Matches Dataset

Key Columns:
date, venue, team, opponent
goals_for, goals_against
expected_goals, expected_goals_against
shots, shots_on_target, possession
formation, attendance, season

Target Variable: result → (W, D, L)
Final Data Shape after Cleaning: ~3800 rows × 18 columns

Data Cleaning and Preprocessing
Removed irrelevant columns such as time, comp, round, day, match report, notes, and referee.
Converted date to datetime format and standardized the result variable.
Dropped rows with missing values in essential columns such as goals_for, goals_against, team, and opponent.

Renamed key columns for clarity:

gf → goals_for
ga → goals_against
xg → expected_goals
xga → expected_goals_against
sh → shots
sot → shots_on_target
poss → possession





Logistic Regression	~60%	Struggled with class imbalance
Random Forest	~70%	Captured non-linear feature interactions effectively
XGBoost	~72%	Achieved best balance between precision and recall
