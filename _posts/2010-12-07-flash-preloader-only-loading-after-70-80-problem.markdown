---
date: 2010-12-07 18:00:33+00:00
title: Flash Preloader only loading after 70-80% problem
categories:
  - Flash
---

After adding lots of music to a flash project the file size grew, I looked at pre loaders which show progress of loading the flash game, I found a lot of good tutorials and the basic theory and implementation of loaders and created a nice simple flash loading bar, however it would only show after 70-80% loading? After spending a while trying to figure out why and thinking it was my coding, I searched the internet and found various forums with the problem, and the problem is to do with linking and exporting on the first frame.

Objects such as movie clips may be dynamically created therefore the application needs to make sure these are ready for frame 1 as it doesn’t know when you are going to use them. This is why the game does not show the progress bar until 80% because assets need to be loaded before frame 1.

Solutions to this problem are:

1.      Create another blank SWF file only containing the assets needed for export, and then load this in to the load bar pre loader. Refer to moved assets using the \_root. Or \_level01 depending on how you are loading them in.

2.      Quick solution go through library and go into the assests linkage properties and untick "export in frame 1", Note this solution will not work for Sounds using the attatchSound to embed them into the SWF.

3.      If the asset is a sound/music which its most common problem of the preloader and you are using attatchSound to embed the sound into the SWF, then add new layers for each sound and place the event for that layers first frame to be the sound you want, add a stop all sound() so it won’t play straight away. This will allow them to load on frame 1 but not before frame 1 allowing the preloader to work correctly.
