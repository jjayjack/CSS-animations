# CSS-animations

## Overview

Forked from [advanced-css-course](https://github.com/jonasschmedtmann/advanced-css-course), this is my version while working through the courses that correlate to the topics. This project will create a single landing page for a user to explore available services and be prompted to purchase a service.

---

## Key Features

[Main Concepts](#main-concepts)

[The Visual Formatting Model](#the-visual-formatting-model)

[Universal Selector](#universal-selector)

[Clip-path](#clip-path)

[Position](#position)

[Transform](#transform)

[SASS](#sass)

[Video Background](#video-background)

[Animations on Hover & Click](#animations-on-hover-&-click)

[Form Input](#form)

[Navigation with Scroll](#navigation)

[Responsive Design Principles](#responsive-design-principles)

[Resources](#resources)

---

### **Main CSS Value Concepts**

-   Each property has an initial value, used if nothing is declared

    -   and if there is not inheritance

-   Browsers specify a _root_ font-size for each page (usually 16 px)

    -   _To increase accessibility of the project, we have converted root font-size to percentage for user's browser set defaults to automatically adjust readability_

-   Percentages and relative values are always converted to pixels

-   Percentages are measured relative to their parents's **font-size**, if used to specify font-size

-   Percentages are measured relative to their parent's \*_width_, if used to specify lengths

-   em are measured relative to their **parent** font-size, if used to specify font-size

-   em are measured relative to the **current** font-size, if used to specify lengths

-   rem are always measured relative to the **document's root** font-size

    -   _For this project we have set the root font-size to be 10px, 10px now = 1rem_

-   vh and vw are simply percentage measurements of the viewport's height and width

---

### **The Visual Formatting Model**

-   Algorithm that calculates boxes and determines the layout of these boxes, for each element in the render tree, in order to determine the final layout of the page.

-   Takes into account

    -   **Dimensions of the boxes**: the box model

        -   Content: text, images, etc.

        -   Padding: transparent area around the content, inside of the box _~ generate white space of the box_

        -   Border: goes around the padding and the content

        -   Margin: white space between boxes

        -   Fill area: area that gets filled with background color or background image

        -   _Define height & width_

            -   **total width** = right border + right padding + specific width + left padding + left border

            -   **total height** = top border + top padding + specified height + bottom padding + bottom margin

            -   **border-box** = specified height

    -   **Box Types**: inline, block and inline-block

        -   Inline boxes:

            -   Content is distributed in lines

            -   Occupies only content's space

            -   No line-breaks

            -   No heights and widths

            -   Paddings and margins only horizontal (left & right)

        -   Block-level boxes:

            -   Elements formatted visually as blocks

            -   100% of parent's width

            -   Vertically, one after another

        -   Inline-block boxes:

            -   A mix of block and inline

            -   Occupies only content's space

            -   No line-breaks

    -   **Positioning Scheme**: floats and position

        -   Normal flow:

            -   Default positioning scheme

            -   **NOT** floated

            -   **NOT** absolutely positioned

            -   Elements laid out according to their source order

        -   Floats:

            -   **Element is removed from the normal flow**

            -   Text and inline elements will wrap around the floated element

            -   The container will not adjust its height to the element

        -   Absolute positioning:

            -   **Element is removed from the normal flow**

            -   No impact on surrounding content or elements

            -   We use _top_, _bottom_, _left_ and _right_ to offset the element from its relatively positioned container

    -   **Stacking contexts**: order of rendered elements

        -   Layers that form a stack

            -   Layers on the bottom of the stack appear at first

            -   Elements higher up the stack appear on top

        -   Examples of properties that create new stacking context

            -   Z-index

            -   Opacity Value

            -   Transform

            -   Filter

    -   Other elements in the render tree

    -   External information: Viewport size, dimensions of images, etc.

---

### **Universal Selector**

Used to reset default values of elements on a webpage.

> Implemented by the selector `*`

-_Inheritance_

For this project, demonstated through the use a the `body` selector, inheritance allows for the commencing elements to be given the same properties as their parent `body`. Used to define

-   font-family
-   font-weight
-   font-size
-   line-height
-   color

Key points for understanding Inheritance

-   Inheritance passes the values for some specific properties from parents to child which allows for **more maintainable code**

-   Properties related to text are inherited: _font-family_, _font-size_, _color_, etc.

-   The computed value of a property is what gets inherited, **not** the declared value.

-   Inheritance of a property only works if no one declares a value for that property.

-   The `inherit` keyword forces inheritance on a certain property.

-   The `initial` keyword resets a property to its initial value.

---

### **Clip-path**

Used to set up a shape in which the image is still visible. Define shape by what user should see using x and y coordinates, starting in top left of image. Coordinate values can be in percentages, pixels, viewport, specific fill-shape values, and global values.

In this project, a polygon was selected so the x and y coordinates defined the area that was still visible to the user. To begin, the first x and y will define starting location and moving clockwise each x and y will define how they relate to the previous x and y.

`clip-path: polygon(x y, x y, x y, x y)`

---

### **Position**

Used to define where an element will display. Within this project, absolute positioning was set up for the Logo image. The positioning structure of top and left is dependent on the parent element's _relative_ position, this sets the origin position that will define where the child element is presented.

---

### **Transform**

Used to modify an elements default properties in layout, sizing/scale, and rotation.

---

### **SASS**

What it is: CSS preprocessor, extension of CSS that adds power and elegance to the basic language

-   Main SASS Features:

    1. Variables: for reusable values such as colors, font-sizes, spacing, etc.

        - Defined by use of `$` before name of variable

    2. Nesting: to nest selectors inside of one another, allowing us to write less code

        - Use of `&` indicates of a nesting child that is placed within a parent for CSS properties

    3. Operators: for mathematical operations right inside of CSS

    4. Partials and imports: to write CSS in different files and importing them all into one single file

    5. Mixins: to write reusable pieces of CSS code

    6. Functions: similar to mixins, with the difference that they produce a value that can then be used

    7. Extends: to make different selectors inherit declarations that are common to all of them

    8. Control directives: for writing complex code using conditionals and loops -- writing frameworks

**Syntaxes**

1. Sass Syntax

```
.navigation
  list-style: none
  float: left

  & li
    display: inline-block
    margin-left: 30px
```

2. SCSS Syntax

```
.navigation{
  list-style: none;
  float: left;

  & li{
    display: inline-block;
    margin-left: 30px;
  }
}
```

---

### **Animations on Hover & Click**

To start with adding animations a new item is created that will hold the behavior. This is the `@keyframes`. Once called upon, a custom name is chosen and _time_ components are declared with behaviors (0% and 100%). **Note: for browser performance: it's best to only ever animate _two_ different properties**

---

### **Responsive Design Principles**

1. Fluid Layouts

    - To allow webpage to adapt to the current viewport width (or even height)

    - Use `%` (or `vh` / `vw`) unit instead of `px` for elements that should _adapt_ to viewport (usually layout)

    - Use `max-width` instead of width

    - 3 Major ways to layout web pages:

        1. Float Layouts

            The _old way of building layout_ of all sizes, using the float CSS property

            Still used, but getting outdated.

            **The focus of this project is on using modern CSS properties and techniques**: clips, transforms, animations, background video, etc. NOT on layout. Even though flexbox and CSS Grid are more modern, _every web developer should still know how float layouts work_.

        2. Flexbox

            Modern way of laying out elements in a _1-dimensional row_ without using floats.

            Perfect for **component layouts**

        3. CSS Grid

            For laying out element in a fully-fledged _2-dimensional grid_.

            Perfect for **page layouts and complex components**

2. Responsive Units

    - Use `rem` unit instead of `px` for most lengths

    - To make it easy to scale the entire layout down (or up) automatically

3. Flexible Images

    - By default, images don't scale automatically as we change the viewport, so we need to fix that

    - Always use `%` for image dimensions, together with the `max-width` property

4. Media Queries

    - To change CSS styles on certain viewport widths (**breakpoints**)

---

### **Resources**

1. [Clip-path](https://developer.mozilla.org/en-US/docs/Web/CSS/clip-path)

2. [Clippy Clip-Path](https://bennettfeely.com/clippy)

3. [Node](npm.com)

4. [Node-Sass](https://www.npmjs.com/package/node-sass)
