# PULSE


## Opensource LED pulser for optogenetic applications

This repo provides instructions for building an inexpensive and open-sourced LED pulser for optogenetic applications. The pulser is a multi-output, programmable LED light device. 

IMAGE OF INTERFACE

IMAGE OF IT IN ACTION

IMAGE OF IT BEING BUILT

Service: ...message about contact...


/*
 @author: Justin D Vrana
 @version v2.32
 @since 2014-04-03

What is this?
The basic code needed to control a multi-output, programmable LED light device for optogenetic applications. 
The the code allows for user-defined parameters to alter duration and intensity of light pulses at regular intervals.  
Central to the device is an inexpensive microcontroller and LCD keypad to display and read user input to control 
the duration and intensity of LED light pulses at user-defined intervals. Up to three LED outputs can be independently
programmed and different LED modules can be interchanged.

Usage:
Upload to Arduino Uno via USB. If uploaded properly, "Starting" should display on the LCD display screen and then the main page should display.
If there are issue uploading to the Arduino Uno, consult the Arduino website for help.
    
    To turn an output ON or OFF: From the main page on the LCD display, use the UP and DOWN buttons to select an output (indicated by a cursor)
    to edit. Move the cursor to the right using the RIGHT button and use either the UP or DOWN button to turn the output program ON
    or OFF. A countdown timer which counts down untill the next time the LED is to flash will display when the output program is running. 
    
    To change an output's scheduled flashing: To change an output program, push SELECT to select the output highlighted by the cursor. 
    Use the UP and DOWN buttons to select and attribute to edit. To edit and attribute, move the cursor to the right using the RIGHT
    button and then hold the UP or DOWN button to increase or decease a value. Move the cursor back to the left using the LEFT button 
    to change attributes to edit. Push the SELECT button at any time to return to the main page.

Sources:
- The original "LiquidCrystal" 8-bit library and tutorial
    http://www.arduino.cc/en/uploads/Tutorial/LiquidCrystal.zip
    http://www.arduino.cc/en/Tutorial/LCDLibrary

Tested only with a Arduino Uno (http://arduino.cc/) and DFRobot Keypad Shield (http://dfrobot.com)

*****Important*****:
Check and change "User Defined Paramters" directly below if needed. LCD pins, output pins, and anaolog voltages
must be changed if using an LCD Keypad Shield other than the DFRobot Keypad Shield or SainSmart Keypad Shield.
Refer to the datasheet of the LCD Keypad Shield to determine correct parameter values. 
Button values can be reset for using the "Button Reset Mode"

Button Reset Mode:
If using a different LCD Keypad shield, button values may need to be reset. To initiate button reset mode, during startup hold
down any button and continue holding button for at least three seconds when prompted. Follow the on screen instructions.
The screen will request you press and hold each button while it records the voltage values associated with that button.
Once completed, voltage values will be stored to the Arduino's EEPROM memory. Upon each start-up, these voltage values
will be loaded and used. To reset button values on the Arduino, simply re-upload this program using the "UPLOAD" button.

V 2.0 - New Version with new interface
V 2.1 - Re-vamped interface
V 2.2 - Expanded to three outputs
V2.3 - Created button reset mode
V2.32 (4/10/14) - Corrected coding error, cast timers to int instead of long
*/
