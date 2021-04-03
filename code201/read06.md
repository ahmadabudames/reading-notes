# What are Object literals in JavaScript?

***More than one interviewer has asked me this question for front-end positions. ***

***If you have done any kind of JavaScript development, you have used an object literal at some point.***
***I’ll explain and provide some sample code.***

***In plain English, an object literal is a comma-separated list of name-value pairs inside of curly braces.***
***Those values can be properties and functions. Here’s a snippet of an object literal with one property and one function.***


### The greet function now would look like this:
greet: (message) => {
    console.log(message + " " + this.getFullName() + "!!");
}

***Doing this might look fine at first,***
 ***but any change made to the copied object (anotherGreeting) will reflect in the original object (greeting).***



# The HTML DOM (Document Object Model)
***When a web page is loaded, the browser creates a Document Object Model of the page.***

**With the object model, JavaScript gets all the power it needs to create dynamic HTML:**

>*JavaScript can change all the HTML elements in the page*

>*JavaScript can change all the HTML attributes in the page*

>*JavaScript can change all the CSS styles in the page*

>*JavaScript can remove existing HTML elements and attributes*

>*JavaScript can add new HTML elements and attributes*

>*JavaScript can react to all existing HTML events in the page*

>*JavaScript can create new HTML events in the page*


# What is the HTML DOM?
**The HTML DOM is a standard object model and programming interface for HTML. It defines:**

>*The HTML elements as objects*

>*The properties of all HTML elements*

>*The methods to access all HTML elements*

>*The events for all HTML elements*




