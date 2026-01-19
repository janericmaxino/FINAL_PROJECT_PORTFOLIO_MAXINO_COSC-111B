## Laboratory Activity #4 – Arduino Serial Connection  

### I. Description  
In the fourth installment of the Arduino laboratory series, students delved into the world of *Serial Communication**—a technology that bridges human input and machine response. Through this experiment, the Arduino evolved from a passive processor to an **interactive IoT node*, capable of sending and receiving data in real time.  

The setup incorporated a *photoresistor (LDR)* to sense ambient light while allowing *Serial commands* from the user to dynamically influence the behavior of an *LED indicator*. The system not only monitored environmental changes but also responded to typed commands entered through the *Arduino Serial Monitor*.  

Building upon the fire detection concept from Laboratory Activity #3, this exercise introduced a new level of interactivity: combining sensor-driven actions with *user-controlled overrides*, showcasing two-way communication between a physical system and its operator—a foundational step toward building intelligent, responsive IoT systems.  

***

### II. Objectives  
1. To understand and implement *Arduino Serial communication* for hardware monitoring and control.  
2. To utilize basic *Serial functions* for real-time command interaction and data visualization.  
3. To design a *sensor-based circuit* that can respond dynamically to *Serial input*.  

***

### III. Concepts Applied  
This laboratory made use of both hardware interfacing and programming logic concepts essential for interactive system design:  

- *Serial communication:* Functions such as Serial.begin(), Serial.print(), and Serial.readStringUntil() enable bidirectional data exchange.  
- *Analog signal acquisition:* Using analogRead() to convert light intensity from the LDR into readable values.  
- *Signal mapping:* The map() function scales analog readings for normalized interpretation.  
- *Threshold-based logic:* Determines when the LED alert should be triggered.  
- *Boolean state management:* Maintains memory of the LED’s blinking state even after conditions change.  
- *Command processing:* Handles user input with case-insensitive text comparison.  
- *Digital control:* Powers and manages LED blinking sequences through programmatic logic.  

Together, these techniques form the backbone of *interactive IoT communication systems*, where devices are both autonomous and user-responsive.  

***

### IV. System Behavior  

#### Sensor Input  
- The *photoresistor (LDR)* connects to *Analog Pin A2*, continuously reading ambient light intensity.  
- Each reading is scaled using the map() function and broadcast via *Serial Monitor*, allowing real-time observation of sensor behavior.  

#### LED Control  
- The *LED on Digital Pin 8* acts as the system’s alert signal.  
- Once the mapped brightness surpasses a set threshold, the LED transitions into a *blinking state*.  
- Importantly, this state persists even if light levels drop—illustrating how *state variables* store system conditions.  

#### Serial Command Interaction  
- The *Serial Monitor* in the Arduino IDE becomes a control console where users can send commands to influence system behavior.  
- Typing a keyword such as *“STOP”* through Serial input halts the blinking sequence.  
- This interaction reflects a *Serial command override*, exemplifying remote control of IoT hardware via textual communication.  

The result is a self-aware system that listens, decides, and obeys—a microcosm of how modern smart devices function in the Internet of Things ecosystem.  

***

### V. Circuit Diagram and Wiring  
The experimental setup includes the following connections:  

| Component | Arduino Pin | Function | Notes |
|------------|--------------|-----------|-------|
| Photoresistor (LDR) | A2 | Reads analog light intensity | Input signal source |
| LED Indicator | 8 | Displays alert through blinking | Connected via 220Ω resistor to GND |
| Power Source | USB (5V) | Supplies power and enables Serial link | Connection between PC and Arduino |
| Interface | Serial Monitor | Monitors data and accepts commands | Control hub for user input |

This configuration enables simultaneous *data acquisition*, *signal mapping*, and *real-time user interaction*, tightly integrating physical environment sensing with digital serial control.
