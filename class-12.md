**Canvas**
At first sight a <canvas> looks like the <img> element, with the only clear difference being that it doesn't have the src and
alt attributes. Indeed, the <canvas> element has only two attributes, width and height. These are both optional and can also be set using
DOM properties. When no width and height attributes are specified, the canvas will initially be 300 pixels wide and 150 pixels high.
The element can be sized arbitrarily by CSS, but during rendering the image is scaled to fit its layout size:
if the CSS sizing doesn't respect the ratio of the initial canvas, it will appear distorted.

**Drawing Shape**
Each of these three functions takes the same parameters. x and y specify the position on the canvas (relative to the origin) of
the top-left corner of the rectangle. width and height provide the rectangle's size.
Below is the draw() function from the previous page, but now it is making use of these three functions.

**Applying style & colors**
If we want to apply colors to a shape, there are two important properties we can use: fillStyle and strokeStyle.
we once again use two for loops to draw a grid of rectangles, each in a different color. 
The resulting image should look something like the screenshot. There is nothing too spectacular happening here.
We use the two variables i and j to generate a unique RGB color for each square, and only modify the red and green values. 
The blue channel has a fixed value. By modifying the channels, you can generate all kinds of palettes.
By increasing the steps, you can achieve something that looks like the color palettes Photoshop uses.

**Drawing text**
fillText(text, x, y [, maxWidth])
Fills a given text at the given (x,y) position. Optionally with a maximum width to draw.
strokeText(text, x, y [, maxWidth])
Strokes a given text at the given (x,y) position. Optionally with a maximum width to draw.
font = value
The current text style being used when drawing text. This string uses the same syntax as the CSS font property. The default font is 10px sans-serif.
textAlign = value
Text alignment setting. Possible values: start, end, left, right or center. The default value is start.
textBaseline = value
Baseline alignment setting. Possible values: top, hanging, middle, alphabetic, ideographic, bottom. The default value is alphabetic.
direction = value
Directionality. Possible values: ltr, rtl, inherit. The default value is inherit.
