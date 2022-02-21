**Image Processing and Sound**

## Class 5 - Part 1
### Feb 15 - 1:15pm - 3:55pm

**Week 4!**
* Let's look at homework - 
* Presentation by Fatema and Bato

**Recap**
* Text to points
* How to debug your code

**Topics covered in class**

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

Get function in image
* You can use the get function in 2 ways. If you give it ONLY x and y values, it gives you the rub value for that single pixel.
Example - draw a cat * If you give it 4 values - x, y, width, height - it will give you the pixel values of that part of the image. Meaning, you can display it as an image!
* Note: You can display a part of the image using the (image)[https://p5js.org/reference/#/p5/image] function, but an easier way to do it would be using the (image.get)[https://p5js.org/reference/#/p5.Image/get] function

Example

Let’s work with sprites now! This is going to be very helpful when you are working with games.

 Sounds -  how can you load a sound and play it!
