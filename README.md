# EXPERIMENT-01-INTERFACTING-DIGITAL-OUTPUT-WITH-EDGE-DEVICE---RASPBERRYPI-PICO-
## NAME M.K.Suriya prakash
## DEPARTMENT IoT
## ROLL NO 21224110053
## DATE OF EXPERIMENT 24.02.2025

### AIM
To interface a digital output device (LED) with the Raspberry Pi Pico and control it using MicroPython.

APPARATUS REQUIRED
Raspberry Pi Pico
LED (Light Emitting Diode)
330Ω Resistor
Breadboard
Jumper Wires
USB Cable
Computer with Thonny IDE
## THEORY
Raspberry Pi Pico is a microcontroller board based on the RP2040 chip. It supports MicroPython, making it suitable for IoT and embedded applications.

Digital Output refers to controlling external devices like LEDs, buzzers, or relays using GPIO (General Purpose Input Output) pins. A GPIO pin can be set to HIGH (3.3V) or LOW (0V) to turn the device ON or OFF.

## Working Principle:

The LED is connected to one of the GPIO pins of the Pico.
The MicroPython script sets the GPIO pin HIGH to turn the LED ON and LOW to turn it OFF.
CIRCUIT DIAGRAM
Connect the anode (longer leg) of the LED to GP15 via a 330Ω resistor.
Connect the cathode (shorter leg) of the LED to GND (ground).


## PROGRAM (MicroPython)
Blinking LED
```

from machine import Pin
from utime import sleep



led1 = Pin(0, Pin.OUT)


while True:
    led1.toggle()
    sleep(0.5)
```
Blinking Multiple LED
```

from machine import Pin
from utime import sleep



led1 = Pin(0, Pin.OUT)
led2 = Pin(4, Pin.OUT)
led3 = Pin(9, Pin.OUT)

while True:
    led1.toggle()
    sleep(0.5)
    
    led2.toggle()
    sleep(1)
   
    led3.toggle()
    sleep(2)
```
Blinking Multiple LED with Buzzer
```
from machine import Pin
from utime import sleep



led1 = Pin(0, Pin.OUT)
led2 = Pin(4, Pin.OUT)
led3 = Pin(9, Pin.OUT)
buzz=Pin(3 ,Pin.OUT)
while True:
    led1.toggle()
    sleep(0.5)
    buzz.toggle()
    sleep(0.5)
    led2.toggle()
    sleep(1)
    buzz.toggle()
    sleep(0.5)
    led3.toggle()
    sleep(2)
    buzz.toggle()
    sleep(0.5)
```




## OUPUT  
Blinking LED
![Screenshot 2025-02-24 113205](https://github.com/user-attachments/assets/1b6f7644-c198-4f99-b8c6-8f6673fac15d)

 
Blinking Multiple LED
![Screenshot 2025-02-24 112816](https://github.com/user-attachments/assets/35dce704-f04d-4fe0-b3d4-80adf2b2572a)

Blinking Multiple LED with buzzer
 ![Screenshot 2025-02-24 113205](https://github.com/user-attachments/assets/06958719-4db2-42ee-8703-ac08e4d179c2)



 
## RESULTS
The LED connected to the Raspberry Pi Pico successfully turns ON and OFF at 1-second intervals, confirming the proper interfacing of a digital output.
