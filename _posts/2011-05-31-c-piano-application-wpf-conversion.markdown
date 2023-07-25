---
date: 2011-05-31 11:17:22+00:00
title: C# Piano Application WPF conversion
categories:
  - Other Projects
---

After reading a few chapters of [WPF 4 Unleashed](http://www.amazon.co.uk/WPF-4-Unleashed-Adam-Nathan/dp/0672331195) book I decided to convert my piano application to Windows Presentation Foundation. After reading about WPF for 2 weeks it was quite a daunting task, I was in at the deep end but it was the only way to really learn. WPF adds more style to your application with nice graphical effects running on the hardware GPU rather than traditional software CPU using win forms, running on hardware allows faster, more optimised performance. Before the conversion I had a DPI scaling issue with the C# and Python versions of the piano app. running the piano app at different DPI settings would cause buttons and other components to move around due to auto scaling. I did managed to fix this with the win forms by detecting a change in DPI and then resetting positions and sizes however this resulted in messy code. WPF solves this issue and will scale perfectly in any DPI and supports many devices.

My main goal in converting it to WPF was to learn about WPF and XAML; I also wanted to get all the features I originally planned for, such as all 88 keys of a piano.

I am pleased with the outcome and have achieved more than I thought I would. I am glad I got the 88 keys in and can zoom in and out. WPF has a very steep learning curve and did cause a few problems it wasn’t as easy a process as I first thought, I ended up starting a new project and transferring the logic over. Along the way I fixed up some bugs and added more new functionality, I also put the database online rather than local offline.

Features:

- 88 key piano
- Every key can be mapped to a keyboard shortcut
- Dynamic zooming of the keyboard and auto scrolling
- Colour customisation
- Displays the actual musical note you play and animates and fades away
- Previewing a song now plays a note at the right time
- Online database to load other peoples performances, offline database to store locally
- Audio no longer uses DirectSound but now uses Bass.net for more instant, reliable sound
- Settings such as key mappings and colour can be saved and are automatically loaded in on application start

http://youtu.be/fgUJkOMuAAk

[**Windows Presentation Foundation**](http://en.wikipedia.org/wiki/Windows_Presentation_Foundation)
