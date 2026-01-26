# 1 Selection Sorting
Class: [[Sorting]]
Subject/Topic: #sorting
Date: 2024-12-25

Notes:
## Selection Sort Algorithm


**Problem Statement:** Given an array of **N integers**, write a program to implement the Selection sorting algorithm.

**Examples:**

**Example 1:**
**Input:** N = 6, array[] = {13,46,24,52,20,9}
**Output:** 9,13,20,24,46,52
**Explanation:** After sorting the array is: 9, 13, 20, 24, 46, 52

**Example 2:**
**Input:** N=5, array[] = {5,4,3,2,1}
**Output:** 1,2,3,4,5
**Explanation:** After sorting the array is: 1, 2, 3, 4, 5

### **Solution**

**_Disclaimer_**: _Don't jump directly to the solution, try it out yourself first._

**Approach:**

The algorithm steps are as follows:

1. First, we will select the range of the unsorted array using a loop (say i) that indicates the starting index of the range.  
    The loop will run forward from 0 to n-1. The value i = 0 means the range is from 0 to n-1, and similarly, i = 1 means the range is from 1 to n-1, and so on.  
    (_Initially, the range will be the whole array starting from the first index._)
2. Now, in each iteration, we will select the minimum element from the range of the unsorted array using an inner loop.
3. After that, we will swap the minimum element with the first element of the selected range(_in step 1_). 
4. Finally, after each iteration, we will find that the array is sorted up to the first index of the range. 

**Note:** _Here, after each iteration, the array becomes sorted up to the first index of the range. That is why the starting index of the range increases by 1 after each iteration. This increment is achieved by the outer loop and the starting index is represented by variable_ **_i_** _in the following code. And the inner loop(_**_i.e. j_**_) helps to find the minimum element of the range_ **[i…..n-1].**

**Dry run:**

The following dry run will clarify the concepts:

Assume the given array is: {7, 5, 9, 2, 8}

**Outer loop iteration 1:  
**The range will be the whole array starting from the 1st index as this is the first iteration. The minimum element of this range is 2(**found using the inner loop**).

![](https://static.takeuforward.org/wp/uploads/2023/03/Screenshot-2023-03-13-223901.png)

**Outer loop iteration 2:  
**The range will be from the **[2nd index to the last index]** as the array is sorted up to the first index. The minimum element of this range is 5(**found using the inner loop**).

![](https://static.takeuforward.org/wp/uploads/2023/03/Screenshot-2023-03-13-224021.png)

**Outer loop iteration 3:  
**The range will be from the **[3rd index to the last index]**. The minimum element of this range is 7(**found using the inner loop**).

![](https://static.takeuforward.org/wp/uploads/2023/03/Screenshot-2023-03-13-225729.png)

**Outer loop iteration 4:  
**The range will be from the **[4th index to the last index]**. The minimum element of this range is 8(**found using the inner loop**).

![](https://static.takeuforward.org/wp/uploads/2023/03/Screenshot-2023-03-13-225822.png)

So, after 4 iterations(i.e. n-1 iterations where n = size of the array), the given array is sorted.

## CODE

### Main.java

```java
package com.saransh.sorting;

  

public class Main {

  

    public static void main(String[] args) {

        int[] array = { 5, 7, 1, 18, 2, 43 };

  

        PrintArray prt = new PrintArray();

        SelectionSorting srt = new SelectionSorting();

        prt.printArray(array);

        srt.selectionSorting(array);

        prt.printArray(array);

  

    }

  

}
```

### SelectionSort.java

```java
package com.saransh.sorting;

  

public class SelectionSorting {

    public void selectionSorting(int[] array) {

        for (int i = 0; i < array.length; i++) {

            int mini = i;

            for (int j = i + 1; j < array.length; j++) {

                if (array[mini] > array[j]) {

                    mini = j;

                }

            }

            if (mini != i) {

                int temp = array[mini];

                array[mini] = array[i];

                array[i] = temp;

            }

  

        }

    }

}
```


### Helper Class (Print Array)

```java
package com.saransh.sorting;

  

public class PrintArray {

 public void printArray(int[] arr){

    for (int i : arr) {

        System.out.print(i + " ");

    }

    System.out.println();

 }

}
```

### Time and Space complexity

### **Time Complexity**

$$
 Best case: O(n^2)
$$
$$
 Worst case: O(n^2)
$$ $$
 Average case: O(n^2)
$$

### **Space Complexity**

$$
 O(1)
$$
- (in-place sorting, no extra space required)
