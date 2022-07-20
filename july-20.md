# July 20

## PROBLEM

> You are to open a safe without knowing the combination. Be- ginning with the dial set at zero, the dial must be turned counter-clockwise to the first combination number, (then clockwise back to zero), and clockwise to the second combination number, (then counter-clockwise back to zero), and counter-clockwise again to the third and final combination number, whereupon the door shall immediately spring open; there is no handle or key to turn. The dial has numbers from zero to 40, and the zero is not one of the combination numbers.
>
> Without knowing the combination numbers, what is the maximum number of trials required to open the safe? One trial equals one attempt to dial a full three-number combination, and you must start again from zero for each trial.

## SOLUTION

* an interesting and **carefully worded** question.
* What does "the maximum number of trials required to open the safe" mean?
* **trials to open the safe + open immediately** ---> **at last step, we will always try to turn to the maximum number (40) as possible**
* since if the previous two numbers are correct, if we move toward 40 for the last number, the safe will always open.
* Now the question becomes in how many combination the first two numbers can be. **(maximum number of trials)**
* 40\*40 = 1600.
* Thus, the maximum number is 40.
