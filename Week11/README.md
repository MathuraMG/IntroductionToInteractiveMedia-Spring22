
## Class Plan
https://itp.nyu.edu/physcomp/labs/labs-serial-communication/lab-serial-input-to-the-p5-js-ide/

* Install p5.serialcontrol - https://github.com/p5-serial/p5.serialcontrol/releases 
* Let’s install beta 1.1, (looks like there may lag issues in 1.2 ?)

* p5.serialcontrol is what we are going t0 use to send and receive information from/to Arduino and p5
* Once you install it, let’s write some code on our Arduino, and have the information show on the control app.
(The alternate to using this app is to run a node server)

```
const int POT = A0;
const int PR = A1;
void setup() {
  Serial.begin(9600);
}

void loop() {
  int potValue = analogRead(POT);
  int prValue = analogRead(PR);
  Serial.print(potValue);
  Serial.print(",");
  Serial.println(prValue);
}

```

* Now, the value that we print in the Arduino can be read in the p5 serial control app. (Remember, you can only see it in the monitor or in the app. The port can handle only one communication output at a time)

* In the serial monitor app, first select the port, and press “Open”
* you can then read the value as ascii equivalent, or the value it represents

* Let’s move on to p5 now - 
* First include the p5 serial library in index.html
<script language="javascript" type="text/javascript" src="https://cdn.jsdelivr.net/npm/p5.serialserver@0.0.28/lib/p5.serialport.js"></script>

* Now, you can copy the starter code from the serial app into sketch.js and get it running on the p5 web editor

## Arduino to p5
* Arduino -> Serial.print and Serial.println 
* P5 -> serial.readLine (remember, you can check split the csv by using split)

## P5 to Arduino
* P5 -> serial.write(0), serial.write(1)
* Arduino -> serial.read 

## TODO : 
Read the single sensor value on the p5 side using serial.readLine()
Next, let’s add another sensor on the Arduino, and check the value using serial.readLine again. We can use split() on the p5 side, and read the various sensor values as an array
Next, let’s add code on the p5 editor side to make it turn on an LED everytime we click on the screen

## Exercise to do in class
Depending on where we press, can you make different LEDs light up?
Use 3 sensors to change the RCGB value on the p5 screen
Can you use the potentiometer to control sound on p5?

More resources
* https://itp.nyu.edu/physcomp/labs/#Asynchronous_Serial

## Assignment

* Production:
  * Due Apr. 18 (each person, not just one for a group, should post code for each exercise, and video of just the LED lighting up with the ball bouncing) 
  * Work in the groups from class to finish the three in-class examples exercises:
make something that uses only one sensor  on arduino and makes the ellipse in p5 move on the horizontal axis, in the middle of the screen, and nothing on arduino is controlled by p5
make something that controls the LED brightness from p5

take the gravity wind example (https://editor.p5js.org/aaronsherwood/sketches/I7iQrNCul) and make it so every time the ball bounces one led lights up and then turns off, and you can control the wind from one analog sensor

* Due Apr. 18 (post documentation on blog): Write a preliminary concept for your final project, which must incorporate both Arduino and P5.
  * Final project prompt (examples are listed on syllabus page)
  * Create a physically interactive system of your choice that relies on a multimedia computer for some sort of processing or data analysis. The Final should use BOTH P5 AND Arduino. Your focus should be on careful and timely sensing of the relevant actions of the person or people that you’re designing this for, and on clear, prompt, and effective responses. Any interactive system is going to involve systems of listening, thinking, and speaking from both parties. Whether it involves one cycle or many, the exchange should be engaging. You may work alone or in groups.
* Reading
  * Due Apr. 18 (be prepared to discuss) Fahad and Meera to lead: Design Meets Disability

