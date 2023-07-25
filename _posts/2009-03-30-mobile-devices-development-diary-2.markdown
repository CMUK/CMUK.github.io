---
date: 2009-03-30 19:21:59+00:00
title: Mobile Devices Development Diary 2
categories:
  - Mobile Devices
---

Monday 30th March – Game Logic +AI

Today I started by looking at Layer Manager which allows you to place backgrounds and sprites or any images close or further away from the screen. Behind or in front of each other. This gives the illusion of distance and depth. I created a target that will be used to move across the grids and fire or place ships down. I then went on to implementing user input. The main problem I had with input was with the target getting it to snap to the grid. To fix it, it just needed offsetting and then to be multiplied by the current grid number to move it across. I then set up boundary checks to see if the target had reached the last grid in X or Y, if so then put back to first grid giving a screen wrapping effect.

After that I then implemented firing which would change the cells number to a different image index. The next thing was game logic I made a simple count to check if you had fired three times if so then change it not to place a ship down. It then has to check the current square if there is a ship there then set to the fire index of the image else set to empty. This is the basic check to see if there is a ship and how to handle it.

This is my second milestone reached which was to get a grid with user input working.

I was still missing AI so I wrote some basic AI methods. The first would set up the random three grid squares. This would select a random x number and a random y number making sure to stay in the bounds of the grid. I also made sure to check if the grid contained its own enemy ship image index or the players ship index this was handled in a while loop to which would end if the new random square was empty. This method was called once after the player has placed their three ships. After the player has placed three ships and has now just fired it would go to AI state which was a method to make the AI fire it did the same checks as the initial AI ship place method did.
The next part was to handle if you hit the enemy’s ship. This was a simple method that would get called in the fire method, it checked the current square if enemy the set to destroyed image index else set to empty. I did the same check for the AI but checking my ship index and it worked great apart from the game was becoming more and more like minesweeper.
This was my second phase 1st milestone reached which was to get AI working and simple game logic.
