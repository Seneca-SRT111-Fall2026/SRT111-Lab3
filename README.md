# Lab 3
In this lab, you will create six simple Python scripts. All scripts must be written in GitHub Codespaces. This lab focuses on writing functions.
You will explore how to define and use functions in Python to solve problems more efficiently. Through hands-on practice, you'll learn how functions improve code organization, readability, and reusability — essential skills for building scalable programs.

## Lab Objectives
- To be able to write the programs using functions.
- Reinforce the concept of conditions and loops.
- Build logic to solve a computational problem.

## Submission Instructions
For each task:
1. **Write the script** in Codespaces.  
2. **Run the script** from the **terminal**.  
3. **Take a screenshot** that clearly shows:  
   - Your **code** in the editor.  
   - The **terminal output**, including your **username** visible in the terminal.  
4. **Insert the screenshot** into a Word document under the heading that matches the task name:  
   - Example: **Lab3a**, **Lab3b**, **Lab3c**, etc.  
5. After completing all tasks, **convert the Word document to PDF**.  Name the PDF file using your **Seneca username**, for example salim123.pdf
6. **Submit the PDF file** as your final lab submission on Blackbaord.

## INVESTIGATION 1: Functions

A function is a block of code that performs a specific task. Functions help organize code, make it reusable, and improve readability. They allow us to avoid writing the same code repeatedly. For example, we’ve used the len() function to determine the length of a string. Since measuring the length of a sequence (string or list) is a frequent task, it makes sense to have a function that performs this action whenever needed.

Functions are among the most fundamental tools for reusing code in Python. They also introduce us to the concept of program design. You should use functions when you anticipate reusing a block of code multiple times. By defining a function, you can call the same code without rewriting it, which helps in creating more complex Python scripts.
Let's see how to create our own functions.

### Defining a Function

To define a function in Python, use the `def` keyword followed by the function name and parentheses (). Make sure the name is relevant and does not conflict with built-in Python functions like round or print.

Next, include any arguments your function needs inside the parentheses, separated by commas. These arguments are the inputs for your function, and you can reference them within the function. After the parentheses, add a colon :.

On the next line, write the indented block of code that forms the body of the function.

Inside the body of the function, it is good practice to start with a docstring — a brief description of what the function does. This helps you (and others) understand the function later, especially when working in teams.

After the docstring, write the logic and code of your function. Functions can also return a value or multiple values (packed as a tuple).

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

## lab3a.py - Simple Function
**Objective:** Python function that checks whether any number in a list is even using a loop and conditional logic.

**Instructions:**

- Open the file Lab3a.py and fill in the required fields in the comment section.
- Write a function with the name `is_even` that:  
   - Takes a list as a parameter.
   - Uses a `for` loop to iterate over each element of the list.
   - Uses an `if` statement to check if an element is even.
   - Returns `True` if any number in the list is even. As soon as you find the first even element, `break` out of the loop.
   - Returns `False` otherwise.
   - As soon as you find the first even element, `break` out of the loop.
- Outside and after the  `is_even` function, creates a list of 6 integer values.
- Calls the `is_even()` function with that list.
- Stores the result in a boolean variable.
- Prints the boolean variable.
- Run your script to test it.


## lab3b.py - Filtering Even Numbers
**Objective:** Write a Python function that returns a new list containing only the even numbers from a given list.

**Instructions:** 

- Open the file `lab3b.py` and fill in the required fields in the comment section.
- Write a function named `even_numbers` that:
     - Takes a list of integers as an argument.
     - Uses a `for` loop to iterate through the list.
     - Checks each element to see if it is even.
     - Store even numbers to a new list.
     - Returns the new list of even numbers.
     - If no even numbers are found, return an empty list.
- After defining the function, create a list of 8 integer values outside the function.
- Call the `even_numbers()` function with that list.
- Store the result in a new list variable. 
- Print the resulting list.
- Run your script to test its functionality

## Using the main function.
Remember you learnt in the class that we should use main function as entry point to our program.
The main() function in Python is a convention rather than a built-in function. It organizes code in a clear, structured way.
It serves as the starting point for the program. When the script is executed, the code inside the main() function runs first.
In this next example, write a function `sum` that takes two numbers as parameters and returns their sum. You will call `sum` from `main`.


### lab3c.py - Using the `main()` Function
**Objective:** Introduce the use of the `main()` function as the entry point of a Python program and practice calling another function from within it.

**Instructions:**
- Open the file `lab3c.py` and fill in the required fields in the comment section:
- Write a function named `sum` that:
  - Takes two numbers as parameters.
  - Returns the sum of the two numbers.
- Write a `main()` function that:
  - Prompts the user to enter two numbers.
  - Converts the user input to integers.
  - Calls the `sum()` function and passes the two numbers as arguments.
  - Stores the result in a variable.
  - Prints the result for the user.
- At the end of your script, include the following condition to ensure the `main()` function runs only when the script is executed directly:
  ```python
  if __name__ == "__main__":
      main()
Note that the above line checks whether the script is being run directly or being imported as a module. If it's run directly, main() is called.
- Run your script to test it.


### lab3d.py - Writing the complete calculator function using default parameters and positional parameters
**Objective:** Understand how to use **positional parameters** and **default parameters** in Python functions. Positional parameters are assigned based on the order of arguments passed, while default parameters provide fallback values when arguments are not supplied.

**Instructions:**
- Open the file `lab3d.py` and fill in the required fields in the comment section:
- Write a function named `compute` that:
  - Takes three parameters:
    - `num1`: the first number
    - `num2`: the second number
    - `operation`: a symbol (`+`, `-`, `*`, `/`) with a default value of `+`
  - Performs the specified operation on the two numbers.
  - Returns the result.
Write a `main()` function that:
  - Prompts the user to enter two numbers.
  - Prompts the user to choose an operation (`+`, `-`, `*`, `/`).
  - Calls the `compute()` function using **positional parameters**.
  - Stores the result in a variable.
  - Prints the result for the user.

- Demonstrate the function with the following calls:
    ``` python
    compute(13,45,'*')
    compute(13,45,'/')
    compute(13,45,'-')
    compute(13,45,'+')
    compute(13,45)  # since only two parameters are passed the default value of symbol should be used.
    
    ```
- Call the main function in the conditional statement as shown above in `lab3c`.
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
    
    
