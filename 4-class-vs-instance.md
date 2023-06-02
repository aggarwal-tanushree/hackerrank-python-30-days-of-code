### Task
Write a Person class with an instance variable, _age_, and a constructor that takes an integer, _initialAge_, as a parameter. The constructor must assign _initialAge_ to _age_ after confirming the argument passed as _initialAge_ is not negative; if a negative argument is passed as _initialAge_, the constructor should set _age_ to _0_ and print _Age is not valid_, setting _age to 0._. 
In addition, you must write the following instance methods:

1) yearPasses() should increase the _age_ instance variable by _1_ .
2) amIOld() should perform the following conditional actions:
  - If **age<13** , print _You are young._.
  - If **age>13** and **age<18**  , print _You are a teenager._.
  - Otherwise, print _You are old._.

To help you learn by example and complete this challenge, much of the code is provided for you, but you'll be writing everything in the future. The code that creates each instance of your Person class is in the main method. Don't worry if you don't understand it all quite yet!

**Note:** Do not remove or alter the stub code in the editor.

**Input Format**

Input is handled for you by the stub code in the editor.

The first line contains an integer, **T** (the number of test cases), and the **T** subsequent lines each contain an integer denoting the **age** of a Person instance.


**Constraints**

- 1<=T<=4
- -5<=age<=30

**Output Format**

Complete the method definitions provided in the editor so they meet the specifications outlined above; the code to test your work is already in the editor. If your methods are implemented correctly, each test case will print **2** and **3** lines (depending on whether or not a valid **initialAge** was passed to the constructor).

**Sample Input**

```txt
4
-1
10
16
18
```

**Sample Output**

```txt
Age is not valid, setting age to 0.
You are young.
You are young.

You are young.
You are a teenager.

You are a teenager.
You are old.

You are old.
You are old.
```


### My Solution

```py
class Person:
    def __init__(self,initialAge):
        # Add some more code to run some checks on initialAge
        if (initialAge < 0):
            print("Age is not valid, setting age to 0.")
            self.age = 0
        else:
            self.age = initialAge
                
    def amIOld(self):
        # Do some computations in here and print out the correct statement to the console
        if ( self.age < 13 ):
            print("You are young.")
        elif ( self.age >= 13 and self.age < 18 ):
            print("You are a teenager.")
        else:
            print("You are old.")
                    
    def yearPasses(self):
        # Increment the age of the person in here
        self.age += 1
                
t = int(input())
for i in range(0, t):
    age = int(input())         
    p = Person(age)  
    p.amIOld()
    for j in range(0, 3):
        p.yearPasses()       
    p.amIOld()
    print("")
```
