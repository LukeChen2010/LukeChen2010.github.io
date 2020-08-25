---
layout: post
title:      "Typing Challenge: JavaScript + Rails project"
date:       2020-08-25 00:58:02 +0000
permalink:  typing_challenge_javascript_rails_project
---


For my final project for the module that covers JavaScript and using Rails as an API, I created a game where users can challenge each other to type various passages as quickly as possible. 

The main menu allows the user to select from available passages. Passages are sorted by popularity, i.e. the number of individuals who have completed it. 

![](https://i.imgur.com/QK3CaAB.png)

The game has front-end JavaScript logic to highlight the text while the user is typing. What the user types correctly is highlighted in green, and mistakes are highligted in red. 

![](https://i.imgur.com/3ZZqzSB.png)

And a highscore is available for each passage:

![](https://i.imgur.com/StnWCuA.png)


The application uses a Rails backend for database access and an HTML/CSS/JS front end. The front end communicates via the back-end's API. The API endpoints are simple. There are three GET routes for retrieving all passages, individual passages, and all highscores for a given passage. There is also a nested POST route to create a new highscore for a passage.

![](https://i.imgur.com/W6T3z3A.png)

One of my main challenges for building this project was the JavaScript needed for manipulate the DOM so that the typing game has good interactivity for a good user experience. This was very new to me since it required creative problem solving and also because DOM manipulation was a new topic that was taught in this module. 

Another challenge was writing the front-end code without the use of a framework. I created my own implementations of dynamic routing using HTML and JavaScript.

Finally, I learned about web security. Chrome and Rails appear to have built-in functionality to prevent cross-domain forgery attacks. Since I am using a Windows computer, I need Rails to run on a Ubuntu VM, whereas my frontend application runs on the main Windows environment. This resulted in Chrome blocking API calls to the Rails backend due to the two running on different frameworks. This was fixed by enabling CORS (cross-origin resource sharing) in my backend Rails application.

Another cybersecurity related hurdle that I needed to clear was the use of authentication tokens. Rails appears to require some sort of authentication for POST calls. This appears to be there to prevent an unauthorized user from using your API endpoints to wreack havoc on your database.


