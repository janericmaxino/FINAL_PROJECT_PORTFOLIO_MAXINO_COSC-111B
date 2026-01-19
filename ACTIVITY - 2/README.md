## Laboratory Activity #2 – Working with Analog Signals  

### I. Description  
Building on the foundation of Laboratory Activity #1, this second experiment transitions from the simplicity of digital switching to the subtle art of analog control. Here, an *Arduino Uno* takes charge not just of turning LEDs on and off but of making them *breathe*—their brightness rising and fading in rhythmic motion.  

This laboratory exercise explores *analog signals* and their real-world impact on component behavior. By using *Pulse Width Modulation (PWM)*, the Arduino mimics analog voltage levels, allowing each LED to display varying light intensities. This experiment deepens understanding of how analog outputs integrate with digital systems—an essential concept in *IoT devices* that monitor or regulate continuously changing signals.  

***

### II. Objectives  
1. To discuss analog signal behavior and implementation in Arduino circuits.  
2. To understand the relationship between analog and digital signals, including scaling and signal conversion techniques.  

***

### III. Concepts Applied  
- *Analog Signal Representation* – Continuous variation of voltage values.  
- *Pulse Width Modulation (PWM)* via analogWrite().  
- *Array Usage* – Efficient pin referencing for multiple outputs.  
- *Iterative Control* using while() loops for continuous transitions.  
- *Sequential Logic Execution* – Managing brightness order systematically.  
- *Timing Control* using delay() for smooth visual changes.  

These concepts combine to simulate fluid motion and intensity variation, offering a hands-on look at how analog techniques enrich digital systems with lifelike behavior.  

***

### IV. System Behavior  
- *Pins Used:* Digital Pins 8–12  
- *Control Method:* LED pins stored in an array for structured iteration.  
- *Operational Flow:*  
  - The LEDs *gradually increase in brightness* from *Pin 12 → Pin 8*, each reaching maximum analog intensity.  
  - The sequence then *fades back* from *Pin 12 → Pin 8*, returning to complete darkness.  
- *Visual Effect:*  
  A dynamic flowing light pattern emerges, with LEDs glowing smoothly across the line—demonstrating the visual power of analog modulation compared to the binary snap of digital control.  
- *Program Logic:*  
  Through the combined use of arrays, loops, and precise delay timing, the Arduino choreographs a smooth dance of light resembling a breathing, living system rather than a rigid on/off circuit.  

***

### V. Circuit Diagram and Wiring  
The *Arduino Uno* connects to *five LEDs* through *digital pins 8 to 12*, following an array-based wiring scheme:
  
| LED | Arduino Pin | Wire Color (suggested) | Connection Path |
|------|--------------|------------------------|------------------|
| LED1 | 8            | Orange                | Anode → 220Ω resistor → GND |
| LED2 | 9            | Yellow                | Anode → 220Ω resistor → GND |
| LED3 | 10           | Green                 | Anode → 220Ω resistor → GND |
| LED4 | 11           | Blue                  | Anode → 220Ω resistor → GND |
| LED5 | 12           | Red                   | Anode → 220Ω resistor → GND |

The *PWM effect* is achieved using analogWrite() rather than simple digitalWrite() commands, enabling each LED to exhibit variable brightness levels that represent the analog nature of electrical signals in physical systems.

***
