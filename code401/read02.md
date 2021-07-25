# Testing and Modules

## In Tests We Trust — TDD with Python


> Baby Steps

**The API is pretty straightforward and your work was almost done. But with TDD we need to think about tests first. And to be ok with the possibility of the beginning to be hard sometimes — and it’s totally fine. Really.**

> examples

**Just recaping: we have a name as input and we need to return a gender as output. So, the smaller test is: given a name, return a gender.**
- Input: Ana [name]

- Output: female [gender]

**the soultion:-**

def test_should_return_female_when_the_name_is_from_female_gender():
    detector = GenderDetector()
    expected_gender = detector.run(‘Ana’)
    assert expected_gender == ‘female’


## What does the if __name__ == “__main__”: do?    

> If the python interpreter is running that module (the source file) as the main program, it sets the special __name__ variable to have a value “__main__”. If this file is being imported from another module, __name__ will be set to the module’s name. Module’s name is available as value to __name__ global variable. 

A module is a file containing Python definitions and statements. The file name is the module name with the suffix .py appended. 

When we execute file as command to the python interpreter,  

- python script.py


## Recursion

> What is Recursion? 

- The process in which a function calls itself directly or indirectly is called recursion and the corresponding function is called as recursive function. Using recursive algorithm, certain problems can be solved quite easily. Examples of such problems are Towers of Hanoi (TOH), Inorder/Preorder/Postorder Tree Traversals, DFS of Graph, etc.

> A Mathematical Interpretation

- Let us consider a problem that a programmer have to determine the sum of first n natural numbers, there are several ways of doing that but the simplest approach is simply add the numbers starting from 1 to n. So the function simply looks like,

approach(1) – Simply adding one by one

f(n) = 1 + 2 + 3 +……..+ n


## Python Strings

**Python has a built-in string class named "str" with many handy features (there is an older module named "string" which you should not use). String literals can be enclosed by either double or single quotes, although single quotes are more commonly used. Backslash escapes work the usual way within both single and double quoted literals -- e.g. \n \' \". A double quoted string literal can contain single quotes without any fuss (e.g. "I didn't do it") and likewise single quoted string can contain double quotes. A string literal can span multiple lines, but there must be a backslash \ at the end of each line to escape the newline. String literals inside triple quotes, """ or ''', can span multiple lines of text.**


> String Methods:-

- s.lower(), s.upper() -- returns the lowercase or uppercase version of the string

- s.strip() -- returns a string with whitespace removed from the start and end

- s.isalpha()/s.isdigit()/s.isspace()... -- tests if all the string chars are in the various character classes

- s.startswith('other'), s.endswith('other') -- tests if the string starts or ends with the given other string

- s.find('other') -- searches for the given other string (not a regular expression) within s, and returns the first index where it begins or -1 if not found

- s.replace('old', 'new') -- returns a string where all occurrences of 'old' have been replaced by 'new'

- s.split('delim') -- returns a list of substrings separated by the given delimiter. The delimiter is not a regular expression, it's just text. 'aaa,bbb,ccc'.split(',') -> ['aaa', 'bbb', 'ccc']. As a convenient special case s.split() (with no arguments) splits on all whitespace chars.

- s.join(list) -- opposite of split(), joins the elements in the given list together using the string as the delimiter. e.g. '---'.join(['aaa', 'bbb', 'ccc']) -> aaa---bbb---ccc



## Python Modules

> There are actually three different ways to define a module in Python:

- A module can be written in Python itself.

- A module can be written in C and loaded dynamically at run-time, like the re (regular expression) module.

- A built-in module is intrinsically contained in the interpreter, like the itertools module.


## pytest

***The pytest framework makes it easy to write small, readable tests, and can scale to support complex functional testing for applications and libraries.***


