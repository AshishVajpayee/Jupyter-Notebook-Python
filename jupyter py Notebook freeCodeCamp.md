## PythonCodeCamp


```python
print('Hello World!!')
```

    Hello World!!
    

### using variable to store data


```python
name = "Ashish"
age = "22"

print("My Name is " + name + ", I am " + age + " Years old")
```

    My Name is Ashish, I am 22 Years old
    

## Taking User input
### Example of Taking User input in Python 


```python
name = input("Enter your Name: ")
print("Hello " + name + "!")
```

    Enter your Name: Ashish
    Hello Ashish!
    

### Basic Arithmetic operations


```python
def add(x, y):
    return x+y

def sub(x, y):
    return x-y

def mul(x, y):
    return x*y

def mod(x, y):
    try:
        return x%y
    except:
        print("Enter the Valid Divisor")
        
def div(x, y):
    try:
        return x/y
    except:
        print("Enter the Valid Divisior")
        
num1 = int(input("Enter a number: "))
num2 = int(input("Enter another number: "))

print("The addition of two numbers", num1 ," and ", num2, "is", add(num1, num2))
print("The subtraction of two numbers", num1 ," and ", num2, "is", sub(num1, num2))
print("The multiplication of two numbers", num1 ," and ", num2, "is", mul(num1, num2))
print("The modulus of two numbers", num1 ," and ", num2, "is", mod(num1, num2))
print("The Divison of two numbers", num1 ," and ", num2, "is", div(num1, num2))

```

    Enter a number: 15
    Enter another number: 6
    The addition of two numbers 15  and  6 is 21
    The subtraction of two numbers 15  and  6 is 9
    The multiplication of two numbers 15  and  6 is 90
    The modulus of two numbers 15  and  6 is 3
    The Divison of two numbers 15  and  6 is 2.5
    

### Check number is Odd or Even


```python
def OddorEven(x):
    if(int(x)%2 == 0):
        print("The given Number", x, "is even")
    else:
        print("The given Number", x , "is odd")
        
number = int(input("Enter the Number: "))
OddorEven(number)
```

    Enter the Number: 2
    The given Number 2 is even
    

### Factorial of given number


```python
def fact(x):
    if(x == 0):
        return 1
    else:
        return(x*fact(x-1))
number = int(input("Enter the number: "))
print("The Factorial of", number ," is", fact(number))
```

    Enter the number: 4
    The Factorial of 4  is 24
    

### Fibonacci


```python
def fib(x):
    if(x <= 1):
        return x
    else:
        return(fib(x-1)+fib(x-2))
number = int(input("Enter the number: "))
print("Fibonacci series ")
for i in range(number):
    print(fib(i))
```

    Enter the number: 5
    Fibonacci series 
    0
    1
    1
    2
    3
    

### Mad Lib Game


```python
color = input("Enter a color: ")
plural_noun = input("Enter a Plural Noun: ")
programming = input("Enter a Programming: ")

print("Roses are " + color)
print(plural_noun + " are blue")
print("I love " + programming)
```

    Enter a color: Red
    Enter a Plural Noun: violets
    Enter a Programming: Python
    Roses are Red
    violets are blue
    I love Python
    

### Lists


```python
friends = ["Akash", "Vishnu", "Karthik", "Vaibhav"] ## Index 0 = Akash, 1 = vishnu, 2 = karthik
friends.sort()
print(friends) ## friends[0] prints Akash, [1:] prints list values from index 1 onwards till n;

```

    ['Akash', 'Karthik', 'Vaibhav', 'Vishnu']
    

### Tuples


```python
coordinates = (4, 5) ## Tuples are immutable
print(coordinates[0])
```

    4
    

### Functions


```python
def fun(name, age): ##def your own Function using def keyword
    print("Hello " + name + ", you are " +str(age))
    
fun("Ashish", 22)
fun("Ram", 22)
```

    Hello Ashish, you are 22
    Hello Ram, you are 22
    

### Return Statement


```python
def cube(num):
    return num*num*num
result = cube(4)
print(result)
```

    64
    

### If Statement


```python
is_male = True
is_tall = True

if is_male and is_tall:
    print("You are a tall male")
elif is_male and not(is_tall):
    print("You are a short male")
elif not(is_male) and is_tall:
    print("You are not male but tall")
else:
    print("You are either not male nor tall")
```

    You are a tall male
    

### If statements and comparisions


```python
def max_num(num1, num2, num3):
    if num1 >= num2 and num1 >= num3:
        return num1
    elif num2 >= num1 and num2 >= num3:
        return num2
    else:
        return num3
    
print(max_num(3, 40, 5))
```

    40
    

### Calculator


```python
num1 = float(input("Enter first number: "))
op = input("Enter operator: ")
num2 = float(input("Enter second number: "))

if op == "+":
    print(num1 + num2)
    
elif op == "-":
    print(num1 - num2)
    
elif op == "*":
    print(num1 * num2)
    
elif op == "/":
    print(num1 / num2)
elif op == "%":
    print(num1 % num2)
else:
    print("Enter valid operator")

```

    Enter first number: 5
    Enter operator: +
    Enter second number: 23
    28.0
    

### Dictionaries


```python
monthConversions = {
    "Jan": "January",
    "Feb": "February",
    "Mar": "March",
}
# Key Value Pairs

##print(monthConversions["Feb"])
print(monthConversions.get("Mar"))

```

    March
    

### While Loop


```python
i = 1
while i <= 10: # Until condition is true it keeps executing
    print(i)
    i += 1 # adds 1 to i again goes to condition checks for it and keeps iterating
    
print("Done with Loop")
```

    1
    2
    3
    4
    5
    6
    7
    8
    9
    10
    Done with Loop
    

### Building Basic Guessing Game


```python
secret_word = "giraffe"
guess = ""
guess_count = 0
guess_limit = 3
out_of_guesses = False

while guess != secret_word and not(out_of_guesses):
    if guess_count < guess_limit:
        guess = input("Enter guess: ")
        guess_count += 1
    else:
        out_of_guesses = True
        
if out_of_guesses:
    print("Out of Guesses, YOU LOSE!")
else:
    print("You Win !!")
```

    Enter guess: cs
    Enter guess: s
    Enter guess: giraffe
    You Win !!
    

### For Loop


```python
for index in range(5):
    print(index)
    
friends = ["Jim", "John", "Kevin"]
for friend in friends:
    print(friend)
    
for index in range(5):
    if index == 0:
        print("First Iteration")
    else:
        print("Not first")
```

    0
    1
    2
    3
    4
    Jim
    John
    Kevin
    First Iteration
    Not first
    Not first
    Not first
    Not first
    

### Exponent Component


```python
# print(2**3)

def raise_to_power(base_num, pow_num):
    result = 1
    for index in range(pow_num):
        result = result * base_num
    return result
    
print(raise_to_power(3, 2))
```

    9
    

### 2D Lists and Nested


```python
number_grid = [
    [1, 2, 3],
    [4, 5, 6],
    [7, 8, 9],
    [0]
]

# print(number_grid[2][1])

for row in number_grid:
    for col in row:
        print(col)
```

    1
    2
    3
    4
    5
    6
    7
    8
    9
    0
    

### Build Basic translator


```python
def translate(phrase):
    translation = ""
    for letter in phrase:
        if letter.lower() in "aeiou":
            if letter.isupper():
                translation = translation + "G"
            else:
                translation = translation + "g"
        else:
            translation = translation + letter
    return translation
print(translate(input("Enter a phrase: ")))
```

    Enter a phrase: Ok
    Gk
    

### Comments


```python
#This Program is Comment
print("Comments for Fun") #This prints out a string 

# Single line Comment

```

    Comments for Fun
    

### Try Except


```python
try:
    answer = 10/0
    number = int(input("Enter a number: "))
    print(number)

except ZeroDivisionError:
    print("Divided by Zero")
except ValueError:
    print("invalid input")
except:
    print("Invalid Input")
        
```

    Divided by Zero
    


```python

```
