---
author: cmuk
comments: true
date: 2016-08-01 10:23:23+00:00
layout: post
link: https://mckellar.wordpress.com/2016/08/01/xamarin-game-emulator-collection-wip/
slug: xamarin-game-emulator-collection-wip
title: Xamarin Game Emulator Collection (WIP)
wordpress_id: 782
categories:
  - Xamarin
tags:
  - Csharp
  - HTML5
  - MVC
  - WIP
---

While creating my first Xamarin app ([games collection](https://mckellar.wordpress.com/2016/07/10/xamarin-games-collection-wip/)) I thought wouldn't it be cool to embed a mega drive emulator into the app in html5 and be able to play some of the retro games, I looked around for emulators and sure enough people had ported emulators to html5.

I then bought a Nvidia shield 4K TV box on amazon prime day and found it to be the most powerful android games box to date due to its insanely powerful Tegra X1 graphics chip, It can emulate a lot of different consoles from the past including the Dreamcast and N64 without any frame drops. I then looked at emulator managers on android and found a few issues such as duplicate games showing up in the library, this annoyed me every time I opened it so I decided to write my own emulator manager.

[gallery ids="812,813,814" type="rectangular"]

Here is demo of it running on a shield TV:

https://youtu.be/0bTjY6mTsv0

Key Features:

- Controller support.
- Scrapes box arts for games, saves a copy locally for offline support.
- Scale up/down the box art in the library.
- Combines duplicate ROMs into one.
- Responsive adapts to any device any orientation, works on mobile,tablet and shield TV
