# Data Analysis and Predictive Models Using VCT 2023 Data  

## Introduction and Dataset  
Valorant was my introduction not only into first-person shooter video games, but also the world of esports through the Valorant Champions Tour (VCT). As I further my journey in data science, I knew I wanted to pursue a project on it. I will be using [this Kaggle dataset](https://www.kaggle.com/datasets/ediashtarevin/vct-champions-2023-stats?resource=download) based on the 2023 season results for the majority of the project, and will be explaining useful game terms as we go along.  

## The Game  
The premise of Valorant is simple: there are five players on each team, and for each half of a map (best of 13 rounds), the team is either an attacker or defender. The attackers' main goal is to plant the "spike" before the timer runs out and for the spike to detonate, which ends the round. The defenders' main goal is to either prevent the spike from being planted, or to defuse the bomb. The round also ends when the attackers have eliminated all defenders (attackers win) or if the defenders eliminate all attackers before the spike is planted (defenders win). However, if the spike is already planted, the defenders must defuse it before it detonates to win the round; it is not enough to simply eliminate the team. Compared to other 5v5 games, Valorant also has different characters, which are separated into four different classes. Ideally, every team should have at least one of each to balance the team dynamics, but there are occassional exceptions to this rule.

## Data Exploration  
There are 6,230 rows/observations and 23 columns/features in this dataset. The features are as follow:  
* **`match_id`:** *(Numerical Discrete)* The unique number assigned to the best of 3 (or 5 for finals games) that a team plays.  
* **`game_id`:** *(Numerical Discrete)* Each map within the best of 3 or 5 that the team plays. For each `match_id`, there are anywhere between 2 to 5 `game_id`'s.  
* **`team`:** *(Categorical Nominal)* The name of the team competing.
* **`score_team`:** *(Numerical Discrete)* The number of rounds the `team` won in a map.
* **`opponent`:** *(Categorical Nominal)* The name of the opposing team.
* **`score_opp`:** *(Numerical Discrete)* The number of rounds the `opponent` won in a map.
* **`map`:** *(Categorical Nominal)* The map on which that game was played on. At any given time, there is a map "pool" consisting of seven possible maps to be played, but the map pool changes as season progresses.
* **`map_pick`:** *(Binary)* Whether or not the team decided to play the map. In a standard best of three, each team "picks" one and "bans" two maps from the map pool, and the remaining map is the "decider" (both would be False).
* **`rating`:** *(Numerical Discrete)* The rating calculated by VLR, as explained [here](https://www.vlr.gg/160667/vlr-gg-player-rating-explained#:~:text=This%20rating%20system%20takes%20into,data%20that%20can%20be%20analyzed.).
* **`acs`:** *(Numerical Discrete)* The average combat score, an in-game statistic explained [here](https://dotesports.com/valorant/news/what-is-acs-in-valorant-and-how-is-it-calculated).
* **`kill`:** *(Numerical Discrete)* The number of kills a player got in one map.
* **`death`:** *(Numerical Discrete)* The number of times a player was killed in one map (does not count dying to the spike's detonation).
* **`assist`:** *(Numerical Discrete)* The number of assists a players gets in one map. This is either by causing damage (above 50), or by using an ability that hinders the enemies performance (ex. blinding the opponent for a teammate to get a kill).
* **`kast%`:** *(Numerical Discrete)* A statistic taking into account kills, assists, surviving, or being traded (enemy kills you, your teammate kills them within 5 seconds), as outlined [here](https://www.thespike.gg/forums/topic/introducing-kast-metric/9703).
* **`adr`:** *(Numerical Discrete)* The average damage per round of a player.
* **`hs%`:** *(Numerical Discrete)* The headshot percentage of a player within the map. This metric roughly indicates how good a player's aim is, as the headshot does the most damage to an enemy.
* **`fk`:** *(Numerical Discrete)* The number of times a player kills an enemy first in a round.
* **`fd`:** *(Numerical Discrete)* The number of times a player dies to an enemy first in a round.
* **`team_win`:** *(Binary)* A boolean indicating whether or not the player's team won the map.
