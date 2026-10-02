<div align="center">

<h1>SRT111 Lab 3 - Fall 2026</h1>

<strong>Prepared by:</strong> Tiayyba Riaz  
<strong>Total Marks: 10 </strong>  
<strong>Percentage Towards Final Grade: 2% </strong>  

</div>

In this lab, you will design, implement, and test Python programs that use functions. You will practice defining functions, passing arguments, returning values, using loops and conditional statements, and organizing a program using a main() function.

The lab is divided into two components:
- **Part A: In-Class Lab** (must be completed during the scheduled lab period and demonstrated to the professor for grading).
- **Part B: Take-Home Lab** (can be completed independently after thescheduled class).

## Academic Integrity and Use of AI

This lab is intended to assess your individual understanding of Python programming.
You may use AI tools (e.g., ChatGPT, Copilot, Gemini) to help explain concepts, syntax, or error messages. However, all submitted code must be your own work, and you must be able to explain your solution if asked by the professor.

Submitting copied, shared, or AI-generated solutions as your own work may result in a grade of zero and may be handled according to the College Academic Integrity Policy.

## Lab Objectives

By the end of this lab, you should be able to:

- Define and call Python functions.
- Pass arguments to functions and return values from functions.
- Use conditional statements and loops within functions.
- Use a `main()` function to organize a Python program.
- Use positional arguments, default parameters, and keyword arguments.
- Apply functions and programming logic to solve a computational problem.
- Test and debug Python programs.


 ## Required Comment Header
For every script created in this lab  include the following comment block at the top of the file/cell. 
```Python
# Author: Your Name
# Date: YYYY-MM-DD
# Purpose: Brief description of what the program does.
```

---
## Part A - In-Class Lab [40% of Lab Marks]
- Complete all assigned in-class tasks during your scheduled lab.
- This part can be completed in `Jupyter Lab` or `VS Code`. You have choice. I recommend using `Jupyter Lab`.
  - If you are using Jupyter Lab, then please create a single notebook file called `Lab3.ipynb` and complete each task in a unique cell. 
  - If you are using `VS Code` then,  just follow the instructions for each task and create .py files.
- Demonstrate your completed work to the professor before leaving the lab.
- The professor may ask you to explain portions of your code.
- No PDF submission is required for Part A unless otherwise instructed.


### Task 1- Simple Function
**Objective:** Python function that checks whether any number in a list is even using a loop and conditional logic.

**Instructions:**

- Create a file named `task1.py`.
- Write a function with the name `has_even_number` that:  
   - Takes a `list` as a parameter.
   - Uses a `for` loop to iterate over each element of the list.
   - Uses an `if` statement to check if an element is even.
   - Returns `True` if any number in the list is even.
   - Returns `False` otherwise.
- Outside and after the  `has_even_number` function, creates a list of 6 integer values.
- Calls the `has_even_number()` function with that list.
- Store the returned Boolean value in a variable.
- Print the Boolean result..
- Run your script to test it.

### Task 2 - Filtering Even Numbers
**Objective:** Write a Python function that uses a loop and a conditional statement to create a new list containing only the even numbers from a given list.

**Instructions:** 
- Create the file `task2.py`.
- Write a function named `even_numbers` that:
     - Takes a list of integers as a parameter.
     - Creates an empty list to store the even numbers.
     - Uses a `for` loop to iterate through the list.
     - Checks each element to see if it is even.
     - Store even numbers to a new list.
     - Returns the new list of even numbers.
     - If no even numbers are found, return an empty list.
- After defining the function, create a list of 8 integer values outside the function.
- Call the `even_numbers()` function and pass the list as an argument.
- Store the returned list in a variable
- Print the resulting list.
- Run your script to test its functionality

### Task 3 - Using the `main()` Function
**Objective:** Introduce the use of the `main()` function as the entry point of a Python program and practice calling another function from within it.

**Instructions:**
- Create the file `task3.py`.
- Write a function named `add_numbers` that:
  - Takes two numbers as parameters.
  - Calculates and returns thir sum.
- Write a `main()` function that:
  - Prompts the user to enter two numbers.
  - Converts the input values to integers.
  - Calls the `add_numbers()` function and passes the two numbers as arguments.
  - Stores the returned result in a variable.
  - Prints the result for the user.
- Add a call to the `main()` function.
- Run your script to test it.

---

## Part B - Take-Home Lab [60% marks]
Complete the following tasks independently after the scheduled lab using VS Code.
Before You Begin:
- Open your local Git repository **`SRT111F2026`** on your computer.
- Create a new folder named **`Lab03`** inside the repository.
- Open the **`Lab03`** folder in VS Code.
- Create all Python files for this lab (`task4.py`, `task5.py`, `task6.py`) inside the **`Lab03`** folder.
- For each task:
   - Run the script using the VS Code terminal
   - Take a screenshot that clearly shows:  
      - Your code in the editor.  
      - The terminal output, including your username visible in the terminal.  
   - Insert the screenshots into a Word document under the heading. You will export this word document to PDF and submit it on Blackboard.

### Task 4 - Writing the complete calculator function using default parameters and positional parameters
**Objective:** Practice defining a function with multiple parameters, using a default parameter, and passing arguments using positional arguments..

**Instructions:**
- Create the file `task4.py` and fill in the required fields in the comment section:
- Write a function named `compute` that:
  - Takes three parameters:
    - `num1`: the first number
    - `num2`: the second number
    - `operation`: a symbol (`+`, `-`, `*`, `/`) with a default value of `+`
  - Performs the specified operation on `num1` and `num2`.
  - Returns the calculated result.
- Write a `main()` function that:
  - Prompts the user to enter two numbers.
  - Prompts the user to choose an operation (`+`, `-`, `*`, `/`).
  - Calls the `compute()` function using **positional parameters**.
  - Stores the returned result in a variable
  - Prints the result for the user.
- Demonstrate the function with the following calls:
    ``` python
    print(compute(13,45,'*'))
    print(compute(13,45,'/'))
    print(compute(13,45,'-'))
    print(compute(13,45,'+'))
    print(compute(13,45))  # since only two parameters are passed the default value of symbol should be used.
    ```
- Add a call to the `main()` function.
- Run your script to test it.


## Task 5 - Calculator Function with Keyword Arguments
**Objective:** Practice using **keyword arguments** when calling a function and understand how keyword arguments allow arguments to be passed in a different order

**Instructions:**
- Create the file `task5.py`.
- Copy your `calculate()` function and `main()` function from `task4.py`.
- Modify the `calculate()` function so that it uses **keyword parameters** instead of positional parameters when being called.
- Ensure that the function definition remains the same.
- Demonstrate that keyword arguments allow the arguments to be provided in a different order by using the following function calls in the `main()`:
```Python
print(compute(num1=13, num2=45, operation='*'))
print(compute(operation='/', num2=45, num1=13))
print(compute(num2=45, num1=13, operation='-'))
print(compute(num1=13, num2=45, operation='+'))
print(compute(num1=13, num2=45))  # Uses default operation '+'
```
- Run your program and verify that all function calls produce the expected results.
- Note: Refer to your course notes or lesson slides if you need help with keyword arguments
  
### Task 6 - Using variable number of arguments with `*args`
**Objective:** how to use `*args` to accept a variable number of arguments in a Python function. This allows the function to handle flexible input sizes.

**Instructions:**
- Create the file `task5.py`.
- Write a function named `get_initials` that:
  - Uses `*args` to accept a variable number of names.
  - Uses a for loop to process each name.
  - Extracts the first character from each name.
  - Stores the first characters in a list.
  - Returns the list of initials.
- Call the `get_initials()` function with the names "Samuel", "Ravi", "Chen", "Fatima".
- Store the returned values in variables and print the results.
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
---
## Part B Sign-Off
- commit and push your Lab02 folder to GitHub repo `SRT111F2026`.
- Submit a PDF named using your Seneca username, **<your-username>.pdf** on *Blackbaord*.
- Your PDF must include:
    - Task 4 screenshot(s)
    - Task 5 screenshot(s)
    - Task 6 screenshot(s)
- Ensure the code and output are clearly readable. Screenshots should be high-resolution (minimum 800x600) and not blurry.
- Blurry or unreadable submissions will be returned for redo. Resubmissions will only be graded as "**Satisfactory**" with a grade of 0, provided the work is satisfactory.

