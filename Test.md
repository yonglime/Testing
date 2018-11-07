
## Light Buoy (Electrical Component)
The light buoy is created for the purposes of testing and collecting data in a real life environment for color recognition. The main goal is for the light buoy to flash three colors (Red, Blue, and Green) in a random sequence.  

The light buoy will appear black when it is off. The light assembly on the buoy will successively display colors one at a time to generate a sequential pattern of three colors (e.g., red-green-red). Each individual color will appear for 1 second, after which the lights will remain off (black) for 2 seconds before repeating the same pattern. A color may be repeated in the pattern, but the same color will not appear twice in a row.

[Link to RobotX 2018 competition details
](https://www.robotx.org/images/RobotX-2018-Tasks_v2.0.pdf)

**Supplies**

 - Arduino Mega
 - 3-Channel Relay Board
 - Portable Power Supply (12V+)
 - Voltage Regulator (If needed)
 - Husky Box or any water proof container/box.
 - 90+ ft. of LED strips. 
 - Push Button
 - Water proof ethernet cable

**Software**

 - [Arduino IDE ](https://www.arduino.cc/en/Main/Software)(Preferably)
 or
 - [Arduino Web Editor](https://create.arduino.cc/) (Must have internet connection)
 
 **Arduino**
![Arduino MEga](https://www.arduino.cc/en/uploads/Main/ArduinoMega.jpg)
An Arduino is required to control the color sequences. Further below will contain the Arduino code to control the color sequences of the LED strips. The Arduino will output three signals that will control relay boards to turn colors on/off on the LED strip. The Arduino will also take in an input from a push button that will signal when to randomize the color sequence.
[Link for more about Arduino
](https://www.arduino.cc/en/Tutorial/HomePage)

**Power**

The light buoy will need to be fully functional out in the middle of the ocean. For this to be possible a portable battery is required. A 12V or higher portable battery is recommended to power the LED strips. If the power supply is higher than 12V an voltage regulator is required because the Arduino Mega has a max input of 12V. 

**Relay Board**
 
![enter image description here](https://www.inventelectronics.com/wp-content/uploads/2017/04/3-channel-relay-2.jpg)
 A 3-Channel relay board is required for the light buoy to create multiple color sequences. The relay board will connect to the three individual wires of the LED strip. Each wire is associated with a color (Red, Blue, and Green) and each wire will be connected to a individual channel on the relay board. An Arduino will send a signal to the relay board to control which lights to turn on/off. 
[Link for more information about Relay Boards](https://howtomechatronics.com/tutorials/arduino/control-high-voltage-devices-arduino-relay-tutorial/)



**Schematics**

Fill in stuff here.

**Code**

Below are two different codes that will work for the light buoy. Both codes act accordingly, each individual color will appear for 1 second, after which the lights will remain off (black) for 2 seconds before repeating the same pattern. A color may be repeated in the pattern, but the same color will not appear twice in a row.

The reasoning behind having two different codes are for the different methods of randomizing the color sequences. There will be a push button on the outside of the electrical components when held will randomize the color sequence. However, if there are ever issues with the push button during testing. Below contains code that will avoid using the button and randomize the color patterns after four sequences. 

[Link for code to randomize after four consecutive patterns](https://github.com/riplaboratory/Kanaloa/blob/master/Projects/DeepLearning/ScanTheCode/Arduino/a20181013/a20181013_scanTheCode.ino)

[Link for code to randomize when button is held](https://github.com/riplaboratory/Kanaloa/blob/master/Projects/DeepLearning/ScanTheCode/Arduino/STCRandButton)
