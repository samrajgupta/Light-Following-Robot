FEATURES

	Light follower robot is activated with light. The robot moves as long as it detects the light.
	The robot has two light detection sensors which are prepared with LDRs The sensitivity of the sensors can be set by using the trimpots on each sensor circuit.
	Robot chassis is prepared with 3 mm thick 150 mm diameter plexiglass material.
	The robot has two 6 V geared DC motors, two wheels and a caster ball wheel.
	L298N motor driver board is used for driving of geared DC motors.
	Arduino light follower robot is powered by 12V alkaline battery.




HARDWARE ANALYSIS
 Components required:
	60 rpm DC motor x4
	L298N Motor Drive
	Arduino UNO
	3 pin LDR module
	Wheels
	Chassis
	Jumper Wires
	12V Battery
 
I. 	L298N Motor Driver:  
The motor driver chosen to power and control the motors is a L298N Dual H-Bridge Motor Driver Shield. Each channel on the L298N is capable of delivering an output current up to 2 A, thus it can easily drive two sets of brushed DC motors as illustrated in Figure 
 
Two enable inputs are provided to enable or disable the motors independently of the input signals. Moreover, the motor driver has four pins used for controlling direction of the motors, and two pins where it reads the PWM signal that is sent to the motors. The motors in the same set i.e. the two motors on the same side are in parallel, which means that the PWM output is the same for the two motors on the same side. The motor driver is connected to an external power source, in this case a 7,4V battery pack with the benefit to power the motors directly without having to go through the Arduino
II. 	Arduino Micro-controller: 
 Arduino is an open-source prototyping platform based on easy-to-use hardware and software. Arduino boards are able to read inputs - light on a sensor, a finger on a button, or a Twitter message - and turn it into an output - activating a motor, turning on an LED, publishing something online. We can tell your board what to do by sending a set of instructions to the microcontroller on the board. To do so we use the Arduino programming language (based on wiring), and the Arduino Software (IDE), based   on Processing. 
 The Arduino Uno can be powered via the USB connection or with an external power supply. The power source is selected automatically. External (non-USB) power can come either from an AC-to-DC adapter (wall-wart) or battery. The adapter can be connected by plugging a 2.1mm center-positive plug into the board's power jack. Leads from a battery can be inserted in the Gnd and Vin pin headers of the POWER connector. The board can operate on an external supply of 6 to 20 volts. If supplied with less than 7V, however, the 5V pin may supply less than five volts and the board may be unstable. If using more than 12V, the voltage regulator may overheat and damage the board. The recommended range is 7 to 12 volts. 
 


  What Does it Do? 
The Arduino hardware and software was designed for artists, designers, hobbyists, hackers, newbies, and anyone interested in creating interactive objects or environments. Arduino can interact with buttons, LEDs, motors, speakers, GPS units, cameras, the internet, and even your smart-phone or your TV! This flexibility combined with the fact that the Arduino software is free, the hardware boards are pretty cheap, and both the software and hardware are easy to learn has led to a large community of users who have contributed code and released instructions for a huge variety of Arduinobased projects. 
 
 What's on the board? 
There are many varieties of Arduino boards (explained on the next page) that can be used for different purposes. Some boards look a bit different from the one below, but most Arduinos have the majority of these components in common 

Power (USB / Barrel Jack) 
Every Arduino board needs a way to be connected to a power source. The Arduino UNO can be powered from a USB cable coming from your computer or a wall power supply (like this) that is terminated in a barrel jack. In the picture above the USB connection is labeled (1) and the barrel jack is labelled (2). The USB connection is also how you will load code onto your Arduino board. 
 
Pins (5V, 3.3V, GND, Analog, Digital, PWM, AREF) 
The pins on your Arduino are the places where you connect wires to construct a circuit (probably in conjuction with a breadboard and some wire. They usually have black plastic „headers‟ that allow you to just plug a wire right into the board. The Arduino has several different kinds of pins, each of which is labeled on the board and used for different functions. GND (3): Short for „Ground‟. There are several GND pins on the Arduino, any of which can be used to ground your circuit. 
5V (4) & 3.3V (5): As you might guess, the 5V pin supplies 5 volts of power, and the 3.3V pin supplies 3.3 volts of power. Most of the simple components used with the Arduino run happily off of 5 or 3.3 volts. Analog (6): The area of pins under the „Analog In‟ label (A0 through A5 on the UNO) are Analog In pins. These pins can read the signal from an analog sensor (like a temperature sensor) and convert it into a digital value that we can read. 
Digital (7): Across from the analog pins are the digital pins (0 through 13 on the UNO). These pins can be used for both digital input (like telling if a button is pushed) and digital output (like powering an LED). PWM (8): You may have noticed the tilde (~) next to some of the digital pins (3, 5, 6, 9, 10, and 11 on the UNO). These pins act as normal digital pins, but can also be used for something called Pulse-Width Modulation (PWM). We have a tutorial on PWM, but for now, think of these pins as being able to simulate analog output (like fading an LED in and out). AREF (9): Stands for Analog Reference. Most of the time you can leave this pin alone. It is sometimes used to set an external reference voltage (between 0 and 5 Volts) as the upper limit for the analog input pins. 
 
Reset Button 
Just like the original Nintendo, the Arduino has a reset button (10). Pushing it will temporarily connect the reset pin to ground and restart any code that is loaded on the Arduino. This can be very useful if your code doesn’t repeat, but you want to test it multiple times. Unlike the original Nintendo however, blowing on the Arduino doesn’t usually fix any problems. 
 
Power LED Indicator 
Just beneath and to the right of the word “UNO” on your circuit board, there’s a tiny LED next to the word „ON‟ (11). This LED should light up whenever you plug your Arduino into a power source. If this light doesn’t turn on, there’s a good chance something is wrong. Time to re-check your circuit! 
 
TX RX LEDs 
TX is short for transmit; RX is short for receive. These markings appear quite a bit in electronics to indicate the pins responsible for serial communication. In our case, there are two places on the Arduino UNO where TX and RX appear – once by digital pins 0 and 1, and a second time next to the TX and RX indicator LEDs (12). These LEDs will give us some nice visual indications whenever our Arduino is receiving or transmitting  
2.8 Main IC 
The black thing with all the metal legs is an IC, or Integrated Circuit (13). Think of it as the brains of our Arduino. The main IC on the Arduino is slightly different from board type to board type, but is usually from the A Tmega line of IC‟s from the ATMEL company. This can be important, as you may need to know the IC type (along with your board type) before loading up a new program from the Arduino software. This information can usually be found in writing on the top side of the IC. If you want to know more about the difference between various IC‟s, reading the datasheets is often a good idea. 
 
Voltage Regulator 
The voltage regulator (14) is not actually something you can (or should) 
interact with on the Arduino. But it is potentially useful to know that it is there and what it’s for. The voltage regulator does exactly what it says – it controls the amount of voltage that is let into the Arduino board. Think of it as a kind of gatekeeper; it will turn away an extra voltage that might harm the circuit. Of course, it has its limits, so don’t hook up your Arduino to anything greater than 20 volts. 
 
The Arduino Family 
Arduino makes several different boards, each with different capabilities. In addition, part of being open-source hardware means that others can modify and produce derivatives of Arduino boards that provide even more form factors and functionality

III. Light Dependent Resistor: 
A photoresistor or light dependent resistor is an electronic component that is sensitive to light. When light falls upon it, then the resistance changes. Values of the resistance of the LDR may change over many orders of magnitude the value of the resistance falling as the level of light increases.
It is not uncommon for the values of resistance of an LDR or photoresistor to be several megohms in darkness and then to fall to a few hundred ohms in bright light. With such a wide variation in resistance, LDRs are easy to use and there are many LDR circuits available. The sensitivity of light dependent resistors or photoresistors also varies with the wavelength of the incident light.
LDRs are made from semiconductor materials to enable them to have their light sensitive properties. Many materials can be used, but one popular material for these photoresistors is cadmium sulphide, CdS, although the use of these cells is now restricted in Europe because of environmental issues with the use of cadmium.
Similarly cadmium CdSe is also restricted. Other materials that can be used include lead sulphide, PbS and indium antimonide, InSb. 
  
Software simulation on Tinkercad


4.1 CONCLUSION
In this project we have studied and implemented a Light  Following Robot using Arduino Uno best suitable for military application . The programming and interfacing of Arduino Uno has been mastered during the implementation.
4.2 FUTURE WORK
	An array of LDR’s Sensor can be used for improvement of light sensing that will give a high accuracy of readings. 

	We can also design this using micro controller. 

	If a ultrasonic sensor is added in this robot then it can avoid obstacles which are in its path during following the light.

	The robot can also be made colour specific by installing photosensors that provide response to specific wavelengths of light.

	The motor drive can be improved with higher rpm values for quick accessibility depending on the task.

