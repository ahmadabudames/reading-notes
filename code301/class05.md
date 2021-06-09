# Putting it all together

> Break The UI Into A Component Hierarchy

***The first thing you’ll want to do is to draw boxes around every component (and subcomponent) in the mock and give them all names. If you’re working with a designer, they may have already done this, so go talk to them! Their Photoshop layer names may end up being the names of your React components!***

***But how do you know what should be its own component? Use the same techniques for deciding if you should create a new function or object. One such technique is the single responsibility principle, that is, a component should ideally only do one thing. If it ends up growing, it should be decomposed into smaller subcomponents.***

***Since you’re often displaying a JSON data model to a user, you’ll find that if your model was built correctly, your UI (and therefore your component structure) will map nicely. That’s because UI and data models tend to adhere to the same information architecture. Separate your UI into components, where each component matches one piece of your data model.***

> Props vs State

**There are two types of “model” data in React: props and state. It’s important to understand the distinction between the two; skim the official React docs if you aren’t sure what the difference is.**

### single-responsibility principle

***is a computer-programming principle that states that every module, class or function in a computer program should have responsibility over a single part of that program's functionality, and it should encapsulate that part***

> Identify The Minimal (but complete) Representation Of UI State

***To make your UI interactive, you need to be able to trigger changes to your underlying data model. React achieves this with state.***

***To build your app correctly, you first need to think of the minimal set of mutable state that your app needs. The key here is DRY: Don’t Repeat Yourself. Figure out the absolute minimal representation of the state your application needs and compute everything else you need on-demand. For example, if you’re building a TODO list, keep an array of the TODO items around; don’t keep a separate state variable for the count. Instead, when you want to render the TODO count, take the length of the TODO items array.***

> Think of all the pieces of data in our example application. We have:

- The original list of products

- The search text the user has entered

- The value of the checkbox

- The filtered list of products

> Let’s go through each one and figure out which one is state. Ask three questions about each piece of data:

***Is it passed in from a parent via props? If so, it probably isn’t state.***
***Does it remain unchanged over time? If so, it probably isn’t state.***
***Can you compute it based on any other state or props in your component? If so, it isn’t state.***
***The original list of products is passed in as props, so that’s not state. The search text and the checkbox seem to be state since they change over time and can’t be computed from anything. And finally, the filtered list of products isn’t state because it can be computed by combining the original list of products with the search text and value of the checkbox.***

> So finally, our state is:

- The search text the user has entered

- The value of the checkbox


