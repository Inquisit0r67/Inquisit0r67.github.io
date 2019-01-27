# <u>Programming Basics</u>

| Keyword     | Definition                                                   |
| ----------- | ------------------------------------------------------------ |
| Record      | One line of text file                                        |
| Memory      | The location where the instructions and data are stored on the computer. |
| Algorithm   | A sequence of steps that can be followed to complete a  task that always terminates. |
| Mem Address | A specific location in memory where instructions or data is stored |
| Assignment  | The process of giving a value to a variable on constant      |
| Debug       | The process of finding and correcting errors in programs.    |
| Pointer     | A data item that identifies a particular element data structure |


## <u>Naming And Storing Data</u>

The computer program uses instructions and data, which is stored in the memory along with the instructions when it is running. Each memory location has unique address that points to it.

The computer uses the **Fetch, Decode and Execute** cycle to retrieve instructions and carry out processes. 

- This is an example of storing data as a variable on python:
   - `int_number = 12`
- The process of giving data values is called **assigning**.
   - `Number1 <-- 23`
   - `Name <-- "Jason"`

### Constants and Variables

Data can be stored as **constants** or **variables**. It is important to give sensible names to all variables 

- It allows the code to be understood with ease and also allows for easier debugging. 

- Multiple people may be working on the same project so meaningful names allow ease of access.

- It also allows to code to be updated more easily.

Constants are values that remain the same during the duration of the program.

- `ConvertMilestoKm = 1.6`

Variables  are values that can change during the execution of the program.

- `Counter = 0`

### Student Record Task

```python
from enum import Enum

class Gender(Enum):
    UNKNOWN = 0
    MALE = 1
    FEMALE = 2
    OTHER = 3

class Student:
    def __init__(self,
                 name='unnamed',
                 age=-1,
                 gender=Gender.UNKNOWN,
                 lessons_count=-1):
        self.name = name
        self.age = age
        self.gender = gender
        self.lessons_count = lessons_count

    def print(self):
        just = 20
        print(('Name:').ljust(just) + str(self.name))
        print(('Age:').ljust(just) + str(self.age))
        print(('Gender:').ljust(just) + str(self.gender.name))
        print(('Lessons Count:').ljust(just) + str(self.lessons_count))


student1 = Student(name="Deku", age=16, gender=Gender.MALE, lessons_count=3)
```

This is a record for students containing name, age, gender and total number of lessons. It uses classes to enable more efficient code so multiple students can be added with relative ease. This code uses user defined data types.

`Enums` are  a set of symbolic names that can be used to represent certain constant values.

## <u>Data Types</u>

```python
number = 1
string = 'seven'
Boolean = True
Groceries = ['apple', 'pear', 'Lego']
number2 = 3.141
```

There are many data types and you must choose the one most appropriate for the task at hand.

- **Integer**: Any positive or negative whole number. The range of numbers that can be stored depends on the memory of the computer system.
- **Real/Float**: This is a number that contains a decimal or fraction.
- **String**: This data types stores characters that incudes text or numbers. This is also sometimes referred to as *Alphanumeric* data as it can contain any character you want. However you can not perform mathematical operands on this type of data.
- **Boolean**: This is simply a **True** or **False**. These are used in logic statements.
- **Date/Time**: This stores data in a format that is recognised as date or time.
- **Array**: This is a collection of data items of the same type. Each individua item in the array is called an *element*. Here is an example:
  - `Groceries = {'apple', 'fruit', 'pork', 'Lego'}`

Inputting erroneous data will result in an exception to be thrown:

`SyntaxError: invalid syntax`

In python as you do not need to explicitly define what data type a variable is it will throw a syntax error. However, if the program is forced to do a method that requires a specific data type and that data type in incorrect:

`TypeError: expected int got str`

This error will be thrown.

### User-Defined Data Types

Most languages allow for the user too combine existing types of data together, this is called a user defined data type:

```python
class Logon:
    def __init__(self, name, pin):
        self.name = str(name)
        self.pin = int(pin)

        
Operator = Logon('Fuze', 1223)

print(Operator.name)
print(Operator.pin)
```

Above is a user defined type `Logon`. This new data type has the attributes of `name`  as a string and `pin` as a integer. The uses of user defined data types are primarily to do with the efficiency of the code and elegance. This is because it allows programmers to reuse a block of code multiple times rather than write new code. This makes the code less complex and easier to understand and can save time.

## <u>Activities</u>  

#### Higher or Lower Game:

```python
import random

int_numGuess = random.randint(1, 101)
turns = 0
bool_correct = False
while not bool_correct:
    guess = int(input('guess a number between 1 and 100'))
    if guess == int_numGuess:
        print('you won')
        bool_correct = True
    if guess > int_numGuess:
        print('too high')
    if guess < int_numGuess:
        print('too low')
```

This code generates a random number to be guessed and then will loop through a section of code that asks for inputs for user to enter guesses. Each time it will check if the guess is correct, too high, or too low and it will print an appropriate message. 

#### Finding the next 20 leap years:

```python
from datetime import datetime
y=datetime.now().year
for i in range(y, y+(20*4)+1):
  if i%4==0: print(i)
```

This code uses a method to find the next leap year from current year. It does this by using `mod` that gives the remainder of a division. If the year is divisible by 4 without any remainder (so a leap year) it will save that as the next leap year. The code then iterates 20 times printing the next 20 leap years after the next leap year from the current year.

#### Multiplication Table:

```python
print('Here are the twelve times tables')
for i in range(1, 13):
    print(i * 12)
```

This will iterate through the numbers 1 to 13 and print out each number multiplied by 12.

#### Sum of two Numbers:

```python
int_num1 = int(input('enter a number '))
int_num2 = int(input('enter another number '))
print('the sum of those two numbers is ', int_num1 + int_num2)
```

This code will take two integer inputs and then print the sum using mathematical operands

#### Greetings:

```python
name = input('enter username ')
print('hello ', name)
```

This code will take an input in the form of a string as a username and then print it out whilst simultaneously greeting them.

#### String Reversal:

```python
def reverse(a_string):
    return a_string[::-1]


print(reverse('name'))
```

This code has a function that will reverse a string using a python feature. Then using the self made `reverse` method it can reverse any string.

## <u>End Of Chapter Tasks</u>

1. *completed earlier*
2. *completed earlier*

3. It is important to declare all variables and constants at the start of a program as they need to be defined before they are are used in the program. This will force the maker to plan out their code first and allow the computer to identify variables it does not recognise.
4. A variable is an item that contains data and a value if what is usually contained by it.
5. Suitable data types:
   1. For VAT, **Float**
   2. Todays date, **Date/Time**
   3. Revenue, **Float**
   4. DOB, **Date/Time**
   5. Wrist watch worn, **Record/String**

## <u>Study Task</u>

### Multi Dimensional  Arrays:

Multi dimensional arrays allow more complex data to be represented by computers, examples of these are matrices and images. They allow data that is related to be "kept in line".

Here is an example of a 2d array:

```python
a = [[1, 2], ['one', 'two']]
```

Multi Dim arrays are used in Movies:

- Movies are made from a sequence of images.
- An image is a 2d array with each element representing a colour.
- A colour has three components:
  - Red
  - Green
  - Blue

This allows us to model a movie as a multi dim array.



### Data Types (sound):

Sound is stored as most things are in binary. 0s and 1s representing every variation in pitch, tone and frequency. However different **encoding** methods produce different binary code.

It can either be stored: 

- **uncompressed(lossless)**, such as **.wav** files .
-  **compressed(lossless)**, such as **.flac** files.
- **compressed(lossy)**, such as **.mp3** files.

To interpret this data and construct the sound a specific media player will **decode** it using **codecs** and play the sound based on the encoding and the sequence of 0s and 1s.

To record sound a mic is used that converts the electric pulses in **analogue** form to a **digital** format (binary).