# EASILY CREATE STUNNING ANIMATED CHARTS WITH CHART.JS

**Charts are far better for displaying data visually than tables and have the added benefit that no one is ever going to press-gang them into use as a layout tool. Theyâ€™re easier to look at and convey data quickly, but theyâ€™re not always easy to create.**

**A great way to get started with charts is with Chart.js, a JavaScript plugin that uses HTML5â€™s canvas element to draw the graph onto the page. Itâ€™s a well documented plugin that makes using all kinds of bar charts, line charts, pie charts and more, incredibly easy.**


# Drawing shapes with canvas

`<canvas>`  looks like the `<img>` element but without a src or alt, the `<canvas>` element has only two attributes, width and height.
- the canvas will initially be 300x150px
- The canvas element can be styled just like any normal image (margin, border, backgroundâ€¦)
- the `<canvas>` element requires the closing tag `</canvas>`
- The `<canvas>` element creates a fixed-size drawing surface that exposes one or more rendering contexts, which are used to create and manipulate the content shown.

Example:

```JavaScript
{
    var canvas = document.getElementById('tutorial');

if (canvas.getContext) {
  var ctx = canvas.getContext('2d');
  // drawing code here
} else {
  // canvas-unsupported code here
}

}
```
- Draws a filled rectangle.
```JavaScript
{
    fillRect(x, y, width, height)

}
```
- Draws a rectangular outline.
```JavaScript
{
strokeRect(x, y, width, height)
}
```
- Clears the specified rectangular area, making it fully transparent.
```JavaScript
{
clearRect(x, y, width, height)
}
```
Rectangular shape example
```JavaScript
function draw() {
  var canvas = document.getElementById('canvas');
  if (canvas.getContext) {
    var ctx = canvas.getContext('2d');

    ctx.fillRect(25, 25, 100, 100);
    ctx.clearRect(45, 45, 60, 60);
    ctx.strokeRect(50, 50, 50, 50);
  }
}
```
**Drawing paths**

**Now let's look at paths. A path is a list of points, connected by segments of lines that can be of different shapes, curved or not, of different width and of different color. A path, or even a subpath, can be closed. To make shapes using paths, we take some extra steps:**

  *First, you create the path.*

Then you use drawing commands to draw into the path.
Once the path has been created, you can stroke or fill the path to render it.
Here are the functions used to perform these steps:

    - beginPath()
    Creates a new path. Once created, future drawing commands are directed into the path and used to build the path up.  

    - Path methods
    Methods to set different paths for objects.

    - closePath()
    Adds a straight line to the path, going to the start of the current sub-path.

    - stroke()
    Draws the shape by stroking its outline.

    - fill()
    Draws a solid shape by filling the path's content area.

    - moveTo(x, y)
    Moves the pen to the coordinates specified by x and y.

    - lineTo(x, y)
    Draws a line from the current drawing position to the position specified by x and y.

    - arc(x, y, radius, startAngle, endAngle, anticlockwise)
    Draws an arc which is centered at (x, y) position with radius r starting at startAngle and ending at endAngle going in the given direction  indicated by anticlockwise (defaulting to clockwise).

    - arcTo(x1, y1, x2, y2, radius)
    Draws an arc with the given control points and radius, connected to the previous point by a straight line.

    - quadraticCurveTo(cp1x, cp1y, x, y)
    Draws a quadratic BÃ©zier curve from the current pen position to the end point specified by x and y, using the control point specified by cp1x and   cp1y.

    - bezierCurveTo(cp1x, cp1y, cp2x, cp2y, x, y)
    Draws a cubic BÃ©zier curve from the current pen position to the end point specified by x and y, using the control points specified by (cp1x,    cp1y) and (cp2x, cp2y).
    
    - Path2D()
    The Path2D() constructor returns a newly instantiated Path2D object, optionally with another path as an argument (creates a copy), or optionally    with a string consisting of SVG path data.

# Applying styles and colors

## Colors

**Up until now we have only seen methods of the drawing context. If we want to apply colors to a shape, there are two important properties we can use: fillStyle and strokeStyle.**

    - fillStyle = color
    Sets the style used when filling shapes.

    - strokeStyle = color
    Sets the style for shapes' outlines.

    - lineWidth = value
    Sets the width of lines drawn in the future.

    - lineCap = type
    Sets the appearance of the ends of lines.

    - lineJoin = type
    Sets the appearance of the "corners" where lines meet.

    - miterLimit = value
    Establishes a limit on the miter when two lines join at a sharp angle, to let you control how thick the junction becomes.

    - getLineDash()
    Returns the current line dash pattern array containing an even number of non-negative numbers.

    - setLineDash(segments)
    Sets the current line dash pattern.

    - lineDashOffset = value
    Specifies where to start a dash array on a line.

## Transparency

**In addition to drawing opaque shapes to the canvas, we can also draw semi-transparent (or translucent) shapes. This is done by either setting the globalAlpha property or by assigning a semi-transparent color to the stroke and/or fill style.**

globalAlpha = transparencyValue
Applies the specified transparency value to all future shapes drawn on the canvas. The value must be between 0.0 (fully transparent) to 1.0 (fully opaque). This value is 1.0 (fully opaque) by default.
The globalAlpha property can be useful if you want to draw a lot of shapes on the canvas with similar transparency, but otherwise it's generally more useful to set the transparency on individual shapes when setting their colors.

**Because the strokeStyle and fillStyle properties accept CSS rgba color values, we can use the following notation to assign a transparent color to them.**

## Drawing text
    - fillText(text, x, y [, maxWidth])
    Fills a given text at the given (x,y) position. Optionally with a maximum width to draw.
    - strokeText(text, x, y [, maxWidth])
    Strokes a given text at the given (x,y) position. Optionally with a maximum width to draw.

## Styling text
    - font = value
    The current text style being used when drawing text. This string uses the same syntax as the CSS font property. The default font is 10px    sans-serif.
    - textAlign = value
    Text alignment setting. Possible values: start, end, left, right or center. The default value is start.
    - textBaseline = value
    Baseline alignment setting. Possible values: top, hanging, middle, alphabetic, ideographic, bottom. The default value is alphabetic.
    - direction = value
    Directionality. Possible values: ltr, rtl, inherit. The default value is inherit.

-  JavaScript plugin that uses HTML5â€™s canvas element to draw the graph onto the page.
1. To draw a line chart, the first thing we need to do is create a canvas element in our HTML in which Chart.js can draw our chart. 

2. we need to get the context and to instantiate the chart
 
3. Next we need to create the data.

4. Finally add  a bar chart to our page. 




---

[home](/README.md) | [About me](/about-me.md) | [contact me](/contact-me.md)
