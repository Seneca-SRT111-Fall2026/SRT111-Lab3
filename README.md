<div align="center">

<h1>SRT111 Lab 3 - Fall 2026</h1>

<strong>Prepared by:</strong> Tiayyba Riaz  
<strong>Total Marks: 10 </strong>  
<strong>Percentage Towards Final Grade: 2% </strong>  

</div>

In this lab, you will design, implement, and test Python programs that use functions.

The lab is divided into two components:
- **Part A: In-Class Lab** (must be completed during the scheduled lab period and demonstrated to the professor for grading. ).
- **Part B: Take-Home Lab** (can be completed independently after thescheduled class).

## Academic Integrity and Use of AI

This lab is intended to assess your individual understanding of Python programming.
You may use AI tools (e.g., ChatGPT, Copilot, Gemini) to help explain concepts, syntax, or error messages. However, all submitted code must be your own work, and you must be able to explain your solution if asked by the professor.

Submitting copied, shared, or AI-generated solutions as your own work may result in a grade of zero and may be handled according to the College Academic Integrity Policy.

## Lab Objectives
- To be able to write the programs using functions.
- Reinforce the concept of conditions and loops.
- Build logic to solve a computational problem.

 ## Required Comment Header
For every script created in this lab  include the following comment block at the top of the file/cell. 
```Python
# Author: Your Name
# Date: YYYY-MM-DD
# Purpose: Brief description of what the program does.
# Usage: python ./task1.py
```

---
## Part A - In-Class Lab [40% marks]
- Complete all assigned in-class tasks during your scheduled lab.
- This part can be completed in `Jupyter Lab` or `VS Code`. You have choice. I recommend using `Jupyter Lab`.
  - If you are using Jupyter Lab, then please create a single notebook file called `Lab2.ipynb` and complete each task in a unique cell. 
  - If you are using `VS Code` then,  just follow the instructions for each task and create .py files.
- Demonstrate your completed work to the professor before leaving the lab.
- The professor may ask you to explain portions of your code.
- No PDF submission is required for Part A unless otherwise instructed.
- Each task carries 1.0 marks.

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

## Task 1- Simple Function
**Objective:** Python function that checks whether any number in a list is even using a loop and conditional logic.

**Instructions:**

- Open the file task1.py and fill in the required fields in the comment section.
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

## Task 2 - Filtering Even Numbers
**Objective:** Write a Python function that returns a new list containing only the even numbers from a given list.

**Instructions:** 
- Open the file `task2.py` and fill in the required fields in the comment section.
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
Remember you learned in the class that we should use main function as entry point to our program.
The main() function in Python is a convention rather than a built-in function. It organizes code in a clear, structured way.
It serves as the starting point for the program. When the script is executed, the code inside the main() function runs first.
In this next example, write a function `sum` that takes two numbers as parameters and returns their sum. You will call `sum` from `main`.


### Task 3 - Using the `main()` Function
**Objective:** Introduce the use of the `main()` function as the entry point of a Python program and practice calling another function from within it.

**Instructions:**
- Open the file `task3.py` and fill in the required fields in the comment section:
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


### Task 4 - Writing the complete calculator function using default parameters and positional parameters
**Objective:** Understand how to use **positional parameters** and **default parameters** in Python functions. Positional parameters are assigned based on the order of arguments passed, while default parameters provide fallback values when arguments are not supplied.

**Instructions:**
- Open the file `task4.py` and fill in the required fields in the comment section:
- Write a function named `compute` that:
  - Takes three parameters:
    - `num1`: the first number
    - `num2`: the second number
    - `operation`: a symbol (`+`, `-`, `*`, `/`) with a default value of `+`
  - Performs the specified operation on the two numbers.
  - Returns the result.
- Write a `main()` function that:
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
- Call the main function in the conditional statement as shown above in `task4.py.
- Run your script to test it.


## Task 5 - Writing the complete calculator function using keyword parameters
**Objective:** Learn how to use **keyword parameters** in Python functions. Keyword arguments allow you to pass values to function parameters by explicitly naming them, enabling flexibility in the order of arguments.

**Instructions:**
- Open the file `task5.py` and fill in the required fields in the comment section:
- Copy the code from `task4.py`.
- Modify the `compute()` function so that it uses **keyword parameters** instead of positional parameters when being called.
- Ensure that:
  - The function definition remains the same.
  - All function calls explicitly name the parameters (e.g., `compute(num1=13, num2=45, operation='*')`).
  - You demonstrate that keyword arguments allow calling the function with parameters in any order.
- Refer to your lesson slides if you need help on how to use keyword arguments.
- Run your script to test its functionality.
- Following are the function calls using keyword arguments
```Python
print(compute(num1=13, num2=45, operation='*'))
print(compute(operation='/', num2=45, num1=13))
print(compute(num2=45, num1=13, operation='-'))
print(compute(num1=13, num2=45, operation='+'))
print(compute(num1=13, num2=45))  # Uses default operation '+'
```
## Task 6 - Using variable number of arguments with `*args` (Optional)
**Objective:** how to use `*args` to accept a variable number of arguments in a Python function. This allows the function to handle flexible input sizes.

**Instructions:**
- Open the file `task5.py` and fill in the required fields in the comment section:
- Write a function named `get_initials` that:
  - Uses `*args` to accept a variable number of name inputs.
  - Iterates through each name and extracts the first letter.
  - Collects these first letters into a list.
  - Returns the list of initials.
- Call the `get_initials()` function with the names "Samuel", "Ravi", "Chen", "Fatima".
- Store the result in a list variable.
- Print the result.
- Run your script to test its functionality.
**Sample Output**
```Python
print(get_initials("Emma", "Maija", "Sophia"))
#Output: ['E', 'M', 'S']

print(get_initials("John"))
#Output: ['J']

print(get_initials("Olivia", "Ravi", "Chen", "Fatima"))
#Output: ['AO', 'R', 'C', 'F']  # Case preserved exactly as in input
```
## Lab 3 Sign-Off
- Submit a PDF named using your Seneca username, .pdf on Blackboard.
- The document must include screenshots of the following scripts and their terminal output, clearly showing your GitHub username:
    - task1.py
    - task2.py
    - task3.py
    - task4.py
    - task5.py
    - task6.py
- Ensure the code and output are clearly readable. Screenshots should be high-resolution (minimum 800x600) and not blurry.
- Blurry or unreadable submissions will be returned for redo. Resubmissions will only be graded as **Satisfactory** with a grade of 0, provided the work is satisfactory.

