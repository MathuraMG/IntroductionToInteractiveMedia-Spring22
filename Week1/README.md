## Class 1 - Part 1
### Jan 25 - 1:15pm - 3:55pm

**Topics covered in class**

* What is this class about?
* Examples! (check Examples.md for full list)
* Github and markdown [Github for documentation](https://github.com/MathuraMG/Resources/blob/main/Github-for-documentation.md) | [Markdown](https://markdown-it.github.io/)
* p5 editor + what is p5 even!
* First p5 sketch 

* Canvas, coordinates, setup and draw
   * In p5, the origin of the canvas is in the top left. the "x" value increases from left to right, and the "y" value increases top to down.
   * the code inside the `setup` function runs ONCE in the beginning, and the code inside the `draw` function runs forever until the sketch stops or we explicity make it stop 
   * All the code inside `setup` and `draw` shoudl be present inside the `{` and `}`
   * Remember, the code inside the funcitons run one after the other, meaning if you were to call the `background` function in the end of draw, you would not see ny of the other shapes you have as the background would cover them all

* Simple shapes in p5 - shapes we covered in class :
   * `ellipse(x,y,width,height)`  x and y refer to the center of the ellipse
   * `rect(x,y,width,height)` here, by default, x and y refer to the top left point of the rect
   * `line(x1,y1,x2,y2)`
   * `triangle(x1,y1,x2,y2,x3,y3)`
   * `arc(x,y,width,height,startAngle,endAngle)` there are more arguments that you can give to this function that will determine if the arc is a sector or a segment. Check out the reference to see all the possibilities! Also, the angles are to be given in radians by default.

* Colours in p5 - NOTE: for now, we will be sticking to using RGB colours
  * Colours can be denoted in hex values, or RGB. For the first few classes, we will stick to RGB. RGB refers to Red, Blue, and Green. They usually take values from 0 to 255. All colours can be denoted as a combination of these three. For instance red is (255,0,0). Green in (0,255,0). Teal would be (0,128,128)
  * If the RGB values are the same (i.e the colour is on the greyscale), you can denote it with just a single number. 0 is black, 128 is grey and 255 is hite
  * 'fill(r,g,b)` will fill the shapes following the instructions
  * `noFill()` will make the fill transparent
  * 'stroke(r,g,b)` will colour the outline of the shapes following the instructions
  * `noStroke()` will make the outline transparent

* Keeping code clean
  * Always format your code! This means indenting your code, not haveing extra spaces etc. To get started on this, you can use the `Tidy` function in the p5 editor. (Go to Edit-> Tidy Code, ot use the shortcut Cmd/Ctrl+Shift+F)
  * End of instructions must have semicolons. As we discussed, the code will run without them as well, but it is best practice to keep them in so that ot's easy for you when you work wiith other languages.

🔴 💻 **[IN CLASS SKETCH - 1](https://editor.p5js.org/itp42/sketches/15dKNL0yz)**

* **[Always keep the p5 reference handy](https://p5js.org/reference/)**

* A brief look at variables
  * A variable contains values that are subject to change
  * We can create variables of our own, but first lests take a look at variables given to us by p5. These are refered to as inbuild variables.
  * `mouseX` and `mouseY` contain the values of the x position and y position of the mouse respectively.

🔴 💻 **[IN CLASS SKETCH - 2](https://editor.p5js.org/itp42/sketches/QElwCGm-L)**

**TO DO**
* Create p5 accounts
* Create github accounts - email them to me at mmg542@nyu.edu
* Join IM Server - https://discord.gg/g6erD2xz

## Class 1 - Part 2
### Jan 27 - 1:15pm - 2:30pm

**Topics covered in class**
* More inbuilt Varibles 
  * `width`, and `height` contain the width and the height of the canvas
  * `frameCount` keeps a tab of how many frames have run in the sketch. It can be used for some interesting animation.
  * `mouseIsPressed` is a variable that let's us know when the mouse is pressed on the canvas. We will use this more in the upcoming classes.

* Custom variables
  * In many cases we will want to create out own variables to store values. The syntax to do that is `let variableName = InitialValue;`
  * Creating a variable using `let variableName` is also known as declaring a variable. If you chose to give it a value WHEN declaring, that is known as initilising.
  * Note: You may see some videos/references that use `var` instead of `let`. That is the older way of doing it.
  * If you declare a variable outside of setup and draw, it is known as a global variable, it can be accessed anywhere
  * If you declare it inside one of these functions, it can be used only within that function
  * Why do we need variables?
    * reusability 
    * changing the values
  * TO DO : Let's create and print a variable. Change it's value

* Interaction and animation in p5
  * You can use the variables to create some simple animations.
  * TO DO : Let's make a shape move across the canvas.

**Examples for Class 1**
* [Change emoji colour and shape with mouse movement](https://editor.p5js.org/itp42/sketches/DPKwQyIK0)
* [Interactive Mondrian composition](https://editor.p5js.org/itp42/sketches/P4cRwLPYl)
* [Animation with arcs](https://editor.p5js.org/itp42/sketches/HKWOhem2H)
* [Drawing on a canvas](https://editor.p5js.org/itp42/sketches/Oc2UVds7w)


**Assignments:** 
*Will be discussed in Thursday class*
* Production: 
    * Due Jan 31 (post documentation on githu): Make a self-portrait using P5js. ([How to add images in markdown](https://github.com/MathuraMG/Resources/blob/main/Embedding-images-in-markdown.md)) | [Github for documentation](https://github.com/MathuraMG/Resources/blob/main/Github-for-documentation.md) | [Markdown](https://markdown-it.github.io/)
        * The portrait must be entirely created by your code i.e. you must not interact with your computer while the portrait is being made (e.g. no drawing using the mouse)
        * The portrait does not need to be dynamic (i.e. it does not need to change while we look at it)
        * The portrait does not need to be realistic. The purpose is to practice using the simple drawing functions.
* Reading:
    * Due Feb 1:
        * [Getting Started with P5js](https://p5js.org/get-started/)
        * [Coordinate systems and space](https://p5js.org/learn/coordinate-system-and-shapes.html)
