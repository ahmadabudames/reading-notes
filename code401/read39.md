# React 3


## Assets

Next.js can serve static assets, like images, under the top-level public directory. Files inside public can be referenced from the root of the application similar to pages.

The public directory is also useful for robots.txt, Google Site Verification, and any other static assets.

## Download Your Profile Picture


- Download your profile picture in .jpg format (or use this file).

- Create an images directory inside of the public directory. 
Save  the picture as profile.jpg in the public/images directory.

- The image size can be around 400px by 400px.

- You may remove the unused SVG logo file directly under the public directory.


## Unoptimized Image

> this means you have to manually handle:


- Ensuring your image is responsive on different screen sizes

- Optimizing your images with a third-party tool or library

- Only loading images when they enter the viewport


## Using the Image Component


Instead of optimizing images at build time, Next.js optimizes images on-demand, as users request them. Unlike static site generators and static-only solutions, your build times aren’t increased, whether shipping 10 images or 10 million images.

Images are lazy loaded by default. That means your page speed isn’t penalized for images outside the viewport. Images load as they are scrolled into viewport.

Images are always rendered in such a way as to avoid Cumulative Layout Shift, a Core Web Vital that Google is going to use in search ranking.

Here’s an example using next/image to display our profile picture. The height and width props should be the desired rendering size, with an aspect ratio identical to the source image.


## Metadata

What if we wanted to modify the metadata of the page, such as the < title> HTML tag?

< title > is part of the < head> HTML tag, so let’s dive into how we can modify the < head> tag in a Next.js page.


## CSS Styling


Let’s now talk about CSS styling.

As you can see, our index page (http://localhost:3000) already has some styles. If you take a look at pages/index.js, you should see code like this:


```
<style jsx>{`
  …
`}</style>

```


This page is using a library called styled-jsx. It’s a “CSS-in-JS” library — it lets you write CSS within a React component, and the CSS styles will be scoped (other components won’t be affected).

Next.js has built-in support for styled-jsx, but you can also use other popular CSS-in-JS libraries such as styled-components or emotion.