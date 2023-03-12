# World-Cup-2022-I-round

This repository contains a code for predicting the results (win, lose, drawn) of matches for the first round of the World Cup. This repository contains the code for the first round of the World Cup 2022. The code is written in Python and uses various libraries for data analysis and visualization.

The data used in this project is sourced from Kaggle (https://www.kaggle.com/datasets/brenda89/fifa-world-cup-2022). The data contains information on international matches, including the date of the match, the teams that played, and the scores.

# Methodology
The project follows the following methodology:

1. Data Cleaning and Preparation: The historical match data is cleaned and prepared by dropping irrelevant columns, creating dummy variables, and dividing the data into explanatory variables and explanatory variable.
2. Model Selection and Evaluation: Three different machine learning models (DecisionTreeClassifier, RandomForestClassifier, and AdaBoostClassifier) are trained and tested on the historical match data to evaluate their accuracy.
3. Prediction and Results: The AdaBoostClassifier model is selected as the best-performing model, and is used to predict the outcomes of the upcoming matches. The predicted outcomes of the matches are saved in a results.xlsx file.

# Data Cleaning and Preparation
The data was prepared by using the following explanatory variables for the model:
1. home_team
2. away_team
3. home_team_fifa_rank
4. away_team_fifa_rank
5. home_has_advantage (if the game is played at the host stadium)
6. home_team_goalkeeper_score
7. away_team_goalkeeper_score
8. home_team_mean_defense_score
9. home_team_mean_offense_score
10. home_team_mean_midfield_score
11. away_team_mean_defense_score
12. away_team_mean_offense_score
13. away_team_mean_midfield_score
14. home_team_score_rolling (average goals scored in last 3 games)
15. away_team_score_rolling (average goals lost in last 3 games)

Missing data was filled using the bfill() and ffill() functions. When a country had no team data (goalkeeper_score, defense_score, mean_offense_score, midfield_score), then the team was assumed to be weak enough to assign it the lowest value in a given category.

# Model Selection and Evaluation
A function named metrics_display was created to train the model on the training set, determine the predictions, and compare them with the real results using the classification_report and ConfusionMatrixDisplay functions from Scikit-learn.

The metrics_display function was used to train three different classification models: DecisionTreeClassifier, RandomForestClassifier, and AdaBoostClassifier. Among the three models, the AdaBoostClassifier model had the highest accuracy of 59% and was chosen for predicting the results of the first round of the World Cup.
![image](https://user-images.githubusercontent.com/55345644/224542284-6c013cbd-44bc-4048-9a20-753e00fa1015.png)


# Prediction and Results
The AdaBoostClassifier model was used to predict the results of the first round of the World Cup using the predict function from Scikit-learn. The results were then saved in an Excel file named results.xlsx using Pandas.

The results.xlsx file contains the predicted results for each match, with the home_team_if_win column indicating the predicted outcome for the home team. The results file is attached in the repository.
![image](https://user-images.githubusercontent.com/55345644/224542306-c753b51b-bc3c-4d9c-8740-b6fb9ba0e01d.png)

