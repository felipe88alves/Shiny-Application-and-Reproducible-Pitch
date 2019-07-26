---
title       : "Shiny Application and Reproducible Pitch"
subtitle    : "Course Project: Womens World Cup Championship Analysis"
author      : "Felipe Alves"
date        : "26/07/2019"
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : []            # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides
---

## Goal

  - This presentation was developed as the Course Project of the Developing Data Products course of the John's Hopksins Data Science Specialization, this is an online course hosted in Coursera.

  - The goal of the Project is to develop a Shiny App and to produce a 5 page presentation that explains how the application works and what are its capabilities.

### Dataset:

  - The Dataset used in the project was provided as part of the TidyTuesday, a social data project in R that provides weekly datasets from the RD4S online learning community.

  - The data used contains historical information on the Womens World Cup. It includes the final score and win/loss status data from 1991-2019. The data can be found in the following [Link](https://github.com/rfordatascience/tidytuesday/tree/master/data/2019/2019-07-09).
  
  - The Shiny application developed for this project allows its user to analyze the chosen dataset.

  - The data was processed so as to individually id each match, to map team acronym with team name and to provide the challenger information for each row. The full processed data can be found in the last slide.

```
## Observations: 568
## Variables: 11
## Groups: team [36]
## $ year                <int> 1991, 1991, 1991, 1991, 1991, 1991, 1991, ...
## $ team                <chr> "CHN", "NOR", "DEN", "NZL", "JPN", "BRA", ...
## $ score               <dbl> 4, 0, 3, 0, 0, 1, 4, 0, 2, 3, 0, 5, 4, 0, ...
## $ round               <chr> "Group", "Group", "Group", "Group", "Group...
## $ yearly_game_id      <fct> 1, 1, 2, 2, 3, 3, 4, 4, 5, 5, 6, 6, 7, 7, ...
## $ team_num            <dbl> 1, 2, 1, 2, 1, 2, 1, 2, 1, 2, 1, 2, 1, 2, ...
## $ win_status          <chr> "Won", "Lost", "Won", "Lost", "Lost", "Won...
## $ game_id             <chr> "1991_1", "1991_1", "1991_2", "1991_2", "1...
## $ country             <chr> "China PR", "Norway", "Denmark", "New Zeal...
## $ opposing_team       <chr> "NOR", "CHN", "NZL", "DEN", "BRA", "JPN", ...
## $ opposing_team_score <dbl> 0, 4, 0, 3, 1, 0, 0, 4, 3, 2, 5, 0, 0, 4, ...
```


--- .class #id 

## Data Visualization Project: Women's World Cup Data

The shiny app contains two tabs:

1. The first tab contains:
    - A Barchart graph enables the visualization of all Game Results separated by Year and Tournament Group.
    - A dynamic table provides Game Result Statistics for each Selected Team.
    - The Barchart and the dynamic table can be filtered using the following widgets:
        - A slider for selection of Year(s).
        - A dropdown box for selection of a specific Team or all Teams.
        - Checkboxes for the selection of the Tournament round.

2. The second tab contains a dynamic table containing the full dataset. This dataset can be ordered and filtered by the user.

### Shiny App Capabilities

 - The two following slides will display some of the shiny app's capabilities.

--- .class #id 
## First Tab - Wins and Losses
The section below is separated as such:
 - Question.
 - Widget instructions on how to reach the answer.
 - How to interpret the graphs and table to prove the answer.
 
 1. Who where the winners of the World Cup from 1991 to 2019?
    - Widget:
        - Years: 1991 to 2019
        - Team: All Teams
        - Tournament Round: Final
    - Result: Check the graphs for who scored more in the final game of each year

 2. What team had the highest goal difference during the World Cup of 2015?
    - Widget:
        - Years: 2015 to 2015
        - Team: All Teams
        - Tournament Round: (Select All Items)
    - Result: Check the table. Order the Goal Difference from highest to Lowest.
 3. In what position did German team finish during the World Cup of 2015?
    - Widget:
        - Years: 2015 to 2015
        - Team: Germany
        - Tournament Round: (Select All Items)
    - Result: Check the graph. Find the highest Tournament Round. Check if the team Won of Lost the highest Tournament Round.

--- .class #id 

## Second Tab - Full Dataset

The section below is separated as such:
 - Question.
 - Search bar instructions on how to reach the answer.
 - How to interpret the table to prove the answer.
 
 1. What was the result of the Italy vs Germany Womens world cup match of 1999?
    - Insert the following in the Search Filter:
        - ITA GER 1999
    - Result: Check the win_status column for the filtered items.
    
 2. Which team won third place in the 2007 World Cup?
    - Insert the following in the Search Filter:
        - Third 2007
    - Result: Check the team and win_status column for the filtered items.
