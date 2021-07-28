# topic

### Classes and Objects

> Objects are an encapsulation of variables and functions into a single entity. Objects get their variables and functions from classes. Classes are essentially a template to create your objects.

### Accessing Object Variables

> To access the variable inside of the newly created object 

>You can create multiple different objects that are of the same class(have the same variables and functions defined). However, each object contains independent copies of the variables defined in the class

### Accessing Object Functions

>To access a function inside of an object you use notation similar to accessing a variabl




## Thinking Recursively in Python


***The algorithm for iterative present delivery implemented in Python:***

> for example :-

houses = ["Eric's house", "Kenny's house", "Kyle's house", "Stan's house"]

def deliver_presents_iteratively():
    for house in houses:
        print("Delivering presents to", house)


> propose an algorithm with which he can divide the work of delivering presents among his elves: 


- Appoint an elf and give all the work to him

- Assign titles and responsibilities to the elves based on the number of houses for which they are responsible:

=> 1 He is a manager and can appoint two elves and divide his work among them

=> 1 He is a worker and has to deliver the presents to the house assigned to him


### Recursive Functions

***A recursive function is a function defined in terms of itself via self-referential expressions.***

***This means that the function will continue to call itself and repeat its behavior until some condition is met to return a result. All recursive functions share a common structure made up of two parts: base case and recursive case.***


> To demonstrate this structure, let’s write a recursive function for calculating n!:

- Decompose the original problem into simpler instances of the same problem. This is the recursive case:

n! = n x (n−1) x (n−2) x (n−3) ⋅⋅⋅⋅ x 3 x 2 x 1
n! = n x (n−1)!

- As the large problem is broken down into successively less complex ones, those subproblems must eventually become so simple that they can be solved without further subdivision. This is the base case:

n! = n x (n−1)! 
n! = n x (n−1) x (n−2)!
n! = n x (n−1) x (n−2) x (n−3)!
⋅
⋅
n! = n x (n−1) x (n−2) x (n−3) ⋅⋅⋅⋅ x 3!
n! = n x (n−1) x (n−2) x (n−3) ⋅⋅⋅⋅ x 3 x 2!
n! = n x (n−1) x (n−2) x (n−3) ⋅⋅⋅⋅ x 3 x 2 x 1!


### Maintaining State


> When dealing with recursive functions, keep in mind that each recursive call has its own execution context, so to maintain state during recursion you have to either:

- Thread the state through each recursive call so that the current state is part of the current call’s execution context

- Keep the state in global scope


### Recursive Data Structures

***A data structure is recursive if it can be deﬁned in terms of a smaller version of itself. A list is an example of a recursive data structure. Let me demonstrate***


### Naive Recursion is Naive

***The Fibonacci numbers were originally deﬁned by the Italian mathematician Fibonacci in the thirteenth century to model the growth of rabbit populations. Fibonacci surmised that the number of pairs of rabbits born in a given year is equal to the number of pairs of rabbits born in each of the two previous years, starting from one pair of rabbits in the ﬁrst year.***

> To count the number of rabbits born in the nth year, he deﬁned the recurrence relation:

Fn = Fn-1 + Fn-2

> The base cases are:

F0 = 0 and F1 = 1



