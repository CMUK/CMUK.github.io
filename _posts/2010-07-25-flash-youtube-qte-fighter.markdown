---
author: cmuk
comments: true
date: 2010-07-25 16:47:20+00:00
layout: post
link: https://mckellar.wordpress.com/2010/07/25/flash-youtube-qte-fighter/
slug: flash-youtube-qte-fighter
title: Flash youtube QTE Fighter
wordpress_id: 472
categories:
  - Flash
---

QTE fighter is an experiment I came up with after stumbling upon YouTube’s API for Flash, integrating YouTube’s API I was able to stream videos off YouTube into my flash so I thought what could I make with this, Originally I started off with a jigsaw puzzle game with the video in the background and on the pieces, I managed to get this working however I couldn’t get any drop shadow or outline on the pieces which meant total confusion for the player that an I couldn’t store the swf on a local server it needed YouTube. So next thing I came up with was a scary point and clicker on rails, I got this up and running and had ghosts alphaed flying in at key parts in the movie this was kinda creepy, I then thought about QTEs and made QTE fighter, This project only took a day to do and I say a project because it’s not really a game well it has parts which you could argue define it as a game such as the score a start and end, but I like to think of it more as an interactive movie. So how does it work well I get the current seconds played from YouTube and write down key seconds where action happens and a QTE should trigger, then I simply put these in an array and loop through checking if secondsPlayed >= QTETime[i], if it is then its then pause the YouTube video and launch a QTE. Simple, if the player should fail the QTE then it seeks back 6 seconds and plays, if the player passes it resumes play. The hardest thing about this project has been the buffering of YouTube there was a bug where if it was the first time you went on YouTube there would be no cached video and it would have to fetch it this would cause a bug where currentLoadedBytes would be the same as totalBytes for one second so it would launch the ending. To get around this it just waits 3 seconds while loading to make sure. The other issue was what if the player has a really slow connection and its starting and stopping all the time, Well to get around this I just did a simple pre loader to say if(currentLoadedBytes >= totalBytes/2) then play. This is saying if its half way loaded of the total amount of bytes for the video then play. I had a lot of fun making this especially as it’s never been done before if you want to check it out you can play it [here](http://www.kongregate.com/games/CMUK/qte-fighter) it also has leader boards for when you finish.

[![Click to Play](https://mckellar.files.wordpress.com/2017/10/qtefighter.jpg)](http://www.kongregate.com/games/CMUK/qte-fighter)
