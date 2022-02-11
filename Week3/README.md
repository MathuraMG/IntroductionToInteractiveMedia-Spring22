## Class Plan
* Housekeeping - masks, class break, attendance
* Homework submission time
* Soumen, Shamsa Discussion
* What is generative artwork
* Go over homework
* Transformations?
* Start working on Functions
* Break
* Arrays
* Objects

## Recap
* How is everyone feeling about loops and if statements?

## Topics we will cover in class
* Transformations?
* Functions
* Arrays
* Objects

## Lecture Notes
* Transformations
  * push, pop
  * translate
  * rotate 

**🔹💻[In Class Code](https://editor.p5js.org/itp42/sketches/nrccPUcPR4)**


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
    * to call a function you would just call it by the functions name **Make sure to name your function well!** Give it an understtandable, and contextual name.
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

**🔹💻[In Class Code](https://editor.p5js.org/itp42/sketches/M6vCfxiEF)**

* Ararys
  * Why do we use arrays?
    * To deal with a collection of values in code
  * Array syntax
    * let a = [];
    * As always, make sure to give understandable variable names. For arrays, its helpful to name the variable in plural    
    * In most languages, the array has to have a collection of similar items (all numbers, strings etc.) - not in Javascript. BUT, a best practice is to always have similar items.
    * Array indexing starts at 0. Meaning the first element in an array is considered to be in the 0th position. the 2nd is 1st position. This "position" is also known as "index"
    * Given an array `a`, you can access the first element in the array by saying `a[0]`, the next one as `a[1]` and so on
    * An arrays lenght -> the number of items/ elements it has can be found with `a.length`
    * Given that the index of an array goes from 0 to `a.length-1`
  * **PRACTICE**  : Let's make an array containing 5 numbers in setup, and print all the numbers inside it. Can you do it with a for loop?
  * **TODO** : Let's go back to the car code, and add more cars with more positions

**🔹💻[In Class Code](https://editor.p5js.org/itp42/sketches/w2tv9CZIB)**

* Objects
  * What is an object?
    * It is an entity, with properties (attributes or functions)
    * Eg - let's take the car - it has a startingX, startingY, a colour, a size etc.
    * **DEMO** Make a car object
    * Now you could even define how this object is drawn as well
    * But we still have the issue that if we need to make multiple car objects, we have to do this each time!
    * So we will çreate a class <- a blueprint of how to make a car!

* Classes and Objects
  * **TODO** Let's create a car class!
  * Create a new object using the car class
  * Make an array of cars!

**🔹💻[In Class Code - 1 - Objects](https://editor.p5js.org/itp42/sketches/BHx99EDVz)**

**🔹💻[In Class Code - 1 - Objects | Arrays](https://editor.p5js.org/itp42/sketches/aDRvuABPM)**

**🔹💻[In Class Code - 1 - Objects | Arrays | MousePressed](https://editor.p5js.org/itp42/sketches/1FD-dKWxg)**
 
## Assignment

* Production:
    * Due Feb. 14 (post documentation on blog): Create an artwork using Object-Oriented Programming. You may use arrays if you wish. Pay attention to the structure, clarity, and organization of your program. As always, document your project:
        * Well commented code, especially for any confusing or tricky parts
        * References to any examples or inspiration
        * Functions as needed to organize your program
        * Excellent names for variables and functions
        * Post code and one or more images
        * Describe the overall concept of your artwork
        * Include the image(s) or link(s) to video
        * Describe any problems you ran into
* Reading:
    * Due Feb. 15: read [The Art of Interactive Design, Ch. 1](https://intro.nyuadim.com/wp-content/uploads/2020/08/theArtOfInteractiveDesign.pdf), be prepared to discuss **Dilnaz and Jannah**
    * Watch this two part ([part 1](https://www.youtube.com/watch?v=o9sgjuh-CBM&ab_channel=TheCodingTrain) and [part 2](https://www.youtube.com/watch?v=pkHZTWOoTLM&ab_channel=TheCodingTrain)) video tutorial on transformations
    * Watch this video tutorial on [Perlin noise](https://www.youtube.com/watch?v=Qf4dIN99e2w&ab_channel=TheCodingTrain)

