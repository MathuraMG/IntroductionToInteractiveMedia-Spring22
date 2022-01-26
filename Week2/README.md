**Animation, Conditionals, Loops**

## Class 2 - Part 1
### Feb 1 - 1:15pm - 3:55pm

**Recap**
* Variables
* frameCount and frameRate
* angleMode

**Topics covered in class**
* Functions - why do we need them? How to we make and use them?
  * `setup` and `draw` are functions that we are defining, but are being "called" by p5. ("Call" refers to actually running the lines of code inside the function)
  * `background`, `ellipse` are functions that are already defined that we are "calling" 
  * But why do we need them?
    * Modularity of code
    * Reusability of code
  * p5 has a couple more inbuild functions that we can use along with `setup` and `draw'
    * `mousePressed` - all lines of code inside this function will run when the mouse is pressed on the canvas
    * `keyPressed`
    * **TODO** : Go to the reference and check out what other similar functions we can use
  * Defining and calling custom functions
    * The syntax to define a function is  
    ```
      function functionName() {
        // code goes here
      }
    ```
    * to call a function you would just call it by the functions name
    ```
    functionName();
    ```
    * If the function has any arguments
    ```
    //function definition
    function functionName(arg1, arg2) {
      // code goes here
    }
    
    //calling the function
    functionName(val1, val2);
    ```
  * **TODO** : make a function that draws a car in a given x and y

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
  * **TODO** : use if-else to draw a red ellipse when on the left half of the canvas, and draw a blue ellipse on the right half
  * Multiple conditions! In case of multiple conditions, we will use the `else if` conditional
  * **TODO** : Draw different coloured ellipses in each quadrant
  * We can now use the inbuilt variable - `mouseIsPressed`
  * **TODO** : update the previous code to draw only when the mouse is pressed
  * NOTE: `mouseIsPressed` is a boolean variable, it either provides true or false. If we use it in draw, we are always checking for the condition. Whereas, if we use the function `mousePressed`, then we are running the code inside it ONLY when the mosue is pressed.

* Loops
  * Loops are used to repeat code
  * There are 2 kinds of loops we will be looking at - `for` loops and `while` loops.

* While loops
  * The syntax for while loops is similar to `if` statement. The main difference is that, in a `if` block, the code inside runs once after the condition is checked. In a `while` loop, the code inside the while block runs as long as the condition is satisfied before leaving the code block.
  ``` 
  while(condition) {
    //code goes here
  }
  ```
  * **TODO**: use while loop to draw 10 ellipses on the screen
 * Be careful of infinite loops!!


🔴 💻 **[IN CLASS SKETCH - TBD]()**


## Class 2 - Part 2
### Feb 3 - 1:15pm - 2:30pm

**Topics covered in class**
* For loops
* Nested loops


**Examples for Class 2**



**Assignments:** 
*Will be discussed in Thursday class*
* Production:
    * Due Feb. 7th (post documentation on blog): Using loops (for() or while()) in some way, along with everything that you’ve learned so far, make a simple work of art. You may want to look at these old computer art magazines for inspiration, but you don’t need to make your so elaborate. Scroll through and look for images:
        * COMPUTER_GRAPHICS_AND_ART_Aug1977
        * ProgrammInformation21_PI21
        * COMPUTER_GRAPHICS_AND_ART_May1976
* Reading:
    * Due Feb. 8: Watch Casey Reas’ Eyeo talk on chance operations, be prepared to discuss
        * Guidance on this discussion format can be found here
    * If you are new to functions or want to review, watch Dan Shiffman’s functions tutorials. There are four videos, each less than 10 minutes.
    * Watch at least the first four of Dan Shiffman’s Object Oriented Programming tutorials.

