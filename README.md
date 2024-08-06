# Task-2---Potentiometer

## File: project2.ino

## Author: "Melgarejo, Comora, Bandivas, Balitaan & Poblete"

## Description:

This Arduino code demonstrates how to control the blinking speed of an LED using a potentiometer. The potentiometer's position determines the delay between LED on and off states.

## Hardware Required:

- Arduino board
- LED
- 220 ohm resistor
- Potentiometer

## Circuit:

- Connect the long leg (anode) of the LED to pin 13 through the 220 ohm resistor.
- Connect the short leg (cathode) of the LED to ground.
- Connect the middle pin of the potentiometer to analog input A0.
- Connect the outer pins of the potentiometer to 5V and ground.

## Code Explanation:

### potPosition: An integer variable to store the value read from the potentiometer.
### setup(): Runs once when the Arduino board starts up.
- Serial.begin(9600): Initializes serial communication for debugging.
- pinMode(13, OUTPUT): Configures pin 13 as an output to control the LED.

### loop(): Runs repeatedly in a loop.
- potPosition = analogRead(A0): Reads the value from the potentiometer (0-1023).
- Serial.println(potPosition): Prints the potentiometer value to the serial monitor for debugging.
- digitalWrite(13, HIGH): Turns on the LED.
- delay(potPosition): Delays for a time determined by the potentiometer value (in milliseconds).
- digitalWrite(13, LOW): Turns off the LED.
- delay(potPosition): Delays for a time determined by the potentiometer value (in milliseconds).

## Functionality:

As you turn the potentiometer knob, the blinking speed of the LED will change. The further the knob is turned, the faster the LED will blink. The serial monitor can be used to view the potentiometer value while the code is running.
