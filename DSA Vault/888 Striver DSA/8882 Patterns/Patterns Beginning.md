[Must do Pattern Problems before starting DSA - Tutorial](https://takeuforward.org/strivers-a2z-dsa-course/must-do-pattern-problems-before-starting-dsa)
They are just for the practice not important for any exam or anything tbh.
All the patterns have the nested loops present in them.

Outer loop is for the rows and the inner loop is for the columns.

1. For the outer loop count the number of rows which will determine the number of iterations for the pattern.
2. For the inner loop, focus on the columns and connect them somehow to the rows.
3. Whatever we are printing, print them inside the inner loop.
4. Observe symmetry incase of some patterns.

**Problem 1:**
# Pattern 1

Given an integer n. You need to recreate the pattern given below for any value of N. Let's say for N = 5, the pattern should look like as below:

```
  *****  
  *****
  *****
  *****
  *****
```

Print the pattern in the function given to you.

Example 1

**Input**: n = 4

**Output**:

  

![](https://static.takeuforward.org/content/ProblemSetter-dEELhBlC)

Example 2

**Input**: n = 2

**Output**:

  

![](https://static.takeuforward.org/content/ProblemSetter-CGhtDPay)

Constraints

- 1 <= n <= 100

**Solution:**
```java
class Solution {
    public void pattern1(int n) {
        for (int i=0;i<n;i++){
            for(int j=0;j<n;j++){
                System.out.print("*");
            }
            System.out.println();
        }
    }
}

```



