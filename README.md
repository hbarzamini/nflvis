
# How does effect speed and acceleration on a successful punt return!


# Datasets:

In this project, I would like to work on [NFL Data](https://www.kaggle.com/competitions/nfl-big-data-bowl-2022), which contains multiple **csv** files for tracking, play, game, and player data for all 2018-2020 Special Teams play. We can use this dataset to analyze statistics of competitions, plays, and players. As I am unfamiliar with the Football game rule, it would be great for me to learn it from this project.

To be specific in this project I would like to know if is there any correlation between far punt return and speed or acceleration. To answer to this question we have to use the **plays** dataset and **tracking** datasets. To do my analysis I am interested in these attributes which have been described below. Please note that Q, O, and C respectively refer to the quantitative, ordered, and categorical.

## Plays Data:
-   _gameId_: Game identifier, unique (C)
-   _playId_: Play identifier, not unique across games (C)
-   _specialTeamsPlayType_: Formation of play: Extra Point, Field Goal, Kickoff or Punt (C)
-   _specialTeamsResult_: Special Teams outcome of play dependent on play type: Blocked Kick Attempt, Blocked Punt, Downed, Fair Catch, Kick Attempt Good, Kick Attempt No Good, Kickoff Team Recovery, Muffed, Non-Special Teams Result, Out of Bounds, Return or Touchback (C)
-   _returnerId_: nflId(s) of returner(s) on play if there was a special teams return. Multiple returners on a play are separated by a ; (C)
-   _penaltyYards_: yards gained by possessionTeam by penalty (Q)
-   _kickLength_: Kick length in air of kickoff, field goal or punt (Q)
-   _kickReturnYardage_: Yards gained by return team if there was a return on a kickoff or punt (Q)
-   _playResult_: Net yards gained by the kicking team, including penalty yardage (Q)

## tracking Data

-   _gameId_: Game identifier, unique (C)
-   _playId_: Play identifier, not unique across games (C)
-   _frameId_: Frame identifier for each play, starting at 1 (C)
-   _nflId_: Player identification number, unique across players (C)
-   _s_: Speed in yards/second (Q)
-   _a_: Speed in yards/second^2 (Q)
-   _event_: Tagged play details, including moment of ball snap, pass release, pass catch, tackle, etc (C)

There are many other attributes in these tow datasets but I think those I have mentiond here are most related one to answer the question of my project.

## Task:
First of all, as I am interested in the return yardage of a play type I would like to visualize the different outcomes by special team contributions to gain return yardage for each team. Then I will try to find out speed and acceleration who does affect punt return.


- Which play type has more contribution to return yardage by each team?
- What is more important for a punt returner, speed or acceleration?
- Is there any correlation between speed and acceleration against return yardage?
- If there is any correlation,  how do different kick length ranges have an effect on that correlation?

## Sketch: 
One of the visualizations that I am looking for is shown below. This chart shows the total kick return yardage for each team consisting of which team results. 

![Special team results](https://github.com/hbarzamini/nflvis/raw/main/sb1.jpg)
Please consider this image a berif scratch and did not contain all team results.
Also we can used stack bar chert  to show the total kick return yardage for each special play type. 
![Special team play type](https://github.com/hbarzamini/nflvis/raw/main/sb2.jpg)

Another visualization I'll employ is a correlation matrix, which I'll use to determine the relationships between the various attributes. As seen in the following photos, two attributes have a higher association if they are darker in color (each atrributes has high correlation by itself so its correlation values is 1).
![Correlation Matrix](https://github.com/hbarzamini/nflvis/raw/main/corr.jpeg)

Another way to show the correlation between parameter is scatter plot, so we can depict the correlation between each two attributes. For each attribute in correation matrix we can create a scater plot. Here you can see one skatch example for KickReturnYardage aginst of speed.
![Scatter Plot](https://github.com/hbarzamini/nflvis/raw/main/sscat.jpeg)

## Ideas

The depiction of the chart can be improved in a number of ways, including by including interactive methods. The user can select any additional attributes for the stack bar chart, like kick length, to compare it between several teams. Additionally, we may allow the user to modify the attributes in scatter plots. Additionally, we may use a variety of channels that the user can choose from to determine whether certain patterns and attributes are related.

# Designs

Please look at the [Designs](https://github.com/hbarzamini/nflvis/blob/main/Designs.md) page for a detailed explanation of my design choices.

