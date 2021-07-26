#  FileIO & Exceptions

## Reading and Writing Files in Python

**One of the most common tasks that you can do with Python is reading and writing files. Whether it’s writing to a simple text file, reading a complicated server log, or even analyzing raw byte data, all of these situations require reading or writing a file.**

> In this tutorial, you’ll learn:

- What makes up a file and why that’s important in Python

- The basics of reading and writing files in Python

- Some basic scenarios of reading and writing files


***This tutorial is mainly for beginner to intermediate Pythonistas, but there are some tips in here that more advanced programmers may appreciate as well.***


### What Is a File?


***file is a contiguous set of bytes used to store data. This data is organized in a specific format and can be anything as simple as a text file or as complicated as a program executable. In the end, these byte files are then translated into binary 1 and 0 for easier processing by the computer.***

> Files on most modern file systems are composed of three main parts:

- 1-**Header:** metadata about the contents of the file (file name, size, type, and so on)

- 2-**Data:** contents of the file as written by the creator or editor

- 3-**End of file (EOF)**: special character that indicates the end of the file


### Line Endings

***One problem often encountered when working with file data is the representation of a new line or line ending. The line ending has its roots from back in the Morse Code era, when a specific pro-sign was used to communicate the end of a transmission or the end of a line.***


>Windows uses the CR+LF characters to indicate a new line, while Unix and the newer Mac versions use just the LF character. This can cause some complications when you’re processing files on an operating system that is different than the file’s source. Here’s a quick example. Let’s say that we examine the file dog_breeds.txt that was created on a Windows system:

Pug\r\n
Jack Russell Terrier\r\n
English Springer Spaniel\r\n
German Shepherd\r\n
Staffordshire Bull Terrier\r\n
Cavalier King Charles Spaniel\r\n
Golden Retriever\r\n
West Highland White Terrier\r\n
Boxer\r\n
Border Terrier\r\n

>This same output will be interpreted on a Unix device differently:


Pug\r
\n
Jack Russell Terrier\r
\n
English Springer Spaniel\r
\n
German Shepherd\r
\n
Staffordshire Bull Terrier\r
\n
Cavalier King Charles Spaniel\r
\n
Golden Retriever\r
\n
West Highland White Terrier\r
\n
Boxer\r
\n
Border Terrier\r
\n



## Python Exceptions: An Introduction

 **Exceptions versus Syntax Errors**


> ***Syntax errors occur when the parser detects an incorrect statement. Observe the following example:***

>>> print( 0 / 0 ))
  File "<stdin>", line 1
    print( 0 / 0 ))
                  ^
SyntaxError: invalid syntax


> ***The arrow indicates where the parser ran into the syntax error. In this example, there was one bracket too many. Remove it and run your code again:***

>>> print( 0 / 0)
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
ZeroDivisionError: integer division or modulo by zero


