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



Homework
Production:
* Due Apr. 5 (post documentation on blog): Get information from at least one analog sensor and at least one digital sensor (switch), and use this information to control at least two LEDs, one in a digital fashion and the other in an analog fashion, in some creative way.
Reading:
* Due Apr. 5 (be prepared to discuss both)  :
[Physical Computing’s Greatest hits and misses](https://www.tigoe.com/blog/category/physicalcomputing/176/)
[Making Interactive Art: Set the Stage, Then Shut Up and Listen](https://www.tigoe.com/blog/category/physicalcomputing/405/)
Read about the [voltage divider](https://learn.sparkfun.com/tutorials/voltage-dividers). Don’t worry about the theory too much or the section on level shifting. The important thing is to absorb a little of the concept of a voltage divider.
