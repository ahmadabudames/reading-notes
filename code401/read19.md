# Automation

## Python Regular Expression Tutorial

***Regular Expressions, often shortened as regex, are a sequence of characters used to check whether a pattern exists in a given text (string) or not. If you've ever used search engines, search and replace tools of word processors and text editors - you've already seen regular expressions in use. They are used at the server side to validate the format of email addresses or passwords during registration, used for parsing text data files to find, replace, or delete certain string, etc. They help in manipulating textual data, which is often a prerequisite for data science projects involving text mining.***

### Regular Expressions in Python

- In Python, regular expressions are supported by the re module. That means that if you want to start using them in your Python scripts, you have to import this module with the help of import:

import re

### Basic Patterns: Ordinary Characters

***You can easily tackle many basic patterns in Python using ordinary characters. Ordinary characters are the simplest regular expressions. They match themselves exactly and do not have a special meaning in their regular expression syntax.***

> Examples are 'A', 'a', 'X', '5'.

**Ordinary characters can be used to perform simple exact matches:**

pattern = r"Cookie"
sequence = "Cookie"
if re.match(pattern, sequence):
    print("Match!")
else: print("Not a match!")
Match!


### Wild Card Characters: Special Characters

***Special characters are characters that do not match themselves as seen but have a special meaning when used in a regular expression. For simple understanding, they can be thought of as reserved metacharacters that denote something else and not what they look like***



***But before you do, the examples below make use of two functions namely: search() and group().***
***With the search function, you scan through the given string/sequence, looking for the first location where the regular expression produces a match.***
***The group function returns the string matched by the re. You will see both these functions in more detail later.***

**Back to the special characters now.**

. - A period. Matches any single character except the newline character.

re.search(r'Co.k.e', 'Cookie').group()
'Cookie'
^ - A caret. Matches the start of the strin



### Backslash.
> Perhaps, the most diverse metacharacter!!

- If the character following the backslash is a recognized escape character, then the special meaning of the term is taken (Scenario 1)

- Else if the character following the \ is not a recognized escape character, then the \ is treated like any other character and passed through (Scenario 2).

- \ can be used in front of all the metacharacters to remove their special meaning (Scenario 3).



> [ ] ->  **Matches the set of characters you specify within it.**

> < > -> **Creates a named group when performing matches.**

> ( ) -> **Creates a group when performing matches.**

> { } -> **Checks for an explicit number of times.**

> ? -> **Checks if the preceding character appears exactly zero or one time.**

> \Z -> **Uppercase Z. Matches only at the end of the string.**

> $ -> **Dollar sign. Matches the end of the string.**


### Function provided by 're'


**The re library in Python provides several functions to make your tasks easier. You have already seen some of them, such as the re.search(), re.match(). Let's check out more...**

compile(pattern, flags=0)

Regular expressions are handled as strings by Python. However, with compile(), you can computer a regular expression pattern into a regular expression object. When you need to use an expression several times in a single program, using compile() to save the resulting regular expression object for reuse is more efficient than saving it as a string. This is because the compiled versions of the most recent patterns passed to compile() and the module-level matching functions are cached.


### Compilation Flags

> **n expression's behavior can be modified by specifying a flag value. You can add flags as an extra argument to the different functions that you have seen in this tutorial. Some of the more useful ones are:**

- IGNORECASE (I) - Allows case-insensitive matches.

- DOTALL (S) - Allows . to match any character, including newline.

- MULTILINE (M) - Allows start of string (^) and end of string ($) anchor to match newlines as well.

- VERBOSE (X) - Allows you to write whitespace and comments within a regular expression to make it more readable.