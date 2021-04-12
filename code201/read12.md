# chart.js Apl
***Charts are far better for displaying data visually than tables and have the added benefit that no one is ever going to press-gang them into use as a layout tool.***
***They’re easier to look at and convey data quickly, but they’re not always easy to create.***


## basic usage
Let's start this tutorial by looking at the <*canvas> HTML element itself.* 
*At the end of this page, you will know how to set up a canvas 2D context and have drawn a first example in your browser.*

The <**canvas> element**
At first sight a <*canvas> looks like the <img> element,*
*with the only clear difference being that it doesn't have the src and alt attributes.*
Indeed, the <*canvas> element has only two attributes, width and height.*
These are both optional and can also be set using DOM properties. 
When no width and height attributes are specified, 
the canvas will initially be 300 pixels wide and 150 pixels high. 
The element can be sized arbitrarily by CSS, but during rendering the image is scaled to fit its layout size:
if the CSS sizing doesn't respect the ratio of the initial canvas, it will appear distorted.

## drawing shapes with canves

#### The grid
*All elements are placed relative to this origin.*
*So the position of the top left corner of the blue square becomes x pixels from the left and y pixels from the top, at coordinate (x,y).*
Later in this tutorial we'll see how we can translate the origin to a different position, rotate the grid and even scale it, but for now we'll stick to the default.

#### Drawing rectangles

Unlike SVG, <*canvas> only supports two primitive shapes: rectangles and paths (lists of points connected by lines).*
*All other shapes must be created by combining one or more paths. Luckily, 
we have an assortment of path drawing functions which make it possible to compose very complex shapes.*

## applying styles and colors

*we used only the default line and fill styles.*
*Here we will explore the canvas options we have at our disposal to make our drawings a little more attractive.*
*You will learn how to add different colors, line styles, gradients, patterns and shadows to your drawings.*


## drwing text

> The canvas rendering context provides two methods to render text:

>fillText(text, x, y [, maxWidth])
***Fills a given text at the given (x,y) position. Optionally with a maximum width to draw.***
>strokeText(text, x, y [, maxWidth])
***Strokes a given text at the given (x,y) position. Optionally with a maximum width to draw.***

#### Styling text
***the font property to make the text a bit larger than the default size.***
> there are some more properties which let you adjust the way the text gets displayed on the canvas:

- font = value
