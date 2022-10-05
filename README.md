# CSS-animations

## Overview

Forked from [advanced-css-course](https://github.com/jonasschmedtmann/advanced-css-course), this is my version while working through the courses that correlate to the topics. This project will create a single landing page for a user to explore available services and be prompted to purchase a service.

**Main CSS Value Concepts**

- Each property has an initial value, used if nothing is declared

  - and if there is not inheritance

- Browsers specify a _root_ font-size for each page (usually 16 px)

- Percentages and relative values are always converted to pixels

- Percentages are measured relative to their parents's **font-size**, if used to specify font-size

- Percentages are measured relative to their parent's \*_width_, if used to specify lengths

- em are measured relative to their **parent** font-size, if used to specify font-size

- em are measured relative to the **current** font-size, if used to specify lengths

- rem are always measured relative to the **document's root** font-size

  - _For this project we have set the root font-size to be 10px, 10px now = 1rem_

- vh and vw are simply percentage measurements of the viewport's height and width

---

## Key Features

[Universal Selector](#universal-selector)

[Clip-path](#clip-path)

[Position](#position)

[Transform](#transform)

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

For this project, demonstated through the use a the `body` selector, inheritance allows for the commencing elements to be given the same properties as their parent `body`. Used to define

    - font-family
    - font-weight
    - font-size
    - line-height
    - color

Key points for understanding Inheritance

- Inheritance passes the values for some specific properties from parents to child which allows for **more maintainable code**

- Properties related to text are inherited: _font-family_, _font-size_, _color_, etc.

- The computed value of a property is what gets inherited, **not** the declared value.

- Inheritance of a property only works if no one declares a value for that property.

- The `inherit` keyword forces inheritance on a certain property.

- The `initial` keyword resets a property to its initial value.

---

### **Clip-path**

Used to set up a shape in which the image is still visible. Define shape by what user should see using x and y coordinates, starting in top left of image. Coordinate values can be in percentages, pixels, viewport, specific fill-shape values, and global values.

In this project, a polygon was selected so the x and y coordinates defined the area that was still visible to the user. To begin, the first x and y will define starting location and moving clockwise each x and y will define how they relate to the previous x and y.

`clip-path: polygon(x y, x y, x y, x y)`

---

### **Position**

Used to define where an element will display. Within this project, absolute positioning was set up for the Logo image. The positioning structure of top and left is dependent on the parent element's _relative_ position, this sets the origin position that will define where the child element is presented.

---

### Transform

Used to modify an elements default properties in layout, sizing/scale, and rotation.

---

### Animations on Hover & Click

To start with adding animations a new item is created that will hold the behavior. This is the `@keyframes`. Once called upon, a custom name is chosen and _time_ components are declared with behaviors (0% and 100%). **Note: for browser performance: it's best to only ever animate _two_ different properties**

---

### Resources

1. [Clip-path](https://developer.mozilla.org/en-US/docs/Web/CSS/clip-path)

2. [Clippy Clip-Path](https://bennettfeely.com/clippy)
