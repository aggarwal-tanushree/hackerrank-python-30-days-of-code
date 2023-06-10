### Task
You are given two classes, Person and Student, where Person is the base class and Student is the derived class. Completed code for Person and a declaration for Student are provided for you in the editor. Observe that Student inherits all the properties of Person.
Complete the Student class by writing the following:
- A Student class constructor, which has 4 parameters:
    1. A string, _firstName_.
    2. A string, _lastName_.
    3. An integer, _idNumber_.
    4. An integer array (or vector) of test scores, _scores_.
- A char calculate() method that calculates a Student object's average and returns the grade character representative of their calculated average:

![Grading_Scale](https://s3.amazonaws.com/hr-challenge-images/17165/1458142706-3073bc9143-Grading.png)


### Input Format

The locked stub code in the editor reads the input and calls the Student class constructor with the necessary arguments. It also calls the calculate method which takes no arguments.
The first line contains _firstName_, _lastName_, and _idNumber_ separated by a space. The second line contains the number of test scores. The third line of space-separated integers describes _scores_.

### Constraints

- 1 <= length of firstName, length of lastName <= 10
- length of idNumber = 7
- 0 <= score <= 100

### Output Format
Output is handled by the locked stub code. Your output will be correct if your Student class constructor and calculate() method are properly implemented.


### Sample Input

```txt

Heraldo Memelli 8135627
2
100 80

```

### Sample Output

```txt

 Name: Memelli, Heraldo
 ID: 8135627
 Grade: O
 
 ```
 
 ## My Solution
 
 ```py
 
 class Person:
	def __init__(self, firstName, lastName, idNumber):
		self.firstName = firstName
		self.lastName = lastName
		self.idNumber = idNumber
	def printPerson(self):
		print("Name:", self.lastName + ",", self.firstName)
		print("ID:", self.idNumber)

class Student(Person):
    #   Class Constructor
    #   
    #   Parameters:
    #   firstName - A string denoting the Person's first name.
    #   lastName - A string denoting the Person's last name.
    #   id - An integer denoting the Person's ID number.
    #   scores - An array of integers denoting the Person's test scores.
    #
    # Write your constructor here
    def __init__(self, firstName, lastName, idNumber, testScores):
        super().__init__(firstName, lastName, idNumber)
        self.scores = testScores

    #   Function Name: calculate
    #   Return: A character denoting the grade.
    #
    # Write your function here
    def calculate(self):
        totalScore = 0
        size = len(self.scores)
        for i in self.scores:
            totalScore += i
        grade = totalScore / size

        if (grade >= 90 and grade <= 100):
            grade = "O"
        elif (grade >= 80 and grade < 90):
            grade = "E"
        elif (grade >= 70 and grade < 80):
            grade = "A"
        elif (grade >= 55 and grade < 70):
            grade = "P"
        elif (grade >= 40 and grade < 50):
            grade = "D"
        else:
            grade = "T"
        return grade

line = input().split()
firstName = line[0]
lastName = line[1]
idNum = line[2]
numScores = int(input()) # not needed for Python
scores = list( map(int, input().split()) )
s = Student(firstName, lastName, idNum, scores)
s.printPerson()
print("Grade:", s.calculate())
 
 
 ```
