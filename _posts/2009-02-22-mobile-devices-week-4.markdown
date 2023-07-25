---
date: 2009-02-22 22:17:25+00:00
title: Mobile Devices Week 4
categories:
  - Mobile Devices
---

This week in mobile devices I looked at **callSerially, Timers **and** Multi-threading.** We looked at a sample piano application which simulates a piano being played. Our task was to modify it to play a scale. The problem being how it processes the events. The Repaint() method will only request a repaint of the canvas when all of the other events have be processed first so nothing will happen until the current even handling finishes. A way to solve this is to call serviceRepaints() method right after repaint() this will cause the paint method to be called but will mean everything is blocked this should **never** happen.

**Display.callSerially()** - This causes a request to run() method after all other events have been processed.

**Timers** - using a timer you an schedule a task to occur at a certain time or at different intervals.

to use Timers you create a class that inherits from **TimerTask** and must implement a **run()** method. Once the timer expires, the run method will be active.

**Threads** - The piano repaints can be launched in a new thread while the code to play the scale is in a separate thread. To do this you create a runnable object which is an instance of a class that implements the interface of runnable. You then make a thread object using the Runnable object and start the Thread using myThread.start() this will start the execution of run() method.
