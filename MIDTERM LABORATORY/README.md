
## Midterm Laboratory Exam – Smart Lighting System Using Arduino  

### I. Description  
The Midterm Laboratory Exam challenged students to design and implement a *smart lighting system* capable of responding intelligently to changing ambient light conditions. Built around an *Arduino Uno* and a *photoresistor (LDR)*, the system measures real-time light intensity and visualizes lighting levels through three LEDs indicating *low*, *medium*, and *high* brightness.  

What sets this system apart is its dual operation capability: *manual* and *automatic* modes. In manual mode, users can set their own brightness thresholds via *Serial Monitor* commands, while automatic mode adjusts these thresholds dynamically to simulate specific environments like cloudy skies, normal daylight, or bright sunlight.  

By merging sensor input, conditional logic, and Serial-based user interaction, the smart lighting system captures the essence of IoT automation—**responsive decision-making based on environmental data**. Students not only learned to implement adaptive lighting behavior but also engaged in real-world coding practices involving sensor calibration, serial input parsing, and modular function design.  

***

### II. Objectives  
1. To measure analog light intensity using a *photoresistor* and an *Arduino analog input*.  
2. To implement LED-based indicators that represent low, medium, and high brightness levels.  
3. To enable *mode switching* between manual and automatic lighting control.  
4. To configure *adjustable thresholds* using user-defined commands.  
5. To visualize and monitor system operations through the *Serial Monitor*.  

***

### III. Concepts Applied  
This experiment integrates several core embedded system and software programming principles, particularly relevant to *IoT sensing and automated control*:  

- *Analog Input Processing* using analogRead() for continuous light measurement.  
- *Data Mapping* with the map() function to translate sensor readings into percentage values.  
- *Threshold-Based Logic* for LED activation depending on defined light ranges.  
- *Serial Communication* for interactive configuration and feedback.  
- *Command Parsing* using startsWith() and substring() to interpret user instructions.  
- *Automatic Mode Algorithms* for dynamic threshold adjustment under environmental profiles.  
- *Modular Code Design* to maintain readability and reuse across different lighting conditions.  

Collectively, these principles form the cornerstone of smart environment systems that adapt to real-world conditions through sensor-driven logic.  

***

### IV. System Behavior  

#### A. System Overview  
*Primary Components:*  
- *Photoresistor (LDR):* Measures ambient light (connected to Analog Pin A0).  
- *Green LED:* Indicates low light levels.  
- *Yellow LED:* Indicates medium brightness.  
- *Red LED:* Indicates high brightness.  

The system measures light intensity continuously and provides *visual feedback* through corresponding LEDs. The information is also printed on the *Serial Monitor* for observation and debugging.  

***

#### B. Modes of Operation  

*Manual Mode:*  
- The user defines custom low and high light thresholds using command inputs on the Serial Monitor.  
- The Arduino uses these values to determine LED behavior, providing full user control over sensitivity and trigger points.  

*Automatic Mode:*  
- Thresholds are set dynamically based on preconfigured environment profiles, reflecting natural lighting differences.  

| Environment | Low Threshold | High Threshold |
|--------------|----------------|----------------|
| Cloudy | 0% | 40% |
| Normal | 41% | 70% |
| Bright Sunlight | 71% | 100% |

This mode demonstrates adaptive lighting automation—where the system “decides” the appropriate brightness thresholds without human input.  

***

#### C. Serial Monitor Commands  

The Serial Monitor acts as the interface between the user and the Arduino, accepting simple text-based inputs:  

| Command | Description |
|----------|-------------|
| MODE AUTO | Switch to automatic mode |
| MODE MANUAL | Switch to manual mode |
| SET LOW xx | Define the low threshold percentage in manual mode |
| SET HIGH xx | Define the high threshold percentage in manual mode |
| Invalid input | Responds with Error: Wrong command |

These intuitive commands allow users to tune thresholds and control lighting modes dynamically without modifying the Arduino code.  

***

#### D. Runtime Behavior  
During operation, the system outputs a live status update to the *Serial Monitor every second*, showing:  
- Current *light intensity (%)*  
- Current operating *mode* (Manual or Automatic)  
- Currently active *LED color* (Green, Yellow, or Red)  
- In automatic mode: the detected *lighting environment* (Cloudy, Normal, or Bright)  

This real-time feedback loop demonstrates how *raw analog data* can be translated into meaningful, human-readable environmental insights, reflecting how smart devices process and present contextual information.  

***

### V. Circuit Diagram and Wiring  

| Component | Arduino Pin | Function | Additional Notes |
|------------|--------------|-----------|------------------|
| Photoresistor (LDR) | A0 | Analog light sensor | Configured as voltage divider |
| Green LED | 8 | Low light indicator | 220Ω resistor to GND |
| Yellow LED | 9 | Moderate light indicator | 220Ω resistor to GND |
| Red LED | 10 | High light indicator | 220Ω resistor to GND |
| USB Connection | — | Power + Serial communication | Used for command input and system feedback |

Power is supplied via the USB connection, which also serves as the *Serial communication interface*, linking the Arduino board with the computer for monitoring and control.  

***

### VI. System Insight  
The *Smart Lighting System* embodies the principles of adaptive IoT design—capturing environmental data, processing it through logical decisions, and responding visually in near real time. Its dual operating modes highlight the flexibility of combining *autonomous control* and *user-guided configuration* in a single platform.  

Beyond its academic purpose, this system mirrors real-world applications such as *automatic streetlights*, *indoor brightness regulation*, and **energy-efficient lighting automation**—solidifying its relevance in modern smart infrastructure research.  

***
