HBDselector
===========

A simple custom mappack-selector library. To require it, simply do **selector = require("selector")**

selector.load(sizes, spacing[, images, animation, selection, maximumSelection, angle])
======================================================================================

**Sizes**
A table containing tables with the width and height of each selection size, from the center to the edges. Repeats the last value if not enough tables are provided.

**Spacing**
The space between each selection's rectangle.

**Images**
A table containing all the images, if any, to be fit inside each selection rectangle. Must be a drawable (image, canvas, etc.).

**Animation**
The maximum duration in which the sliding animation plays (in seconds). Defaults to 1.

**Selection**
The selected index from the list. Defaults to 1.

**Maximum Selection**
The limit of which the selections can go in order to loop around. Defaults to 1

**Angle**
The angle (in radians) in which the scrolling animation plays. Defaults to 0 (horizontal).

selector.update(dt)
===================

**Dt**
The delta time obtained via love.update. Required for animation sequence.

selector.draw(centerX, centerY[, function1, function2])
====================================================

**Center X**
The central point in the X axis in which the rectangles will be arranged.

**Center Y**
The central point in the Y axis in which the rectangles will be arranged.

**Function 1** and **Function 2**
Optional functions that draw, respectively, before and after the images. Requires the following arguments:

function([x, y, width, height, selection, index])
===========================

**X**
The X position of the selections rectangles.

**Y**
The Y position of the selections rectangles.

**Width**
The width of the selections rectangles.

**Height**
The height of the selections rectangles.

**Selection**
The selection value of each rectangle.

**Index**
The index value of each rectangle (1 for selected item at the center, 2 for the one right above/below it, 3 for the one right above/below #2, etc.)

selector.select(factor)
=======================

**Factor**
A number to be added to the currently-selected item. Must be -1 or 1 only, where -1 decreases the selection and 1 increases it. Function returns the new selection value, based on the selector's previously-set selection and its limit.

Aditional variables
===================

**selector.lockedscrolls**
When ***true***, prevents users from changing the selection while the animation is playing, and when ***false*** allows users to uninterruptedly change selection. Defaults to true.

**selector.color**
A color table that is set while drawing the selector's images (if any). Defaults to white.
