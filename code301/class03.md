# Passing Functions as Props


> Lifting State Up

***Often, several components need to reflect the same changing data. We recommend lifting the shared state up to their closest common ancestor. Let’s see how this works in action.***

*In React, sharing state is accomplished by moving it up to the closest common ancestor of the components that need it. This is called “lifting state up”. (qouting froms ource)*

***There should be a single “source of truth” for any data that changes in a React application. Usually, the state is first added to the component that needs it for rendering. Then, if other components also need it, you can lift it up to their closest common ancestor.***

***Instead of trying to sync the state between different components, you should rely on the top-down data flow.***
> Lists and Keys


***In react the List as in JS we using the array so each element in array have key that is like index for each element WE can render collections of elements and include them in JSX using curly braces {}.***

> EX:: list

> Basic List Component
***Usually we would render lists inside a component by using li and ul list***
#### Keys
***Keys help React identify which items have changed, are added, or are removed. Keys should be given to the elements inside the array to give the elements a stable identity***
NOTES Keys Must Only Be Unique Among Siblings
How to Use the Spread Operator (…) in JavaScript
***The spread operator is a useful and quick syntax for adding items to arrays, combining arrays or objects, and spreading an array out into a function’s arguments.***

> -What is the spread operator?

- In JavaScript, spread syntax refers to the use of an ellipsis of three dots (…) to expand an iterable object into the list of arguments.

**The spread operator was added to JavaScript in ES6 (ES2015), just like the rest parameters, which have the same syntax: three magic dots**

> -What is ... used for?

***Spread operator to the rescue! It looks similar to rest parameters, also using ..., but does quite the opposite.***


> NOTES The Spread Operator using for -Copying an array

- Concatenating or combining arrays

- Using Math functions

- Using an array as arguments

- Adding an item to a list