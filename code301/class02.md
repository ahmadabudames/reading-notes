# React Lifecycle
### Lifecycle of Components
**Each component in React has a lifecycle which you can monitor and manipulate during its three main phases.**

> ***The three phases are: Mounting, Updating, and Unmounting.***

### Mounting
***Mounting means putting elements into the DOM.***

- React has four built-in methods that gets called, in this order, when mounting a component:

>1-constructor()

>2-getDerivedStateFromProps()

>3-render()

>4-componentDidMount()

### constructor

***The constructor() method is called before anything else, when the component is initiated, and it is the natural place to set up the initial state and other initial values.***

***The constructor() method is called with the props, as arguments, and you should always start by calling the super(props) before anything else, this will initiate the parent's constructor method and allows the component to inherit methods from its parent (React.Component).***


### render


***The render() method is required, and is the method that actually outputs the HTML to the DOM.***


### componentDidMount
***The componentDidMount() method is called after the component is rendered.***

***This is where you run statements that requires that the component is already placed in the DOM.***

### Updating


***The next phase in the lifecycle is when a component is updated.***

***A component is updated whenever there is a change in the component's state or props.***

>React has five built-in methods that gets called, in this order, when a component is updated:

- 1-getDerivedStateFromProps()

- 2-shouldComponentUpdate()

- 3-render()

- 4-getSnapshotBeforeUpdate()

- 5-componentDidUpdate()

***The render() method is required and will always be called, the others are optional and will be called if you define them.***


- What types of things can you pass in the props?
> Props (aka "properties") in React allows us to pass values from a parent component down to a child component. The values can be any data type, from strings to functions, objects, etc.

- What is the big difference between props and state?
> Basically, the difference is that state is something like attributes in OOP : it's something local to a class (component), used to better describe it. Props are like parameters - they are passed to a component from the caller of a component (the parent) : as if you called a function with certain parameters.
‏
- When do we re-render our application?

> A re-render can only be triggered if a component's state has changed. The state can change from a props change, or from a direct setState change. The component gets the updated state and React decides if it should re-render the component‏.

