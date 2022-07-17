---
description: what comes up, must come down.
---

# July 17

## PROBLEM&#x20;

> There are 100 light bulbs lined up in a row in a long room. Each bulb has its own switch and is currently switched off. The room has an entry door and an exit door. There are 100 stockbrokers lined up outside the entry door. Each bulb is numbered consecutively from 1 to 100. Each stockbroker is numbered consecutively from 1 to 100.
>
>
>
> Broker number 1 enters the room, switches on every bulb, and exits. Broker number 2 enters and flips the switch on every second bulb (turning off bulbs 2, 4, 6, ...). Broker number 3 enters and flips the switch on every third bulb (changing the state on bulbs 3, 6, 9, ...). This continues until all 100 brokers have passed through the room.
>
>
>
> What is the final state of bulb number 64? Is it illuminated or dark?

## SOLUTION

* the solution is quite simple, as we only need to count the number of factors of 64.
* the initial state is off, and if the number of factors is even, the final state is still off.
* else, the final state is on.
* 64's factors: 1,2,4,8,16,32,64
* which counts 7.
* Thus, the final bulb is on.



## Follow Up

> How many of the light bulbs are illuminated after the 100th person has passed through the room, and which light bulbs are they?

## Solution

* we find out that if we a number _c_ is divided by _a_, there must be a "_b_" to pair it up such that a\*b = c.
* Thus, for any number has a factor, it must have two factors in total.
* e.g. 11 = 1\*11.
* The only exemption is square numbers, where the factor counts itself twice, but when we check the final number of factors, we only count it once.
* e.g. 64's factors: 1,2,4,8,16,32,64
* we will not say that 64's factors: 1,2,4,**8,8,**16,32,64
* Thus, we only need to count the number of square numbers from 1 to 100, and there are 10 numbers in total.
* Thus, the answer is the square numbers between 1 and 100.
