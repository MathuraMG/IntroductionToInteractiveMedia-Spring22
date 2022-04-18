# Week 12

## Class Plan
* Housekeeping - attendance
* Fahad and Meera discussion

## Project Idea discussion
* Can you all please add your ideas here? https://codeshare.io/EBPEov

## Recap
### Arduino handshake 
* A - code in setup - sends out a message until it gets a byte of data from the remote computer:
* A - code in loop - modify the loop() by adding an if() statement to look for incoming serial data and read it.(if (Serial.available() > 0) {) - This ill prompt the Arduino to send data only when asked
* P5 - in gotData callback, send a byte of information 
* P5 - in openPort callback, send a byte of information

## Soldering
* Let’s solder 2 wires together. Let’s solder on a PCB
* How to use a multimeter
    * To check voltage
    * To check connectivity

## Creating enclosures
* https://itp.nyu.edu/fab/intro_fab/week-4-enclosures/
* Create a cardboard prototype first! You can do pretty much anything with it. It allows you to try your ideas fast. 
* Your projects will HAVE to have finished enclosures to it. I expect no loose wires or breadboards

## Motors!
Electromagnets (Electrical devices that rely on the principle of electromagnetism:)
* Loudspeakers and headphones
* Solenoid, Relays
* All kind of motors
  * AC motors
  * DC motors
  * Stepper motors
  * Servo motors (which actually consist of a DC motor + servo circuitry)

(Thank you professor Michael Shihloh!)
* Take the DC motor and connect it directly to 5V and GND
* Now reverse the wires
* Can we connect the motor to an Arduino output just like we did with the piezo buzzer?
* How would we reverse it?
 
* But now, we have a problem, the Arduino has current limitations ( a recap : current is the rate of flow of electrons through a conductor)
* Typically,
 * You don't get to control the current with the Arduino
 * Current is calculated based on the resistance of the component, and the voltage supplied to it (Ohms law -> V= I*R)
 * You can provide a voltage (with Arduino, the voltage is always 5V)
 * Each device has it's own "resistance"
 * LEDs have relatively high "resistance", and so consume low current. Motors have relatively low "resistance", and so consume high current
 * The motor may require a current supply of 500mA but the pins of Arduino can only withstand 40 mA. If any component joined to the pin draws current higher than this limit, then the pin will get damaged due to heating and internal circuit damage due to high current draw (
 * We've not had to worry about that up to now because everything we've done uses very little current

* The reason for using the separate Motor Driver is simple:
 * It has much bigger transistors as compared to the Arduino, adn they can withstand more heat, and thus do not get damaged
 * In addition to the bigger transistors, the Motor Driver includes an H-bridge which allows us to control rotation direction


# Using the motor driver
Let's use sparkfun motor driver!
https://learn.sparkfun.com/tutorials/sik-experiment-guide-for-the-arduino-101genuino-101-board/experiment-12-using-the-motor-driver
https://learn.sparkfun.com/tutorials/tb6612fng-hookup-guide/all


```
const int ain1Pin = 3;
const int ain2Pin = 4;
const int pwmAPin = 5;


void setup() {
  pinMode(ain1Pin, OUTPUT);
  pinMode(ain2Pin, OUTPUT);
  pinMode(pwmAPin, OUTPUT); // not needed really
}

void loop() {
  // turn in one direction, full speed
  Serial.println("full speed");
  analogWrite(pwmAPin, 255);
  digitalWrite(ain1Pin, HIGH);
  digitalWrite(ain2Pin, LOW);
  // stay here for a second
  delay(1000);

  // slow down
  Serial.println("slowing down");
  int speed = 255;
  while (speed--) {
    analogWrite(pwmAPin, speed);
    delay(20);
  }
}
```

## Choosing Pins
* Never use pins 0 and 1 (dedicated for USB communication)
* Avoid pin 13 if possible (it flashes 3 times on reset)
* If you are using only digital signals, avoid pins with extra functionality (analog input, SPI, PWM)
* Inclusion of the servo library disables analogWrite() on pins 9 and 10 
* Use of the tone() function disables analogWrite() on pins 3 and 11 


