---
author: cmuk
comments: true
date: 2008-11-09 13:57:02+00:00
layout: post
link: https://mckellar.wordpress.com/2008/11/09/console-dev-week-56-mips/
slug: console-dev-week-56-mips
title: Console Dev Week 5+6 MIPS
wordpress_id: 144
categories:
  - Console Development
---

Console dev for the past weeks i have been looking at sub routines in MIPS assembly. We looked at the **jal **instruction which means jump and link similar to the **jr** jump to register instruction however it saves the programme counter in register $31 the reason for this is if you jump to a sub routine how would you return. you could use temporary register but you may run out and with going to another sub routine within a subroutine may get confusing.

pseudo code
Main

Jal stringLength() //PC saved in reg $31

void stringLength()
{
jr$31 // Jumps back to main
}

We looked at the call conventions which are like mnemonic names for the registers such as $t0 - $t7 for the temporary values. The call conventions are based on user agreements and change for different assembly such as PSP/n32 convention.

Week 6s console dev we looked at the previous weeks problem of sub routines.  What happens if you go into too many sub routines and the registers run out. The solution is to use memory management we looked at how the stack works. LIFO - last in first out this is how the stack operates the basic idea is like a stack of plates you get at restaurants you **Push** a plate on top and the stack goes down. That plate is still on top so when your taking it off you **Pop** it off so last plate becomes first off. This works for memory

pseudo code

1. push <$ra <to OS>
   2.  jal Sub()
2. push <$ra main>
3. jal Sub1()
4. push <$ra sub>   last in

returning 6. pop <$ra sub>    first out
7. pop <$ra main> 8. pop <$ra to OS>

Main

{
Sub()

return 0
}

void Sub()
{
Sub1()
}

Pop/Push use a pointer to move up and down in memory. Push decreases the $sp. Pop Increases the $sp
