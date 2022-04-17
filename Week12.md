

=> **Electromagnetism**
Electrical devices that rely on the principle of electromagnetism:

Electromagnets
* Loudspeakers and headphones
* Solenoid
* Relays
* All kind of motors
  * AC motors
  * DC motors
  * Brushless DC motors
  * Stepper motors
  * Servo motors (which actually consist of a DC motor + servo circuitry)

## Motors!
(Thank you professor Michael Shihloh!)
* Take the DC motor and connect it directly to 5V and GND
* Now reverse the wires
* Can we connect the motor to an Arduino output just like we did with the piezo buzzer?
* How would we reverse it?
Another problem: Arduino current limitations
Arduino current limitations
What is current? It is the rate of flow of electrons through a conductor.
You don't get to control the current.
The voltage depends on the current and the resistance (Ohm's law: I=V/R)
You can provide a voltage (with Arduino, the voltage is always 5V)
Each device has it's own "resistance"
LEDs have relatively high "resistance", and so consume low current. Motors have relatively low "resistance", and so consume high current

Current flowing through any resistance causes heat (P = I^2/R)
Everything has resistance
Therefore, where electricity is flowing there will be heat

Heat causes damage

(We've not had to worry about that up to now because everything we've done uses very little current)

Arduino can not protect itself from damaged caused by overheating. It does not limit current, it is damaged by too much current

The amount of heat a component can withstand before it is damaged is governed, to a large extent, by its size

The transistors that make up Arduino are tiny





The reason for using the separate Motor Driver is simple:

It has much bigger transistors

(It also makes it easier to control both direction and speed, but you could do that with the Arduino alone, it would just be more complicated)

In addition to the bigger transistors, the Motor Driver includes an H-bridge which allows us to control rotation direction

Circuit Schematic



How did I choose which pins to use?

Never use pins 0 and 1 (dedicated for USB communication)
Avoid pin 13 if possible (it flashes 3 times on reset)
Directional control pins (ain1, ain2, bin1, bin2) only require digital signals so avoid pins with extra functionality (analog input, SPI, PWM)
Inclusion of the servo library disables analogWrite() on pins 9 and 10 (I'm not using the servo library now but perhaps I'll add it later)
Use of the tone() function disables analogWrite() on pins 3 and 11 (I'm not using the tone() function now but perhaps I'll add it later)
This leaves PWM pins 5 and 6 for the speed controls (pwma and pwmb)
Might as well choose nearby digital pins
Code

https://learn.sparkfun.com/tutorials/sik-experiment-guide-for-the-arduino-101genuino-101-board/experiment-12-using-the-motor-driver


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
