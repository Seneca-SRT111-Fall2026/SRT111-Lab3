# PRG101-Lab4
### Submission Details

In this lab, you will create 5 simple scripts (and an optional sixth script). Write the scripts in GitHub codespaces. 
Please note that you must complete the lab during class hours and show your progress to the professor to receive the marks for the lab.

### Lab Objectives
- To be able to write the programs using functions.
- Reinforce the concept of conditions and loops.
- Build logic to solve a computational problem.
  
## INVESTIGATION 1: Functions

A function is a block of code that performs a specific task. Functions help to organize code, make it reusable, and improve readability. 
Functions help us avoid writing the same code repeatedly. If you remember, we used the len() function to determine the length of a string. Since measuring the length of a sequence (string or list) is a frequent task, it makes sense to have a function that can perform this action whenever needed.
Functions are among the most fundamental tools for reusing code in Python, and they also introduce us to the concept of program design. You should use functions when you anticipate reusing a block of code multiple times. By defining a function, you can call the same code without needing to rewrite it, which helps in creating more complex Python scripts.
Let's see how to create our own functions.

### Defining a Function

To define a function in Python, use the `def` keyword followed by the function name and parentheses (). Make sure the name is relevant and does not conflict with built-in Python functions like `round` or `print`.

Next, include any arguments your function needs inside the parentheses, separated by commas. These arguments are the inputs for your function, and you can reference them within the function. After the parentheses, add a colon ":" 

On the next line, write the indented block of code that forms the body of the function.
Inside the body of the function, as a convention, and, as a good programming practice you shouldstart with the docstring. This is where you write a basic description of the function so that you can refer to it when you comeback to your code later, or, if you are working in a team, so that your team members can know what is this function about.
After the docsting you write the logic and code of your function.
Functions can also return a value or multiple values (all packed as a tuple).


#### Syntax

```python
def function_name(parameters):
    # Code block
    return value  # Optional
```
#### Example

```python
def greet(name):
    print(f"Hello, {name}!")
```

#### Explanation

- `def`: Keyword to start the function definition.
- `function_name`: The name of the function.
- `parameters`: Variables passed to the function (optional).
- `return`: Ends the function and optionally returns a value.

### Calling a Function

To execute a function, call it by its name followed by parentheses, optionally including arguments. If you forget the parenthesis (), it will simply display the statement that `greet` is a function.

#### Example
```python
greet("Alice")
Output: Hello, Alice!
```

### Function Parameters

Functions can accept parameters to make them more flexible.

#### Example

```python
def add(a, b):
    return a + b

result = add(3, 5)
print(result)
# Output: 8
```

### Default Parameters

You can define default parameter values in a function.

#### Example

```python
def greet(name="Guest"):
    print(f"Hello, {name}!")

greet()
# Output: Hello, Guest!

greet("Bob")
# Output: Hello, Bob!
```

### Return Values

Functions can return values using the `return` statement.

#### Example

```python
def multiply(a, b):
    return a * b

result = multiply(4, 5)
print(result)
# Output; 20
```

## lab4a.py 
### Simple Function

- Fill in the required fields in the comment section.
- Write a function with the name `is_even`. The function takes a list as a parameter and returns `True` if any number in the list is even, the function returns `False` otherwise.
- You must use a `for` loop to iterate over each element of the list.
- You must use an `if` statement to check if an element is even.
- As soon as you find the first even element, `break` out of the loop.
- Call the function with a list of 6 integer values. Receive the result in a boolean variable.
- Print the boolean variable.
- Run your script to test it.



## lab4b.py 
### Adding some complexity to the function  logic.

- Fill in the required fields in the comment section.
- Write a function called `even_numbers` that  takes a list as argument and returns a new list of all the even numbers from the list.
- If the passed list does not contain any even numbers, return an empty list.
- Call the function with a list of 8 integer values.
- Receive the result in a list variable and print the list variable.
- Run your script to test it.

## Using the main function.
Remember you learnt in the class that we should use main function as entry point to our program.
The main() function in Python is a convention rather than a built-in function. It organizes code in a clear, structured way.
It serves as the starting point for the program. When the script is executed, the code inside the main() function runs first.
In this next example, write a function `sum` that takes two numbers as parameters and returns their sum. You will call `sum` from `main`.


### lab4c.py 
-  Fill in the required fields in the comment section.
-  Write a function `sum` that takes two numbers as parameters and returns their sum.
-  Write the `main` functions.
-  In the main function get two numbers from user. Convert the user input to int.
-  Call the `sum` function and pass the two numbers as argument.
-  In the main() function, receive the sum in a variable, and print the sum for the user.
-  Call the main function inside the condition:
 
  ``` python
if __name__ == __main__:
main()
```
Note that the above line checks whether the script is being run directly or being imported as a module. If it's run directly, main() is called.
- Run your script to test it.


## lab4d.py 
### Writing the complete calculator function using default parameters and positional parameters
Positional parameters are arguments passed to a function based on their position (order) in the function definition.
When calling the function, the first argument provided is assigned to the first parameter, the second argument to the second parameter, and so on. Default parameters are explained above. 


- Fill in the required fields in the comment section.
- Write a function `compute` which takes three parameters; two numbers and one operation.
    - first parameter is num1
    - second parameter is num2
    - third parameters is the operation as a symbol ( +, -, *, /)
    - third parameter should have a default value of +

- The function performs the required operation on the two numbers and returns the result. The function should receive the parameters as positional parameters.
- Write the `main` functions.
- In the main function get two numbers from user.
- In the main also ask the user to chose which operation they want to perform. Show the operation symbols in the prompt.
- Call the  `compute` function as follows:
    ``` python
    compute(13,45,'*')
    compute(13,45,'/')
    compute(13,45,'-')
    compute(13,45,'+')
    compute(13,45)  # since only two parameters are passed the default value of symbol should be used.
    
    ```
- Call the main function in the conditional statement as shown above in `lab4c`.
- Run your script to test it.


## lab4e.py 
### Writing the complete calculator function using keyword parameters
Keyword parameters (or keyword arguments) are arguments passed to a function by explicitly naming each parameter, allowing you to pass arguments out of order.
- Fill in the required fields in the comment section.
- Copy the code from lab4d.py and modify the parameters to behave as keyword parameters rather than positional parameters.
- Refer to lesson slides if you need help on how to use keyword arguments.
- Run your script to test it.


## lab4f.py
### Using variable number of arguments with *args
- Fill in the required fields in the comment section.
- Write a function called `get_initials` that returns the first letter from each provided name. It can handle a variable number of name inputs.
- The function uses `*args` to accept a variable number of name inputs.
- The function iterates through each name and extract the first letter.
- The function collects these first letters into a list.
- Finally, the function returns the list of initials.
- Given the names "Alice", "Bob", "Charlie", and "David", the function will return the list `['A', 'B', 'C', 'D']`.
- Call the  `get_initials` function from `main` function and receive the result in a list variable.
- Print the result in `main`.
- Run your script to test it.

 ## lab4g.py  (Optional Activity: Adavanced Level)
### Using map, filter and lambda expressions.
map() applies a function to all items in an iterable.

```Python
result = map(lambda x: x * 2, [1, 2, 3])  # Output: [2, 4, 6]
```

filter() selects items from an iterable based on a function that returns True or False.

```Python
result = filter(lambda x: x > 2, [1, 2, 3, 4])  # Output: [3, 4]
```

lambda creates small, anonymous functions for quick, on-the-fly use.

```Python
square = lambda x: x ** 2  # Usage: square(3) -> 9
```
- Create a variable list named numbers containing numbers from 2 to 10.
- square all elements of this list using map and lambda function.
- Print variable numbers.
- Make a new variable named divisible_by_2.
- Filters out all numbers from numbers list that are divisible by 2 using filter and lambda, and save them in this variable.
- Print variable divisible_by_2.

## Lab 4 Sign-Off
- Submit the screenshots of each individual script, the screenshot must show your scripts and command line interface and output.
- The screenshot must also show your username on github codespaces.
- Submit individual screenshots of the following scripts on blackboard. If the screenshots do not correctly show the information mentioned above, you will get zero marks for the lab.
    - lab4a.py
    - lab4b.py
    - lab4c.py
    - lab4d.py
    - lab4e.py
    - lab4f.py
    
    
