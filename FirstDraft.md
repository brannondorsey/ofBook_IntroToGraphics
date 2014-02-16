# Graphics #

Introduction TDB

## Drawing Basic Shapes, and Then Drawing Many, Many Basic Shapes ##

**[Insert Section on Setup/Update/Draw]**

**[Insert Section on XY coordinate system]**

You might be wondering why we would start with making digital brushes?   

We will get coding as soon as possible and survive this chapter together.

To get started creating brushes, we need to find the basic building blocks of graphics.  You can classify the 2D graphics functions that openFrameworks provides into two categories: predefined shapes and freeform shapes.  The predefines shapes are rectangles, circles, triangles and straight lines.  The freeform shapes are polygons and paths.

### Predefined Shapes ###

Okay, okay.  Time for actual code.  Add the following line to your `draw()` function and like magic you will have a black void of a window on your screen.

```c++
    ofBackground(0);
```

Now that we have our background in place, we can start drawing on top of it.  Let's draw a rectangle, a circle, an ellipse, a triangle and some straight lines:

```c++
    ofSetColor(0);
    
    ofRect(50, 50, 100, 100);
    ofCircle(250, 100, 50);
    ofEllipse(400, 100, 80, 100);
    ofTriangle(500, 150, 550, 50, 600, 150);
    for (int i=0; i<11; i++) {
		    ofLine(650, 50+(i*10), 750, 75+(i*5));
		}
```

The first line of code tells openFrameworks what color it should be using when drawing.  You can think of it as telling openFrameworks to pull out a particular colored sharpie - it will draw in that color until you tell it to switch to another color.  Then we make use of some handy functions to draw shapes: `ofRect`, `ofCircle`, `ofEllipse`, `ofTriangle` and `ofLine`.  

The documentation page for [`ofRect`](http://openframeworks.cc/documentation/graphics/ofGraphics.html#!show_ofRect "ofRect Documentation Page") shows that we can create a rectangle in a number of different ways.  Here, we are passing in the x and y values of the top left corner as well as the width and height that we would like, all in that order.  For [`ofCircle`](http://openframeworks.cc/documentation/graphics/ofGraphics.html#show_ofCircle "ofCircle Documentation Page"), we are passing in the x and y values of the center of the circle and the radius.  With [`ofEllipse`](http://openframeworks.cc/documentation/graphics/ofGraphics.html#show_ofEllipse "ofEllipse Documentation Page"), we are passing in the x and y values of the center as well as the width and height.  For [`ofTriangle`](http://openframeworks.cc/documentation/graphics/ofGraphics.html#show_ofTriangle "ofTriangle Documentation Page"), we pass in the x and y positions of the three corners of the triangle.  Finally, with [`ofLine`](http://openframeworks.cc/documentation/graphics/ofGraphics.html#show_ofLine "ofLine Documentation Page"), we pass in the x and y coordinates of the two endpoints of our desired straight line. 

![Basic Shapes](images/intrographics_basicshapes.png "Basic Shapes With and Without Fill")
 
