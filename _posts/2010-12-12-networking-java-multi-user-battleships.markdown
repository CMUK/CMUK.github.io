---
date: 2010-12-12 18:35:11+00:00
title: Networking Java multi user battleships
categories:
  - Java
---

In this project I developed a multi user network application in java, my application was the game of Battleships, It supports multiple users and have yet to test it to its limit, In theory it should support as much as server can handle, I’ve only tested with 5 users all playing same game which works perfectly.
It features:

TCP - for the game data, sending and receiving data so it’s reliable and guaranteed delivery for uninterrupted game play.

UDP - for the chat room.

Chat room - for players waiting to go into a game, Users can send a challenge to another user and get put into a game with them, multiple users can challenge each other to get in the same game.

Admin/Server panel - Can see all game related messages which are hidden from normal clients, and also chat messages, with the ability to kick players out of the game. Admin also has forced commands such as entering everyone into the same game of battleships; this was used for debugging purposes.

Swear filter - to prevent user's from disrupting other user’s experiences.

Threading – used for listening for connection both UDP/TCP, receiving messages.

Application layer protocol – used for the game logic and interfacing with the server messages, a state machine was used to control the flow of game play and structure the logic easier.

[![](/assets/images/2017/10/battleshipsgame.png)](/assets/images/2017/10/battleshipsgame.png)
