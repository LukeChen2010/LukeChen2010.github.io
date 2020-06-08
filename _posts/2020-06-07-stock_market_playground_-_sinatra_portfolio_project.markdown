---
layout: post
title:      "Stock Market Playground - Sinatra Portfolio Project"
date:       2020-06-08 02:19:38 +0000
permalink:  stock_market_playground_-_sinatra_portfolio_project
---


We all had quirky interests when we were growing up. For me, it has always been watching the news. Unlike just about every child my age, I loved tuning into the evening news to keep up with what was happening in the world: Yasser Arafat, the conflict in the former Yugoslavia, the persecution of Falun Gong, or Bill Clinton's scandal which I was probably too young to understand at the time. 

Of course, I was also exposed to economic news at a very early age. Living through the recession in 2001 and 2008 gave me an appreciation of how all lives are impacted by the global economy. As a high schooler during the great recession, I began learning and paying more attention to economics. That also included signing up and playing a virtual stock market game. I was too young and didn't have the funds to play in the real stock market just yet. 

My Sinatra portfolio project is just that. It is my attempt at recreating a stock market game. The game requires users to create an account to start playing. Each player is given $100,000 to start. Players may use that money to purchase stocks. Stock prices are updated in real time via an API. All game data is persisted via an ActiveRecord database. A leaderboard adds a competitive touch to the game.

I kept the models library simple with just a User and Stock class. These classes inherit from ActiveRecord, and instances of these classes are persisted to the database. There is a has_many relationship where a User has many Stocks. There is a third class called StockQuote. This class is used to make calls to the API and obtain information about a stock symbol. Instances of the StockQuote class are not persisted in the database since the information stored in that class will change with the market.

The controllers and models provide the business logic behind the application. Players may not incur a negative balance in their account by spending more money than what they have. Players attempting to sell stocks may also only sell up to the quantity which they currently own. The has_many relationship between User and Stocks also required more logic than I had anticipated. If a user owns, for example, 10 shares of Apple stock, and the user purchases 10 more, the application will find the existing Apple stock object that belongs to that user and add 10 to the quantity owned. I had intially implemented the code where a new Stock object would be created with each purchase, but this would create difficulty with selling stocks. If the user in the example wanted to sell 15 of his/her 20 shares of Apple stock, how would the database need to be manipulated to handle this request?

One limitation of the app is the free version of the API. The free version allows for up to 30 calls per second. This may seem like a lot, but can be easily exceeded even on a small-scale deployment. For example, when generating the leaderboard, the application will make one call to the API for each stock owned by each user. If you have 10 users who own 3 stocks each, that will exceed the call limit. 



