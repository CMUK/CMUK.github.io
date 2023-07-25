---
date: 2010-07-30 11:34:34+00:00
title: Flash Game Fruit Frenzy
categories:
  - Flash
---

[![](/assets/images/2017/10/froot.jpg)](http://cm.1free.ws/)
[![](/assets/images/2017/10/froot1.jpg)](http://cm.1free.ws/)
[Click here to Play](http://cm.1free.ws/)

Fruit Frenzy is a flash game built on my previous flash game buster, It does just look a lot like a Reskin but there is actually a lot more to it. The main feature I wanted buster to have all along was a dynamically resizing grid, The reason I couldn’t manage this the first time round was due to time constraints, work and just general lack of experience with flash and action script. This time around I’ve managed it, I am very pleased with the way Fruit Frenzy has turned out Its still very much experimental and a learning exercise for me to get more familiar with flash and action script. It suffered quite bad feature creep which was fun and challenging, but a real headache because it created so many new bugs some as severe as crashing the game, most of them were quite rare and hard to track down, a lesson learned the very hard way luckily I had the time to fix them.

So what are the main features of Fruit Frenzy:

- **Dynamically scaling grid** – The grid will add extra rows and columns on remove rows and columns in real time, this changes the gameplay a lot allowing more fruit and eventually making it harder as more different types of fruit gets introduced depending on your skill level.
- **Skill Level** – The game features 8 levels of skill, at each level a new type of fruit is added to random pool of the game, This makes the game harder or easier for the player.
- **5 random events** – Theses take place randomly throughout the game, The random events are as follows:

  - Bird – The bird flies over and marks some fruit bad meaning you can’t swap it for a certain amount of time.

  - Monkey – The monkey will throw 3 bananas and randomly tag 3 sets of cells making them un swappable for a certain amount of time making it very frustrating for the player.

  - Blackout – The fruit gets darker making it harder to see the fruit.

  - Underwater – The game board gets submerged making it hard to see the fruit beneath similar to blackout.

  - Swaps – get 3 or more swaps signs and the board randomly swaps the fruit about, can be very useful if used on a big grid, can also get in the way.

- **Day/Night cycle** – A nice transitioning background fading from day to night and back, very sutle but nice touch to give the game some atmosphere.
- **Frenzy Meter **– Gain frenzy by quickly matching fruit and gaining combos, Fill the meter to the top to activate frenzy, Frenzy allows the player to speed up swapping and animations almost like a reverse adrenaline effect, The player will be able to match and score faster while frenzy is activated, The player will be constantly battling the meter as it loses frenzy every few seconds.
- **One click swap** – swapping fruit now only requires one click for the fruit you wish to swap and then a mouse hover over the other fruit to activate the swap, This takes away some of the repetitive clicking and makes it more fluid gameplay
- **Dynamically adjusting difficulty** – This has been the real challenge, developing a way to scale the difficulty to the player, The way I achieved this or have come very close to is by dumping out statistics about the game, exposing variables to a debug panel to see values changing in real time has helped me gauge how well the player is doing or responding, I used various calculations to come up with a way to measure success which is all based around timings and so far has been pretty excellent. The grid will scale up/down the skill level also increased/decreases
- **Stat logging server side** – This has been a real frustration from the start, After learning flash doesn’t like http/ftp or any type of connection without the support of AIR, I did manage to find another way which is loadvars, This required me setting up a web server and brushing up on some php. Essentially the flash communicates with the php which in turn takes vars sent and outputs it to a text file stored on the server. This was all working great until I tested the flash game in html suddenly it wouldn’t log anything, on further investigation it looks like it’s coming up as a security threat and the browser is blocking the communication. A real shame as this was going to dump out scores and various stats at the end of the game, this data would have been invaluable and could have been averaged out and be sent back to the game as the default variables making the players balance the game on others experiences.
