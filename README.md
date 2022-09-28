# CSS-animations

## Overview

Forked from [advanced-css-course](https://github.com/jonasschmedtmann/advanced-css-course), this is my version while working through the courses that correlate to the topics. This project will create a single landing page for a user to explore available services and be prompted to purchase a service.

---

## Key Features

[Universal Selector](#universal-selector)

[Clip-path](#clip-path)

[Video Background](#video-background)

[Animations on Hover & Click](#animations)

[Form Input](#form)

[Navigation with Scroll](#navigation)

[Resources](#resources)

---

### **Universal Selector**

Used to reset default values of elements on a webpage.

> Implemented by the selector `*`

-_Inheritance_

Demonstated through the use a the `body` selector, inheritance allows for the commencing elements to be given the same properties as their parent `body`. Used to define

    - font-family
    - font-weight
    - font-size
    - line-height
    - color

---

### **Clip-path**

Used to set up a shape in which the image is still visible. Define shape by what user should see using x and y coordinates, starting in top left of image. Coordinate values can be in percentages, pixels, viewpoint, specific fill-shape values, and global values.

In this project, a polygon was selected so the x and y coordinates defined the area that was still visible to the user. To begin, the first x and y will define starting location and moving clockwise each x and y will define how they relate to the previous x and y.

`clip-path: polygon(x y, x y, x y, x y)`

---

### Resources

1. [Clip-path](https://developer.mozilla.org/en-US/docs/Web/CSS/clip-path)
