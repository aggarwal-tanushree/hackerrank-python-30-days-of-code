### Task
Given an integer, , perform the following conditional actions:

- If **n** is odd, print _Weird_
- If **n**  is even and in the inclusive range of **2 to 5**, print _Not Weird_
- If **n**  is even and in the inclusive range of **6 to 20**, print _Weird_
- If **n**  is even and greater than **20**, print _Not Weird_

Complete the stub code provided in your editor to print whether or not **n** is weird.

### Input Format

A single line containing a positive integer, **n** .

### Constraints

1<=n<=100

### Output Format

Print Weird if the number is weird; otherwise, print _Not Weird_.

### Sample Input 0

```txt
3
```

### Sample Output 0

```txt
Weird
```

### Sample Input 1

```txt
24
```

### Sample Output 1

```txt
Not Weird
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
    N = int(input().strip())
    if N % 2 != 0:
        print("Weird")
    elif N % 2 == 0 and 2 <= N <= 5:
        print("Not Weird")
    elif N % 2 == 0 and 6 <= N <= 20:
        print("Weird")
    else:
        print("Not Weird")  

```

