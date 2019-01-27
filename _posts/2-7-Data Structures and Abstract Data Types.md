# <u>Data Structures and Abstract Data Types</u>

| Keyword                | Definition                                                   |
| ---------------------- | ------------------------------------------------------------ |
| Data Structure         | A format for storing large volumes of related data (abstract data type) |
| Abstract Data Type     | A conceptual model of how data can be stored and the operations that can be carried out on the data |
| File                   | A collection of related data                                 |
| Array                  | A set of related data items stored under one identifier, these can be multi dimensional |
| Text File              | A file that contains human readable characters               |
| Binary File            | A file that contains a sequence of zeros and ones            |
| Record                 | One line of a text file                                      |
| Field                  | An item of data                                              |
| Queue                  | A data structure where the first item added is the first item removed |
| Stack                  | A data structure where the first item added is the last item removed |
| Static Data Structure  | A method of storing data where the amount of data stored is fixed |
| Dynamic Data Structure | A method of storing data where the amount of data stored will vary as the program runs |
| Heap                   | A pool of un-used memory that can be allocated to a dynamic data structure |

## <u>Data Structures and Abstract Data Types</u>

A data structure is any method of storing data in an organised and reachable format. They normally contain data that is related and can be manipulated by programs in different ways hence, each having different applications.

An **abstract** data type is a conceptual model of how data is stored and the operations that can be performed on it.

## <u>Arrays</u>

An array is a list or table of data that has a variable name that identifies the object. Arrays usually are one dimensional although there is multi dimensional arrays.

These are static data types and can be used to store large amounts of data, some programming languages require the user to define the size of the array before use of the variable. An example of an array is 

`List_groceries = ['appls', 'manan, 'food,]`

Items can be **appended** to it:

`List_groceries.append('more food')`

A multi dimensional array for example to store stock of items in a shop can be 2 dimensions. One for the item and the other for the amount of it (stock).

| Item | 1    | 2    | 3    |
| ---- | ---- | ---- | ---- |
| 1    | 3    | 7    | 4    |
| 2    | 8    | 6    | 5    |
| 3    | 8    | 7    | 4    |

The rows and columns are never labelled and it is up to the programmer to remember what axis refers to the amount and the item. In the diagram above the column on the left represents the item and the top row is the stock.

## <u>Files</u>

Some files are specific and can only be used with certain applications and some are portable formats such as **text files** and **binary files** that can be used anywhere.

### Text File

A text file simply contains lines of text (human readable characters). It may contain a **header** that explains the content and structure of the file and an **End Of File** marker (EOF). All types of txt files have an internal structure, **csv** (comma separated variable) files have fields that are split up using commas.

Main actions that can be carried out with txt files are:

- Read
- Write

### Binary File

This type of file contains a series of zeroes and ones. They contain binary code and also have header information although these kinds of files are not easily readable by humans but a computer can interpret them very quickly.

`open('lol.bin', Binary) as file`

Main actions that can be carried out are:

- Read
- Write