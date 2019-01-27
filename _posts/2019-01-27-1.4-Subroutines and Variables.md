# <u>Subroutines and Variables</u>

| Keyword                | Definition                                              |
| ---------------------- | ------------------------------------------------------- |
| Subroutine             | A named block of code made to carry out a specific task |
| Procedure              | Synonym for a subroutine                                |
| Local Variable         | A variable only available in specific subroutines       |
| Global Variable        | A variable available anywhere in the program            |
| Event                  | Something that occurs while the program is running      |
| Module                 | A number of subroutines that make up part of a program  |
| Function               | A subroutine that returns a value                       |
| Functional Programming | A technique that uses functions to create programs      |
| Parameter              | Data being passed through a subroutine                  |
| Argument               | An item of data being passed into a subroutine          |
| Block Interface        | Code that describes the data that is being passed       |

### Subroutines 

Subroutines are blocks of code found in structured programs that can be called for certain functions. 

For example, if a game was built involving a dice throw, then a separate function may be written for rolling the dice each time. This allows for the dice throw to simply be called whenever, rather than having to copy out the code each time. Subroutines can also come in the form of functions, where the code usually takes an input from elsewhere in the code (as an argument or parameter), then returns a different value to be used. 

### Functions 

Functions do the same as a subroutine but also **return** a variable. Similarly to subroutines they keep code clean and elegant as well as save time for the programmer as they can be used multiple times. **Functional Programming** uses functions to work.

### Parameters and Arguments

This is how data is provided to a subroutine or function. They work similarly to variables and is the actual value being passed through the subroutine.

### Local and Global Variables

Variables can be defined to either exist anywhere in the code or only in a specific subroutine. They come in the form or **Global** and **Local** variables.

It is better practise to use local variables as to avoid inadvertently changing variables causing errors. Using local variables also allows you to use the same variable names in different places. Typically if a variable is used thorough the whole program it should be defined as a global variable and vice versa.

```python
global Constant_R = 8.314
```

 Above is an example of a global variable in python

## <u>End Of Chapter Tasks</u>

1. A function returns a value (it is called) whilst the code usually runs through the subroutine and so does not return a value. 
2. Python contains many built in functions to just the base language including string manipulation functions and mathematical functions, but can also import and download modules for much more functionality. 
3. Subroutines is a way of structuring your code into blocks so you can easily see what happens where. If you need to take a lot of input and processing, and output a lot of numbers and values, then it may be best to split your program into input and output subroutines. 
4. Functions can be used to repeatedly call algorithms to process data multiple times. 
5. A module is a complete separate 'area' of code. Whilst subroutines are usually in the same area as others, modules are isolated environments that do not have any access to variables from other modules unless specified otherwise. This is good for running separate programs from the same main program. 
6. Parameters are indicators to what values or data types should be used in a subroutine – and the arguments are what is passed in. 
7. A piece of code denoted by INTERFACE lines that moves code from one subroutine to another. 
8. An exception handler 'catches' the exception, stopping the program from breaking, and instead carries out a process written in the code. 

## <u>Study/Research</u>

```python
import math
global inpt

try:
    inpt = float(input('Enter num'))
except TypeError:
    print('not correct data type')
    break

def square_root(num):
    num = math.sqrt(num)
    return num

def Square(num):
    num = number**2
    return num

```

This code uses multiple techniques covered in these notes to find a square root of any number. It is in no way the most efficient way and is only used to fulfil the tasks set.