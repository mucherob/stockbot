### About Project

The purpose of this project was to create an AI AGENT. I was hoping to create an agent that
would use sentiment scores from financial text to suggest what stocks to look into. I went on to
include stock prices as well with the hope of allowing the agent to learn if sentiment scores
(positive or negative) would affect the stock price (whether it increases or decreases).

What I currently have is an agent that can retrieve several news headlines from NewsAPI, use NLTK to
perform sentiment analysis, and then calculate a sentiment score. If the score is greater than 0.05 then
the stock sentiment for the day is tagged as having positive sentiment and negative if the score is lesser
than -0.01. Everything else that is in between that range is said to be neutral. Since the agent retrieves
a lot of news headlines, the daily sentiment is known as a compound score.

Once all the analysis is done, the agent returns a response that includes the average sentiment score,
whether it is positive, negative, or neutral, the reasons why the stock got that sentiment score
(the reasons are just the headlines the agent was able to pull), the current stock price from yfinance,
and a prediction of whether the price will increase or decrease depending on the sentiment score.

If a user wants the agent to track this stock, the agent will active its scheduler (which allows it to run
at a specific time each day) and create a data file to store the headlines of the day (reasons
for sentiment score), the price, the sentiment score, and the prediction (increase or decrease).

I am hoping that this data file will allow the agent to compare sentiments, prices, and predictions
between days and hopefully, it will allow the agent to learn to make better predictions. However, this
part is still in the works

## Workflow

1. When the agent is initialized, it will ask the user to enter the stock ticker.
   
2 (a). It will use the ticker to search the News API for news and analyze the content that is returned.

2 (b). At the same time, the stock will retrieve the price from yfinance.

3. The agent returns a response that includes the stock price, the sentiment score, and whether it is positive,
negative, or neutral, the price prediction (whether it will increase or decrease) and whether the user wants
to track this stock
4. If the user says yes to tracking the stock, the agent will create a data file where it will store the current
information returned, and then add to that document daily.

## Conclusion

I believe this project is far from over as there are aspects of it that are not working as they should. In
addition, I have struggled to test if the agent will run daily according to the scheduler, so I cannot say
if that feature works as intended or not.

