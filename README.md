Infinigrid
==========

Infinigrid is a minimalistic SCSS grid system that just get the job
done. It can be configured with any number columns, gutter size,
container width and `@media` breakpoints.

It exposes two operational modes. The **simple mode** creates a number
of classes named `.col-#` for each multiple of the base column size.
The **complex mode** creates all the classes of the simple mode and
all fractional divisions in between, meaning that in a 12 column
layout we will have also 11, 10, 9, etc. columns divisions available.

You can see an example of both modes
[here](kniren.github.io/infinigrid).

Installation & usage
--------------------

Clone the repository on your scss folder. You can then start using it
from your main `scss` file:

```
@import 'infinigrid/infinigrid'

// Include the simple grid
@include infinigrid();

// Include the complex grid
@include infinigrid('complex');

// Include the media queries for simple mode
@include infinigridMediaQueries();

// Include the media queries for simple mode
@include infinigridMediaQueries('complex');
```

On your `html` file you need a `.container` element that will contain
`.row` boxes with the differen columns `.col-*`

```
<div class="container">
        <div class="row">
        <h2>Simple mode</h2>
            <div class="col-1"><p>col-1</p></div> 
            <div class="col-1"><p>col-1</p></div> 
            <div class="col-1"><p>col-1</p></div> 
            <div class="col-1"><p>col-1</p></div> 
            <div class="col-1"><p>col-1</p></div> 
            <div class="col-1"><p>col-1</p></div> 
            <div class="col-1"><p>col-1</p></div> 
            <div class="col-1"><p>col-1</p></div> 
            <div class="col-1"><p>col-1</p></div> 
            <div class="col-1"><p>col-1</p></div> 
            <div class="col-1"><p>col-1</p></div> 
            <div class="col-1"><p>col-1</p></div> 
        </div> 
        <div class="row">
            <div class="col-2"><p>col-2</p></div> 
            <div class="col-2"><p>col-2</p></div> 
            <div class="col-2"><p>col-2</p></div> 
            <div class="col-2"><p>col-2</p></div> 
            <div class="col-2"><p>col-2</p></div> 
            <div class="col-2"><p>col-2</p></div> 
        </div> 
```

Responsive design
-----------------

The responsive design is set up differently for simple and complex
mode. In simple mode we will duplicate the size of each column at each
breakpoint, whereas on complex mode we will stack the columns on top
of each other after the breakpoint.
