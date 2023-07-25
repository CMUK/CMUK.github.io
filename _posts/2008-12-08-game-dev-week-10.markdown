---
date: 2008-12-08 08:29:54+00:00
title: Game Dev Week 10
categories:
  - Game Development Techniques
---

This week i have been mainly bug fixing and cleaning my code up. I implemented flooding in the caves this happens if the timer for the tide counts down to zero. This is about 4 minutes for the player to find their way out of the maze. If you don't make it when the tide comes in you have to swim around the maze and the smugglers will be swimming too. I had to rewrite my mini game pickup as it didn't really work well with a timer so now Ive made it you have to pickup the coins without being seen by the smugglers this works well as it introduces stealth into the game. I made my own animation which is a treasure chest wobbling about to attract the player when the player gets to it it stops and plays a still animation if the player uses a crowbar on it it plays the open chest animation and rewards the player with a map to the maze.

I spent alot of time adding more player feedback to the game i did this by taking a photo of my notepad and implementing it in the game as help/tutorial system. After adding this i extended it to make an objectives list  by pressing the back button shows what you have to do. When your progress to a new bit of the game it will say objectives updated so the player is never lost. The bug fixes i had were things like using the magnifying glass and quickly changing item would keep the view zoomed in as if you were still using the magnifier. Another bug was the text and inventory being set with my resolution i fixed this by using scaling so it stays in the same place at any resolution. I added more sound with the smugglers now shouting when you get near them. All pickups now have a nice rewarding sound to them. I also fixed the AI as they were set to follow any navigation point and would walk into walls trying to get to a point across the map i changed this to path node and they now work better. My end matinée is also nearly finished.

[![](/assets/images/UT20042008-12-0808-25-52-89.png)](/assets/images/UT20042008-12-0808-25-52-89.png)[![](/assets/images/notepad.png)](/assets/images/notepad.png)
