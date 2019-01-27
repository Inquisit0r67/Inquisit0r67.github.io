# <u>Programming Concepts</u>

| Keyword              | Definition                                                   |
| -------------------- | ------------------------------------------------------------ |
| Selection            | The principle of choosing what action to take based on certain criteria. |
| Nesting              | Placing one set of instructions within another.              |
| Iteration            | The principle of repeating processes.                        |
| Definite Iteration   | A process that repeats a set number of times                 |
| Indefinite Iteration | A process that repeats until a set condition is met          |
| Loop                 | A repeated process                                           |
| Sequence             | The principle of putting correct instructions in the right order within a program |

## <u>Sequencing</u>  

This makes sure that each line of code is executed in the correct order for it to function as required. This could mean the order of when a variable is defined and then subsequently used in the code.

Coding statements change depending on the language being used and is largely dictated by the syntax of the language.

#### Compilers and Interpreters

- **Compiler**
  - Compiles the entire code first then proceeds to execute it.
  - This means it takes a longer time to run code.
  - Shows any errors after it compiles the code and before it executes.
- **Interpreter**
  - Executes the program one line at a time.
  - Naturally this means it is able to execute code faster.
  - Shows errors as they appear, this allows for easier debugging.

## <u>Selection</u>

Selection is the process of comparing a variety of values and then deciding a route to take. Take this `If` statement for example:

```python
if Height < minHeight:
    print('too small')
    break
else:
    print('acceptable')
    break
```

This code will compare two values; `Height` and `minHeight` using mathematical operands and then use the result of that comparison to see if it meets a certain condition which will dictate its next course of action.

Adding a `elseif` statement will transform this into a **Nested selection**.

```python
if Height < minHeight:
    print('too small')
    break
elif Height = minHeight:
    print('thats very close')
    break
else:
    print('acceptable')
    break
```

This is a more complex form of a selection that can be used to complete more complex tasks.

## <u>Iteration</u>

### Definite

This is the method of carrying out a process for a set number of times.

```python
from datetime import datetime
y=datetime.now().year
for i in range(y, y+(20*4)+1):
  if i%4==0: print(i)
```

This code will repeat 21 times as it goes through the range from the current year till the 20th leap year from the current year and will stop after that.

### Indefinite

This method of iteration will loop through code until a specific condition is met after which it will proceed to the next section of code or carry on looping doing different things each time.

```python
from bs4 import BeautifulSoup
import urllib3
import certifi
import discord
import asyncio
import random

Token = 'ND0kwMTQ0OTU0NjAy0MjI1Njc1.sDn1HoA.zYw4NKvw6gXGPsJo45RMFr0'
client = discord.Client()
status_options = ['Gathering News', 'Falsifying Stories', 'Interviewing People']
search_term = 'Anime'


@client.event
async def on_ready():
    print('Logged in as')
    print(client.user.name)
    print(client.user.id)
    print('------')

    last_post = ''
    tweets_content = []
    https = urllib3.PoolManager(cert_reqs='CERT_REQUIRED', ca_certs=certifi.where())
    url = 'https://mobile.twitter.com/' + search_term

    run = True
    while run:
        await client.change_presence(game=discord.Game(name=random.choice(status_options)))
        await asyncio.sleep(5)
        tweets_content.clear()
        page = https.request('GET', url)
        soup = BeautifulSoup(page.data, 'html.parser')

        tweets_author = soup.find('strong', {'class': 'fullname'})
        tweets_content = soup.find_all('div', {'class': 'dir-ltr'} and {'dir': 'ltr'})[1]
        tweets_link = soup.find('a', {'class': 'twitter_external_link dir-ltr tco-link'})

        if tweets_link.get('href') == last_post:
            print('pass')
            pass
        else:
            print(tweets_author.text + ':' + tweets_content.text + '--> ' + tweets_link.get('href'))
            await client.send_message(client.get_channel('489855343292186624'), tweets_author.text + ':' +
                                      tweets_content.text +
                                      '--> ' + tweets_link.get('href') + '\n')
            last_post = tweets_link.get('href')

client.run(Token)
```

This code will Indefinitely loop through the section of code after `While run` carrying out the tasks inside until the script is terminated or the condition of `run = True` is not met. This process will theoretically when started run forever collecting data from a website at regular intervals and only updating if the data which is passed through a form of **Selection** in new.

## <u>Nested Loops</u>

This a an iteration or any form of repetition inside of a repetition or iteration.

```python
for i in range(1,n+1):
  for k in range(1,i+1):
    print k,
  print
```

The above code will print a pyramid of numbers indefinitely. 

```python
int_num = 2
while int_num < 100:
    divisor = 2
    while divisor <= (int_num/divisor):
        if not int_num % divisor: break
        divisor = divisor + 1
    if divisor > int_num/divisor:
        print(int_num, 'is prime')
    int_num = int_num + 1
```

This code is somewhat more useful and will  print all the prime numbers up to 100 using a nested Loop. The first loop iterated from 2 to 100 while the second embedded loop works out if each number is prime or not and prints it out if it is prime.

## <u>End Of Chapter Tasks</u>

1. *completed earlier*

2. An iterative process may be used to reach a specific element in an array or as a counter for a game.

3. A definite iteration is on which will iterate a set number of times whereas an indefinite iteration will iterate through until a certain condition is met (or not met).

4. Nesting is the concept of putting something inside of something else to be able to complete a more complex task such a nesting a loop a selection.

5. The sequence of programming statements is very important as it can completely change what you r program does if not ordered carefully or even stop you program from working in some cases.

   ```python
   list_groceries = []
   for i in list_foodstock:
       if i == 0:
           list_groceries.append(list_foodstock[i])
     
   list_foodstock = []    
   ```

   In this case the the list that we want to iterate through is not defined before we attempt to iterate through it. This will cause our code to throw and error index out of range and will fail to execute properly

6. Syntax is the rules of how a certain programming language should be written , it is important as without correct syntax for our code it would fail to work. Syntax varies between programming languages and so something correct for *python* many not be correct for *c#*.

   ```python
   print 'this is not the correct syntax'
   ```

   The code above is an example of incorrect syntax as in *python 3.x.x* a `print `statement must be followed by `()` with the content inside those parentheses. 

## <u>Research Tasks</u>

#### Grading Program:



