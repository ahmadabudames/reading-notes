# Topic


## Pain vs. Suffering

**That price is pain, the pain of growth.**
**The pain that you’ll experience during this course is no exception; most times it won’t feel good. You won’t feel good.**

> You’ll be pushed mentally, having to think your way through problems that you had only even heard about a few hours beforehand.

> You’ll have to forge your own path toward a solution.

> You’ll have to research for hours on end, fleshing out the skeleton that we discuss in class, piling information on top of application so that you can reach your goals.

> You’ll be pushed emotionally, constantly confronted with your own lack of understanding of a topic.

> You’ll Constantly be having to figure out how to collaborate with new people and deal with their (and your own) emotional quirks.

> You’ll Constantly be thrust far outside of your comfort zone with the expectation that you’ll survive for the next push forward.

> You’ll Constantly be dealing with uncertainty of what awaits you at the end of the 10 weeks, and whether or not you’ll make it.

> You’ll be pushed physically, and while sitting in a chair and staring at your screen isn’t the most strenuous exercise in the world, the consecutive hours of it will take its toll.

> You’ll lose sleep, you’ll forget to work out, and you’ll feel exhausted all while being filled with information day after day.



## A beginner's guide to Big O Notation

**As a programmer first and a mathematician second (or maybe third or fourth) I found the best way to understand Big O thoroughly was to produce some examples in code. So, below are some common orders of growth along with descriptions and examples where possible.**

- O(1)

O(1) describes an algorithm that will always execute in the same time (or space) regardless of the size of the input data set.

bool IsFirstElementNull(IList<String> elements)
{
    return elements[0] == null;
}

- O(N)

O(N) describes an algorithm whose performance will grow linearly and in direct proportion to the size of the input data set. The example below also demonstrates how Big O favours the worst-case performance scenario; a matching string could be found during any iteration of the for loop and the function would return early, but Big O notation will always assume the upper limit where the algorithm will perform the maximum number of iterations.

bool ContainsValue(IEnumerable<string> elements, string value)
{
    foreach (var element in elements)
    {
        if (element == value) return true; 
    }     
    return false; 
}


- O(N²)

O(N²) represents an algorithm whose performance is directly proportional to the square of the size of the input data set. This is common with algorithms that involve nested iterations over the data set. Deeper nested iterations will result in O(N³), O(N⁴) etc.

bool ContainsDuplicates(IList<string> elements)
{
    for (var outer = 0; outer < elements.Count; outer++) 
    {
        for (var inner = 0; inner < elements.Count; inner++) 
        { 
            // Don't compare with self 
            if (outer == inner) continue;             
            
            if (elements[outer] == elements[inner]) return true; 
        }
    }    
    return false;
}


- O(2^N)

O(2^N) denotes an algorithm whose growth doubles with each addition to the input data set. The growth curve of an O(2^N) function is exponential — starting off very shallow, then rising meteorically. An example of an O(2^N) function is the recursive calculation of Fibonacci numbers:

int Fibonacci(int number)
{
    if (number <= 1) return number;
       
    return Fibonacci(number - 2) + Fibonacci(number - 1); 
}


## Awesome Python Environment

**Coding in Python is awesome and is getting more awesome with every new release! For me, this is mainly due to the massive amount of freely available libraries, its readability, and the recently introduced type annotations. However, especially we as Data Scientists tend to often produce big and messy Jupyter notebooks or python files that are hard to follow. Apart from that, we often run into version clashes when one project depends on a different version fo the same library. Fixing this takes too much time and often leads to issues with other projects. There must be a way to avoid that and facilitate our lives. In this article, I will go through the tools that I use and the techniques that I usually follow. This hopefully will help future me to remember all of that, and more importantly, will help you also learn something helpful. Without further ado, let’s get our hands dirty.**


> The Interpreter :-

***the interpreter. For sure you could just simply download and install your favorite version of python and put everything into that. But what if you have programs that require different python versions or programs that depend on different versions of the same third-party module and you want to switch between those programs seamlessly?***

***Pyenv is a set of three tools, from which I present two here, that are pyenv (used to install python) and pyenv-virtualenv (used to configure your global tools). You can install them by***


> Dependency Management :-

*The one that I use the most is poetry.*

#### Apart from many other things, poetry helps you to easily

- manage your projects’ dependencies,

- separate your projects through virtual environments,

- build both applications as well as libraries without headaches.



## Python 3 Module of the Week


*PyMOTW-3 is a series of articles written by Doug Hellmann to demonstrate how to use the modules of the Python 3 standard library. It is based on the original PyMOTW series*




