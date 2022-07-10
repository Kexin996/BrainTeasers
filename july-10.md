# July 10

## PROBLEM

> There are two bells. One rings five times per minute, and the other rings four times per minute. If they start at the same time, how long will it be until they next ring together?

## SOLUTION

* we analyze the problem in this way:
* One bell ringing interval is 12 seconds, and the other bell ringing interval is 15 seconds
* They start and end at the same time ---> their total time is the same, and if the two bell ring together, the result of dividing total time by their interval must be an integer.
* ex. 72 / 12 = 6, meaning that the first bell has rung 6 times
  * 72 / 15 = 4.8, which is impossible ---> the bell must ring an integer times.
* Thus, we need to find the situation where:
* total time mod 15 = total time mod 12 = 0.
* If the first bell has rung **a** times, the second bell has rung **b** times:
* $$12*a = 15 * b$$, $$a : b = 15:12=5:4$$
* Since we need to get the next time the two bells ring together after they begin, we want the smallest a and b in integer form.
* $$a = 5, b = 4$$
* The total time is 60s, which is 1 min.



****

