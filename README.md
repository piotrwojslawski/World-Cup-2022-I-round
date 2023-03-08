# World-Cup-2022-I-round

This repository contains a code for predicting the results of the first round of the World Cup using the AdaBoostClassifier model. This repository contains the code for the first round of the World Cup 2022. The code is written in Python and uses various libraries for data analysis and visualization.

# Methodology
The project follows the following methodology:

1.Data Cleaning and Preparation: The historical match data is cleaned and prepared by dropping irrelevant columns, creating dummy variables, and dividing the data into explanatory variables and explanatory variable.

2.Model Selection and Evaluation: Three different machine learning models (DecisionTreeClassifier, RandomForestClassifier, and AdaBoostClassifier) are trained and tested on the historical match data to evaluate their accuracy.

3.Prediction: The AdaBoostClassifier model is selected as the best-performing model, and is used to predict the outcomes of the upcoming matches.

4.Results: The predicted outcomes of the matches are saved in a results.xlsx file.

#Libraries Used
The following libraries have been used in this project:
Pandas (v1.3.4)
NumPy (v1.20.3)
Matplotlib (v3.4.3)
Seaborn (v0.11.2)
SciPy (v1.7.0)

#Data Source
The data used in this project is sourced from Kaggle. The data contains information on international matches, including the date of the match, the teams that played, and the scores.

#Data Preparation
The data was prepared by using the following explanatory variables for the model:
home_team
away_team
home_team_fifa_rank
away_team_fifa_rank
home_has_advantage (if the game is played at the host stadium)
home_team_goalkeeper_score
away_team_goalkeeper_score
home_team_mean_defense_score
home_team_mean_offense_score
home_team_mean_midfield_score
away_team_mean_defense_score
away_team_mean_offense_score
away_team_mean_midfield_score
home_team_score_rolling (average goals scored in last 3 games)
away_team_score_rolling (average goals lost in last 3 games)

Missing data was filled using the bfill() and ffill() functions. When a country had no team data (goalkeeper_score, defense_score, mean_offense_score, midfield_score), then the team was assumed to be weak enough to assign it the lowest value in a given category.

#Teams
The following teams are playing in the first round of the World Cup:

group1: Qatar, Senegal, England, USA, France, Denmark, Mexico, Argentina, Belgium, Spain, Germany, Morocco, Switzerland, Uruguay, Portugal, Brazil
group2: Ecuador, Netherlands, IR Iran, Wales, Australia, Tunisia, Poland, Saudi Arabia, Canada, Costa Rica, Japan, Croatia, Cameroon, Korea Republic, Ghana, Serbia

#Model Training and Evaluation
A function named metrics_display was created to train the model on the training set, determine the predictions, and compare them with the real results using the classification_report and ConfusionMatrixDisplay functions from Scikit-learn.

The metrics_display function was used to train three different classification models: DecisionTreeClassifier, RandomForestClassifier, and AdaBoostClassifier. Among the three models, the AdaBoostClassifier model had the highest accuracy of 59% and was chosen for predicting the results of the first round of the World Cup.

#Prediction and Results
The AdaBoostClassifier model was used to predict the results of the first round of the World Cup using the predict function from Scikit-learn. The results were then saved in an Excel file named results.xlsx using Pandas.

The results.xlsx file contains the predicted results for each match, with the home_team_if_win column indicating the predicted outcome for the home team. The results file is attached in the repository.
