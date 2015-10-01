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

selector.draw(width, height[, function1, function2])
====================================================

**Width**
The width of the area through which
