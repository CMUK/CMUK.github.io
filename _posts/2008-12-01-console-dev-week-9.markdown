---
date: 2008-12-01 07:51:05+00:00
title: Console Dev week 9
categories:
  - Console Development
---

This week we did presentations on our linked source file programs. Most people had gone over the top and had taken code from the hello triangle psp example which was interesting to see how it works but wasn’t really needed. My group had just done a simple math and printer source which in main passes a value to the math.c which the returns the result. Then sends the result to printer to printf(). Another group did a similar example with hello world that talked back which worked really well as it was simple enough and they had talked about making their own makefile stripping the stuff they didn’t need out of it. One thing noted about most the presentations was half the people were using Extern the other using #Include to access there .c files they both work but we will look at the difference in the coming weeks.

We looked at performance in code and talked about how you measure it. The CPU time is the way to measure code with the equation being CPU time = cycles/clock rate. The PSPs CPU is 222MHZ which is 222 million clock cycle, giving the CPU time 4.5 nano seconds. We then looked at how to improve performance by reducing the number of cycles. Finding the CPU cycles by getting the instruction count and multiplying it by the Average cycles per instruction (CPI).

After that we looked at memory allocations and ways to boost performance
Static memory is when you use globals
Dynamic on the heap is when you use New
Automatic on the stack is local variables
