# How does effect speed and acceleration on a successful punt return!


# Datasets:

In this project, I would like to work on [NFL Data](https://www.kaggle.com/competitions/nfl-big-data-bowl-2022), which contains multiple **csv** files for tracking, play, game, and player data for all 2018-2020 Special Teams play. We can use this dataset to analyze statistics of competitions, plays, and players. As I am unfamiliar with the Football game rule, it would be great for me to learn it from this project.

To be specific in this project I would like to know if is there any correlation between far punt return and speed or acceleration. To answer to this question we have to use the **plays** dataset and **tracking** datasets. To do my analysis I am interested in these attributes which have been described below. Please note that Q, O, and C respectively refer to the quantitative, ordered, and categorical.

## Plays Data:
-   _gameId_: Game identifier, unique (numeric)
-   _playId_: Play identifier, not unique across games (numeric)
-   _specialTeamsPlayType_: Formation of play: Extra Point, Field Goal, Kickoff or Punt (text)
-   _specialTeamsResult_: Special Teams outcome of play dependent on play type: Blocked Kick Attempt, Blocked Punt, Downed, Fair Catch, Kick Attempt Good, Kick Attempt No Good, Kickoff Team Recovery, Muffed, Non-Special Teams Result, Out of Bounds, Return or Touchback (text)
-   _returnerId_: nflId(s) of returner(s) on play if there was a special teams return. Multiple returners on a play are separated by a ; (text)
-   _penaltyYards_: yards gained by possessionTeam by penalty (numeric)
-   _kickLength_: Kick length in air of kickoff, field goal or punt (numeric)
-   _kickReturnYardage_: Yards gained by return team if there was a return on a kickoff or punt (numeric)
-   _playResult_: Net yards gained by the kicking team, including penalty yardage (numeric)

## tracking Data

-   _gameId_: Game identifier, unique (numeric)
-   _playId_: Play identifier, not unique across games (numeric)
-   _frameId_: Frame identifier for each play, starting at 1 (numeric)
-   _nflId_: Player identification number, unique across players (numeric)
-   _s_: Speed in yards/second (numeric)
-   _a_: Speed in yards/second^2 (numeric)
-   _event_: Tagged play details, including moment of ball snap, pass release, pass catch, tackle, etc (text)

There are many other attributes in these tow datasets but I think those I have mentiond here are most related one to answer the question of my project.

## Task:
First of all, as I am interested in the return yardage of a play type I would like to visualize the different outcomes by special team contributions to gain return yardage for each team. Then I will try to find out speed and acceleration who does affect punt return.


- Which play type has more contribution to return yardage by each team?
- What is more important for a punt returner, speed or acceleration?
- Is there any correlation between speed and acceleration against return yardage?
- If there is any correlation,  how do different kick length ranges have an effect on that correlation?
