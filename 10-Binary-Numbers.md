### Task
Given a base- integer, _n_, convert it to binary (base-2). Then find and print the base-10 integer denoting the maximum number of consecutive 1's in n's binary representation. When working with different bases, it is common to show the base as a subscript.

**Example**
n=125

The binary representation of 125<sub>10</sub> is 1111102<sub>2</sub>. In base **10**, there are 5 and 1 consecutive ones in two groups. Print the maximum, 5.  


**Input Format**

A single integer, **n**.


**Constraints**
- 1<=n<=10<sup>6</sup>



**Output Format**

Print a single base-10 integer that denotes the maximum number of consecutive 1's in the binary representation of n .


**Sample Input 1**
```txt

5

```

**Sample Output 1**

```txt

1

```

**Sample Input 2**

```txt

13

```

**Sample Output 2**

```txt

2

```


## My Solution

```py

#!/bin/python3

import math
import os
import random
import re
import sys



if __name__ == '__main__':
    n = int(input().strip())

result = 0
maximum = 0

while n > 0:
    if n % 2 == 1:
        result += 1
        if result > maximum:
            maximum = result

    else:
        result = 0
    n //= 2
print(maximum)


```
