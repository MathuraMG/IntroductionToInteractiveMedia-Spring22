## Class Plan
* Soumen, Shamsa Discussion
* What is generative artwork
* Go over homework
* Start working on Functions
* Break
* Arrays
* Continue with Arrays 

## Recap

## Topics we will cover in class
* Functions
* Arrays
* Objects

## Lecture Notes
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
  * We will be starting with this piece of code - https://editor.p5js.org/itp42/sketches/1teX1P5t6

## Assignment

