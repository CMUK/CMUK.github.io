---
date: 2008-10-30 11:46:31+00:00
title: Game Dev Week 4
categories:
  - Game Development Techniques
---

This weeks game dev was about unreal scripting. We learnt that we could extend classes and make our own pickup class and still be able to use the original scripts. We looked casting in unreal and the benefits of using scripting even though it is still 20 times slower unreal only uses about 5% scripting the rest C++. This weeks tasks was to get a simple pickup mini game implemented this would get us use to looking through unreals codebase and seeing how everything inherits and extends from each class. Getting the basic pickup into my game was the easy part i did this using a touch function which enabled it to be picked up by the pawn. The next bit was to get it displaying on screen "Collected Pickup" this was the hard part my HUD class was very bare and needed to extend the HUDBase class to gain more functionality. I spent a good 10 hours looking for a way to display messages to the screen from my pickup i started by seeing what gets called when the touch function happens and followed it back to HUD classes on paper this was about 12 parent classes. The solution was simple it was extending my HUD to extend from HUDbase to inherit one simple thing "DisplayLocalMessages(Canvas);" this was all i needed to get my pickup displaying text to screen but as unreal codebase is large and confusing at first it took me 12 hours to work it out. I did however gain a good knowledge of how different parts are linked and found some pretty interesting stuff that i may use later on. Here is some screenshots of my mini game working

[![](/assets/images/Final.png)](/assets/images/Final.png)[![](/assets/images/failed.png)](/assets/images/failed.png)
