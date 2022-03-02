**Computer Vision**

## Class 6 - Part 1
### March 1 - 1:15pm - 3:55pm

**Week 5!**
* Presentation by Maisha and Aakarsh 

**Recap**
* How to use grids as part of games
* return functions
* Switch case as an alternate to if statement

**Examples**
* Trigger Sounds in Space 
* Video Drum Machine (show them just for fun)
* [Kyle McDonald Computer Vision Examples (go over a few other CV methods)](https://kylemcdonald.github.io/cv-examples/)

**Topics covered in class**

* This week we will be looking at 
  * loading pixels and updating them
  * updating images' pixels
  * Playing video from camera
  * Reading pixel values from the videos and manipulating the video
  * Reading the difference in videos
  
* **Loading pixels and updating them**
  * Pixel information is stored in an array called `pixels` in p5. `pixels` stores the RGBA values as seperate values. So if there are 1000 pixels, there are actually 4000 values in the pixels array 
  * We can update the pixels on the canvas after we call `loadPixels()`, and call `updatePixels()` after we update the array
  * **NOTE** : [Remember to call `pixelDensity(1);`](https://p5js.org/reference/#/p5/pixelDensity). This ensures that the image size is same as the canvas size. More on that in the next example.
  * You can also add images before loadPixels and manipulate them as well.
  * We can extend the same to videos

🔴💻[Example - loadPixels](https://editor.p5js.org/itp42/sketches/R5QAQSSC4)

🔴💻[Example - loadPixels - TV grain](https://editor.p5js.org/itp42/sketches/E7F7_2P_-)

🔴💻[Example - loadPixels-Cat](https://editor.p5js.org/itp42/sketches/wVqOqP0-E)

🔴💻[Example - loadPixels-Cat-Grainy](https://editor.p5js.org/itp42/sketches/2sbnjgvfb)

* **Working with videos**
  * You can load the live video feed from our computer using [createCapture](https://p5js.org/reference/#/p5/createCapture)
  * You can then update the pixels similar to the previous situation

🔴💻[Example - play video](https://editor.p5js.org/itp42/sketches/V0INKJ8sw)

🔴💻[Example - BW video](https://editor.p5js.org/itp42/sketches/s8p4EwKjo)

🔴💻[Example - Diff in video](https://editor.p5js.org/itp42/sketches/FyMUFb2Wh)

 ## Class 6 - Part 2
### March 3 - 2:40pm - 3:55pm
Work on project in class
HTML and p5
 
### Assignment
* Production:
  Complete your midterm!
