## Stockbot: Financial Sentiment Analysis (work in progress)

Stockbot is a sentiment analysis model that uses Gemini Flash LLM and NLTK to analyze financial text.
The model is meant to serve as an AI Agent that is able to retrieve daily news stories about a specific stock
along with the stock price, and try to use a combination of sentiment score and price to suggest if the stock price
will increase or decrease because of public sentiment. Hopefully, by establishing a connection between sentiment and price,
the agent will be able to provide suggestions on potential stocks to consider looking into.

It's worth mentioning that the price prediction won't be 100% accurate because many factors play into determining the stock price.
However, the goal is to have the agent appreciate the relationship between sentiment and stock price and use that to suggest stocks or 
even portfolios to look into further.

### Furthermore, the agent itself still has a long way to go because there are methods that are currently within the script that have not been tested yet and improvements that can be made to make the agent whole.

## Installing

The agent (in its current state) has been working best in Google Colab. This makes it easier to download the necessary packages and dependencies.
However, Colab is cloud-based, it's bound to shut down if it's not active for too long. This makes it harder to host the agent on Colab because the agent needs to run daily to perform its tasks.

As for running the agent itself, all you need is the stock_agent.py script. If you are working in Colab, I recommend separating the code into chunks, one dedicated to the pip installations, one for importing the dependencies, one for the chatbot class itself, and lastly one to initialize the Chatbot.

## Requirements

For this agent to work, you will need two (2) API keys, one from Google for the Gemini Flash model and one from NewsAPI. Without the API keys, the agent won't work.
