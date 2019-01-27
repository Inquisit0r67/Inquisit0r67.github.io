# <u>Basic Operations</u>

| Keywords                        | Definition                                                   |
| ------------------------------- | ------------------------------------------------------------ |
| Arithmetic Operation            | common expressions such as +, -, / and *.                    |
| Rounding                        | Reducing the number of digits used to represent a number while maintaining value that is approximately equivalent. |
| Truncating                      | The process of cutting off a number after a certain number of characters or decimal places. |
| Pseudo-random number generation | Common function that produces a random number that is not 100% random. |
| Relational Operations           | Expressions that compare to values such as equal to or greater than. |
| String handling Functions       | Actions that can be carried out on a sequence of characters. |
| Character Code                  | A binary representation of a particular letter, number or specific character. |

## <u>Arithmetic Operations</u> 

### Division

```python
int_num1 = 4342
int_num2 = 3423

product_remainder = int_num1 % int_num2
product_quotient = int_num1 // int_num2

print('Remainder is ' + str(product_remainder) + '. Quotient is ' + str(product_quotient))
```

Output is: `Remainder is 919. Quotient is 1`

### Random Number Generation

Most random number generators are actually **pseudorandom** number generators and they actually use a seed value and a pre-set algorithm to create random numbers. This means the numbers are never truly random.

### Relational Operations

| Operator | Definition               |
| -------- | ------------------------ |
| >        | Greater than             |
| <        | Less than                |
| ==       | Equal to                 |
| <=       | Greater than or equal to |
| *>=      | Less than or equal to    |
| !=       | Not equal to             |

The results of all relational operations are either **True** or **False**.

### Boolean Operations

Booleans expressions hold a True or False value. They cannot hold any other value other than a binary 1 or 0 option. 

Booleans operators can be used in statements such as If statements, or to write out flowcharts and pseudocode. Examples of Boolean operators in binary include: 

AND:

| A    | B    | Output |
| ---- | ---- | ------ |
| 0    | 0    | 0      |
| 0    | 1    | 0      |
| 1    | 0    | 0      |
| 1    | 1    | 1      |

OR:

| A    | B    | Output |
| ---- | ---- | ------ |
| 0    | 0    | 0      |
| 1    | 0    | 1      |
| 0    | 1    | 0      |
| 1    | 1    | 1      |

## <u>String Handling Functions</u>

These are methods that can be applied to strings to produce a desired affect.

- length: `len('')`
- String: `str()`
- Position: `var.index('')`
- ASCII (American Standard Code for Information Interchange): `ord('')`
- Char: `chr()`
- Integer: `int()`

#### Three Blind Mice Activity:

```python
# Declaring vaiables
og = """Three blind mice. Three blind mice.
See how they run. See how they run.
They all ran after the farmer's wife,
Who cut off their tails with a carving knife,
Did you ever see such a sight in your life,
As three blind mice?"""
i = 0
x = 0
l = len(og)
asc = []

while i < l - 1:
    temp = og[i]
    temp = ord(temp)                       # converts the letter to ascii
    asc.append('{0:08b}'.format(temp))     # converts the ascii to 8 bit binary
    i += 1
for x in range(len(asc)):
    print(asc[x])                          # prints each binary value on a line
```

## <u>End Of Chapter Tasks</u>

1. A real/float is a number that is not whole so has decimal points after it. Therefore the result of a float or real division must also be a float or real. 
2. An integer division can be divided into another integer, but should also be stored as a float because it can become a decimal number. 
3. Variables are used soo the values can have names and be easily called and used later in code. If they are not assigned variables, the raw values cannot be used later in the code or parsed somewhere else. 
4. Truncation is  cutting off a number by a certain amount of decimal points (or units), whilst rounding does not cut off numbers but rather simplifies them, removing decimal points by changing the units. 
5. An OR statement will return true if any input is true, including multiple true inputs. An XOR will only return true if one input is true. If none or multiple are true, the result will be false. 
6. Python strings are **immutable** after initialisation, but they can be 'sliced' in order to get portions of the code. 
7. Strings can be converted to other formats provided the values they hold are able to be used. For example, if a string is '1', then it can be changed to an int, but is a string is 'a', it cannot and will throw an error. 
8. Computers cannot make random numbers as they work off a basis of **explained earlier**.

## <u>Study/Research Task</u>

### Extracting Vowels

```python
a = list('abcdefghijklmnopqrstuvwxyz')
v = 'aeiou'

for i range(0, len(a)):
    for h in range(0, 5):
        if a[i] == v[h]:
            a[i] = " "
            
print(a)
```

This code will iterate through the alphabet and replace all vowels with an empty space, it will then print the alphabet that now has no vowels.