# Programming-100-Fundamentals
# TCM - Programming 100 Fundamentals

## 1. Introduction of Python


```python
# Printing Single Strings <-- Commnets

print("Hello World!")
```

    Hello World!
    


```python
# Printing Multiline Strings

print(""" 
This String runs
multi lines
""")
```

     
    This String runs
    multi lines
    
    


```python
# Tells the type of the variable

a = 2
b = 3.3
c = "Hello"

print(type(a))
print(type(b))
print(type(c))
```

    <class 'int'>
    <class 'float'>
    <class 'str'>
    

## 2. Strings

- The `str` (string) data type represents a sequence of characters enclosed within single quotes (' ') or double quotes (" "). 
- Strings in Python are immutable, which means they cannot be changed after they are created.


```python
# Newline

print("Hello")
print("\n")
print("World")
```

    Hello
    
    
    World
    


```python
# String Creation

my_str1 = 'Hello, World!'
my_str2 = "Hello, World!"
```


```python
# Accessing Single Characters:

print(my_str1[0] +"\t"+ 
      my_str1[1]+"\t"+ 
      my_str1[2]+"\t"+ 
      my_str1[3]+"\t"+ 
      my_str1[4])

```

    H	e	l	l	o
    


```python
# String Concatenation

print("Hello " + "String")
```

    Hello String
    


```python
# String Length

print(my_str1)
print(len(my_str1))

```

    Hello, World!
    13
    


```python
# String Slicing

substring = my_str1[0:4+1] # last index is ignored, to prevent +1
print(substring)

print(my_str1[::-1]) # Reverse the Full String
```

    Hello
    !dlroW ,olleH
    


```python
# String Methods

# upper(), lower(), strip(), split(), replace()

st = "   Hello   "

print(st.upper())
print(st.lower())
print(st.strip()) # Remove spaces at the beginning and at the end
print(st.replace('e','zz'))
```

       HELLO   
       hello   
    Hello
       Hzzllo   
    


```python
# String Formatting:

name,age = 'Alice',30
print("My name is %s and I'm %d years old." % (name, age))
print(f"My name is {name} and I'm {age} years old.")
```

    My name is Alice and I'm 30 years old.
    My name is Alice and I'm 30 years old.
    

## 3. Arithmetic Operations

### Math Operators:

- Addition (+): Adds two numbers.
- Subtraction (-): Subtracts one number from another.
- Multiplication (*): Multiplies two numbers.
- Division (/): Divides one number by another.
- Integer Division (//): Performs division and returns the quotient as an integer (rounds down).
- Modulo (%): Returns the remainder of division.
- Exponentiation (**): Raises a number to a power.


```python
a,b = 4,4

print(a + b) # Add
print(a - b) # Minus
print(a * b) # Multiply
print(a / b) # Divide
print(a % b) # Modulus
print(a // b) # Quotient
print(a ** b) # Power

```

    8
    0
    16
    1.0
    0
    1
    256
    

### Math Functions in the math Module

- `math.sqrt(x)`: Calculates the square root of x.
- `math.pow(x, y)`: Raises x to the power of y.
- `math.exp(x)`: Calculates the exponential value of x (e^x).
- `math.log(x)`: Calculates the natural logarithm of x (base e).
- `math.log10(x)`: Calculates the logarithm of x to base 10.
- `math.sin(x), math.cos(x), math.tan(x)`: Calculate the sine, cosine, and tangent of x, respectively (where x is in radians).
- `math.degrees(x)`: Converts x from radians to degrees.
- `math.radians(x)`: Converts x from degrees to radians.


```python
import math

print(math.sqrt(5))
print(math.pow(5,2))
print(math.exp(5))
print(math.log10(4))
print(math.sin(45),math.cos(45),math.tan(45))
print(math.degrees(45))
```

    2.23606797749979
    25.0
    148.4131591025766
    0.6020599913279624
    0.8509035245341184 0.5253219888177297 1.6197751905438615
    2578.3100780887044
    

## 4. Variables and Basic Methods

- A variable is a named storage location used to store data or values in a program. 
- It acts as a placeholder for data that can be accessed, modified, or used in calculations throughout the program. 
- Variables in Python are dynamically typed, meaning their data type can change during program execution.


```python
age = 23 #int
name = "Michael" #string
gpa = 8.6 #float

print(int(age))

print(type(age))
print(type(name))
print(type(gpa))

# Not Round Off
print(int(35.1))
print(int(35.9))
```

    23
    <class 'int'>
    <class 'str'>
    <class 'float'>
    35
    35
    

### Methods

- A method is a block of reusable code that performs a specific task or action. 
- Methods are associated with `objects` or `classes` and are called upon to perform certain operations. 
- In Python, methods are commonly referred to as functions. 
- `Built-in functions` and `User-defined` functions both fall under the category of methods.


```python
# Methods 

quote = "All is fair in love and war."
print(quote)

print(quote.upper()) #uppercase
print(quote.lower()) #lowercase
print(quote.title()) #title case
print(len(quote)) # count characters + spaces are charaters
```

    All is fair in love and war.
    ALL IS FAIR IN LOVE AND WAR.
    all is fair in love and war.
    All Is Fair In Love And War.
    28
    


```python
print("My name is "+name+" and I am "+str(age)+" years old.")
```

    My name is Michael and I am 23 years old.
    


```python
# Built-in method 

numbers = [1, 2, 3, 4, 5]
length = len(numbers)
print("Length:", length)


# User-defined method

def greet(name):
    print("Hello, " + name)


greet("Michael")
```

    Length: 5
    Hello, Michael
    

## 5. User Input

- To interact with the user and receive input using the `input()` function. 
- The `input()` function allows you to prompt the user for input and receive the input as a string.


```python
name = input("Enter your name: ")
print("Hello, " + name + "!")
```

    Enter your name: 3
    Hello, 3!
    


```python
# By Default input type is String
a = input("Enter 1st number: ")
b = input("Enter 2nd Number: ")
print(a+b)
```

    Enter 1st number: 3
    Enter 2nd Number: 4
    34
    


```python
# Type Caste during Input as int

a = int(input("Enter 1st number: "))
b = int(input("Enter 2nd Number: "))
print(a+b)

```

    Enter 1st number: 3
    Enter 2nd Number: 4
    7
    


```python
# Type Caste during Input as float

a = float(input("Enter 1st number: "))
b = float(input("Enter 2nd Number: "))
print(a+b)

```

    Enter 1st number: 3
    Enter 2nd Number: 4
    7.0
    

## 6. Introduction to Functions

- A function is a reusable block of code that performs a specific task. 
- Functions allow you to organize code into logical & modular units, making your code more readable, maintainable, & reusable.

- A function is defined using the `def` keyword, followed by the function name, parentheses, and a colon `:`. 
- The function may also have parameters (optional) and a `return` statement (optional) to send back a result. 
- Indentation is very important in functions


```python
def hi():
    print("Hello World")
```


```python
# Function Call
hi()
```

    Hello World
    


```python
# Function Parameters
def hi(name):
    print("Hello, " + name + "!")


hi("Michael")
```

    Hello, Michael!
    


```python
# Return Statement
def add_numbers(a, b):
    return a + b


result = add_numbers(3, 4)
print(f"Output returned: {result}")
```

    Output returned: 7
    


```python
def who_am_i(name,age):
    print(f"My name is {name} and I am {age} years old")

who_am_i("Michael",23)
```

    My name is Michael and I am 23 years old
    


```python
def add(x,y):
    print(x + y)

add(7,7)
```

    14
    


```python
def multiply(x,y):
    return x * y

result1 = multiply(7,7)
result2 = multiply(8,8)

print(result1 + result2)

```

    113
    


```python
def square_root(x):
    print(x ** .5)

square_root(64)
```

    8.0
    


```python
def nl(): #new line
    print('\n')

print("Hello World ")
nl()
print("is the beginning...!!")

```

    Hello World 
    
    
    is the beginning...!!
    

## 7.  Boolean Expressions and Relational Operators

- Boolean expressions are expressions that evaluate to either True or False. 
- They are typically used in conditional statements & logical operations to make decisions based on the truth or falsity of certain conditions. 
- Relational operators are used to compare values and create boolean expressions.

### Relational Operators

Python provides several relational operators to compare values.

- Equality (`==`): Checks if two values are equal.
- Inequality (`!=`): Checks if two values are not equal.
- Greater than (`>`): Checks if the left value is greater than the right value.
- Less than (`<`): Checks if the left value is less than the right value.
- Greater than or equal to (`>=`): Checks if the left value is greater than or equal to the right value.
- Less than or equal to (`<=`): Checks if the left value is less than or equal to the right value.



```python
x = 5
y = 10


# Relational operators
print(x == y)   # Output: False
print(x < y)    # Output: True
```

    False
    True
    


```python
# Relational operators

greater_than = (7 > 5)
print(greater_than)

less_than = (5 < 7)
print(less_than)

greater_than_equal_to = (7 >= 7)
print(greater_than_equal_to)

less_than_equal_to = (7 <= 7)
print(less_than_equal_to)

```

    True
    True
    True
    True
    

### Boolean Expressions:

Boolean expressions are formed by combining relational expressions using logical operators.

- Logical AND (`and`): Returns True if both operands are True.
- Logical OR (`or`): Returns True if at least one operand is True.
- Logical NOT (`not`): Negates the value of the operand.

![Boolean Operators](https://content.codecademy.com/practice/art-for-practice/new-pngs/Boolean-operators-dk.png)


```python
# Boolean expressions

x = 5
y = 10

print(x < y and y > 0)    # Output: True
print(x < y or y < 0)     # Output: True
print(not (x == y))       # Output: True
```

    True
    True
    True
    


```python
bool1 = True
bool2 = 3*3 == 9
bool3 = False
bool4 = 3*3 != 9

print(bool1,bool2,bool3,bool4)
print(type(bool1))

bool5 = "True"
print(type(bool5))

```

    True True False False
    <class 'bool'>
    <class 'str'>
    


```python
# Boolean operators

test_and = (True and True) #True
print(test_and)

test_and2 = (True and False) #False
print(test_and2)

test_or = (True or True) #True
print(test_or)

test_or2 = (True or False) #True
print(test_or2)

test_not = (not True) #False
print(test_not)
```

    True
    False
    True
    True
    False
    

## 8. Conditional Statements

- Conditional statements are used to perform different actions based on certain conditions. 
- They allow you to control the flow of your program by executing specific blocks of code when certain conditions are met.

### if Statement:
It executes a block of code if a given condition is true.


```python
x = 5
if x > 0:
    print("x is positive")
```

    x is positive
    

### if-else Statement:
One block to be executed if the condition is true and another to be executed if the condition is false. 


```python
x = 5
if x > 0:
    print("x is positive")
else:
    print("x is not positive")
```

    x is positive
    

### if-elif-else Statement:
- Check multiple conditions and execute different blocks of code based on those conditions. 
- It provides more than two options for branching.


```python
x = 5
if x > 0:
    print("x is positive")
elif x < 0:
    print("x is negative")
else:
    print("x is zero")
```

    x is positive
    


```python
def drink(money):
    if money >= 2:
        return "You've got yourself a drink!"
    else:
        return "No drink for you!"
    
print(drink(3))
print(drink(1))
```

    You've got yourself a drink!
    No drink for you!
    


```python
def alcohol(age,money):
    if (age >= 21) and (money >= 5):
        return "We're getting a drink!"
    elif (age >= 21) and (money < 5):
        return "Come back with more money."
    elif (age < 21) and (money >= 5):
        return "Nice try, kid!"
    else:
        return "You're too young and too poor."

print(alcohol(21,5))
print(alcohol(21,4))
print(alcohol(20,5))
print(alcohol(20,4))
```

    We're getting a drink!
    Come back with more money.
    Nice try, kid!
    You're too young and too poor.
    

## 9. Loops

- Looping allows you to repeat a block of code multiple times. 
- It is a fundamental concept used for iterating over data structures, performing repetitive tasks, & controlling the flow of your program. 
- There are two main types of loops in Python: `for` loops and `while` loops.

### for Loop:
- `for` loop is used to iterate over a sequence (such as a `list`, `tuple`, `string`, or `range`) or any iterable object. 
- It executes a block of code a fixed number of times, based on the elements or items in the sequence.


```python
fruits = ["apple", "banana", "orange"]
for fruit in fruits:
    print(fruit)
```

    apple
    banana
    orange
    


```python
vegetables = ["cucumber", "spinach", "cabbage"]
for veggies in vegetables:
    print(veggies)

```

    cucumber
    spinach
    cabbage
    


```python
for i in range(5):
    print(i)
```

    0
    1
    2
    3
    4
    


```python
word = "Python"
for letter in word:
    print(letter)

```

    P
    y
    t
    h
    o
    n
    

### while Loop:
- The `while` loop is used to repeatedly execute a block of code as long as a given condition is true. 
- It continues looping until the condition becomes false.
- the `while` loop will continue executing the code inside the loop `(print(count))` as long as the condition `count < 5` is true.


```python
count = 0
while count < 5:
    print(count)
    count += 1
```

    0
    1
    2
    3
    4
    

### The `break` and `continue` Statements:
- `break` statement to exit the loop prematurely. 
- `continue` statement to skip the current iteration and move to the next one.


```python
i = 1

while i < 10:
    print(i)
    if i == 5:
        break
    i += 1
```

    1
    2
    3
    4
    5
    

### Project 1 - Basic Calculator


```python
x = float(input("Enter 1st number: "))
o = input("Enter operator: ")
y = float(input("Enter 2nd number: "))

if o == '+':
    result = x + y
elif o == '-':
    result = x - y
elif o == '*':
    result = x * y
elif o == '/':
    result = x / y
elif o == '**' or o == '^':
    result = x ** y
else:
    result = "Unknown Operator..!!"

print(result)
```

    Enter 1st number: 3
    Enter operator: +
    Enter 2nd number: 4
    7.0
    

# Data Structures

## 10. Lists

- A list is a versatile and mutable data structure that can hold a collection of items. 
- It allows you to store multiple values of different data types in a single variable.

- Lists are powerful data structures in Python that allow you to store and manipulate collections of items. 
- They are widely used for managing and processing data in various applications.

### List Creation:

To create a list, you enclose comma-separated values within square brackets `[ ]`


```python
fruits = ["apple", "banana", "orange"] 
```

### List Access:

You can access individual elements in a list using indexing. Indexing starts from 0 for the first element and goes up to the length of the list minus one. 


```python
print(fruits[0])    # Output: "apple"
print(fruits[2])    # Output: "orange"
```

    apple
    orange
    


```python
for i in fruits:
    print(i,end=",")
```

    apple,banana,orange,


```python
fruits = ["apple", "banana", "orange"]
for i in range(len(fruits)):
    if i == len(fruits) - 1:  # Last fruit, no comma
        print(fruits[i])
    else:
        print(fruits[i], end=", ")
```

    apple, banana, orange
    

### List Modification:

Lists are mutable, which means you can modify their elements. You can assign new values to specific positions in the list or use methods to modify the list itself.


```python
fruits[1] = "grape"     # Modifying an element
fruits.append("kiwi")   # Adding an element to the end
fruits.remove("apple")  # Removing an element
```

### List Operations:

Python provides various operations that can be performed on lists. Some common operations include:

1. Concatenation: You can use the + operator to concatenate two or more lists.
2. Length: The len() function returns the number of elements in a list.
3. Slicing: You can extract a sublist from a list using slicing.
4. Iteration: You can use a loop to iterate over the elements of a list.


```python
movies = ["When Harry Met Sally", "The Hangover", "The Perks of Being a Wallflower", "The Exorcist"]

print(movies[1]) #return the second item in the list - index
print(movies[0]) #return the first item in the list
print(movies[1:3]) #returns the first number given until right before the last number given
print(movies[1:4]) #returns 1-3
print(movies[1:]) #return 1-end
print(movies[:1]) #everything before 1
print(movies[:2])
print(movies[-1]) #grabs last item
```

    The Hangover
    When Harry Met Sally
    ['The Hangover', 'The Perks of Being a Wallflower']
    ['The Hangover', 'The Perks of Being a Wallflower', 'The Exorcist']
    ['The Hangover', 'The Perks of Being a Wallflower', 'The Exorcist']
    ['When Harry Met Sally']
    ['When Harry Met Sally', 'The Hangover']
    The Exorcist
    


```python
print(len(movies)) # count the items in the list
movies.append("JAWS") # add an item to the end of our list
print(movies)
```

    4
    ['When Harry Met Sally', 'The Hangover', 'The Perks of Being a Wallflower', 'The Exorcist', 'JAWS']
    


```python
movies.insert(2, "Hustle")
print(movies)
```

    ['When Harry Met Sally', 'The Hangover', 'Hustle', 'The Perks of Being a Wallflower', 'The Exorcist', 'JAWS']
    


```python
# removes the last item

movies.pop() 
print(movies)
```

    ['When Harry Met Sally', 'The Hangover', 'Hustle', 'The Perks of Being a Wallflower', 'The Exorcist']
    


```python
# remove the first item

movies.pop(0) 
print(movies)
```

    ['The Hangover', 'Hustle', 'The Perks of Being a Wallflower', 'The Exorcist']
    


```python
amber_movies = ['Just Go With It', '50 First Dates']
our_favorite_movies = movies + amber_movies #combine lists
print(our_favorite_movies)
```

    ['The Hangover', 'Hustle', 'The Perks of Being a Wallflower', 'The Exorcist', 'Just Go With It', '50 First Dates']
    


```python
# 2x2 Matrix - Nested List

grades = [["Bob", 82], ["Alice", 90], ["Jeff", 73]]
bobs_grade = grades[0][1]
print(bobs_grade)
grades[0][1] = 83
print(grades)
```

    82
    [['Bob', 83], ['Alice', 90], ['Jeff', 73]]
    


```python
# 3x4 Matrix - Nested List

nested_list = [[1, 2, 3], [4, 5, 6], [7, 8, 9]]
print(nested_list[1][2])
```

    6
    

### Important List Methods

| Method              | Description                                      | Example Usage                    |
|---------------------|--------------------------------------------------|-----------------------------------|
| `append(item)`      | Adds an item to the end of the list.             | `payloads.append(new_payload)`    |
| `extend(iter)`      | Extends the list by appending elements from an iterable. | `payload_list.extend(new_data)`   |
| `insert(i, item)`   | Inserts an item at a specific index.            | `commands.insert(1, 'sudo')`      |
| `remove(item)`      | Removes the first occurrence of an item.        | `payloads.remove('test')`         |
| `pop(i)`            | Removes and returns the item at the specified index. | `payload.pop(0)`                |
| `clear()`           | Removes all elements from the list.             | `data.clear()`                    |
| `index(item)`       | Returns the index of the first occurrence of an item. | `payload.index('GET')`          |
| `count(item)`       | Returns the number of occurrences of an item.   | `payload.count('A')`              |
| `sort()`            | Sorts the list in ascending order.              | `ports.sort()`                    |
| `reverse()`         | Reverses the order of the list.                 | `payload.reverse()`               |
| `copy()`            | Returns a shallow copy of the list.             | `payload_copy = payload.copy()`   |
| `len(list)`         | Returns the number of elements in the list.     | `len(payloads)`                  |
| `max(list)`         | Returns the largest item in the list.           | `max(port_list)`                 |
| `min(list)`         | Returns the smallest item in the list.          | `min(port_list)`                 |
| `sum(list)`         | Returns the sum of all items in the list (numbers). | `sum(response_times)`           |
| `list(iterable)`    | Converts an iterable (like a string or tuple) to a list. | `list(payload)`              |
| `any(list)`         | Returns `True` if any element in the list is `True`. | `any(results)`                 |
| `all(list)`         | Returns `True` if all elements in the list are `True`. | `all(is_safe)`                |


## 11. Tuples

- A `tuple` is an ordered collection of elements, similar to a list. 
- However, unlike lists, tuples are `immutable`, meaning their elements cannot be modified once they are created.

- Tuples are useful in situations where you want to store a collection of values that should not be changed. 
- They can be used to group related data elements and can also be used as keys in dictionaries. 
- While tuples are immutable, they offer advantages such as faster performance and protection against unintentional modification.

### Tuple Creation:

To create a tuple, you enclose comma-separated values within parentheses `( )`


```python
fruits = ("apple", "banana", "orange")
```

### Tuple Access:

- To access individual elements in a tuple using indexing, similar to lists. 
- Indexing starts from 0 for the first element.


```python
print(fruits[0])    # Output: "apple"
print(fruits[2])    # Output: "orange"
```

    grape
    kiwi
    

### Tuple Immutability:

- Tuples are immutable, meaning you cannot modify their elements. 
- Once a tuple is created, its values cannot be changed. 
- For example, attempting to assign a new value to an element will result in an error. 


```python
fruits[1] = "grape"    # This will raise an error
```


    ---------------------------------------------------------------------------

    TypeError                                 Traceback (most recent call last)

    Cell In[65], line 1
    ----> 1 fruits[1] = "grape"
    

    TypeError: 'tuple' object does not support item assignment


### Tuple Operations:

Although tuples are immutable, you can perform certain operations on them:

1. Concatenation: You can use the `+` operator to concatenate two or more tuples.
2. Length: The `len()` function returns the number of elements in a tuple.
3. Slicing: You can extract a subtuple from a tuple using slicing.


```python
fruits = ("apple", "banana", "orange")
fruits2 = ("grape", "kiwi")


combined = fruits + fruits2
print(combined)         # Output: ("apple", "banana", "orange", "grape", "kiwi")


print(len(fruits))      # Output: 3


subtuple = fruits[1:3]  # slicing of Tuple
print(subtuple)         # Output: ("banana", "orange")
```

    ('apple', 'banana', 'orange', 'grape', 'kiwi')
    3
    ('banana', 'orange')
    


```python
# Tuples - Immutable (cannot be changed) - ()

coordinates = (40.7128, 74.0060) #New York

red = (255, 0, 0)
green = (0, 255, 0)
blue = (0, 0, 255)

student = ("John Doe", 8675309, "Computer Science")

print(student[2])

# student.pop() - will not work (Tuples are Not used mostly)
```

    Computer Science
    

### Important Tuple Methods

| Method          | Description                                      | Example Usage                    |
|-----------------|--------------------------------------------------|-----------------------------------|
| `count(item)`   | Returns the number of occurrences of an item in the tuple. | `response_codes.count(200)`      |
| `index(item)`   | Returns the index of the first occurrence of an item in the tuple. | `payloads.index('SQL')`         |
| `len(tuple)`    | Returns the number of elements in the tuple.     | `len(ip_addresses)`              |
| `tuple(iterable)`| Converts an iterable (like a list) to a tuple.    | `tuple(payload_list)`            |

### Tuple Operations:

- **Indexing**: Access elements using indices. Example: `payloads[0]`
- **Slicing**: Extract a subset of elements. Example: `payloads[1:3]`
- **Concatenation**: Combine tuples using `+`. Example: `tuple1 + tuple2`
- **Repetition**: Repeat elements using `*`. Example: `tuple1 * 3`


## 12. Dictionaries

 - A dictionary is an unordered collection of `{key:value}` pairs. 
 - It is a versatile and powerful data structure that allows you to store, retrieve, and manipulate data based on unique keys. 

- Dictionaries are powerful data structures that provide a flexible way to store and retrieve data based on keys. 
- They are commonly used for organizing and manipulating data that requires quick and efficient access.

### Dictionary Creation:

To create a dictionary, you enclose key-value pairs within curly braces `{ }`, separating each pair with a colon `:`.


```python
student = {
    "name": "Michael",
    "age": 23,
    "major": "Computer Science"
}
```

### Dictionary Access:

You can access the values in a dictionary by referring to their corresponding keys. Keys provide a way to uniquely identify and retrieve values. 


```python
print(student["name"])   # Output: "Michael"
print(student["age"])    # Output: 23
```

    Michael
    23
    

### Dictionary Modification:

Dictionaries are mutable, which means you can modify their values by assigning new values to specific keys.


```python
student["age"] = 24       # Modifying a value
student["city"] = "Canada"    # Adding a new key:value pair
```

### Dictionary Operations:

Python provides various operations that can be performed on dictionaries. Some common operations include:

1. Length: The `len()` function returns the number of key-value pairs in a dictionary.
2. Iteration: You can iterate over the keys, values, or key-value pairs of a dictionary using `loops`.
3. Deletion: You can remove a key-value pair from a dictionary using the `del` keyword.


```python
student = {
    "name": "Michael",
    "age": 23,
    "major": "Computer Science"
}


print(len(student))          # Output: 3


for key in student:
    print(key, student[key])  # Output: "name Michael", "age 23", "major Computer Science"


del student["age"]           # Deleting a key-value pair
```

    3
    name Michael
    age 23
    major Computer Science
    


```python
# Dictionaries - key:value pairs {}

drinks = {"White Russian": 8, "Old Fashioned": 12, "Lemon Drop": 5} # drink is key, price is value
print(drinks)

employees = {"Finance": ["Bob", "Linda", "Tina"], "IT": ["Gene", "Louise", "Teddy"], "HR": ["Jimmy Jr.", "Mort"]}
print(employees)

employees['Legal'] = ["Mr. Frond"] # add a new key:value pair
print(employees)

employees.update({"Sales": ["Andie", "Ollie"]}) # add a new key:value pair
print(employees)

drinks['White Russian'] = 9
print(drinks)

print(drinks.get("White Russian"))
```

    {'White Russian': 8, 'Old Fashioned': 12, 'Lemon Drop': 5}
    {'Finance': ['Bob', 'Linda', 'Tina'], 'IT': ['Gene', 'Louise', 'Teddy'], 'HR': ['Jimmy Jr.', 'Mort']}
    {'Finance': ['Bob', 'Linda', 'Tina'], 'IT': ['Gene', 'Louise', 'Teddy'], 'HR': ['Jimmy Jr.', 'Mort'], 'Legal': ['Mr. Frond']}
    {'Finance': ['Bob', 'Linda', 'Tina'], 'IT': ['Gene', 'Louise', 'Teddy'], 'HR': ['Jimmy Jr.', 'Mort'], 'Legal': ['Mr. Frond'], 'Sales': ['Andie', 'Ollie']}
    {'White Russian': 9, 'Old Fashioned': 12, 'Lemon Drop': 5}
    9
    

### Important Dictionary Methods

| Method               | Description                                      | Example Usage                    |
|----------------------|--------------------------------------------------|-----------------------------------|
| `get(key, default)`  | Returns the value for a specified key, or a default value if the key is not found. | `config.get('timeout', 30)`       |
| `keys()`             | Returns a view of all keys in the dictionary.    | `config.keys()`                   |
| `values()`           | Returns a view of all values in the dictionary.  | `config.values()`                 |
| `items()`            | Returns a view of all key-value pairs in the dictionary. | `config.items()`               |
| `update(other_dict)` | Updates the dictionary with key-value pairs from another dictionary. | `config.update(new_settings)`   |
| `pop(key, default)`  | Removes and returns the value for a specified key. If the key is not found, returns the default value. | `config.pop('port', 8080)`       |
| `popitem()`          | Removes and returns a random (key, value) pair from the dictionary. | `item = config.popitem()`        |
| `setdefault(key, default)` | Returns the value for a specified key, or sets and returns the default value if the key is not present. | `config.setdefault('host', 'localhost')` |
| `clear()`            | Removes all items from the dictionary.           | `config.clear()`                 |
| `copy()`             | Returns a shallow copy of the dictionary.        | `config_copy = config.copy()`    |
| `fromkeys(seq, value)` | Creates a new dictionary from a sequence of keys with a specified value. | `dict.fromkeys(['a', 'b'], 0)`  |
| `dict()`             | Constructs a dictionary from keyword arguments.  | `dict(a=1, b=2)`                 |


## 13. Strings Revisited - Advanced Strings


```python
# Slicing Strings

my_name = "Michael"
print(my_name[0]) # first letter
print(my_name[-1]) # last letter
print(my_name[-2]) # Second last letter
```

    M
    l
    e
    


```python
sentence = "This is a Sentence.. !!"

s2=sentence.split() # delimeter - default is a space

print(s2) 
print(type(s2))
```

    ['This', 'is', 'a', 'Sentence..', '!!']
    <class 'list'>
    


1. **split() Method**:
   - Purpose: Splits a string into a list of substrings based on a specified delimiter.
   - In this case, the string `"192.168.138.1"` is split into parts wherever the period (`.`) appears, resulting in the list `['192', '168', '138', '1']`.

2. **join() Method**:
   - Purpose: Joins elements of a list into a single string using a specified separator.
   - Here, the list `['192', '168', '138', '1']` is joined back into a string using `.` as the separator, resulting in `"192.168.138.1"`.


```python
sentence = "192.168.138.1"
print(sentence[:4]) # 0 - 3 print

print(sentence.split('.')) # delimeter - seperate the chars with custom symbol '.'

sentence_split = sentence.split('.')

sentence_join = '.'.join(sentence_split) # Join Sentence with a delimeter
print(sentence_join)
```

    192.
    ['192', '168', '138', '1']
    192.168.138.1
    

| Escape Sequence | Description                        | Example Usage                    |
|-----------------|------------------------------------|-----------------------------------|
| `\\n`           | Newline                            | `print("Line 1\\nLine 2")`       |
| `\\t`           | Tab                                | `print("Name\\tAge")`            |
| `\\\\`          | Backslash (`\`)                    | `print("C:\\\\path\\\\to\\\\file")`|
| `\\\'`          | Single quote (`'`)                 | `print('It\\\'s a test')`        |
| `\\\"`          | Double quote (`"`)                 | `print("He said, \\\"Hello\\\"")`|
| `\\r`           | Carriage return                    | `print("Hello\\rWorld")`         |
| `\\b`           | Backspace                          | `print("Hello\\bWorld")`         |
| `\\f`           | Form feed                          | `print("Hello\\fWorld")`         |
| `\\v`           | Vertical tab                       | `print("Line 1\\vLine 2")`       |
| `\\a`           | Bell/alert                         | `print("\\a")`                   |
| `\\0`           | Null character                     | `print("Null char\\0after this")`|



```python
# Character Escape

quote = "He said, 'give me all your money'"
quote = "He said, \"give me all your money\""
print(quote)
```

    He said, "give me all your money"
    


```python
# Remove WhiteSpaces

too_much_space = "                   hello       "
print(too_much_space)
print(too_much_space.strip())
```

                       hello       
    hello
    


```python
# Finding character inside a word (case-sensitive)

print("A" in "Apple") # return True
print("a" in "Apple") # return False - case sensitive
```

    True
    False
    


```python
# Finding character from a word by changing cases

letter = "A"
word = "Apple"
print(letter.lower() in word.lower()) # improved
```

    True
    


```python
# using strip() method to take down whitespaces

user_input = input("Enter yes or no: ")
if user_input.lower().strip() == "yes":
   print("You agree!")
else:
   print("You disagree!")
```

    Enter yes or no: yes
    You agree!
    


```python
# String formatting different ways

movie = "The Hangover"
print("My favorite movie is {}.".format(movie))
print("My favorite movie is %s." % movie)
print(f"My favorite movie is {movie}.")
```

    My favorite movie is The Hangover.
    My favorite movie is The Hangover.
    My favorite movie is The Hangover.
    

**Mostly Used Methods for Projects**

| Method              | Description                                                                 | Example Usage                     |
|---------------------|-----------------------------------------------------------------------------|------------------------------------|
| `encode(encoding)`  | Encodes the string using a specified encoding (e.g., `utf-8`, `hex`, `base64`). | `payload.encode('base64')`        |
| `decode(encoding)`  | Decodes an encoded string back to its original form.                         | `payload.decode('base64')`        |
| `replace(old, new)` | Replaces all occurrences of a substring with another. Useful for encoding payloads or obfuscation. | `payload.replace("get", "post")`    |
| `split(delimiter)`  | Splits a string into a list based on a specified delimiter, useful for parsing data. | `response.split(';')`             |
| `join(iterable)`    | Joins a list of strings into a single string with a specified delimiter, useful for constructing payloads. | `'.'.join(ip_segments)`           |
| `strip(chars)`      | Removes leading and trailing characters (e.g., whitespace) from a string. Useful for cleaning input. | `input.strip()`                   |
| `find(sub)`         | Returns the index of the first occurrence of a substring. Can be used to detect injection points or specific patterns in responses. | `response.find("root")`           |
| `count(sub)`        | Counts the occurrences of a substring in a string, useful for analyzing responses or payloads. | `payload.count('A')`              |
| `startswith(prefix)`| Checks if a string starts with the specified prefix, often used to verify URLs or input validation. | `url.startswith("http://")`       |
| `endswith(suffix)`  | Checks if a string ends with the specified suffix, useful for file extension checks. | `file_name.endswith('.php')`      |
| `format()`          | Formats a string by inserting values, often used for constructing dynamic payloads. | `payload.format(ip, port)`        |
| `lower()`           | Converts a string to lowercase, useful for case-insensitive comparisons.     | `header.lower()`                  |
| `upper()`           | Converts a string to uppercase, helpful for encoding or normalizing input.   | `command.upper()`                 |
| `isalnum()`         | Checks if a string consists of alphanumeric characters, useful for input validation. | `user_input.isalnum()`            |
| `isdigit()`         | Checks if a string contains only digits, often used for validating numerical input. | `port.isdigit()`                  |
| `replace(old, new)` | Replaces all occurrences of a substring with another. Useful in crafting exploits where special characters need to be escaped or encoded. | `input.replace("'", "\'")`        |
| `isnumeric()`       | Checks if all characters in the string are numeric.                         | `user_input.isnumeric()`  |



## 14. Importing Modules

- Importing modules allows you to access and use code that resides in external Python files or libraries. 
- Modules are a way to organize and reuse code, making it easier to manage and maintain large projects. 

- Importing modules enables you to access and utilize a wide range of functionality provided by the Python standard library or third-party libraries. 
- It promotes code reusability, modularity, and maintainability in your Python programs.

### Importing Entire Modules:
- To import an entire module, you use the import keyword followed by the module name.
- The math module is imported, and the `sqrt()` function from the module is used to calculate the square root of 25.


```python
import math


result = math.sqrt(25)
print(result)   # Output: 5.0
```

    5.0
    

### Importing Modules with an Alias:
- You can also import a module and give it an alias using the as keyword. 
- This can be helpful when dealing with modules with long names or to avoid naming conflicts.
- The `math` module is imported and assigned the alias `m`, so you can use `m.sqrt()` instead of `math.sqrt()`.


```python
import math as m


result = m.sqrt(25)
print(result)   # Output: 5.0
```

    5.0
    

### Importing All Functions and Variables:
- If you want to import all functions and variables from a module, you can use the `*` wildcard character. 
- However, it is generally recommended to import only what you need to avoid namespace pollution.
- All functions and variables from the math module are imported directly, allowing you to use them without prefixing with the module name.


```python
from math import *


result = sqrt(25)
print(result)   # Output: 5.0
```

    5.0
    


```python
# IMPORTING - Importing is important.

import sys # system functions and parameters
from datetime import datetime as dt # import with alias 

print(sys.version)
print(dt.now())
```

    3.11.5 | packaged by Anaconda, Inc. | (main, Sep 11 2023, 13:26:23) [MSC v.1916 64 bit (AMD64)]
    2024-09-26 10:19:28.552441
    

### Pentest Modules

| Module          | Description                                                                                     |
|-----------------|-------------------------------------------------------------------------------------------------|
| `nmap`          | Interface for interacting with the Nmap port scanner.                                           |
| `scapy`         | Packet manipulation and analysis; used for crafting and sending packets, sniffing, and more.    |
| `requests`      | Simplified HTTP requests; useful for interacting with web applications.                        |
| `beautifulsoup4`| Web scraping and parsing HTML/XML; useful for extracting data from web pages.                |
| `urllib`        | Standard library for fetching data across the web and handling URLs.                           |
| `socket`        | Low-level networking interface; used for creating network connections and custom protocols.    |
| `paramiko`      | SSH protocol implementation; used for remote command execution and file transfers.            |
| `pycryptodome`  | Cryptographic functions; used for encryption, decryption, and hashing.                        |
| `pytz`          | Time zone handling; useful for logging and handling time-based data.                           |
| `pwntools`      | CTF and binary exploitation tools; includes features for exploit development and binary analysis. |
| `sqlalchemy`    | SQL toolkit and ORM; used for database interaction and management.                             |
| `pyshark`       | Wrapper for TShark (Wireshark) for network packet parsing.                                      |
| `smtplib`       | SMTP protocol handling; useful for sending emails.                                             |
| `imaplib`       | IMAP protocol handling; useful for retrieving emails.                                           |
| `shodan`        | API for interacting with Shodan search engine; used for querying devices and services on the internet. |
| `pypdf2`        | PDF file manipulation; useful for extracting and modifying PDF documents.                     |
| `exifread`      | Extracts metadata from image files; useful for analyzing images and their metadata.            |
| `http.server`   | Simple HTTP server module; useful for serving files and testing HTTP requests.                 |
| `ipaddress`     | Standard library for creating, manipulating, and validating IP addresses and networks.         |
| `os`            | Standard library for interacting with the operating system; useful for file and process management. |

### Specialized Modules:

| Module              | Description                                                                                     |
|---------------------|-------------------------------------------------------------------------------------------------|
| `frida`         | Dynamic instrumentation toolkit for analyzing and manipulating applications at runtime.       |
| `burp`          | Integration with Burp Suite for automated testing and custom extensions.                       |
| `cobaltstrike`  | Interface for interacting with Cobalt Strike; used for advanced post-exploitation activities. |
| `fuzzing`       | Framework for fuzzing applications to discover vulnerabilities.                                |
| `applitools`    | Visual AI testing; used for visual validation of web applications.                            |
| `metasploit`    | Interface for interacting with the Metasploit Framework; used for exploit development.       |


## 15. Exception Handling


### What is Exception Handling?

- When you write a program, things can go wrong due to mistakes or unexpected events. 
- For example, dividing a number by zero or trying to open a file that doesn't exist can cause errors. 
- These errors are called **exceptions**. 
- Python has a way to deal with these exceptions so your program doesn't crash. This is called **exception handling**.

### Key Terms:
- **Exception**: An error that occurs during the execution of a program.
- **Try Block**: Code that may raise an exception is placed inside the `try` block.
- **Except Block**: Code that handles the exception is placed in the `except` block.
- **Finally Block**: Code that will run no matter what (whether an exception occurs or not).
- **Raise**: Used to manually raise an exception.

#### Why Use Exception Handling?
Exception handling allows your program to handle errors gracefully, showing messages or taking action instead of crashing.

### Code Examples


```python
# 1. Basic Try-Except Example


try:
    num = int(input("Enter a number: "))
    result = 10 / num
    print(f"Result: {result}")
except ZeroDivisionError:
    print("You can't divide by zero!")
except ValueError:
    print("Please enter a valid number.")
```

    Enter a number: 0
    You can't divide by zero!
    

**Explanation**: If you enter `0`, it will catch the `ZeroDivisionError` and print a message. If you enter something other than a number, it catches the `ValueError`.


```python
# 2. Try-Except-Finally Example

try:
    file = open("testfile.txt", "r")
    content = file.read()
    print(content)
except FileNotFoundError:
    print("File not found!")
finally:
    print("This will always run, no matter what.")
```

    File not found!
    This will always run, no matter what.
    

**Explanation**: If the file does not exist, the `except` block will handle it. The `finally` block will run regardless.


```python
# 3. Raising Exceptions

def check_age(age):
    if age < 18:
        raise ValueError("Age must be 18 or older.")
    else:
        print("Access granted.")

try:
    check_age(15)
except ValueError as e:
    print(e)
```

    Age must be 18 or older.
    

**Explanation**: We raise a `ValueError` if the age is less than 18.

### Table of Common Python Exceptions

| **Exception**           | **Description**                                           |
|-------------------------|-----------------------------------------------------------|
| `ZeroDivisionError`      | Raised when division by zero is attempted.                |
| `ValueError`             | Raised when a function receives an argument of the wrong type. |
| `FileNotFoundError`      | Raised when trying to open a file that does not exist.    |
| `IndexError`             | Raised when accessing an index that is out of range in a list. |
| `KeyError`               | Raised when a dictionary key is not found.                |
| `TypeError`              | Raised when an operation is applied to an object of an inappropriate type. |
| `AttributeError`         | Raised when an attribute reference or assignment fails.   |
| `ImportError`            | Raised when an import statement fails.                    |

### Summary:
- Use `try` to catch potential errors.
- Handle errors with `except`.
- Use `finally` for code that should always run.
- Use `raise` to manually trigger exceptions when needed.

## A1. Sockets

### Short Description of Sockets

- Sockets are a fundamental networking concept used for communication between computers over a network. 
- Sockets enable programs to establish connections, send data, and receive data over various network protocols, such as TCP (Transmission Control Protocol) and UDP (User Datagram Protocol). 

- Socket programming in Python allows you to create client-server applications, networked applications, and perform various networking tasks. 
- It provides a powerful and flexible way to communicate over networks using different protocols. 
- The socket module in Python provides a wide range of functions and methods to handle network communication efficiently.

### Socket Creation:

- To use sockets in Python, you need to import the socket module. 
- You can create a socket object using the `socket.socket()` function, which takes 2 parameters: 
    - the address family (e.g., `socket.AF_INET` for IPv4)
    - the socket type (e.g., `socket.SOCK_STREAM` for TCP or `socket.SOCK_DGRAM` for UDP).


```python
import socket as s

# Creating a TCP Socket
# tcp_sk = socket.socket(socket.AF_INET,socket.SOCK_STREAM)
tcp_sk = s.socket(s.AF_INET,s.SOCK_STREAM)


# Creating a UDP Socket
# udp_sk = socket.socket(socket.AF_INET,socket.SOCK_DGRAM)
udp_sk = s.socket(s.AF_INET,s.SOCK_DGRAM)
```

### Socket Communication:

Once you have a socket object, you can use various methods to establish connections, send data, and receive data. Here are some commonly used methods:

1. `socket.connect(address)`: Establishes a connection to a remote address.
2. `socket.bind(address)`: Binds the socket to a specific address and port.
3. `socket.listen(backlog)`: Listens for incoming connections on a TCP socket.
4. `socket.accept()`: Accepts an incoming connection and returns a new socket object for communication.
5. `socket.send(data)`: Sends data over the socket.
6. `socket.recv(buffer_size)`: Receives data from the socket.


```python
# SOCKETS - Sockets can be used to connect two nodes together.  

# Terminal 1 - Client Side
import socket

HOST = '127.0.0.1'
PORT = 7777

s = socket.socket(socket.AF_INET, socket.SOCK_STREAM) #af_inet is ipv4, sock stream is a port
s.connect((HOST,PORT))
```

Client: This script is the client-side code. It creates a socket and attempts to connect to a server using the IP address 127.0.0.1 (localhost) and port 7777. It uses TCP (stream socket) for communication.


```python
# Terminal 2 - Server Side
nc -nvlp 7777

# OUTPUT
# nc -nvlp 7777
# Listening on 0.0.0.0 7777
# Connection received on 127.0.0.1 45102
```

Server: This command uses netcat (or nc) to start a server that listens for incoming connections on port 7777.

- `-n` : Show numeric IP addresses instead of resolving hostnames.
- `-v` : Enable verbose mode to see detailed output.
- `-l` : Listen for incoming connections.
- `-p` : Specify the port number to listen on.


```python
# Basic TCP server that listens for incoming connections

# SERVER SIDE

import socket

# Create a TCP socket
server_socket = socket.socket(socket.AF_INET, socket.SOCK_STREAM)


# Bind the socket to a specific address and port
# server_address = ('localhost', 1234)

server_address = ('127.0.0.1', 1234)  
# print(type(server_address))
server_socket.bind(server_address)


# Listen for incoming connections
server_socket.listen(5)


while True:
    # Accept a client connection
    client_socket, client_address = server_socket.accept()


    # Receive and send data
    data = client_socket.recv(1024)
    client_socket.send(b"Received: " + data)


    # Close the client socket
    client_socket.close()
```

**Explanation**

1. Server: This code sets up a TCP server that:
2. Creates a TCP socket (socket.AF_INET and socket.SOCK_STREAM).
3. Binds the socket to localhost on port 1234.
4. Listens for incoming connections with a maximum backlog of 5.
5. Accepts client connections in a loop.
6. Receives data from the client and sends a response back to the client.
7. Closes the client connection after handling the request.


```python
# CLIENT SIDE

import socket

# Create a TCP socket
client_socket = socket.socket(socket.AF_INET, socket.SOCK_STREAM)

# Connect to the server
server_address = ('localhost', 1234)
client_socket.connect(server_address)

# Send data to the server
client_socket.send(b"Hello, Server!")

# Receive response from the server
response = client_socket.recv(1024)
print(response.decode())

# Close the connection
client_socket.close()

```

## Short Notes on Sockets

The `socket` module in Python provides a low-level networking interface for communication between nodes over a network. It supports both TCP and UDP protocols and is used for creating clients and servers.

### Key Concepts

- **Socket**: An endpoint for sending or receiving data across a network.

- **TCP (Transmission Control Protocol)**: A connection-oriented protocol that ensures reliable data transfer.

- **UDP (User Datagram Protocol)**: A connectionless protocol that sends data without establishing a connection.

### Commonly Used Functions

#### Socket Creation

- `socket(socket.AF_INET, socket.SOCK_STREAM)`: Creates a TCP socket using IPv4.

- `socket(socket.AF_INET, socket.SOCK_DGRAM)`: Creates a UDP socket using IPv4.

#### Server-Side

- `socket.bind(address)`: Binds the socket to an address and port.
  - `address`: A tuple `(host, port)`. <br>

- `socket.listen(backlog)`: Enables the server to accept connections.
  - `backlog`: Number of unaccepted connections that the system will allow before refusing new connections.  

- `socket.accept()`: Accepts an incoming connection and returns a tuple `(client_socket, client_address)`.  

- `client_socket.recv(buffer_size)`: Receives data from the client.
  - `buffer_size`: Maximum amount of data to be received at once.  

- `client_socket.send(data)`: Sends data to the client.  

#### Client-Side

- `socket.connect(address)`: Connects the client socket to a server.
  - `address`: A tuple `(host, port)`.

- `socket.send(data)`: Sends data to the server.

- `socket.recv(buffer_size)`: Receives data from the server.

#### Additional Notes
- Ensure that the server is running before the client attempts to connect.

- Handle exceptions such as socket.error to manage network-related issues gracefully.

- Consider using select or asyncio for handling multiple connections in more advanced scenarios.

### Closing

- `socket.close()`: Closes the socket to free up resources.

### Example Code

#### Server-Side Example

```python
import socket

# Create a TCP socket
server_socket = socket.socket(socket.AF_INET, socket.SOCK_STREAM)

# Bind the socket to a specific address and port
server_address = ('localhost', 1234)
server_socket.bind(server_address)

# Listen for incoming connections
server_socket.listen(5)

while True:
    # Accept a client connection
    client_socket, client_address = server_socket.accept()

    # Receive and send data
    data = client_socket.recv(1024)
    client_socket.send(b"Received: " + data)

    # Close the client socket
    client_socket.close()
```


#### Client-Side Example
```py

import socket

# Create a TCP socket
client_socket = socket.socket(socket.AF_INET, socket.SOCK_STREAM)

# Connect to the server
server_address = ('localhost', 1234)
client_socket.connect(server_address)

# Send data to the server
client_socket.send(b"Hello, Server!")

# Receive response from the server
response = client_socket.recv(1024)
print(response.decode())

# Close the connection
client_socket.close()


```

# Capstone Project: Port Scanner


```python
# My Code
import sys
import socket
from datetime import datetime
import threading  # used for concurrency

# Function for scanning port
def scan_port(target, port):
    try:
        s = socket.socket(socket.AF_INET, socket.SOCK_STREAM)  # IPV4, PORT
        s.settimeout(1)  # set timeout after 1s the socket operations

        result = s.connect_ex((target, port))  # error indicator - if 0, port is open

        if result == 0:
            print(f"Port {port} is open")
        s.close()

    except socket.error as e:
        print(f"Socket error on port {port} : {e}")
    except Exception as e:
        print(f"Unexpected error on port {port} : {e}")

# Main Function - argument validations & target definition
def main():
    if len(sys.argv) == 2:
        target = sys.argv[1]  # argv[1] because --$'python.exe [0]->file.py [1]->127.0.0.1'
    else:
        print("""Invalid number of arguments.
        Usage: python3 scanner.py <IP Address>
        """)
        sys.exit(1)  # 1 means exit with error & 0 means exit with No errors

    # Resolve the target hostname to an IP Address
    try:
        target_ip = socket.gethostbyname(target)
    except socket.gaierror:
        print(f"Error: Unable to resolve hostname {target}")
        sys.exit(1)

    # Add a pretty banner
    print(f"""
             __   __                    __     ___       __   __   ___ ___    
            /__` /  `  /\  |\ | | |\ | / _`     |   /\  |__) / _` |__   |     
            .__/ \__, /~~\ | \| | | \| \__>     |  /~~\ |  \ \__> |___  |     : {target_ip}
                                                                   
            ___          ___     __  ___       __  ___  ___  __                    
             |  |  |\/| |__     /__`  |   /\  |__)  |  |__  |  \                   
             |  |  |  | |___    .__/  |  /~~\ |  \  |  |___ |__/                   : {datetime.now()}
                                                                                 
    """)

    try:
        # Using Multi Threading to scan multiple ports at the same time - concurrently
        threads = []
        for port in range(1, 65536):
            thread = threading.Thread(target=scan_port, args=(target_ip, port))
            threads.append(thread)
            thread.start()

        # Wait for all threads to complete
        for thread in threads:
            thread.join()

    except KeyboardInterrupt:
        print("\nExiting Program CTRL+^")
        sys.exit(0)

    except socket.error as e:
        print(f"\nSocket Error {e}")
        sys.exit(1)

    except Exception as e:
        print(f"Unknown error: {e}")

    print("\nScan Completed!")


if __name__ == "__main__":  # It does not run script directly if imported to other script (our code will run in this file only)
    main()

```


```python
# TCM Code

import sys
import socket
from datetime import datetime
import threading

# Function to scan a port

def scan_port(target,port):
    try:
        s = socket.socket(socket.AF_INET, socket.SOCK_STREAM)
        s.settimeout(1)
        result = s.connect_ex((target,port)) #error indictor - if 0, port is open
        if result == 0:
            print(f"Port {port} is open")
        s.close()
    except socket.error as e:
        print(f"Socket error on port {port}: {e}")
    except Exception as e:
        print(f"Unexpected error on port {port}: {e}")

#Main function - argument validation and target definition
def main():
    if len(sys.argv) == 2:
        target = sys.argv[1]
    else:
        print("Invalid number of arguments.")
        print("Usage: python.exe scanner.py <target>")
        sys.exit(1)

    # Resolve the target hostname to an IP address
    try:
        target_ip = socket.gethostbyname(target)
    except socket.gaierror:
        print(f"Error: Unable to resolve hostname {target}")
        sys.exit(1)

    # Add a pretty banner
    print("-" * 50)
    print(f"Scanning target {target_ip}")
    print(f"Time started: {datetime.now()}")
    print("-" * 50)

    try:
        # Use multithreading to scan ports concurrently
        threads = []
        for port in range(1,65536):
            thread = threading.Thread(target=scan_port, args=(target_ip, port))
            threads.append(thread)
            thread.start()

        # Wait for all threads to complete
        for thread in threads:
            thread.join()

    except KeyboardInterrupt:
        print("\nExiting program.")
        sys.exit(0)

    except socket.error as e:
        print(f"Socket error: {e}")
        sys.exit(1)

    print("\nScan completed!")

if __name__ == "__main__":
    main()
```

    Invalid number of arguments.
    Usage: python.exe scanner.py <target>
    


    An exception has occurred, use %tb to see the full traceback.
    

    SystemExit: 1
    


    C:\Users\Bourne\anaconda3\Lib\site-packages\IPython\core\interactiveshell.py:3534: UserWarning: To exit: use 'exit', 'quit', or Ctrl-D.
      warn("To exit: use 'exit', 'quit', or Ctrl-D.", stacklevel=1)
    

# Some Theory

## B1. Writing Pseudocode

- Highlevel description of a computer program or algorithm, Its not actual code but designed in simple english for easy to read. 

- Goal: Describe the steps of an algorithm in easy way, later can be translated to any programming language.

### Why Use Pseudocode?
- **Simplify Logic**: Focus on program structure without worrying about syntax.
- **Communication**: Share ideas across teams without needing a specific language.
- **Planning**: Plan code flow early before writing actual code.
- **Learning & Teaching**: Easy to explain concepts without syntax complexities.
- **Debugging**: Helps identify logical errors before coding.

### Examples of Pseudocode

1. **Linear Search Algorithm**
   ```plaintext
   Procedure LinearSearch(arr, target)
       For each element in arr
           If element equals target
               Return "Found"
       Return "Not Found"
   End Procedure
   ```

2. **Finding Maximum in a List**
   ```plaintext
   Procedure FindMaximum(arr)
       Set max to arr[0]
       For each element in arr
           If element > max
               Set max to element
       Return max
   End Procedure
   ```

3. **Password Validation**
   ```plaintext
   Procedure ValidatePassword(password)
       If length < 8
           Return "Too Short"
       If no number
           Return "Must Contain Number"
       If no special char
           Return "Must Contain Special Character"
       Return "Valid"
   End Procedure
   ```

4. **ATM Withdrawal**
   ```plaintext
   Procedure ATMWithdrawal(balance, amount)
       If amount > balance
           Print "Insufficient Funds"
       Else If amount <= 0
           Print "Invalid Amount"
       Else
           Subtract amount from balance
           Print "Success"
   End Procedure
   ```

5. **Bubble Sort Algorithm**
   ```plaintext
   Procedure BubbleSort(arr)
       For i = 0 to length - 1
           For j = 0 to length - i - 1
               If arr[j] > arr[j+1]
                   Swap arr[j], arr[j+1]
   End Procedure
   ```

### Advantages of Pseudocode
- **Language-Independent**: No need to use specific syntax.
- **Focus on Logic**: Concentrate on problem-solving.
- **Improves Planning**: Reduces errors and enhances code structure.
- **Collaboration-Friendly**: Helps teams work together on algorithms.

### When to Use Pseudocode
- **Planning Phase**: Outline before writing real code.
- **Complex Algorithms**: Simplify algorithm logic.
- **Learning Concepts**: Learn algorithm flow without syntax hurdles.

### Translating Pseudocode to Code
1. **Pseudocode**:
   ```plaintext
   Procedure FindMaximum(arr)
       Set max to arr[0]
       For each element in arr
           If element > max
               Set max to element
       Return max
   End Procedure
   ```
2. **Python Translation**:
   ```python
   def find_maximum(arr):
       max_value = arr[0]
       for element in arr:
           if element > max_value:
               max_value = element
       return max_value
   ```

### Core Concepts
- **Logic before Syntax**: Focus on solving the problem, not on language-specific syntax.
- **Early Debugging**: Map out code behavior before implementation.
- **Simplified Communication**: Collaborate without coding language barriers.

## B2. Writing Reusable and Testable Code - Unit Testing

- Writing testable code means organizing your code in a way that makes it easy to test individual components (e.g., functions or classes) without relying on external systems (like databases, APIs, or user input). 
- Testable code typically follows principles such as separation of concerns, clear inputs and outputs, and minimal side effects.

### Understanding Non-Testable vs. Testable Code

**Non-Testable Code** is code that depends heavily on external factors like user inputs or printing outputs directly to the console. This makes it difficult to simulate different scenarios during testing.

Example of non-testable code:
```python
def atm_withdrawal():
    balance = int(input("Enter your current balance: "))
    amount = int(input("Enter the amount to withdraw: "))
    
    if amount > balance:
        print("Insufficient funds")
    elif amount <= 0:
        print("Invalid amount")
    else:
        balance -= amount
        print(f"Transaction successful. Your new balance is: {balance}")
```
**Problems:**
- Hardcoded input/output (`input()` and `print()`) make it difficult to test.
- No clear inputs or outputs for testing specific scenarios.

### Refactoring to Testable Code

Testable code is structured so that inputs and outputs are clear, and the function behavior can be tested in isolation without requiring user interaction.

Example of refactored, **testable code**:
```python
def atm_withdrawal(balance, amount):
    if amount > balance:
        return "Insufficient funds", balance
    elif amount <= 0:
        return "Invalid amount", balance
    else:
        balance -= amount
        return "Transaction successful", balance
```
**Improvements:**
- The function now accepts parameters (`balance` and `amount`).
- It returns values, allowing test cases to check results without relying on `print()`.

### `unittest` Library in Python

The `unittest` library allows you to write unit tests to verify that code works as expected.

Key features:
- **Test cases**: Defined by creating a class that extends `unittest.TestCase`.
- **Assertions**: Methods like `assertEqual()` are used to compare actual results with expected outcomes.

**Example:**
```python
import unittest
from atm import atm_withdrawal

class TestATMWithdrawal(unittest.TestCase):

    def test_insufficient_funds(self):
        message, new_balance = atm_withdrawal(100, 150)
        self.assertEqual(message, "Insufficient funds")
        self.assertEqual(new_balance, 100)

    def test_invalid_amount(self):
        message, new_balance = atm_withdrawal(100, -20)
        self.assertEqual(message, "Invalid amount")
        self.assertEqual(new_balance, 100)

    def test_successful_transaction(self):
        message, new_balance = atm_withdrawal(100, 50)
        self.assertEqual(message, "Transaction successful")
        self.assertEqual(new_balance, 50)

if __name__ == "__main__":
    unittest.main()
```

**Why It Works:**
- The refactored function can be tested by calling it with different inputs.
- Each test checks whether the function behaves as expected in different situations.
- The `unittest` library runs the tests automatically and provides feedback on test results.

### Key Principles for Writing Testable Code:
1. **Avoid Hardcoding I/O**: Pass inputs as arguments and return results, rather than using `input()` and `print()`.
2. **Clear Inputs and Outputs**: Design functions with clear parameters and return values.
3. **Test in Isolation**: Functions should not rely on external systems like databases or user inputs to be testable.
4. **Use Assertions**: Test the expected behavior using `assertEqual()` and other assertion methods.

## B3.   Additional Reading: Variable Best Practices

### Best Practices for Variable Naming in Python: *snake_case*

- **Snake Case Format**:
  - All letters are lowercase.
  - Words are separated by underscores (`_`).
  
  **Example**:
  ```python
  total_amount = 100
  user_name = "JohnDoe"
  is_valid = True
  ```

### Why Use Snake Case?
- **Readability**: Separates words clearly, making code easier to understand.
- **Consistency**: Following this convention across the project ensures uniformity.
- **PEP 8 Compliance**: Snake case is recommended by Python's official style guide, PEP 8, for variables and function names.

### Additional Best Practices

1. **Meaningful Names**:
   - Use descriptive names that clearly indicate the variable’s purpose.
   - Avoid single-letter names unless widely accepted (e.g., `i` for loop counters).

   **Good**:
   ```python
   total_sales = 500
   number_of_items = 10
   ```

   **Bad**:
   ```python
   x = 500
   n = 10
   ```

2. **Avoid Reserved Keywords**:
   - Don’t use Python reserved words (e.g., `class`, `def`, `if`) as variable names.

   **Bad**:
   ```python
   class = "example"  # SyntaxError: 'class' is a reserved keyword
   ```

3. **Constants in All Uppercase**:
   - For values that do not change, use `ALL_UPPERCASE` with underscores between words.

   **Example**:
   ```python
   MAX_SIZE = 100
   DEFAULT_TIMEOUT = 30
   ```

4. **Private Variables with Leading Underscore**:
   - Prefix internal/private variables with an underscore (`_`) to indicate they are not intended for external use.

   **Example**:
   ```python
   _cache = {}
   _internal_variable = 42
   ```

5. **Avoid Mixing Naming Styles**:
   - Stick to **snake_case** and avoid mixing it with **camelCase** (used in languages like Java).

   **Bad**:
   ```python
   userName = "John"  # camelCase
   ```

   **Good**:
   ```python
   user_name = "John"  # snake_case
   ```

### Summary of Best Practices:
- Use **snake_case** for variable names.
- Use **meaningful** and **descriptive** names.
- Avoid using **reserved keywords**.
- Use **ALL_UPPERCASE** for constants.
- Use a **leading underscore** for internal/private variables.
- Be **consistent** with naming conventions throughout the code.

## B3.   Additional Reading: Statically Typed Variables

### Statically Typed Variables

In statically typed languages, the type of a variable is explicitly declared and determined at **compile time**, meaning that once you assign a type to a variable, it cannot change. If you try to assign a value of a different type later, a compilation error occurs.

#### Key Characteristics:
- **Type Declaration**: You must explicitly declare a variable's type (e.g., integer, string) when you define it.
- **Compile-time Type Checking**: The compiler checks for type errors before running the code, reducing certain bugs.
- **Type Consistency**: The variable can only hold values of its defined type throughout the program.

#### Example (Java):
```java
int age = 25;  // 'age' is an integer
age = "twenty";  // Compilation error! Can't assign a string to an integer
```

In this example, `age` is an integer, and the compiler ensures it always holds integer values.

### Dynamically Typed Variables (Python)

In dynamically typed languages like Python, variables are not required to have an explicit type declaration. The type of a variable is determined at **runtime** based on the value assigned to it, and the same variable can hold values of different types at different points in the code.

#### Key Characteristics:
- **No Type Declarations**: You don't need to declare variable types; they are inferred from the assigned values.
- **Runtime Type Checking**: Python checks types when the code runs, not during the compile phase.
- **Type Flexibility**: Variables can change types as the program runs.

#### Example (Python):
```python
age = 25        # 'age' is an integer
age = "twenty"  # Now, 'age' is a string; no error occurs
```

Here, Python automatically allows `age` to change from an integer to a string without any issues.

### Differences Between Statically and Dynamically Typed Variables

| Feature                     | Statically Typed Languages                | Dynamically Typed Languages (e.g., Python) |
|-----------------------------|-------------------------------------------|-------------------------------------------|
| **Type Declaration**         | Types must be declared explicitly         | No need to declare variable types         |
| **Type Checking**            | Done at compile time                      | Done at runtime                           |
| **Type Safety**              | Type errors caught before runtime         | Type errors caught during execution       |
| **Type Flexibility**         | Variables always have the same type       | Variables can change types                |
| **Performance**              | Generally faster (types known at compile time) | Slower due to runtime type checks         |

### Benefits and Drawbacks

#### Statically Typed Variables:
- **Advantages**:
  - **Early error detection**: Errors are caught at compile time, improving reliability.
  - **Performance**: Compilers can optimize code based on known types, leading to faster execution.
  - **Predictability**: The type of a variable remains consistent, making the code easier to debug.
  
- **Disadvantages**:
  - **Less flexibility**: Once a type is assigned, it cannot be changed.
  - **More code**: Explicit type declarations may result in more verbose code.

#### Dynamically Typed Variables (Python):
- **Advantages**:
  - **Flexibility**: Variables can hold different types of values at different times.
  - **Faster development**: No need to declare types, leading to quicker prototyping.

- **Disadvantages**:
  - **Potential runtime errors**: Type errors can only be caught during execution, not before.
  - **Performance overhead**: Python has to check variable types at runtime, which can slow execution.

### Type Hinting in Python (Optional)

To combine the best of both static and dynamic typing, Python introduced **type hinting** (since Python 3.5). Type hinting allows you to specify types in your code for readability and potential error detection, but Python does not enforce these types.

#### Example of Type Hinting:
```python
def atm_withdrawal(balance: float, amount: float) -> float:
    if amount > balance:
        return balance
    return balance - amount
```

Here, `balance: float` and `amount: float` are type hints indicating that both parameters should be floats, and the function returns a float (`-> float`).

### Conclusion:
- **Statically Typed Variables**: Provide type safety and performance benefits by enforcing types at compile time, but require more explicit code.
- **Dynamically Typed Variables (Python)**: Offer flexibility and ease of development by determining types at runtime, with the trade-off of potential runtime errors.
- **Type Hinting in Python**: Combines readability and clarity with Python’s dynamic nature, without enforcing strict type rules.

## B4.   Additional Reading: Debugging Basics

### Python Debugging Basics Explanation

Debugging is the process of identifying and fixing errors or bugs in your code. While writing Python programs, it's common to encounter mistakes, and learning how to find and fix them is an essential skill for becoming a proficient programmer. Debugging can be as simple as using print statements to inspect variables or as advanced as using Python’s built-in debugger, `pdb`. Below, I’ll explain some basic debugging techniques that will help you better understand what’s happening in your code and how to fix errors effectively.

---

### Debugging Techniques Notes:

**1. Using `print()` to Inspect Variables**
The `print()` function allows you to see the values of variables at different points in your code. This is a quick way to check if your program behaves as expected.

```python
def add_numbers(a, b):
    print(f"a: {a}, b: {b}")  # Inspect values of a and b
    return a + b

result = add_numbers(5, 3)
print(f"Result: {result}")
```
- **Why Useful:** Helps check variable values when troubleshooting errors.

---

**2. Commenting Out Code**
If you're unsure where the bug is, commenting out parts of your code helps narrow down the issue. By disabling certain sections, you can isolate the problematic area.

```python
def divide_numbers(a, b):
    # result = a / b  # Might cause an error
    result = a // b   # Test with integer division
    return result

print(divide_numbers(10, 2))
```
- **Why Useful:** Allows you to test small parts of the code and find issues.

---

**3. Reading Python Error Messages**
Python provides detailed error messages (tracebacks) when your program crashes. These messages show where the error happened and what type of error occurred.

```python
def divide_numbers(a, b):
    return a / b

print(divide_numbers(10, 0))  # This will raise a ZeroDivisionError
```
- **Why Useful:** Tracebacks help identify where the error occurred, saving time.

---

**4. Using `assert` for Validation**
The `assert` statement allows you to test conditions in your code. If the condition isn’t true, an error is raised, helping you catch issues early.

```python
def square_number(n):
    result = n * n
    assert result >= 0, "Result should never be negative"
    return result

print(square_number(5))
```
- **Why Useful:** Ensures assumptions are valid while the program runs.

---

**5. Using the `pdb` Debugger**
`pdb` is Python’s built-in debugger, allowing you to step through your code and inspect its state. You can pause the execution and issue commands like `p` (print variables) or `n` (next step).

```python
import pdb

def add_numbers(a, b):
    pdb.set_trace()  # Pause execution here
    result = a + b
    return result

print(add_numbers(2, 3))
```
- **Why Useful:** Enables line-by-line inspection of your code for deeper debugging.

---

**6. Debugging Tools in IDEs (e.g., VSCode)**
In IDEs like VSCode or PyCharm, debugging tools let you set breakpoints (places where the program pauses) and inspect the values of variables visually.

- **Why Useful:** Easier visual debugging experience with less manual work compared to print statements.

---

**7. Common Python Errors**
- **SyntaxError:** Typos or missing syntax (e.g., colon).
- **TypeError:** Mismatched data types (e.g., adding a string to an integer).
- **IndexError:** Accessing a list element that doesn’t exist.

```python
my_list = [1, 2, 3]
print(my_list[5])  # Raises IndexError
```
- **Why Useful:** Knowing common errors helps you fix them faster.

---

### Final Debugging Tips:
- Start with `print()` to see what’s going wrong.
- Comment out code to pinpoint issues.
- Read error messages to locate problems quickly.
- Use `assert` to validate assumptions.
- Practice using `pdb` or IDE debuggers for deeper analysis.
- Familiarize yourself with common Python errors to resolve them more efficiently.



## B5.   Additional Reading: Setting Up a Reproducible Environment

#### What is a Development Environment?
A development environment includes the tools, programming languages, and software you need to build and test your code. Having a consistent setup across all team members avoids issues where the project works on one computer but fails on another.

---

#### Why Do You Need a Reproducible Environment?
A reproducible environment ensures that everyone on a project uses the same setup, eliminating version conflicts and setup issues across different machines. This avoids the classic "it works on my machine" problem.

---

### Steps to Set Up a Reproducible Development Environment:

#### Step 1: Version Control with Git
Git helps track changes in your code and ensures everyone works on the same version.

- **Install Git**: Download from [git-scm.com](https://git-scm.com/).
- **Initialize a Git repository**:
  ```bash
  git init
  ```
- **Track changes**:
  ```bash
  git add .
  git commit -m "Initial commit"
  ```
- **Share with teammates** by pushing to GitHub.

---

#### Step 2: Using a Virtual Environment
Virtual environments isolate dependencies for each project, allowing you to use different tools or versions without conflicts.

- **Create a virtual environment** in Python:
  ```bash
  python -m venv venv
  ```
- **Activate the environment**:
  - On Windows:
    ```bash
    venv\Scripts\activate
    ```
  - On macOS/Linux:
    ```bash
    source venv/bin/activate
    ```
- **Install project dependencies**:
  ```bash
  pip install <package-name>
  ```

---

#### Step 3: Recording Your Project’s Dependencies
Save your installed packages in a `requirements.txt` file so others can replicate your environment.

- **Save installed packages**:
  ```bash
  pip freeze > requirements.txt
  ```
- **Reproduce the environment** by running:
  ```bash
  pip install -r requirements.txt
  ```

---

#### Step 4: Sharing Environment Files with Git
Use a `.gitignore` file to prevent unnecessary files, like the virtual environment folder, from being uploaded to Git.

- **Create a `.gitignore` file** and add:
  ```bash
  venv/
  ```

---

#### Step 5: Using Docker (Optional for Advanced Beginners)
Docker can package your entire environment into a container, ensuring your project runs the same way on any machine.

---

### Conclusion: Why Reproducibility is Important
With version control, virtual environments, and shared dependencies, everyone can set up the same development environment, ensuring consistency across team members and avoiding common errors.

---

**Key Takeaways:**
- **Git**: Version control for tracking code.
- **Virtual environments**: Isolated setups for different projects.
- **Dependency management**: Save tools with `requirements.txt`.
- **Collaboration**: Share and ensure consistency across setups using Git and virtual environments.
