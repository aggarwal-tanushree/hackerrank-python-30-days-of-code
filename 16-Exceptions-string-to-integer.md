### Task
Read a string, _S_, and print its integer value; if _S_ cannot be converted to an integer, print ```Bad String```.

**Note:** You must use the String-to-Integer and exception handling constructs built into your submission language. If you attempt to use loops/conditional statements, you will get a _0_ score.

### Input Format
A single string, _S_.

### Constraints
- 1 <= |S| <=6, where |S| is the length of the string _S_.
- _S_ is composed of either  lowercase letters (a-z) or decimal digits (0-9).

### Output Format
Print the parsed integer value of _S_, or ```Bad String``` if  cannot be converted to an integer.

### Sample Input 0

```txt
3
```

### Sample Output 0
```txt
3
```

### Sample Input 1
```txt
za
```

### Sample Output 1
```txt

Bad String
```

### My Solution

```py

#!/bin/python3

import math
import os
import random
import re
import sys



S = input()
try:
    print(int(S))
except ValueError:
    print("Bad String")
        


```
