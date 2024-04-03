# Data Analysis and Predictive Models Using VCT 2023 Data  

## Introduction and Dataset  
Valorant was my introduction not only into first-person shooter video games, but also the world of esports through the Valorant Champions Tour (VCT). As I further my journey in data science, I knew I wanted to pursue a project on it. I will be using [this Kaggle dataset](https://www.kaggle.com/datasets/ediashtarevin/vct-champions-2023-stats?resource=download) based on the 2023 season results for the majority of the project, and will be explaining useful game terms as we go along.  

## Data Exploration  
There are 6,230 rows/observations and 23 columns/features in this dataset. The features are as follow:  
 **`match_id`:** *(Numerical Discrete)* The unique number assigned to the best of 3 (or 5 for finals games) that a team plays.  
 **`game_id`:** *(Numerical Discrete)* Each map within the best of 3 or 5 that the team plays. For each `match_id`, there are anywhere between 2 to 5 `game_id`'s.  
 **`team`:** *(Categorical Nominal)* The name of the team competing.
 **`score_team`:** *(Numerical Discrete)* The number of rounds the `team` won in a map.
 
