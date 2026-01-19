## Laboratory Activity #5 – Receiving Serial Connection Using Arduino from Python  

### I. Description  
In the fifth and final laboratory exercise, the boundary between software and hardware was bridged through an experiment in *cross-platform serial communication*. Using the programming power of *Python* and the embedded control of *Arduino*, students created a fully interactive lighting control system capable of *real-time command execution* and *bidirectional data exchange*.  

Through this setup, the *Python script* acted as a digital command center, sending coded messages over a serial link to the *Arduino Uno*, which responded by controlling three LEDs—**red, green, and blue**. Each light responded instantly to user input, toggling, activating, or deactivating based on the commands received. Simultaneously, the Arduino sent textual feedback messages back to the terminal, acknowledging each action or reporting errors for invalid inputs.  

This activity showcased the seamless communication between high-level software (Python) and low-level embedded hardware (Arduino), a critical capability in *IoT systems and intelligent device control*.  

***

### II. Objectives  
1. To understand and implement *Serial data communication* between Python and Arduino.  
2. To utilize *Python* as a control interface for real-time hardware management.  
3. To design an *interactive LED control system* managed through serial commands.  

***

### III. Concepts Applied  
The experiment combined elements of programming logic, serial communication, and modular code design:  

- *Arduino Serial Communication:* Using Serial.begin(), Serial.available(), and Serial.read() for message handling.  
- *Python Integration:* Implemented via the *PySerial* library to establish and manage the COM port connection.  
- *Case-Insensitive Command Handling:* Accepted both uppercase and lowercase inputs for ease of control.  
- *Digital Output Control:* Used digitalWrite() to manipulate three LEDs representing different color channels.  
- *Interactive Menu System in Python:* A continuously running loop provided live command prompts.  
- *Error Handling:* Displayed feedback for unrecognized commands to ensure robust interaction.  
- *Modular Programming:* Incorporated header-based function definitions in Arduino for reusable LED logic.  

Together, these components gave students a practical understanding of cross-language communication—a foundation for creating intelligent IoT dashboards, home automation interfaces, or data-driven robotics systems.  

***

### IV. System Behavior  

#### Hardware Setup  
- *Arduino Uno* connected via USB to a Python-programmed host computer.  
- *Three color LEDs:*  
  - Red → *Digital Pin 8*  
  - Green → *Digital Pin 9*  
  - Blue → *Digital Pin 10*  
- Each LED wired through a *220Ω resistor* to ground.  

#### Communication Workflow  
The Python application acts as the *command sender*. Users type control characters which are transmitted via the serial link. The Arduino reads and interprets these commands, performs the appropriate LED actions, and returns a confirmation response.  

#### Command and Response Mapping  

| Command | Function | Description | Arduino Response |
|----------|-----------|--------------|------------------|
| R / r | Toggle Red LED | Switches red LED ON/OFF | RED ON / RED OFF |
| G / g | Toggle Green LED | Switches green LED ON/OFF | GREEN ON / GREEN OFF |
| B / b | Toggle Blue LED | Switches blue LED ON/OFF | BLUE ON / BLUE OFF |
| A / a | All LEDs ON | Activates all LEDs simultaneously | ALL ON |
| O / o | All LEDs OFF | Turns all LEDs OFF | ALL OFF |
| X / x | Exit | Terminates the Python program | EXITING... |
| Other | Invalid command | Not recognized | ERR: UNKNOWN COMMAND |

Each command triggers an immediate *visual response* (LED change) and a *textual update* in both the Arduino Serial Monitor and the Python terminal—creating an interactive control experience.

***

### V. Circuit Diagram and Wiring  

| Component | Arduino Pin | Connection Path | Function |
|------------|--------------|------------------|-----------|
| Red LED | 8 | Anode → 220Ω resistor → GND | LED 1 indicator |
| Green LED | 9 | Anode → 220Ω resistor → GND | LED 2 indicator |
| Blue LED | 10 | Anode → 220Ω resistor → GND | LED 3 indicator |
| USB Cable | — | Arduino ↔ Computer | Power + Serial communication |
| Python Interface | — | PySerial COM port | User command input/output |

The system runs entirely on *USB power and communication*, making it portable, efficient, and representative of actual IoT command pipelines used in distributed control environments.  

***

This project concluded the laboratory series by blending *software logic*, *hardware control*, and *bi-directional communication* into one cohesive system—effectively demonstrating how personal computers can act as intelligent command hubs for real-world devices.

***
