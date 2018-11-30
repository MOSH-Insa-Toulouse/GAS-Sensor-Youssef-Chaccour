# MICRO-CONTROLLERS AND OPEN-SOURCE HARDWARE - Gas Sensor and LoRa Communication - Arduino Shield
This project was realized as part of "Microcontrollers and Open-Source Hardware" by Youssef Chaccour

# Goal
The goal of this project is to design a complete printed circuit board (PCB).
The circuit is then used with an Arduino board and a LoRa.
The collected data will be sent via the LoRa protocol on the TTN platform (The Things Network).


# Equipment
- Shield Gas Sensor
- Arduino uno
- LoRa module RN2483 breakout


# Features
- Gas sensor with connection (Requiring completion AIME)
- Adaptation circuit of the gas sensor to the ADC of the Arduino UNO:
- Filtering noises containing 2 passive filters and an active filter with AOP LTC1050
- Anti-aliasing filtering to perform ADC sampling
- Adaptation of the caliber
 
# Contents
This project contains source code and design files:
- The schematic part, describing the implemented electronic circuit (components, routing of pins)
- The layout part, describing the shape of the map, the location of the various elements on it and the trajectory of the routing tracks.
- Arduino code for LoRa

# Schemas PCB
Schematic design:
Here are some features of the schema:
- The input resistor (R1) is a protection resistor, it protects the operational amplifier from electrostatic discharges. Moreover, it is associated with the capacitor C1 to filter the voltage noise.
- The circuit between the capacitor C1 and the resistor R2 allows us to filter the current noise.
- Resistor R3 is used to adapt our assembly to the correct size. The resistance R3 can be modified to better calibrate the assembly.
- I had set up an active filter thanks to the circuit between the capacitor C2 and the resistor R4 at the output of the amplifier.
The resistor R5 and the capacitor C4 constitute a low-pass filter at the output of the assembly.
Finally, the capacitor C3 filters the noise coming from the voltage input 5V.


# PCB footprint on KiCad
Layout Design:
In order to realize the footprint correctly, I had to put into practice the following points:
- I chose a track width of 0.8 mm, so that the builder can achieve it with his equipment.
- I decided to insert only the RN2483 Breakout plate connector to optimize footprint space. Especially since we consider that the RN2483 card will not be directly integrated on the shield but connected by wires (connector).
- I used a layer of GND on the back of the plate allowing us to further optimize our space by reducing the number of connections.

Also, I have attached solution of the “exercise 5” (In Real Folder and requested by Mr. Jeremie Grisolia), as this exercise summarize the hole course, choosing the best technology with the least error.