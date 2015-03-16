Infinigrid
==========

Infinigrid is a minimalistic SCSS grid system that just get the job
done. It can be configured with any number columns, gutter size,
container width and `@media` breakpoints.

It exposes two operational modes. The **simple mode** creates a number
of classes named `.col-#` for each multiple of the base column size.
The **complex mode** creates all the classes `.col-#-#` of the simple
mode and all fractional divisions in between, meaning that in a 12
column layout we will have also 11, 10, 9, etc. columns divisions
available.

You can see an example of both modes
[here][demo].

Note that the responsive typographic design on the [demo][demo] is
achieved thanks to [minitype][minitype]. Infinigrid exclusively
handles the grid system.

[demo]:http://kniren.github.io/infinigrid
[minitype]:https://github.com/kniren/minitype

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

```
<div class="container">
        <h2>Complex mode</h2>
        <div class="row">
            <div class="col-1-5"><p>col-1-5</p></div> 
            <div class="col-1-5"><p>col-1-5</p></div> 
            <div class="col-1-5"><p>col-1-5</p></div> 
            <div class="col-1-5"><p>col-1-5</p></div> 
            <div class="col-1-5"><p>col-1-5</p></div> 
        </div> 
        <div class="row">
            <div class="col-1-4"><p>col-1-4</p></div> 
            <div class="col-1-4"><p>col-1-4</p></div> 
            <div class="col-1-4"><p>col-1-4</p></div> 
            <div class="col-1-4"><p>col-1-4</p></div> 
        </div> 
        <div class="row">
            <div class="col-1-3"><p>col-1-3</p></div> 
            <div class="col-1-3"><p>col-1-3</p></div> 
            <div class="col-1-3"><p>col-1-3</p></div> 
        </div> 
```

Responsive design
-----------------

The responsive design is set up differently for simple and complex
mode. In simple mode we will duplicate the size of each column at each
breakpoint, whereas on complex mode we will stack the columns on top
of each other after the breakpoint.

License
-------

The MIT License (MIT)

Copyright (c) 2015 Alejandro Sánchez Brotons

Permission is hereby granted, free of charge, to any person obtaining
a copy of this software and associated documentation files (the
"Software"), to deal in the Software without restriction, including
without limitation the rights to use, copy, modify, merge, publish,
distribute, sublicense, and/or sell copies of the Software, and to
permit persons to whom the Software is furnished to do so, subject to
the following conditions:

The above copyright notice and this permission notice shall be
included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF
MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT.
IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY
CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT,
TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE
SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
