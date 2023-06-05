### Task
Given an array, **A** , of **N** integers, print **A**'s elements in reverse order as a single line of space-separated numbers.

**Example**

**A=[1,2,3,4]**

Print ```4 3 2 1```. Each integer is separated by one space.

**Input Format**

The first line contains an integer, **N**  (the size of our array).
The second line contains N space-separated integers that describe array A's elements.

**Constraints**

- 1<=N<=1000
- 1<=A[i]<=1000, where A[i] is the i<sup>th</sup> integer in the Array.

**Output Format**

Print the elements of array **A** in reverse order as a single line of space-separated numbers.

**Sample Input**

```txt
4
1 4 3 2
```

**Sample Output**

```txt
2 3 4 1
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

    arr = list(map(int, input().rstrip().split()))

    print (*arr[::-1], sep=' ')

```
