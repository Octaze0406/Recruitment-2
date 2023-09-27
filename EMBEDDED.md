**ARDUINO**
---

To read input from devices and to control outputs.
Mainly consits of 3 factors;

  1.ARDUINO IDE
  2.MICROCONTROLLER
  3.CODE

**A. HARDWARE**
---
+Basically means the physical components that makes up the board.eg: 

  1.Microcontroller : The microcontroller is the central processing unit of the board, where you upload the code that instructs the board on how to interpret inputs and generate outputs.
  
  2.Power supply : Can be powered using USB port, VIN PIN etc.
  
  3.INPUT AND OUTPUT PINS: where all the components are connected to and based on the code classifies specific pins as inputs or outputs.

+The pins on the board include :

 a.GPIO ; general purpose input output pins which works by reading voltage changes at the pins ends and by changing voltage at the pin ends respectively.
 
 b.DIGITAL PINS; to read binary (ie. on/off) inputs. tx(transmit) and rx(receive) are available to communicate using USB port.
 
   (~) after pin number means pins are capable of Pulse Width Modulation which is used to toggle between high and low voltages. Hence by using data cycle(number of times pin was high) we can set intensity .

 c.ANALOG PINS; to read continous outputs which can be converted to digital binary values for microcontroller to understand. Mainly used to take read from temperature sensors which provides contant outputs.

 d.POWER ; GND- ground,  V- external voltage source to power the board.
 
   
 **B.IDE**
 ---

 The IDE (Integrated Development Environment) is a crucial software component of the Arduino platform. It provides an interface for writing, compiling, and uploading code to Arduino microcontroller boards.
 
 It includes key components like : 
  1.library for pre written codes, 
  2.serial monitor to monitor the outputs
  3.code editor to write the codes
  
**C.CODE**
---

 +To store variables: type name = "__"; where tpye includes integers(int), boolean(bool) ,char (to store single digits characters -specifically 8 bit ASCII .
 
 Bit-smallest unit data that a computer can process. Bytes-Bits are usually assembled into a group of eight to form a byte .KB- 1024 bytes.

 +pinMOde(pin, INPUT/OUTPUT); -configures pins as output/inputs

 +digitalWrite(pin, HIGH/LOW); configures pin as high or low voltage

 +digitalRead(pin); read the current stae of pin.

 +analogRead(pin); read the analog output in the range 0 to 1023.


 **ARDUINO PRACTICE PROJECTS**
 ---

 1. POTENTIOMETER CONTROLLED SERVO: https://www.tinkercad.com/things/6GKcPaK4JrF
 2. PUSH BUTTON CONTROLLED TRAFIC LIGHT : https://www.tinkercad.com/things/8AihR7Yj9or

 PRACTICE PORJECTS: 
 
  1.Fading of an led and to displaying its output on an oscillometer: https://www.tinkercad.com/things/4hLyOHPvs5O.
  
  2. Rotating a Servo using a temerature sensor: https://www.tinkercad.com/things/0063zHm5H8m





