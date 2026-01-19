## Laboratory Activity #1 – Working with Digital Signals  

### I. Description  
This laboratory experiment demonstrates digital output control using the *Arduino Uno*, focusing on how digital signals can be manipulated to control physical components. The setup employs five LEDs to produce a running light or chase light effect. This effect is achieved through sequential illumination of LEDs in both forward and reverse order.  

The program makes use of *digital HIGH (5V)* and *LOW (0V)* transitions, with each state maintained for one second. Through this exercise, students gain practical understanding of *digital timing, sequencing, and control*, which are foundational in *IoT-based automation systems*.

***

### II. Objectives  
1. To review the functionality of Arduino as a platform for implementing Internet of Things (IoT) systems.  
2. To understand and apply the principles of digital signals in basic Arduino circuits.  

***

### III. Concepts Applied  
- *Digital Signal States:*  
  - HIGH = 5V  
  - LOW = 0V  
- *pinMode(pin, OUTPUT):* Configures a digital pin as an output.  
- *digitalWrite(pin, HIGH/LOW):* Sends a digital signal (5V or 0V) to a pin.  
- *delay(ms):* Introduces a time delay in milliseconds between state transitions.  
- *Sequential Programming:* Used to implement the chase light logic.  
- *Breadboard Prototyping:* Incorporates current-limiting resistors to protect LEDs.  

***

### IV. System Behavior  
- *Pins Used:* 8, 9, 10, 11, and 12  
- *Forward Sequence:*  
  LEDs turn ON in order from Pin 8 → Pin 9 → Pin 10 → Pin 11 → Pin 12, each with a one-second interval.  
- *Reverse Sequence:*  
  LEDs turn OFF in reverse order from Pin 12 → Pin 11 → Pin 10 → Pin 9 → Pin 8, again with one-second intervals.  
- *Cycle Duration:* Approximately 10 seconds per complete loop.  
- *Visual Output:* A smooth left-to-right running light followed by a right-to-left extinguishing sequence, simulating bidirectional motion.  

***

### V. Circuit Diagram and Wiring  
The circuit consists of five LEDs connected to the *Arduino Uno* through a *breadboard*. Each LED is connected in series with a *220Ω resistor* to limit current and prevent damage.  

*Wiring Configuration:*  
| Arduino Pin | Wire Color | Component | Connection |
|--------------|-------------|------------|-------------|
| 8            | Orange      | LED1       | Anode through resistor to GND |
| 9            | Yellow      | LED2       | Anode through resistor to GND |
| 10           | Green       | LED3       | Anode through resistor to GND |
| 11           | Blue        | LED4       | Anode through resistor to GND |
| 12           | Red         | LED5       | Anode through resistor to GND |

***
