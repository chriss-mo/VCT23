# Data Analysis and Predictive Models Using VCT 2023 Data  

## Introduction and Dataset  
Valorant was my first video game that introduced me to the world of esports through the Valorant Champions Tour (VCT), and as I further my journey in data science, I knew I wanted to pursue a project on it. I will be using [this Kaggle dataset](https://www.kaggle.com/datasets/ediashtarevin/vct-champions-2023-stats?resource=download) based on the 2023 tournament results for the majority of the project, and will be explaining useful game terms as we go along.  

## Data Exploration  
`match_id`: corresponds to the unique number assigned to the best of 3 (or 5 for finals games) that a team plays.
`game_id`: corresponds to each map within the best of 3 or 5 that the team plays. Thus, for each `match_id`, there are anywhere between 2 to 5 `game_id`'s within them. 
