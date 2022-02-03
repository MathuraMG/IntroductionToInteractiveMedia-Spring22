**Animation, Conditionals, Loops**

## Class 2 - Part 1
### Feb 1 - 1:15pm - 3:55pm

**Submitting your homework**
* Create a sketch on the p5 editor
* Document your process, nxt steps, challenges, discoveries on github using markdown
* Make sure that this is done by 12 noon on Monday

**Recap**
* Variables
* frameCount and frameRate
* angleMode

**Topics covered in class**

* Conditionals
  * You would use a conditional (if-else) when you want certain blocks of code to run only when a certain condition is satisfied
  * Syntax is as follows
  ```
  if(customCondition) {
    //What code to run if the condition is satisfied
  }
  else {
    //What code to run if the above condition is not satisfied
  }
  ```
  * Try if else by drawing different coloured ellipses on different halves of the canvas
  * We can now use the `mouseIsPressed` variable to create interactions when the mouse is pressed
  * NOTE: You can also use the mousePressed() function. Note that there is a huge difference between the mouseIsPressed variable and the mousePressed() function: the variable mousePressed is true as long as any mouse button is pressed, while the function mousePressed() is called only once whenever a mouse button is pressed, no matter how long it's pressed for
  * **TODO** : if mouse is pressed, change the colour of the canvas! (Can pressing in different areas call for different background colours)
  * **TODO** : Continuing on the above, can we make a button?
  * Multiple conditions! In case of multiple conditions, we will use the `else if` conditional
  * **TODO** : can we make multiple buttons?
  * We can use the if statements to now make a bouncing ball!

🔴 💻 **[IN CLASS SKETCH - Change the colour of the ellipse depending on where on the canvas it is](https://editor.p5js.org/itp42/sketches/78SmP6ATp)**

🔴 💻 **[IN CLASS SKETCH - Make a button using if else](https://editor.p5js.org/itp42/sketches/vNxA3MhBt)**

🔴 💻 **[IN CLASS SKETCH - Make a bouncing ball](https://editor.p5js.org/itp42/sketches/0xfz3K82K)**
  
* Loops
  * Loops are used to repeat code
  * There are 2 kinds of loops we will be looking at - `for` loops and `while` loops.
* For loops
* **TODO**: use while loop to draw 10 ellipses on the screen
* Nested loops
* **TODO**: use while loop to draw 100 ellipses on the screen!
* **Be careful of infinite loops!!**

* Random function
  * `random(x,y)` - gives a random number between x and y.
  * If you want a whole number, you can use `floor(random(x,y))` 
  
🔴 💻 **[IN CLASS SKETCH - Make a grid of colour changing squares](https://editor.p5js.org/itp42/sketches/6WQ_2AAEy)**

🔴 💻 **[IN CLASS SKETCH - 10PRINT](https://editor.p5js.org/itp42/sketches/HUHHrIk2O)**

**Notes from class**
* Make sure to always indent your code!
* When creating variables make sure to give them meaningful names.
* Try and use variables as much as possible. Eg- to detemine the size of an ellipse, the distance between jumps in for loops.


## Class 2 - Part 2
### Feb 3 - 2:40pm - 3:55pm

**Topics covered in class**

* While loops - a quick look
  * The syntax for while loops is similar to `if` statement. The main difference is that, in a `if` block, the code inside runs once after the condition is checked. In a `while` loop, the code inside the while block runs as long as the condition is satisfied before leaving the code block.
  ``` 
  while(condition) {
    //code goes here
  }
  ```

* Other Functions we can use!
  * random function *completed in previous class*
  * noise function 
  * sin

* Noise function
  * Perlin noise is a random sequence generator producing a more naturally ordered, harmonic succession of numbers compared to the standard random() function.
  * [Perlin noise reference](https://p5js.org/reference/#/p5/noise)
  * TODO : Make a 1-D perlin noise space to change the size of an ellipse / make a wave
  * TODO : Make a 2-D perlin noise space to get a greyscale screen!

* Sin function
  * You can also use the sin wave to ease animations
  * TODO : make a sine wave (remember, you can use `angleMode(DEGREES)`) 
  * TODO : use it to gradually change the colour/size in your previous sketches

* IF time permits - translation and rotation

**Examples for Class 2**
* You can find the examples under ["Week_2" in the p5 editor collection](https://editor.p5js.org/itp42/collections/7rk8Q1jPf)


**Assignments:** 
*Will be discussed in Thursday class*
* Production:
    * Due Feb. 7th (post documentation on blog): Using loops (for() or while()) in some way, along with everything that you’ve learned so far, make a simple work of art. You may want to look at these old computer art magazines for inspiration, but you don’t need to make your so elaborate. Scroll through and look for images:
       * [COMPUTER_GRAPHICS_AND_ART_Aug1977](http://dada.compart-bremen.de/docUploads/COMPUTER_GRAPHICS_AND_ART_Aug1977.pdf)
	      * [ProgrammInformation21_PI21](http://dada.compart-bremen.de/docUploads/ProgrammInformation21_PI21.pdf)
       * [COMPUTER_GRAPHICS_AND_ART_May1976](http://dada.compart-bremen.de/docUploads/COMPUTER_GRAPHICS_AND_ART_May1976.pdf)
* Reading:
    * Due Feb. 8: Watch [Casey Reas’ Eyeo talk on chance operations](https://vimeo.com/45851523), be prepared to discuss **STUDENTS WILL BE PICKED IN CLASS**
        * [Guidance on this discussion format can be found here](https://github.com/MathuraMG/IntroductionToInteractiveMedia/blob/master/syllabus.md#student-led-discussions)
    * If you are new to functions or want to review, watch Dan Shiffman’s functions tutorials. There are four videos, each less than 10 minutes.
    * Watch at least the first four of Dan Shiffman’s Object Oriented Programming tutorials.

