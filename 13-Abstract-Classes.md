### Task
Given a Book class and a Solution class, write a MyBook class that does the following:

- Inherits from Book
- Has a parameterized constructor taking these  parameters:
    1. string _title_
    2. string _author_
    3. int _price_
- Implements the Book class' abstract display() method so it prints these 3 lines:
    1. _Title:_, a space, and then the current instance's _title_.
    2. _Author:_, a space, and then the current instance's _author_.
    3. _Price:_, a space, and then the current instance's _price_.
    4
    
  **Note:** Because these classes are being written in the same file, you must not use an access modifier (e.g.: _public_) when declaring MyBook or your code will not execute.
  
  ### Input Format

You are not responsible for reading any input from stdin. The Solution class creates a Book object and calls the MyBook class constructor (passing it the necessary arguments). It then calls the display method on the Book object.

### Output Format

The _void display()_ method should print and label the respective _title_, _author_, and _price_ of the MyBook object's instance (with each value on its own line) like so:

```txt

Title: $title
Author: $author
Price: $price

```
Note: The  is prepended to variable names to indicate they are placeholders for variables.

### Sample Input

The following input from stdin is handled by the locked stub code in your editor:

```txt

The Alchemist
Paulo Coelho
248

```

### Sample Output

The following output is printed by your display() method:

```txt

Title: The Alchemist
Author: Paulo Coelho
Price: 248

```


## My Solution:

```py

from abc import ABCMeta, abstractmethod
class Book(object, metaclass=ABCMeta):
    def __init__(self,title,author):
        self.title=title
        self.author=author   
    @abstractmethod
    def display(): pass

#Write MyBook class
class MyBook(Book):
    def __init__(self, title, author, price):
        super().__init__(title, author)
        self.price = price
        
    def display(self):
        print("Title: " + self.title + "\nAuthor: " + self.author + "\nPrice: " + str(self.price))
        
title=input()
author=input()
price=int(input())
new_novel=MyBook(title,author,price)
new_novel.display()

```

