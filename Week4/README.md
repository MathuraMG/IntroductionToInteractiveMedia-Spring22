**Loading data and displaying text**

## Class 4 - Part 1
### Feb 15 - 1:15pm - 3:55pm

**Week 4!**
* Let's look at homework - 
* Presentation by Dilnaz and Jannah

**Recap**
* Noise
* Transformation

**Topics covered in class**

* This week we will be looking at 

* Polar coordinates
   * What are cartesian coordinates
   * What are the sine and cos function
   * Using sine and cos, how can we transform polar and cartesian cordinates
   * Here is some extra recap if anyone is interested - https://www.mathsisfun.com/polar-cartesian-coordinates.html
   * **TODO** : Let's make an ellipse revolve around the center of the canvas

* Text in p5.js
  * Simply showing text on the canvas can be done using the `text` function
  * Each of the letters in the string can be accessed like an array element
  * That means that we can loop through induvidual letters in a string, and we can animate them!
  * **TODO** : Make each letter move seperately 

🔸💻 **[Example for making text move](https://editor.p5js.org/itp42/sketches/X3BWWO3KO)**


* Animating text! Making art with text
  * Loading a font into p5 has to be done in the `preload` function. This is because we want the font to be loaded even before the program starts.
  * As a best practice, I would request you all to load a font into an assets folder. This will help keep your code organised
  * You can take animating text to the next level if you manage to get the points of the text itself. This would require us to convert text to points. 
  * Thankfully, p5 has a function that does exactly this
  * https://p5js.org/reference/#/p5.Font/textToPoints
  * Another piece of information that you can use when you convery text to points is the bounding box of the text itself. Technically, you can make generative art without this, but it is helpful to have
  * https://p5js.org/reference/#/p5.Font/textBounds
  * **TODO** : Convert a text into points and draw ellipses at each point
 
🔸💻 **[Example for animating text](https://editor.p5js.org/itp42/sketches/hBozBZDr-)**

You can find codes we did in class below

🔸💻 **[In Class - Polar Coordniates](https://editor.p5js.org/itp42/sketches/rn15hJZf5)**

🔸💻 **[In Class - Text -1](https://editor.p5js.org/itp42/sketches/qG_oODYYf)**

🔸💻 **[In Class - text-2](https://editor.p5js.org/itp42/sketches/_grgx9Gao)**

🔸💻 **[In Class - text-t-points](https://editor.p5js.org/itp42/sketches/gsbl01ead)**

## Class 4 - Part 2
### Feb 17 - 2:40pm - 3:55pm

**Topics covered in class**


* **TODO** : can you now animate each of the ellipses by putting it in a class?

**If time permits**

* Data
  * What is data, how can we load it into our program? 
  * There are 2 forms of data that we are going to be looking at - csv and json
  * CSV -> comma seperated values (you can use the `laodCVS` function
  * JSON -> Javascript object notation - very very very similar to objects that we did in last class - you can use the `loadJSON` function


🔸💻 **[In Class - Bounce Class](https://editor.p5js.org/itp42/sketches/xbtAIZ9u1)**

🔸💻 **[In Class - Bouncing Text](https://editor.p5js.org/itp42/sketches/PHGlLPU0-)**

🔸💻 **[In Class - Load CSV](https://editor.p5js.org/itp42/sketches/HJT2hX2kT)**

🔸💻 **[Extra example - Load JSON](https://editor.p5js.org/itp42/sketches/VUdopW8Mz)**

**Assignments:** 
*Will be discussed in Thursday class*
* Production:
  * Due Feb. 21 (post documentation on blog): Either make some sort of data visualization, or create a generative text output.
  * Due Feb. 22 (no blog post needed): Bring an idea (or ideas) to class for your midterm. We will spend part of class next week working on your midterms.

* Reading:
  * Due Feb. 22: Read [The Design of Everyday Things, The Psychopathology of Everyday Things](https://pages.ucsd.edu/~mboyle/COGS1/readings/Norman-COGS1-The%20Psychopathology-of-Everyday-Things.pdf) be prepared to discuss **Fatema and Bato**
Read about image processing in p5js: https://idmnyu.github.io/p5.js-image/ or watch Shiffman’s videos: https://www.youtube.com/watch?v=nMUMZ5YRxHI&ab_channel=TheCodingTrain

## * Midterm Project Details :
    * Make a game using everything you have learned so far
    * Due Mar. 10th
    * Can be one or more players
    * Must include
        * At least one shape
        * At least one image
        * At least one sound
        * At least one on-screen text
    * The game must start with a screen giving instructions, and must wait there until a button or key (your choice) is pressed
    * After the game is won or lost, there must be a way to restart the game without closing and restarting the program
