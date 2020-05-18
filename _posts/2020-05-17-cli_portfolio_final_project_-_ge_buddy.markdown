---
layout: post
title:      "CLI Portfolio Final Project - GE Buddy"
date:       2020-05-17 23:37:34 -0400
permalink:  cli_portfolio_final_project_-_ge_buddy
---


## Introduction

For my module 1 final project, I developed a command line interface application in Ruby called GE Buddy. The application is designed to work in conjuction with RuneScape, which is a massively multiplayer online role playing game (MMORPG) developed by Jagex, Inc in the United Kingdom. The application helps players track the historic prices of items in RuneScape, input in-game transactions, and provides analysis of the user's transactions. 

RuneScape is a game which the player controls an in-game character. It is set in a fantasy world with a medieval-theme. The game features an open-world, sandbox gameplay with many activities that the player can participate in. The game was originally released in 2001 and has been continually updated with new content ever since. The game is free to play with limited content, with the full game locked behind a paid subscription model. 

The game can be accessed here: https://www.runescape.com/

## Investing in RuneScape

A core feature of RuneScape is the economy. Players can trade with one another using either other items (bartering) or though currency. The economy operates on a 100% laissez-faire capitalism model, with supply and demand dicating prices. Most transactions are handled by the Grand Exchange (GE), which is a marketplace where players can list items for sale and place bids on items to buy. Transactions are awarded to sellers who list items for sale at the lowest price and to buyers who place bids at the highest price. Prices change daily depending on the average buy/sell price and quantity traded. The GE also displays a "guide price", which is the average price of the item. In fact, there are many analogies between the GE and the real-life stock market. 

The GE also provides opportunities for players to make money through investment. Since item prices are fluid, players can exploit market trends to buy items when prices are are low and sell them when the prices rise. The game maintains a history of prices going back 180 days. A savvy players, like a savvy investor, would view item price history and identify trends to decide what items to invest in and when to buy/sell items. 

*Figure 1: Example of guide price in RuneScape. This is for item "White berries". The Y-axis represents price, and the X-axis represents date. The blue line charts daily prices. The orange line is a "30-day average", which is the average of the last 30 days.*
![](https://i.imgur.com/9Pewi4j.png)

## Introduction to GE Buddy

RuneScape has an API to access its item database. It can return details about the item and also its price history. API documentation and endpoint URL's can be found here: https://runescape.fandom.com/wiki/Application_programming_interface

Because there are many analogies to the RuneScape GE and the stock market, investors also could make use of tools similar to the ones available to real-life investors. This is what inspired me to develop the GE Buddy app.

The application allows the player to:
- Create an investment portfolio
- Add items to a watch list
- Retrieve 180-day price history of items
- Add transactions that were made in the game
- Calculate portfolio performance: amount spent, amount sold for, and return-on-investment

*Figure 2: GE Buddy main menu*
![](https://i.imgur.com/rgCq2dn.png)

## Object Model

*Figure 3: classes used*
![](https://i.imgur.com/2vtACrR.png)

GE Buddy is written with an object-oriented architecture. The following classes are used:

1. API_Bootstrap.rb

Contains static methods to abstract calls to the API

2. CLI.rb

Contains the code to run the command line interface application.

3. Portfolio.rb

Stores a user's investment portfolio. Stores items in a hash and transactions in an array. Contains methods to calculate portfolio performance. 

4. RuneScapeItem.rb

Stores information about an item in RuneScape. All item information is obtained by calls to the API.

4. Transaction.rb

Used to store information about a transaction made by the player: item, type (buy or sell), quantity, price. 

## Usage

Follow the in-game menu prompts. Enter your selection with the numbers 1-6:

1. View items in portfolio
2. Get price history 
3. Add item to portfolio  
4. Add transaction        
5. View performance       
6. Exit

Description of functions:
   
1. View items in portfolio

Prints a list of current items in your investment portfolio.

2. Get price history 

Select an item in your portfolio to view the last 180 days of prices. The game updates prices once per day.

3. Add item to portfolio  

Add an item to your portfolio. You must know the item's ID number. You can obtain each item's ID number by searching the Internet.

4. Add transaction    

Add a transaction that you have completed in the game. Select the item from your portfolio, enter whether or not the transaction represents a sale (y/n), the quantity of items bought or sold, the total value of the transaction. 

5. View performance  

View the overall performance of your portfolio as well as a breakdown of each item's performance. The program will display cost, revenue, and profit margin. Profit margin is expressed as a percentage and is defined as revenue minus cost all over cost. 

6. Exit

Exit the program.





