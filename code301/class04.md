# React and Forms

> What is a ‘Controlled Component’? 
- controlled component is a react component that controls the values of input elements in a form using setState

> Should we wait to store the users responses from the form into state when they submit the form OR should we update the state with their responses as soon as they enter them? 

- we should update the state with their responeses as soon as they enter them because the React take some time to update the state so if we did this after the submition maybe anonther compenent depends on these values will not work propely

>  How do we target what the user is entering if we have an event handler on an input field? 
- by using the (event.target.name)for that input filed.

### Form
***Controlled Components.***
*In HTML, form elements such as , and typically maintain their own state and update it based on user input. In React, mutable state is typically kept in the state property of components, and only updated with setState(). We can combine the two by making the React state be the “single source of truth”. Then the React component that renders a form also controls what happens in that form on subsequent user input. An input form element whose value is controlled by React in this way is called a “controlled component”. NOW LET'S GET SOME TAG THAT WE CAN USING IN HTML The textarea Tag In HTML, a  element defines its text by its children: In React, a  uses a value attribute instead. This way, a form using a  can be written very similarly to a form that uses a single-line input. The select Tag In HTML, creates a drop-down list. For example, this HTML creates a drop-down list of flavors EX:: select*

#### The file input Tag
***In HTML, an lets the user choose one or more files from their device storage to be uploaded to a server or manipulated by JavaScript via the File API .***

#### Handling Multiple Inputs
***When we need to handle multiple controlled input elements, you can add a name attribute to each element and let the handler function choose what to do based on the value of (event.target.name.)***

#### The Conditional (Ternary) Operator
***Starting With the Basics — The if statement Using a conditional, like an if statement, allows us to specify that a certain block of code should be executed if a certain condition is met.***


### Form controls

***For textual form controls—like inputs, selects, and textareas—use the FormControl component. FormControl adds some additional styles for general appearance, focus state, sizing, and more.***


### Readonly

***Add the readOnly prop on an input to prevent modification of the input's value. Read-only inputs appear lighter (just like disabled inputs), but retain the standard cursor.***

## Conditional Rendering

> Conditional rendering in React works the same way conditions work in JavaScript. Use JavaScript operators like if or the conditional operator to create elements representing the current state, and let React update the UI to match them.

