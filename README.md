# Trailing Zeros

## 1

* **How many trailing zeros does 1000! have?**

**Solution 1:**

* We know the 2\*5 = 10, which adds to one trailing zero
* We begin with the number of 5s in 1000:
* 1000 / 5 = 200, we have 200 numbers which can be factored out by 5.
* However, how about the number of 5's multiples, such as 25, 125?
* 25 = 5\*5, and 125 = 5 \* 5 \* 5.
* The extra 5s in 25 and 125 can be multiplied by 2s to create 10s.
* we have 1000 / 25 = 40, 1000 / 125 = 8, 1000 / 625 = 1.6, and we only take the integer part, so adding them up, the number of fives that can be multiplied by 2 to get 10 is 200+40+8+1 = 249.
* Then we consider the number of 2: how many 2 can we have?
* 1000 / 2 = 500. We can have 500 2s, which is much bigger than 249 ---> **each of the 249 5s can be paired with a corresponding 2, so we can have 249 0's finally.**

****





**Extension: can you extend to any factorial?**

```java
// we use code to extend to any factorial.
class Solution {
    public int trailingZeroes(int n) 
    {
        int count = 0;
        // why divison works?
        // we just rewrite the formula we get in solution.
        // count = n/5+n/5^2+n/5^3+... (until n/5^k = 0)
        // which can be rewritten as:
        // count = n/5+(n/5)/5+((n/5)/5)/5+...
        // we get the iterative formula
        while (n > 0)
        {
            count += (n/5);
            n = n/5;
        }
        return count;
    }
}
```

****

\
