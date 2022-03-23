## Introduction to Electricity, Arduino, Digital I/O 

### Housekeeping
* Attendance
* Do you have your kit?
* Arduino IDE?
* Install this -> https://docs.arduino.cc/cloud/web-editor/tutorials/getting-started/getting-started-web-editor

### Electricity
* Refers to the flow of electrons
* Electrons want to move from place of higher potential energy to place of lower potential energy
    * Like a rock or water falling from a height
    * Unlike a rock or water, electricity can only travel in a conductor

### Circuit
* What is a circuit - a path for electricity to flow
* Typically contains 
    * Power supply (battery, wall charger, USB port) - we will be using the Arduino
    * An output - something that uses the electrical energy and converts it into another form of energy- eg - light -LED, movement -motors
    * Something to control the flow of energy, eg - switch
    * We can also use a resistor to control the amount of power passing through the output 
* The main values we look at in a circuit - Current, Voltage, and Resistance. The 3 of them are related by Ohm’s Law - V = I*R. This is important. Remember this, memorize it, say it in your sleep.
* All components have a voltage across them, current flowing through them, and an internal resistance.  We will go into the details of Ohm’s Law the next week
* We always draw schematics for the circuits we build - schematics basically refers to symbolic representation of the circuit (similar to blueprints for a building) (Image courtesy - https://makeabilitylab.github.io/)
![Circuit schematics]()

* Let’s draw out our first circuit
* Let’s also take a quick look at how a breadboard works 
![Breadboard connections]()
* TODO : We can connects the LED directly to the power source first and see what happens. We’re also going to add a resistor to reduce the voltage across the LED
* TODO :  what if we want to turn this off?


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

### Code on the Arduino + Breadboard - 1
* Try the first circuit with an LED alone
![Circuit 1]()
* Now let’s connect the breadboard to the Arduino and see what we can do
* We will be using the digital output pins for controlling the LED. The digital output will give an output of wither 0V or 5V

### Code on the Arduino + Breadboard - 2
* Note about using buttons - we need to add pull down resistors, this is to ensure that when we are NOT pressing the button, the button does not pick up a floating value, but is instead connected to ground (current likes to take the path of least resistance, so when the button is pressed it will be connected to 5V)
![Circuit 2]()
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

## Assignment
* Production:
    * Due Mar. 28 (post documentation on blog): Create an unusual switch that doesn’t require the use of your hands. Use Arduino digital input and output for the interaction.
        * Examples:
            * Get creative with switches: https://itp.nyu.edu/physcomp/labs/switches/#Get_Creative_With_Switches 
* Reading:
    * Due Mar. 28 (be prepared to discuss both):
        * [Norman,“Emotion & Design: Attractive things work better”](https://jnd.org/emotion_design_attractive_things_work_better/)
        * [Her Code Got Humans on the Moon](http://www.wired.com/2015/10/margaret-hamilton-nasa-apollo/)
    * Read about [analog output](https://itp.nyu.edu/physcomp/lessons/analog-output/)
    * Read about [analog Input](https://itp.nyu.edu/physcomp/lessons/analog-input/)



