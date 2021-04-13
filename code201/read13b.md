# CSS Transitions

*CSS transitions allows you to change property values smoothly, over a given duration.*

 **Mouse over the element below to see a CSS transition effect:**

> CSS
**In this chapter you will learn about the following properties:**

- transition
- transition-delay
- transition-duration
- transition-property
- transition-timing-function

### How to Use CSS Transitions?


**To create a transition effect, you must specify two things:**
***the CSS property you want to add an effect to***
***the duration of the effect***
- Note: If the duration part is not specified, the transition will have no effect, because the default value is 0.

The following example shows a 100px * 100px red <*div> element. The <*div> element has also specified a transition effect for the width property, with a duration of 2 seconds:*

>Example

div {
  width: 100px;

  height: 100px;

  background: red;

  transition: width 2s;
}


***The transition effect will start when the specified CSS property (width) changes value.***

Now, let us specify a new value for the width property when a user mouses over the <*div> element:*

Example

div:hover {

  width: 300px;
}


## Specify the Speed Curve of the Transition

***The transition-timing-function property specifies the speed curve of the transition effect.***

**The transition-timing-function property can have the following values:**

- ease - specifies a transition effect with a slow start, then fast, then end slowly (this is default)

- linear - specifies a transition effect with the same speed from start to end

- ease-in - specifies a transition effect with a slow start

- ease-out - specifies a transition effect with a slow end

- ease-in-out - specifies a transition effect with a slow start and end

- cubic-bezier(n,n,n,n) - lets you define your own values in a cubic-bezier function



### Delay the Transition Effect

***The transition-delay property specifies a delay (in seconds) for the transition effect.***

**The following example has a 1 second delay before starting:**

Example

div {

  transition-delay: 1s;
}


### Transition + Transformation

***The following example adds a transition effect to the transformation:***

Example

div {
    
  transition: width 2s, height 2s, transform 2s;
}