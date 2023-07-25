---
date: 2008-12-17 08:05:58+00:00
title: Game Dev Week 12
categories:
  - Game Development Techniques
---

This week i finished my game completely, Going from knowing nothing about Unreal Script/UnrealEd to making a total conversion in 12 weeks was quite a journey. I am pleased with the way it has turned out and have learned a lot during the time. I tried to get my famous five game as close to my vision as i could.  This week was about play testing i got three people to sit down and play my game this was interesting to watch as i had been testing it for so long and knew where to go and what to do. Watching people play may game gave me a different view on my game firstly it took longer to complete which was good as it made it more challenging. Secondly there was a few bugs that i hadn't found before, This was really important as one of the bugs was very serious. Lastly the general view was my game was fun and challenging to play this was good too hear as it makes it all worth it. One thing i noticed was no one took any notice of the objectives and worked them out on there own i have fixed that now by forcing the objectives to display when they get update at different stages of the game. The maze bit in my game was also interesting as everyone seemed to head north and get lost but manage to find there way out without any help.

###

[googlevideo=http://video.google.com/videoplay?docid=-1833918377477334664]

### **Bugs found/fixed during play test**

1. Turning the magnifier on and picking up the key would cause the view to get stuck in first person and not allow to cycle through the inventory

2. Cut scene music playing hard to hear voices

3. Looking in first box and getting the torch straight away would cause the key to disappear completely. Fixed by making the torch spawn instead of setting the values manually

### **Bugs found/fixed**

1. Turning the torch on would interfere with QTE puzzle triggering it off. Changed the collision on the torch light to fix this

2. Looking in a box with the magnifier and finding the torch and picking up the key at the same time would cause torch or the key to disappear

3. When getting caught by smugglers wouldn't always reset you back to the start this was due to both smugglers being with each others radius trying to reset each other.

4. Fluid surface area stuck

5. Matinée end sequence character getting stuck

6. Chance of not finding a torch in the box

7. Looking in a box,turn on the inventory, look in the same box already searched and the inventory would get stuck

8. Have inventory open and look in all boxes would cause the torch not to spawn

### **Overall Changes**

1. Added subtitles to matinée sequences

2. Re done the ending with movers,items,character animation

3. Random falling rocks

4. Waterfall near the end with sound

5. Re position of the chest containing the map in the maze

6. Sound redone to both L+R speakers

7. More sounds added Fire,water ambiance ,Anne speech,Julian speech

8. Lighthouse map room fixed matinée

9. Added furniture Radio,Chess board,Paintings

10. Code cleaned up no warnings or errors on compile

11. All items now needed to progress down into the caves

12. More player feedback on mini games

### Features Cut

1. Mischief monkey playable character

2. Underwater Puzzle rooms

3. Push block puzzles

4. Central cave leading off to different caves

5. Item combining

6. Seagull intro matinée

7. MGS type overhead maze puzzle

8. Point and click style interface

9. Karma bridge sequence
