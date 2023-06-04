### Task
Given a string, **S**, of length **N** that is indexed from **0** to **N-1**, print its even-indexed and odd-indexed characters as **2** space-separated strings on a single line (see the Sample below for more detail).

Note: **0** is considered to be an even index.

**Example**

s = abcdef

Print ```abc def```

**Input Format**

The first line contains an integer, **T** (the number of test cases).
Each line **i** of the **T** subsequent lines contain a string, **S**.

**Constraints**

- 1<=T<=10
- 2<=length of S<= 10000

**Output Format**

For each String **S**<sub>j</sub> (where  0<=j<=T-1), print **S**<sub>j</sub>'s even-indexed characters, followed by a space, followed by **S**<sub>j</sub>'s odd-indexed characters.

**Sample Input**

```txt
2
Hacker
Rank

```

**Sample Output**

```txt

Hce akr
Rn ak

```

### My Solution

```py

# Enter your code here. Read input from STDIN. Print output to STDOUT
T = int(input())

for i in range(0, T):
    S = input()

    for j in range(0, len(S)):
        if j % 2 == 0:
            print(S[j], end='')

    print(" ", end='')

    for j in range(0, len(S)):
        if j % 2 != 0:
            print(S[j], end='')

    print("")

```
