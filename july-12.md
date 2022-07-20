---
description: get 3 from 2
---

# July 12

## PROBLEM

> You are given a set of scales and 12 marbles. The scales are of the old balance variety. That is, a small dish hangs from each end of a rod that is balanced in the middle. The device enables you to conclude either that the contents of the dishes weigh the same or that the dish that falls lower has heavier contents than the other. The 12 marbles appear to be identical. In fact, 11 of them are identical, and one is of a different weight. Your task is to identify the unusual marble and discard it. You are allowed to use the scales three times if you wish, but no more. Note that the unusual marble may be heavier than the others, or it may be lighter; you do not know which. You are asked to both identify it and determine whether it is heavy or light.

## SOLUTION

* this problem uses a technique, which I call "**get 3 from 2**"
* We just split the 12 marbles in this order:
* {(1) (2 3 4)}, {(5) (6 7 8)}, {(9) (10 11 12)}&#x20;
* We randomly compare two sets
* we compare {(1) (2 3 4)} and {(5) (6 7 8)}
* Case 1: {(1) (2 3 4)} = {(5) (6 7 8)}
  * we locate the problematic marble to {(9) (10 11 12)}&#x20;
  * we compare (6 7 8) and (10 11 12)
  * if they are equal, we compare (5) to (9) since (5) is a normal marble
  * if (6 7 8) < (10 11 12)
    * we compare 11 and 12 ---> 11 == 12, 10 is the problematic marble
    * 11 > 12 ---> 11 is the problematic marble
    * 11 < 12 ---> we is the problematic marble
  * same processes for (6 7 8) > (10 11 12)
* Case 2: {(1) (2 3 4)} > {(5) (6 7 8)}
  * we **rotate, since we know {(9) (10 11 12)}  must be normal**
  * **we know either there is a bigger marble in {(1) (2 3 4)} or smaller marble in {(5) (6 7 8)}**
  * we compare {(1) (6 7 8)} and {(5) (10 11 12)}
  * if {(1) (6 7 8)} == {(5) (10 11 12)}
    * we locate the problem to (2 3 4)
    * we do internal comparison
  * if {(1) (6 7 8)} > {(5) (10 11 12)}
    * we test the four cases:
    * case 1: (1) is larger ---> possible
    * case 2: one of (2 3 4) is larger ---> **impossible**
    * case 3: (5) is smaller ---> possible
    * case 4: one of (6 7 8) is smaller ---> **impossible, since {(1) (6 7 8)}  should be smaller instead of larger**
  * we only need to compare (1) with (9)
    * if (1) == (9) ---> (5) is the answer
    * if (1) > (9) ----> (1) is the answer
  * if {(1) (6 7 8)} < {(5) (10 11 12)}
    * it belongs to case 4
    * we do internal comparison to (6 7 8)
* Note: **\*we are actually splitting the 3 sets into 6 sets\***
