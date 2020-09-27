---
layout: post
title:      "Stock Market Playground - React/Redux "
date:       2020-09-27 22:17:03 +0000
permalink:  stock_market_playground_-_react_redux
---


For my final project in the bootcamp, I decided to make a redux'ed (pun intended) version of my Sinatra project, which is a virtual stock trading game. I really liked the idea of the stock trading game, but my Sinatra version lacked the polish and interactivity that I would like for a project that will be part of my portfolio. It had no JavaScript and instead relied on routes to change the views in response to user input.

Users can grab a quote using the "Get a Quote!" interface. The prices and information are pulled from a third-party API:
![](https://i.imgur.com/pmSKtcW.png)

A green badge with "Success!" will display when a purchase is successfully made. If the user attempts to spend more money than what is in their account, it will display "Insufficient balance!"
![](https://i.imgur.com/CdjW92O.png)

The NavBar at the bottom of the page displays either total stocks owned or a list of all individual transactions:
![](https://i.imgur.com/OJ70Xco.png)

![](https://i.imgur.com/MuyxBGy.png)

Clicking on one of the rows in the the "Your Stocks" view opens an interface to allow the user to sell that stock. Attempting to sell more stock than what the user currently owns will return an error:
![](https://i.imgur.com/B1Ethvm.png)


