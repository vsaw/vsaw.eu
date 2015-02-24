---
title: "A rough introduction to mathematical games"
date: 2011-09-10
categories:
tags: Math
---

In this Post I'll give a very rough explanation on games from a mathematical point of view. But first let's dig deep to find the essence of a game.

# Essentials: Players and Rules
Obviously a game needs **Players** and **Rules**. If we look at poker for example, the rules define which hand is better and which player deals the cards next or has to pay the blinds. The rules also define the valid **States** of the game, in poker this would be that you need money to play and can not make debts. The set of all valid states is called the **Domain** of the game. Formally one would define the state as an `uint[] array`. Each component holds the amount of dollars Player `i` has.

# "Normal world Rules" = Rules + Objective
And now comes a very tricky thing to grasp. When we teach kids new games we always tell them what they are allowed to do during the game and what the goal of the game is. In Mathematics there is a difference between the rules of a game and the **Objective** of the game. The mathematical Rules of a game just tell us what we are allowed to do. But they don't tell us what we shall do to win the game, or in other words: What terminal state of the game is desirable! For example the objective of poker is to maximize your money! So the most desirable terminal state would be the one where your pockets are full! The other players however prefer a different terminal state, that where their pockets are full while yours are empty. This desire of reaching different terminal states leads to what we would call "gameplay".

But now let's take a look at another example. If we played hide and seek the objective of the seeker may be to minimize seek time while the objective of the hider may be to maximize that time. However we could also change the objective slightly. For example it does not matter when you get caught, instead the winner will be the player who traveled the most. The rules of those two chase games might still be the same since they only define the valid state changes. (how the players are allowed to get from point A to B, e.g. you are not allowed to travel by car, etc.)
Mathematically speaking one would define the rules as a differential equation if the game is continuous or a "similar" discrete map that describes how valid state changes can appear.

# Strategy and Actions
However it is very clear that the hider would play those two games in totally different ways. With objective 1 you could just try find a perfect hideout and then stay there. With objective 2 you want to travel as much as you can.Which brings us to the **Strategy** of a game. A strategy defines what Actions you will take depending on the current State of the game. So, for our Hide and Seek Game with Objective Number 1 a good strategy for the hider might be to find a hiding spot and don't take any action until the seeker comes around.

# Everything is a game
It is pretty clear that any sport consists of Players, Domains, States, Objectives, Strategies and Actions. The interesting thing is however that almost everything is a game. Take the economy for example. The players would be the companies. The Domain of the Game is a little bit harder to define, but one could simplify it and say it is their market share, their money, the amount of their customers and other relevant data. The objectives of the companies might be to win customers, increase sales, gain stock value, etc. The rules of the game will be some legal frameworks, like that you can not bribe someone to buy your product and a couple of other things that you just can't do in business. A strategy of a company and their actions are also very self explanatory. And now we found every component of our mathematical game in economy.

# Why all the talk about games?
So if you are still reading this: Thanks! The reason why I wrote this post is pretty simple: I'm writing my Bachelor Thesis about Pursuit Evasion Games and I wanted to share my progress and thoughts with you guys.

Pursuit Evasion Games are a very special kind of mathematical games with a lot of applications in traffic (and sadly war). And my thesis will cover numerical approximation schemes on the trajectories of a special pursuit evasion game. So stay tuned!
