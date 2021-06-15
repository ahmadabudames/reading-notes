# Functional Programming


> QUESTIONS OF FUNCTIONAL

- 1- What is functional programming? 
**its a style of building the structure and elements of computer programs.**

- 2- What is a pure function and how do we know if something is a pure function?
 **the function is pure when it returns the same result if given the same arguments, and does not cause any observable side effects.**
 \
 - 3- What are the benefits of a pure function?

  ***The code’s definitely easier to test. We don’t need to mock anything.***

- 4- What is immutability?

***Immutability means value Unchanging over time or unable to be changed.***

- 5- What is Referential transparency?

***A function is considered a referentially transparent when we can replace it with a constant value.***

- 6- What is a module?
**A module is another JavaScript file.**

- 7- What does the word ‘require’ do? 
***we use it so we can use global functions from other files.***
- 8- How do we bring another module into the file the we are working in?
 ***using require and passing to it the path of the file we want.***

- 9- What do we have to do to make a module available?

***we have to export the parts we want to use in another file by using module.exports, then we have to assign it to a variable in the other file.***
> A programming paradigm - a style of building the structure and elements of computer programs - that treats computation as the evaluation of mathematical functions and avoids changing-state and mutable data
>Pure Functions
***returns the same result if given the same arguments aka deterministic does not cause observable side effects Reading Files is not pure because the file’s content can change***

### Benefits of Pure Functions
code becomes easier to test
Immutability
Immutability means value Unchanging over time or unable to be changed.

When data is immutable, its state cannot change after it’s created. If you want to change an immutable object, you can’t. Instead, you create a new object with the new value.

Referential transparency
A function is considered a referentially transparent when we can replace it with a constant value. So, if a function consistently yields the same result for the same input, it is referentially transparent.
Functions as first-class entities
The idea is to treat functions as values and pass functions like data. This way we can combine different functions to create new functions with new behavior.
Higher-order functions
A higher-order functions are functions that either:

takes one or more functions as arguments, or
returns a function as its result.