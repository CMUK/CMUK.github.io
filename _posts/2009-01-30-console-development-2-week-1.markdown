---
date: 2009-01-30 19:27:53+00:00
title: Console Development 2 Week 1
categories:
  - Console Development Semester 2
---

After a long needed break it was good to get back into console development, having not done any for about 5 weeks i struggled to get the PSP dev kit to compile. After looking over my notes i soon realised the problem i was having was with wrong psp-gcc command. We returned to the problem about the impact of optimisation on a for loop with a 2D array in which way round [i][j] affected performance. int data[500][500] data[i][j] or data[j][i]? we did this by measuring performance compiling it using gcc as psp-gcc had problems implementing the profiler. [i][j] was more optimised giving faster times only by a small amount this was due to the way the cache works in how it can see j as adjacent in memory whereas if it was the other way around it would order differently on the cache and produce a cache miss every so often, while the speed difference was not that different having a bigger array may produce more misses and be slower. being 500 by 500 2D array of type int would be close to 1mb which would too much for the cache and needed to break it down into smaller arrays.

We looked at Christer Ericson's GDC 2003 slides on optimisation.

When data is fetched in memory and finds it in the cache this is known as a **cache hit**. If the data is not found it is called a **cache miss**. there are three types of cache misses called the three C's they are:

Compulsory misses - Unavoidable misses when the data is read for the first time

Capacity misses -Not enough cache space to hold all active data. Too much data accessed inbetween successive use

Conflict misses - Cache thrashing due to data mapping to same cache lines.
The main areas of interest were the methods of optimising such as:

•    Preloading cache lines - loading the next elements in a for loop ready for processing

•    Struct layout changes - changing the order with the biggest type variable at the top in decreasing order. Grouping similar types of data together if they are likely to get accessed together. hot and cold splitting is creating more structs from the same one and from the memory pool

•    Anti-aliasing compiler support - Multiple reference to the same storage location(pointers) fixed by using more local variables, restrict keyword
