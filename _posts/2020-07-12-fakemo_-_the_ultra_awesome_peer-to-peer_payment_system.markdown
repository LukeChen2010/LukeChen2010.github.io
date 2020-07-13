---
layout: post
title:      "FakeMo - The Ultra Awesome Peer-to-Peer Payment System!"
date:       2020-07-12 22:57:02 -0400
permalink:  fakemo_-_the_ultra_awesome_peer-to-peer_payment_system
---



FakeMo is the web app that I made for my Rails final project. It is an app that lets you send money to or request money from your peers. FakeMo also maintains a public ledger of all transactions that all users can see. This public ledger is intended to serve as a "credit score" so you can see if the users are credible and pay their bills on time.

Long story short: it is a knockoff of Venmo ;)

The front page of the app has standard login and signup functionality:
![](https://i.imgur.com/wDeSVzp.png)

The signup page contains validations for user inputs. Usernames  must not already be taken:
![](https://i.imgur.com/CoEay8I.png)

The login page provides a place to enter your credentials or sign in with your Facebook account:
![](https://i.imgur.com/s1lRTXn.png)

After logging in, you will be greeted buttons to all of the app functionalities:
![](https://i.imgur.com/l2MNXu8.png)

You can send money or request money from other users:
![](https://i.imgur.com/ZkwUmYQ.png)

All of your activity is displayed on the My Activity page. Links are provided to transactions and user profiles:
![](https://i.imgur.com/YV9MAFI.png)

If another user requests payment from you, you can view the request and click "Accept", which will complete the transfer:
![](https://i.imgur.com/QXOoNxb.png)

However, if you are the one making the request, you will instead see an option to withdraw it:
![](https://i.imgur.com/2TyoD67.png/)

You can also view your friends' activity. This displays the activity of all users with whom you have contacted with,  excluding  the ones where you are one of the parties to the transfer.
![](https://i.imgur.com/xcFxGmt.png)

Clicking on a user's name will take you to their activities. Transaction amounts are hidden when viewing other user's activites. Buttons are also provided to interact with that user. This will take you to a nested route where you do not need to manually select the other user.
![](https://i.imgur.com/xKrpaGo.png)








