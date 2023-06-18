### Consider the following version of Bubble Sort:

```py
for (int i = 0; i < n; i++) {
    // Track number of elements swapped during a single array traversal
    int numberOfSwaps = 0;
    
    for (int j = 0; j < n - 1; j++) {
        // Swap adjacent elements if they are in decreasing order
        if (a[j] > a[j + 1]) {
            swap(a[j], a[j + 1]);
            numberOfSwaps++;
        }
    }
    
    // If no elements were swapped during a traversal, array is sorted
    if (numberOfSwaps == 0) {
        break;
    }
}
```

### Task
Given an array, _a_, of size _n_ distinct elements, sort the array in ascending order using the Bubble Sort algorithm above. Once sorted, print the following _3_ lines:
- Array is sorted in _numSwaps_ swaps.
where _numSwaps_ is the number of swaps that took place.
- First Element: _firstElement_
where _firstElement_ is the first element in the sorted array.
-  Last Element: _lastElement_ 
where _lastElement_ s the last element in the sorted array.
Hint: To complete this challenge, you will need to add a variable that keeps a running tally of all swaps that occur during execution.

### Example
a = [4,3,2,1]

```
original a: 4 3 1 2
round 1  a: 3 1 2 4 swaps this round: 3
round 2  a: 1 2 3 4 swaps this round: 2
round 3  a: 1 2 3 4 swaps this round: 0
```

In the first round, the _4_ is swapped with each of the _3_ comparisons, ending in the last position. In the second round, the _3_ is swapped at _2_ of the _3_ comparisons. Finally, in the third round, no swaps are made so the iterations stop. The output is the following:

```txt
Array is sorted in 5 swaps.
First Element: 1
Last Element: 4
```

### Input Format

The first line contains an integer, , the number of elements in array _a_
The second line contains _n_ space-separated integers that describe a[0], a[1], ... , a[n-1].

### Constraints
- 2 <= n <= 600
- 1 <= a[i] <= 2 x 10<sup>6</sup>, where 0 <= i < n.

### Output Format

Print the following three lines of output:

1. Array is sorted in _numSwaps_ swaps.
where _numSwaps_ is the number of swaps that took place.
2. First Element: _firstElement_
where _firstElement_ is the first element in the sorted array.
3.  Last Element: _lastElement_ 
where _lastElement_ s the last element in the sorted array.

### Sample Input 0

```
3
1 2 3
````

### Sample Output 0
```
Array is sorted in 0 swaps.
First Element: 1
Last Element: 3
```

### My Solution

```py

#!/bin/python3

import math
import os
import random
import re
import sys



if __name__ == '__main__':
    n = int(input().strip())

    a = list(map(int, input().rstrip().split()))

    # Write your code here
    numSwaps = 0
    
    for i in range(n):
        for j in range(n - 1):
            if a[j] > a[j + 1]:
                tmp = a[j]
                a[j] = a[j + 1]
                a[j + 1] = tmp
                numSwaps += 1
        if numSwaps == 0:
            break
    print("Array is sorted in " + str(numSwaps) + " swaps.")
    print("First Element: " + str(a[0]))
    print("Last Element: " + str(a[len(a) - 1]))

```
