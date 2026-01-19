## Laboratory Activity #3 – Working with Sensors  

### I. Description  
In this week’s laboratory exercise, students moved deeper into the world of *Internet of Things (IoT)* experimentation by exploring how sensors connect the physical and digital realms. The task: build a *simple fire detection system* using an *Arduino Uno* as the central controller.  

At the heart of this project are two critical sensors—a *thermistor*, which senses temperature changes, and a *photoresistor (LDR)*, which responds to variations in light intensity. Together, they provide the Arduino with streams of analog data that simulate how IoT devices “perceive” their environments. By combining these readings and applying threshold-based decision logic, the system can detect possible fire conditions and activate an LED alert.  

More than a simple circuit, this activity demonstrates the *integration of multiple sensors*, *real-time data analysis*, and *hardware-based safety response mechanisms*, all of which are essential cornerstones of modern IoT systems.  

***

### II. Objectives  
1. Familiarize learners with foundational IoT sensor modules and their respective functions.  
2. Apply multiple sensors simultaneously in an integrated Arduino-based environment.  
3. Design and implement a functioning prototype for basic fire detection and alert notification.  

***

### III. Concepts Applied  
The experiment draws upon key IoT and electronics principles, transformed into hands-on practice:  

- *Analog Sensor Data Acquisition* – Translating real-world readings into measurable electronic signals.  
- *Thermistor Temperature Measurement* – Calculated using the *Beta parameter equation* to approximate ambient temperature.  
- *LDR Light Intensity Detection* – Responds inversely to illumination, simulating environmental light changes.  
- *Threshold-Based Decision Logic* – Determines alarm activation when both conditions indicate fire.  
- *Function Modularization* – Keeps code clean and segmented for sensor-specific tasks.  
- **Use of #define and const** – Simplifies pin configuration and threshold management.  
- *Digital Output Control* – Powers the LED alert that visually signals a hazardous condition.  

These concepts combine programming structure, environmental reading, and automated response—the same triad that drives industrial IoT applications.  

***

### IV. System Behavior  
*Sensors and Connections:*  
- *Thermistor:* Analog Pin *A0* – measures temperature changes in °C.  
- *LDR:* Analog Pin *A2* – measures surrounding light intensity.  
- *LED Alert:* Digital Pin *12* – provides rapid visual blinking during triggered alerts.  

*Program Workflow:*  
The Arduino continuously gathers analog readings from both sensors. Each sensor is handled by a dedicated function, making the source code modular and organized. The readings are compared against predefined thresholds:  
- When *temperature* exceeds its set point and *light intensity* indicates abnormal brightness (such as from flames), the system interprets these conditions as a potential fire.  

The alert mechanism is immediate—**the LED flashes rapidly**, signaling a detected fire scenario. This model demonstrates how logical operators can fuse multiple inputs to create smart, real-time responses typical of IoT safety systems.  

***

### V. Circuit Diagram and Wiring  
The experimental setup links the key components as follows:  

| Component | Arduino Pin | Connection Details |
|------------|--------------|--------------------|
| Thermistor | A0           | Analog input; measures temperature |
| LDR (Photoresistor) | A2 | Analog input; measures light intensity |
| LED Indicator | 12 | Output; connected via 220Ω resistor to GND |
| Power Supply | USB / 5V | Provides system power |

The circuit is designed for *modular testing*, allowing independent validation of each sensor before integration. This step-by-step configuration ensures accuracy in data readings and stability in performance.  

***
