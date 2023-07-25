---
date: 2008-10-21 16:23:37+00:00
title: Console Dev Week 3 MIPS
categories:
  - Console Development
---

This week we have been reading lots on MIPS after a mind boggling late lecture i found myself a bit confused with all the work. After going through the chapters 9 -15 on http://chortle.ccsu.edu/AssemblyTutorial/TutorialContents.html over the weekend i have a clearer understanding of MIPS. I have completed the chapter 12 and 15 programs and have commented the lines. Here is an example from Exc 3 of chapter 15s programs

Ex3.

##

## 6x^3 - 3x^2 + 7x + 2

##

## Registers to Use:

##

## $7 Accumulator

## $8 base register, address of x

## $9 value of x

## $11 polynomial

lui $8, 0x1001    # load .data memory address
lw    $9,0($8)      #load co-officiant x into register $9
ori $7,$0,6      #  Initialize the accumulator to 6 store in $7
mult $7,$9       # multiply by $7 by $9 (6x2)
mflo $11         # store into register $11
addiu $7,$11,-3 # add -3 to (6x2)

mult $7,$9 # multiply accumulator(6x2 - 3x) by x

mflo $11 # store sum into $11

addiu $7,$11,7 # add +7 (6x2^2 - 3x + 7x)

mult $7,$9 # multiply accumulator(6x2^3 - 3x^2 + 7x) by x

mflo $11 # store sum into $11

addiu $11,$11,2 # accumulator(6x2^3 - 3x^2 + 7x + 2)

sw    $11,4($8) # store back in polyno

.data
x:      .word   2           #  value of x
poly:   .word   0           #  Result is placed here.
