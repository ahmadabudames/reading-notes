# Python Scope

***The concept of scope rules how variables and names are looked up in your code. It determines the visibility of a variable within the code. The scope of a name or variable depends on the place in your code where you create that variable. The Python scope concept is generally presented using a rule known as the LEGB rule.***


> I learned :-

- What scopes are and how they work in Python.

- Why it’s important to know about Python scope.

- What the LEGB rule is and how Python uses it to resolve names.

- How to modify the standard behavior of Python scope using global and nonlocal.

- What scope-related tools Python offers and how you can use them.



## Understanding Scope

***In programming, the scope of a name defines the area of a program in which you can unambiguously access that name, such as variables, functions, objects, and so on. A name will only be visible to and accessible by the code in its scope. Several programming languages take advantage of scope for avoiding name collisions and unpredictable behaviors. Most commonly, you’ll distinguish two general scopes:***

- Global scope: The names that you define in this scope are available to all your code.

- Local scope: The names that you define in this scope are only available or visible to the code within the scope. 


## Python Scope vs Namespace

**In Python, the concept of scope is closely related to the concept of the namespace. As you’ve learned so far, a Python scope determines where in your program a name is visible. Python scopes are implemented as dictionaries that map names to objects. These dictionaries are commonly called namespaces. These are the concrete mechanisms that Python uses to store names. They’re stored in a special attribute called .__dict__.**


## Using the LEGB Rule for Python Scope


***Python resolves names using the so-called LEGB rule, which is named after the Python scope for names. The letters in LEGB stand for Local, Enclosing, Global, and Built-in. Here’s a quick overview of what these terms mean:***

- **Local (or function) scope:** 
> is the code block or body of any Python function or lambda expression. This Python scope contains the names that you define inside the function. These names will only be visible from the code of the function. It’s created at function call, not at function definition, so you’ll have as many different local scopes as function calls. This is true even if you call the same function multiple times, or recursively. Each call will result in a new local scope being created.


- **Enclosing (or nonlocal) scope**
> is a special scope that only exists for nested functions. If the local scope is an inner or nested function, then the enclosing scope is the scope of the outer or enclosing function. This scope contains the names that you define in the enclosing function. The names in the enclosing scope are visible from the code of the inner and enclosing functions.


- **Global (or module) scope**
> is the top-most scope in a Python program, script, or module. This Python scope contains all of the names that you define at the top level of a program or a module. Names in this Python scope are visible from everywhere in your code.



- **Built-in scope**
> is a special Python scope that’s created or loaded whenever you run a script or open an interactive session. This scope contains names such as keywords, functions, exceptions, and other attributes that are built into Python. Names in this Python scope are also available from everywhere in your code. It’s automatically loaded by Python when you run a program or script.




## Modules: The Global Scope

***From the moment you start a Python program, you’re in the global Python scope. Internally, Python turns your program’s main script into a module called __main__ to hold the main program’s execution. The namespace of this module is the main global scope of your program.***

> Whenever you assign a value to a name in Python, one of two things can happen:

- **You create a new name**

- **You update an existing name**



*Modifying global names is generally considered bad programming practice because it can lead to code that is:-*


- **Difficult to debug**
>Almost any statement in the program can change the value of a global name.

- **Hard to understand**
>You need to be aware of all the statements that access and modify global names.

- **Impossible to reuse**
>The code is dependent on global names that are specific to a concrete program.


*Good programming practice recommends using local names rather than global names. Here are some tips:-*

- **Write**
>self-contained functions that rely on local names rather than global ones.

- **Try**
>to use unique objects names, no matter what scope you’re in.

- **Avoid**
>global name modifications throughout your programs.

- **Avoid** 
> cross-module name modifications.

- **Use** 
> global names as constants that don’t change during your program’s execution.










