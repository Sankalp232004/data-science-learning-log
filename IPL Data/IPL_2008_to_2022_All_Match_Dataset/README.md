IPL Data Analysis Project (2008-2022) 🏏
This project analyzes IPL match data from 2008 to 2022 using Python and the Pandas library. The goal is to perform data cleaning, exploratory data analysis (EDA), and basic visualizations to uncover key insights and trends in the tournament's history.

Dataset Overview 📋
The project uses two primary datasets, which were successfully loaded as Pandas DataFrames:

1. matches_df
This DataFrame contains information about each match played from 2008 to 2022. It has 950 entries and 20 columns, including match details, venues, toss decisions, winning team, and players of the match.

Key Observations:

The City column has 51 missing values, indicating some matches were played in unspecified locations.

The Margin, SuperOver, WinningTeam, Player_of_Match, and method columns also contain missing values that require cleaning.

The Date, Season, and MatchNumber columns are all of type object, suggesting they may need conversion for time-series analysis.

The ID column is of type int64 and Margin is float64, which are suitable for numerical operations.

2. ball_by_ball_df
This DataFrame contains detailed information for every ball bowled in the IPL from 2008 to 2022. It includes details such as the bowler, batter, runs scored, and if a wicket was taken. This dataset is much larger and provides granular insights into gameplay.

Key Observations:

All columns are of type object or int64. The kind and fielders_involved columns have a significant number of missing values, which is expected for non-wicket-taking deliveries.

This dataset can be merged with matches_df using the ID column to connect individual deliveries to specific matches.

Analysis and Visualizations 📈
The project includes the following analysis steps:

Data Cleaning: Missing values were addressed. For example, missing Player_of_Match values were filled with the string 'unknown' to prevent errors in subsequent analysis.

Team Performance: The number of wins for each team was counted.

Visualization: A bar chart was created to visualize the top 10 winning teams in the history of the IPL, providing a clear and simple overview of team success.

Initial Findings:
The bar chart clearly shows the most successful teams in the IPL over the analyzed period, which is a great starting point for deeper analysis.
