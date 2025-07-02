# Twitter-Stock-Sentiment-Analysis
This tool trains a NLTK Naive Bayes classifier on positive and negative tweet data then collects, cleans, and classifies the sentiments of live and trending tweets about specified stock tickers to gauge overall market sentiment and its effects on stock price.

## Modes

### Top tweets
`topOnly("tsla", "popular", 100)`

Collects the specified number of tweets for the specified ticker symbol to get the overall sentiment for the stock at the given moment.

#### Options:
`ticker`: the ticker to look up

`mode`: 'popular','recent', or 'mixed'

`num`: the number of tweets to get

### Stream
![Example Graph](https://i.imgur.com/Xn8906P.png)
`stream("tsla", 60000, 60, 1)`

Uses Tweepy stream to collect and calculate the sentiments for live tweets for a specified ticker and plots them against a normalized price curve to see the relationship of twitters sentiment on the overall price of the stock over time. Could be used to find potential good times to invest.

### Options:
`ticker`: the ticker to stream

`interval`: how often to update the graph (in milliseconds)

`numpoints`: number of points to display on the graph

`weeksback`: how far back to go for the high/low to normalize stock data

