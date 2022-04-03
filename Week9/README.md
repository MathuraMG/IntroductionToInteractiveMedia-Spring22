### Recap
* Ohms Law -> `V = I*R'
* Current takes the path of least resistence


### Code on the Arduino 
* TODO : Blink example - walk through the example
* There are functions setup and void here just like in p5. But you will notice the work “void” instead of function. Let’s talk more on this next class
* Let’s look at the functions within the code
```
// the setup function runs once when you press reset or power the board
void setup() {
  // initialize digital pin LED_BUILTIN as an output.
  pinMode(LED_BUILTIN, OUTPUT);
}
```
```
// the loop function runs over and over again forever
void loop() {
  digitalWrite(LED_BUILTIN, HIGH);   // turn the LED on (HIGH is the voltage level)
  delay(1000);                       // wait for a second
  digitalWrite(LED_BUILTIN, LOW);    // turn the LED off by making the voltage LOW
  delay(1000);                       // wait for a second
}
```
* TODO - Let’s upload this code and run it
* TODO - Change the delay on the code and see what happens

### Code on the Arduino + Breadboard - Digital Output
* Try the first circuit with an LED alone
![Circuit 1](https://raw.githubusercontent.com/MathuraMG/IntroductionToInteractiveMedia/master/Week8/images/3.png)
* Now let’s connect the breadboard to the Arduino and see what we can do
* We will be using the digital output pins for controlling the LED. The digital output will give an output of wither 0V or 5V

### Code on the Arduino + Breadboard - Digital Input
* Note about using buttons - we need to add pull down resistors, this is to ensure that when we are NOT pressing the button, the button does not pick up a floating value, but is instead connected to ground (current likes to take the path of least resistance, so when the button is pressed it will be connected to 5V)
![Circuit 2](https://raw.githubusercontent.com/MathuraMG/IntroductionToInteractiveMedia/master/Week8/images/4.png)
* TODO : Connect an LED to pin 7 and try making a pattern with the LED
* TODO : Connect button to pin 3 and work on digitalRead
```
// constants won't change. They're used here to set pin numbers:
const int buttonPin = 3;     // the number of the pushbutton pin
const int ledPin =  7;      // the number of the LED pin

// variables will change:
int buttonState = 0;         // variable for reading the pushbutton status

void setup() {
  // initialize the LED pin as an output:
  pinMode(ledPin, OUTPUT);
  // initialize the pushbutton pin as an input:
  pinMode(buttonPin, INPUT);
}

void loop() {
  // read the state of the pushbutton value:
  buttonState = digitalRead(buttonPin);

  // check if the pushbutton is pressed. If it is, the buttonState is HIGH:
  if (buttonState == HIGH) {
    // turn LED on:
    digitalWrite(ledPin, HIGH);
  } else {
    // turn LED off:
    digitalWrite(ledPin, LOW);
  }
}
```

### Arduino - Analog Output
* Arduino is only capable of giving outputs of LOW or HIGH, or 0/5V. But if we want to control dimness/speed, we need values in between - we can trick the Arduino into doing this using PWM
* PWM - Pulse Width Modulation - bursts of high and low in a single loop, this gives us the perception of a voltage in between
* You can use AnalogWrite only in the IO pins with PWM enabled. They are the ones with this symbol  -> ~
```
// C++ code
//
const int LED_PIN = 3;
int value = 0;
void setup()
{
  pinMode(LED_PIN, OUTPUT);
}

void loop()
{
  delay(10);
  analogWrite(LED_PIN,value);
  value = (value+1)%255; //increase value by 1 each loop
}
```
![Circuit analog circuit](https://github.com/MathuraMG/IntroductionToInteractiveMedia/blob/master/Week9/analogOutput.png)


### Arduino - Analog Input
* Arduino Input can be connected only on the "Analog In" pins -> A0 to A5
[Circuit analog input potentiometer](https://www.tinkercad.com/dashboard?type=circuits&collection=designs)
```
// C++ code
//
const int LED = 6;
const int POT = A0;
void setup()
{
  pinMode(LED, OUTPUT);
  Serial.begin(9600);
}

void loop()
{
  int potValue = analogRead(A0);
  Serial.println(potValue);
  int ledValue = potValue/4;
  analogWrite(LED, ledValue);
}
```

[Circuit analog input photoresistor](https://www.tinkercad.com/things/29W69mkjFZd-analog-input-1)
```
// C++ code
//
const int LED = 6;
const int POT = A0;
void setup()
{
  pinMode(LED, OUTPUT);
  Serial.begin(9600);
}

void loop()
{
  int photoValue = analogRead(A0);
  Serial.println(photoValue);
  int ledValue = photoValue/4;
  analogWrite(LED, ledValue);
}
```

**[EXTRA : FORCE SENSOR](https://www.tinkercad.com/things/cGmcyMVPNht)** 

Homework
Production:
* Due Apr. 5 (post documentation on blog): Get information from at least one analog sensor and at least one digital sensor (switch), and use this information to control at least two LEDs, one in a digital fashion and the other in an analog fashion, in some creative way.
Reading:
* Due Apr. 5 (be prepared to discuss both)  :
[Physical Computing’s Greatest hits and misses](https://www.tigoe.com/blog/category/physicalcomputing/176/)
[Making Interactive Art: Set the Stage, Then Shut Up and Listen](https://www.tigoe.com/blog/category/physicalcomputing/405/)
Read about the [voltage divider](https://learn.sparkfun.com/tutorials/voltage-dividers). Don’t worry about the theory too much or the section on level shifting. The important thing is to absorb a little of the concept of a voltage divider.


### Homework clarification
Hello All!

Just wanted to clarify the assignment a bit - the aim is to have you all work with digitalRead, digitalWrite, analogRead, analogWrite and input and output in hardware. (Yes, I am aware this is a long list).

So the idea is that you have -

1) a button (a digital input controlled with digitalRead)

2) 2 LEDs atleast (one controlled with digitalWrite and another with analogWrite)

3) one sensor - eg - potentiometer, photoresistor that can sense light, force sensor (check previous email for details on this) (controlled with analogRead)

And using all this create something creative. Here are 2 examples for that

1) A messaged encoded in morse code. When you press the button, a message shows up in the LED using digitalOutput, and the potentiometer controls the speed of the blinking. The other LED could be a visual indicator for the speed chosen.

2) a strength tester game (like the kind in fairs and in the circus). You could make a little toy hammer, and hit the force sensor, based on how hard you hit it, the light will glow din, or very bright (or not at all). You could use the button here to turn the game "On"

One thing we did not cover in class, is how to control states using a switch (we only used a psuh button). In case of a push button, you have to keep it pressed for it to stay ON, but with a switch, you can leave it ON (similar to the normal switches we do everyday). I have added the circuit for this here. This will a useful way to turn ON a game (such as in the second example). For this assignment, I am also ok if one person needs to hold down the push button in order to be able to play the game.

[Circuit Link](https://www.tinkercad.com/things/5Po9S8SSs0b)

```
// about this circuit
// LED in connected to PIN 7 -> controlled by digitalWrite
// SWITCH is connected to PIN 3 -> controlled by digitalRead

const int LED_PIN = 7;
const int SWITCH_PIN = 3;
int state = 0; //initialise the state variable to 0

void setup() {
  // set up the pin modes
  pinMode(LED_PIN, OUTPUT);
  pinMode(SWITCH_PIN, INPUT);
}

void loop() {

  int buttonValue = digitalRead(SWITCH_PIN);
  
  if(buttonValue == HIGH) {
    digitalWrite(LED_PIN, HIGH);
  } else {
    digitalWrite(LED_PIN, LOW);
  }
  
}
```






