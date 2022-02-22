**Image Processing and Sound**

## Class 5 - Part 1
### Feb 22 - 1:15pm - 3:55pm

**Week 5!**
* Let's look at homework - 
* Presentation by Fatema and Bato 

**Recap**
* Text to points
* How to debug your code
* Working with classes

**Topics covered in class**

**[DOWNLOAD IMAGE AND SOUND FILES HERE](https://intro.nyuadim.com/wp-content/uploads/2022/02/image_sound_files.zip)**

* This week we will be looking at 
  * loading images
  * displaying parts of the image
  * animating sprites
  * loading and playing sounds
  * Making a small music player
  * recording sound with a mic
  
* **Working with images in p5**
  * If we are using a local file, upload it onto the p5 editor. Best practice is to put images/ fonts/ sounds in its own folder. You can create a folder called assets and put it in there
  * Once uploaded, you will have to load the image into p5 and store it in a variable. Remember to do this in the ‘preload’ function
  * After that you can use the (image)[https://p5js.org/reference/#/p5/image] function to display the image

* **Get function in image**
  * You can use the get function in 2 ways. If you give it ONLY x and y values, it gives you the rgb value for that single pixel.
  * If you give it 4 values - x, y, width, height - it will give you the pixel values of that part of the image. Meaning, you can display it as an image!
  * Note: You can display a part of the image using the (image)[https://p5js.org/reference/#/p5/image] function, but an easier way to do it would be using the (image.get)[https://p5js.org/reference/#/p5.Image/get] function

🔴💻[Example - display a cat image, and tint it](https://editor.p5js.org/itp42/sketches/0M6VYcoty)

🔴💻[Example - make a "generative portrait" of a cat using img.get](https://editor.p5js.org/itp42/sketches/_6071CUSf)

* **Sprites**
  * A spritesheet has various parts of a charecter animation linearly layed out.
  * We can use img.get to break them up into smaller images and the store them in an array
  * We can then loop through the array and display the images sequwntially to create the illusion of movement
  * PS - This is going to be very helpful when you are working with games.

🔴💻[Example - working with a spritesheet which has one animation](https://editor.p5js.org/itp42/sketches/jrDRcf2XN)

🔴💻[Example - working with a spritesheet which has multiple animations](https://editor.p5js.org/itp42/sketches/oO0Rt5_cJ)


* **Sounds**
  * You can load a sounds similar to image. In preload, using a function called `loadSound`
  * You can play the sounds by saying `mySound.play`

🔴💻[Example - playing a sound](https://editor.p5js.org/itp42/sketches/DvEsT_BFX)
 
### Practicing Classes
**This is not graded! But I would like for you all to be able to do this**
* Create a class "Flower"
* Flower should have the following functions
  *  draw 
  *  sway
  *  grow (BONUS)
* Your sketch should be able to do the following
  * Create a flower at mouseX and mouseY when you click the mouse on the canvas
  * If user drags the mouse across the canvas, all the flowers should sway ( you can implement the sway functionality either using `random` or `noise`
  * BONUS : Only the flowers close to the mouse sway when you drag the mouse
  * BONUS : The flower grows over time
 
### Assignment
* Production:
  * Due Feb. 28 (post documentation on blog): **Make some progress on your midterm project:**
  * Midterm Project:
    * Make a game using everything you have learned so far
    * Midterm is due Mar. 10th
    * We will go through whatever you have completed so far in class on March 3rd
    * Can be one or more players
    * Must include
      * At least one shape
      * At least one image
      * At least one sound
      * At least one on-screen text
    * The game must start with a screen giving instructions, and must wait there until a button or key (your choice) is pressed
    * After the game is won or lost, there must be a way to restart the game without closing and restarting the program
  * Reading:
    * Due Feb. 28 (be prepared to discuss):
    * Read Computer Vision for Artists and Designers
 
