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

  * **TODO** : can you now animate each of the ellipses by putting it in a class?

**If time permits**

* Data
  * What is data, how can we load it into our program? 
  * There are 2 forms of data that we are going to be looking at - csv and json
  * CSV -> comma seperated values (you can use the `laodCVS` function
  * JSON -> Javascript object notation - very very very similar to objects that we did in last class - you can use the `loadJSON` function

## Class 4 - Part 2
### Feb 17 - 2:40pm - 3:55pm

**Topics covered in class**



**Assignments:** 
*Will be discussed in Thursday class*
* Production:
    * Due Feb. 7th (post documentation on blog): Using loops (for() or while()) in some way, along with everything that you’ve learned so far, make a simple work of art. You may want to look at these old computer art magazines for inspiration, but you don’t need to make your so elaborate. Scroll through and look for images:
       * [COMPUTER_GRAPHICS_AND_ART_Aug1977](http://dada.compart-bremen.de/docUploads/COMPUTER_GRAPHICS_AND_ART_Aug1977.pdf)
	      * [ProgrammInformation21_PI21](http://dada.compart-bremen.de/docUploads/ProgrammInformation21_PI21.pdf)
       * [COMPUTER_GRAPHICS_AND_ART_May1976](http://dada.compart-bremen.de/docUploads/COMPUTER_GRAPHICS_AND_ART_May1976.pdf)
* Reading:
    * Due Feb. 8: Watch [Casey Reas’ Eyeo talk on chance operations](https://vimeo.com/45851523), be prepared to discuss **Shamsa, Soumen**
        * [Guidance on this discussion format can be found here](https://github.com/MathuraMG/IntroductionToInteractiveMedia/blob/master/syllabus.md#student-led-discussions)
    * If you are new to functions or want to review, watch Dan Shiffman’s functions tutorials. There are four videos, each less than 10 minutes.
    * Watch at least the first four of Dan Shiffman’s Object Oriented Programming tutorials.

