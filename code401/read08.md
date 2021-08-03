# List Comprehensions


### Syntax
***The list comprehension starts with a ‘[‘ and ‘]’, square brackets, to help you remember that the result is going to be a list.***
***The basic syntax uses square brackets.***

> [ expression for item in list if conditional ]

***This is equivalent to:***
for item in list:
    if conditional:
        expression


### Create a simple list        

***Let’s start easy by creating a simple list.***

x = [i for i in range(10)]
print x

#This will give the output:
[0, 1, 2, 3, 4, 5, 6, 7, 8, 9]


### Create a list using loops and list comprehension

***For the next example, assume we want to create a list of squares. Start with an empty list.***

#You can either use loops:
squares = []

for x in range(10):
    squares.append(x**2)
 
print squares
[0, 1, 4, 9, 16, 25, 36, 49, 64, 81]

#Or you can use list comprehensions to get the same result:
squares = [x**2 for x in range(10)]

print squares
[0, 1, 4, 9, 16, 25, 36, 49, 64, 81]


### Multiplying parts of a list

***Multiply every part of a list by three and assign it to a new list.***

list1 = [3,4,5]
 
multiplied = [item*3 for item in list1] 
 
print multiplied 
[9,12,15]

### Show the first letter of each word

***We will take the first letter of each word and make a list out of it.***

listOfWords = ["this","is","a","list","of","words"]

items = [ word[0] for word in listOfWords ]

print items

### Lower/Upper case converter

***Let’s show how easy you can convert lower case / upper case letters.***
[x.lower() for x in ["A","B","C"]]
['a', 'b', 'c']

[x.upper() for x in ["a","b","c"]]
['A', 'B', 'C']

### Using list comprehension in functions

***Now, let’s see how we can use list comprehension in functions.***

#Create a function and name it double:
def double(x):
  return x*2

#If you now just print that function with a value in it, it should look like this:
 print double(10)
20


