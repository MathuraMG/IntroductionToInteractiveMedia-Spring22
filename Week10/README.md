# Class Plan
* Attendance
* Insiya, Liza discussion
  * if we define interactive works by its communication to others does it make it less of an ‘art’?
  * what does it mean to “get out of their way” and should there be a limit?
  * can physical computing act as a ‘performance’ and not an ‘expression’?
* Homework
* Recap Analog IO, Digital IO
* Quick Look : Switches
* Speakers
* Motors
* Servos
* Ultrasound sensor
* BlinkWithoutDelay - https://docs.arduino.cc/built-in-examples/digital/BlinkWithoutDelay

## In class sensor - Switch and RGB LED
* try using a switch to turn on a light!
* RGB LED - some notes below
  * Connect the common ground to GND via a 330 ohm resistor (do not forget this)
  * Connecting R, G, B to +ve will turn on that colour. Mix it up and have fun!

[💡🔴 Switch Circuit](https://www.tinkercad.com/things/5Po9S8SSs0b)

## Speakers
* Quick look at `tone` function -> https://www.arduino.cc/reference/en/language/functions/advanced-io/tone/
* How to connect a speaker

[💡🔴 Speaker Circuit](https://www.tinkercad.com/things/19mo8rdYact)
* Including multiple frequencies using a library
* Coding a song
* Making a "piano"
* Quick look at the theremin
* LOOK AT THIS-> https://www.arduino.cc/en/Tutorial/BuiltInExamples/toneMelody (see before April 7)

## Servo Motors
* How to include external libraries
* Controlling the servo 

[💡🔴 Servo Circuit](https://www.tinkercad.com/things/k272AjdBCYp)

## Map
* https://www.arduino.cc/reference/en/language/functions/math/map/ (see before April 7)

## Smoothing
* Sometimes when we have noisy sensors, we can getting random spikes in our readings.
* This is an issue because those are noises, we shouldn;t actually base any output on them
* To fix that, we can average the data so that the noise is filtered out.
* You can find a built-in example for this in the Arduino (File -> Examples -> Analog -> Smoothing)

## Ultrasound sensor - in class exercise
* https://create.arduino.cc/projecthub/abdularbi17/ultrasonic-sensor-hc-sr04-with-arduino-tutorial-327ff6

## Try on your own:

* Flex sensor - https://www.instructables.com/How-to-use-a-Flex-Sensor-Arduino-Tutorial/

[💡🔴 Flex Sensor Circuit](https://www.tinkercad.com/things/9yeh7lFvGbS)
* Force sensor 

[💡🔴 Force Sensor Circuit](https://www.tinkercad.com/things/cGmcyMVPNht)
* How to check sensor details - look at the number - https://datasheets.globalspec.com/ds/1876/ChallengeElectronics/66CF535E-0359-4738-B192-B0554DF4CFD5

# Assignment

* See before  April 7
  * https://www.arduino.cc/reference/en/language/functions/math/map/ 
  * https://www.arduino.cc/en/Tutorial/BuiltInExamples/toneMelody


* Production:
    * Due Apr. 12 (post documentation on blog) – **group assignment (2 people per group)**:  Make a musical instrument
    * You must use at least one digital sensor (switch)
    * You must use at least one analog sensor (photoresistor, potentiometer, or distance measuring sensor)
* Reading:
    * Due Apr. 12 (be prepared to discuss both): **Devyn and Hind**
    * [A Brief Rant on the Future of Interaction Design](http://worrydream.com/ABriefRantOnTheFutureOfInteractionDesign/)
    * [A follow-up article](http://worrydream.com/ABriefRantOnTheFutureOfInteractionDesign/responses.html)
* It is important that you understand the concepts behind [BlinkWithoutDelay](https://github.com/michaelshiloh/resourcesForClasses#arduino-multitasking-resources). Here are links to various other explanations of the same thing. Browse them, and read one deeply enough that you understand. Come to class with questions if none of these help.

# Resources and links for you to look at !
* [Sparkfun](https://learn.sparkfun.com/
* [Arduino reference](https://www.arduino.cc/reference/en/)
* [Arduino tutorials!](https://www.arduino.cc/en/Tutorial/HomePage)

