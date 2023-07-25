---
date: 2008-10-27 21:41:14+00:00
title: Console Dev Week 4 MIPS
categories:
  - Console Development
---

This week we learnt about Jumps in MIPS. This was about how to jump through your code making loops possible. We learnt about loops the most basic fundamental part of any programming language. Unconditional jumps alter the instruction sequence so the next instruction is changed pointing to a different location.

j Address # Basic jump to address
beq # branch if equal $1==$2 > jump
bne # branch if not equal $1 != $2 > jump / if both equal do nothing

jumping to a label solves the problem of looking up all the memory addresses to jump to

label: ... # Assembler works out the address

basic infinite while loop

L1: ....
j L1; # jumps back to L1

To get for loops working with a count you could say if beq count then jump out of while loop.

# quick pseudo code

$1 # value in reg is 10
$2 # counter to increment initial value 1
L1: beq $1,$2, L2 # if reg $1 == $2 then jump out of loop into label L2
addi $2,$2,1 # adds 1 to register $2
j L1 # jumps to L1 while loop

L2: do stuff

Here is an example of the Fibbonachi series written in MIPS

## Fibbo series

##

##1, 1, 2, 3, 5, 8, 13, 21, 34, 55, ...

##

## $8 Sum

## $12 SumPrev

## $9 Counter

## $10 Memory Address

## $11 LoopCount

.text
.globl  main

main:

lui $10, 0x1001  # load .data memory address
lw    $8,0($10)  # Load A
lw    $11,4($10) # Load B
ori   $12, $0, 0 # Init var  Prev
ori   $13, $0, 1 # Init var Current

j Adder             # Jump to label Adder
#bne   $8,$9,Adder

Adder:   beq   $9,$11,exit
add   $12,$13,$12 # Previous
ori  $8,$13,0 # update value
add  $13,$12,$13 # Current
addi  $9,$9,1 #increment counter
ori  $8,$12,0 # update value

j Adder # Jump back to the top of this loop

exit:    j    exit      #  sponge for excess machine cycles
sll   $0,$0,0

.data
A:      .word   0           #  init counter
B:      .word   101         #  counter end
