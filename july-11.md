# July 11

## PROBLEM

> What is the sum of the integers from 1 to 100?

## SOLUTION

* I have not thought before that we can project the series to a matrix.
* If we just think of a matrix consisting of 101 columns and 100 rows, calculate the area and divide it by 2, we will have the answer
* why?&#x20;
* because apparently if we only count 100 \* 100, it doesn't count the other half of the diagonal
* e.g.&#x20;

![](<.gitbook/assets/Screen Shot 2022-07-11 at 1.28.31 PM.png>)

## EXTENSION

* What is we just want to calculate a random series, for example, the sum starting at 50 to 250?
* We will find that now we need to calculate a **** trapezoid, whose area is:
* (50+250)\*201/2 = 30150
* why 201: 250-50+1=201
