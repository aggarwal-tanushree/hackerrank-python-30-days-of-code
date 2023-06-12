### Task
Complete the Difference class by writing the following:

- A class constructor that takes an array of integers as a parameter and saves it to the ___elements_ instance variable.
- A computeDifference method that finds the maximum absolute difference between any _2_ numbers in ___elements_ nd stores it in the _maximumDifference_ instance variable.

### Input Format

You are not responsible for reading any input from stdin. The locked Solution class in the editor reads in _2_ lines of input. The first line contains _N_,  the size of the elements array. The second line has _N_ pace-separated integers that describe the ___elements_ array.

### Constraints
- 1 <= N <= 10
- 1 <= __elements[i] <= 100, where 0 <= i <= N-1

### Output Format

You are not responsible for printing any output; the Solution class will print the value of the _maximumDifference_ instance variable.

### Sample Input

```txt

STDIN   Function
-----   --------
3       __elements[] size N = 3
1 2 5   __elements = [1, 2, 5]

```

### Sample Output

```txt

4

```

## My Solution

```py

class Difference:
    def __init__(self, a):
        self.__elements = a
    # Add your code here
    def computeDifference(self):
        maximum = 0
        
        for i in range(len(self.__elements)):
            for j in range(len(self.__elements)):
                absolute = abs(self.__elements[i] - self.__elements[j])
                if absolute > maximum:
                    maximum = absolute
        self.maximumDifference = maximum

# End of Difference class

_ = input()
a = [int(e) for e in input().split(' ')]

d = Difference(a)
d.computeDifference()

print(d.maximumDifference)


```

