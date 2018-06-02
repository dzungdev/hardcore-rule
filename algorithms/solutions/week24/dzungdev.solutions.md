Problem1: https://leetcode.com/problems/sum-of-square-numbers/description/

We can loop through 0 and each element we use c - i * i and use Math.sqrt to calculate and check whether it is integer or not. 
If yes, then the a and b are existed.

Time Complexity: O(sqrt(c)*log(c)) as Math.sqrt is log(c)

```java
public boolean judgeSquareSum(int c) {
    for (long a = 0; a * a <= c;a++) {
      double b = Math.sqrt(c - a * a);
      if (b == (int) b) return true;
    }
  return false;
}
```
