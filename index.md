# FIFAI

### By Eshaan Lumba, Kenneth Ochieng, Jett Bronstein and Aidan Garton

## Introduction

The Premier League is considered one of the most exciting soccer leagues in all of the world. Given soccer is the most popular sport in the world, Premier League games are some of the most watched cable events in the world, far surpassing all other sports. Like other mainstream sporting leagues, the Premier League attracts enormous attention within the gaming industry. However, there are a multiplicity of factors that makes predicting the victor of a Premier League match impossible...as of now. We, as a group, will construct a comprehensive neural network to successfully predict the winner of Premier League matches on a consistent basis.

Soccer is regarded as one of the most unpredictable sports globally, so building a Neural Networks model to accurately predict the scorelines, or at least the end results of English Premier League soccer matches is a challenging, yet exciting task. 

There has been some success with predicting the results of soccer matches in the past using the Poisson distribution, but we aim to improve on this accuracy and take it a step further by predicting scorelines. 

We will try to use a more robust dataset with more datapoints along with a more optimized algorithm to improve upon previous results. 

Ideally, we would like to have an algorithm that can accurately predict the scoreline, and along with that, the result of the game; we could even extend it by including the most likely goalscorers. 

We acknowledge that predicting the exact scoreline of a Premier League match is a very difficult problem, but if we could predict at least the result with an accuracy of above 50%, it would be a success. 

If we are able to build a successful model, we realise that it might lead to an increase in the amount of bets made on Premier League matches, leading to those consequences faced by excessive gambling. 

## Literature Review

### 1. Soccer Result Prediction Using Deep Learning and Neural Networks
This paper compares several different score/outcome prediction strategies for various sports and leagues (including the NBA and soccer matches) and proposes an RNN (recuring neural network) architecture to predict match outcomes in the English Premier League. Taking as parameters a team's statistics from past seasons (and updating data by adding current games of a season) the RNN constructed in this paper ended up with around an 80% accuracy prediction of match outcomes. Some parameters included were points gained by the home vs. away team (1 for draw, 3 for win, 0 for loss), goals scored by the home vs. away team, winning and losing streak of the home vs. away team (a streak of >3 and >5 were tracked). This paper concludes that RNNs provide a better architecture for the problem of score prediction over other architectures and provide measurable evidence for such in soccer matches in the EPL. 

### 2. Using Deep Convolutional Neural Networks to Predict Goal-scoring Opportunities in Soccer
This paper trained a NN on Bundesliga game data to predict the chance of a goal scoring opportunity based on a given position of the game's players and the game ball. Using 2-dimensional data gathered from the Amisco multi-camera system, this network showed as a high as a 67% accuracy rate for predicting goals. This paper coul be helpful if we wanted to analyze past scoring chances, positional data, and etc... from past games played by a team in order to provide a prediction of current and future game outcomes.

### 3. Predict soccer matches with 50% accuracy
In the article, the author used the Poisson Distribution and Poisson Regression through Python to predict the results of the last 10 matches of the 2018-2019 Premier League season. It was quite clear to see that for that season at least, the Poisson distribution very clearly matched the results of the whole season. The key data points he used were, for a certain team, the likelihood that they would score, the likelihood that they would concede and the likelihoods that they would score if they were a home or away team. It resulted in a success rate of almost 50%. The author also suggested using more data points such as form, more matches and correctness of under/over underestimating results.

### 4. Football Match Statistics Prediction using Artificial Neural Networks
This paper discusses a soccer match statistics prediction NN framwork. The NN is trained with data from two Bundesliga teams (Bayern Munich and Borussia Dortmound). They analyze various input factors selected to help the Neural Net detect patterns and predict match statisitics such as the winning team, goals scored, and bookings. Their data shows that the Neural Net is able to predict the match statistics with a higher accuracy than an existing if-else case framework (Football Result Expert System (FRES) used to predict American soccer. According to their analysis, there are several key factors which affect the outcome of matches and a NN can be trained to learn from previous history to predict future outcomes. These factors include: transfer money spent by a team in a season, a team's UEFA co-effecient (for each team participating in the champions league), year of match, league rank, goals scored and conceded,  wins and losses , home advantage etc. They advice that each of these factors have certain limitations in their application and some teams generally have more data than others because of their length of participation in competitions. A few of these factors can also only be applied within a league in a single country. This paper could be useful to help guide our choices when considering the type of data we need for teams and also the labels we need to train a NN. In addition, we can learn from their backpropagation algorithm and normalization of data points for further improvement. 

## Project Update 1

### Software
We will use a combination of PyTorch and FastAI: https://pytorch.org/, https://docs.fast.ai/

### Our Dataset
We will use a combination of "English Premier League stats 2019-2020" (https://www.kaggle.com/idoyo92/epl-stats-20192020?select=epl2020.csv), "2021-2022 Premier League Stats" (https://fbref.com/en/comps/9/Premier-League-Stats) and "English Premier League (football)" (https://datahub.io/sports-data/english-premier-league#readme).

### Overview of project
We want to use a recurrent neural network along with long short-term memory since we want to keep track of patterns and form. Our inputs will be a vector of floating point values (expected goals for and expected goals against for the home team for the particular game). We will be performing classification. Our algorithm will predict the most probable scoreline out of a multitude of options. Hence, our output will be a vector of floating point values that hold the probablility of the match ending in a given scoreline. 




