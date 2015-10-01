HBDselector
===========

A simple custom mappack-selector library. To require it, simply do **selector = require("selector")**

selector.load(sizes, spacing[, images, animation, selection, maximumSelection, angle])
======================================================================================

**Sizes**
A table containing tables with the width and height of each selection size, from the center to the edges. Repeats the last value if not enough tables are provided.

**Spacing**
The space between each selection's rectangle.

**images**
A table containing all the images, if any, to be fit inside each selection rectangle. Must be a drawable (image, canvas, etc.).
