# July 19

## PROBLEM

> You and I are to play a competitive game. We shall take it in turns to call out integers. The first person to call out “50” wins. The rules are as follows:
>
> 1. The player who starts must call out an integer between one and 10, inclusive;
> 2. A new number called out must exceed the most recent number called by at least one and by no more than 10. For example, if the first player calls out “nine,” then the range of valid numbers for the opponent is 10 to 19, inclusive.
>
> Do you want to go first, and if so, what is your strategy?

## SOLUTION

* We define our own behaviors (the number we say) as x, and the other as y.
* we need to work backward, since we only know that we want to give 50 at the end.
* finally, we want to get 50 --->  y before 50 can only be \[40,49]
* if y must be bigger than 40, x must be 39 before this term.
* e.g. if x = 38, y will belong to \[39,48]
* Thus, we have the table:

| Term / Player | X  | Y                              |
| ------------- | -- | ------------------------------ |
| ?             | 50 | \[40,49]                       |
| ?             | 39 | \[29,38]                       |
| ?             | 28 | \[18,27]                       |
| ?             | 17 | \[7,16]                        |
| ?             | 6  | None - we cannot make y \[1,5] |

* we can see that if we want to win, we must begin with 6.
* we cannot limit y, since y's interval is 10, if we don't start with, y can win since 6 is in \[1,10]&#x20;

