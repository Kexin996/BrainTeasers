# July 18

## PROBLEM

> Your bedroom sock drawer contains eight red socks and 11 blue socks that are otherwise identical. The light is broken in your bedroom, and you must select your socks in the dark. What is the minimum number of socks you need to take out of your drawer and carry into your (well-lit) living room to guarantee that you have with you at least a matching pair to choose from?

## SOLUTION

* we need to understand the **sample space of the results and the worst case**.
* matching pair ---> two socks with the same color
* at least one matching pair ---> number of matching pairs >= 1
* we need to find out where the number of matching pairs < 1
* we have 2 colors, red and blue in total
* the worst case is that we want the existing socks that we pull out to have the same number but < 2\*the number of matching pairs
* e.g. R, B, all < 2\*1 = 2
* However, in this situation, the number of unchosen colors is 0&#x20;
* we reach the "limit" ---> so we need three pairs.
* generalize it ---> we need 3 socks.



## Follow Up

> Following on from the previous two questions, your bedroom sock drawer contains 2 red, 4 yellow, 6 purple, 8 brown, 10 white, 12 green, 14 black, 16 blue, 18 gray, and 20 orange socks. It is dark, so you cannot distinguish between the colors of the otherwise-identical socks. How many socks do you need to take out of the drawer to guarantee that you have at least three pairs of socks of the same color?



## SOLUTION

* we still consider the worst case
* the 3 pairs of socks all have the same color.
* First, we exclude red and yellow. red is 2, and yellow is 4.
* 2+4 = 6, and now we only have 8 colors.
* we follow the logic above: we want the number of pulling out socks of each color all becomes smaller than 3 \* 2 = 6.
* Thus, we want the number of each color to be 5.
* 5\*8 = 40, and if we pull out one more, we will have 3 pairs of socks of the same color.
* Adding them up, we have: 40+6+1 = 47 socks.
