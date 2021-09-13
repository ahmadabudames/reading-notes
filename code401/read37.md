# React 1

React (also known as React.js or ReactJS) is a free and open-source front-end JavaScript library for building user interfaces or UI components. It is maintained by Facebook and a community of individual developers and companies.React can be used as a base in the development of single-page or mobile applications. However, React is only concerned with state management and rendering that state to the DOM, so creating React applications usually requires the use of additional libraries for routing, as well as certain client-side functionality.

## How to Read This Guide

This is the first chapter in a step-by-step guide about main React concepts. You can find a list of all its chapters in the navigation sidebar. If you’re reading this from a mobile device, you can access the navigation by pressing the button in the bottom right corner of your screen.

Every chapter in this guide builds on the knowledge introduced in earlier chapters. You can learn most of React by reading the “Main Concepts” guide chapters in the order they appear in the sidebar. For example, “Introducing JSX” is the next chapter after this one.

## Components

React code is made of entities called components. Components can be rendered to a particular element in the DOM using the React DOM library. When rendering a component, one can pass in values that are known as “props”:

## Virtual DOM

Another notable feature is the use of a virtual Document Object Model, or virtual DOM. React creates an in-memory data-structure cache, computes the resulting differences, and then updates the browser’s displayed DOM efficiently. This process is called reconciliation. This allows the programmer to write code as if the entire page is rendered on each change, while the React libraries only render subcomponents that actually change. This selective rendering provides a major performance boost.[citation needed] It saves the effort of recalculating the CSS style, layout for the page and rendering for the entire page.


## Lifecycle methods

> **Lifecycle methods use a form of hooking that allows the execution of code at set points during a component’s lifetime.**

- **shouldComponentUpdate** allows the developer to prevent unnecessary re-rendering of a component by returning false if a render is not required.

- **componentDidMount** is called once the component has “mounted” (the component has been created in the user interface, often by associating it with a DOM node). This is commonly used to trigger data loading from a remote source via an API.

- **componentWillUnmount** is called immediately before the component is torn down or “unmounted”. This is commonly used to clear resource-demanding dependencies to the component that will not simply be removed with the unmounting of the component (e.g., removing any setInterval() instances that are related to the component, or an “eventListener” set on the “document” because of the presence of the component)


- **render** is the most important lifecycle method and the only required one in any component. It is usually called every time the component’s state is updated, which should be reflected in the user interface.


## JSX


JSX, or JavaScript XML, is an extension to the JavaScript language syntax. Similar in appearance to HTML, JSX provides a way to structure component rendering using syntax familiar to many developers. React components are typically written using JSX, although they do not have to be (components may also be written in pure JavaScript). JSX is similar to another extension syntax created by Facebook for PHP called XHP.

## Architecture beyond HTML

The basic architecture of React applies beyond rendering HTML in the browser. For example, Facebook has dynamic charts that render to < canvas > tags, and Netflix and PayPal use universal loading to render identical HTML on both the server and client.


## React hooks

Hooks are functions that let developers “hook into” React state and lifecycle features from function components. Hooks don’t work inside classes — they let you use React without classes.

React provides a few built-in hooks like useState, useContext, useReducer and useEffect. Others are documented in the Hooks API Reference. useState , useReducer and useEffect, which are the most used, are for controlling state and side effects respectively.

## Unidirectional data flow

To support React’s concept of unidirectional data flow (which might be contrasted with AngularJS’s bidirectional flow), the Flux architecture was developed as an alternative to the popular model–view–controller architecture. Flux features actions which are sent through a central dispatcher to a store, and changes to the store are propagated back to the view. When used with React, this propagation is accomplished through component properties. Since its conception, Flux has been superseded by libraries such as Redux and MobX.



