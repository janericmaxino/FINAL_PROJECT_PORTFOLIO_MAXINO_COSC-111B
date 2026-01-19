## Laboratory Activity #7 – Controlling Arduino Using FastAPI  

### I. Description  
The final laboratory experiment brings together everything learned in previous sessions—microcontrollers, Python integration, and network-based control—through the creation of a *FastAPI-powered web interface* for Arduino. In this setup, students built a *real-time bidirectional control system* where both *hardware inputs (push buttons)* and *software commands (HTTP requests)* could operate simultaneously to toggle LED states.  

By combining *Serial communication* and *web-based interaction*, the system emulates the architecture of modern *IoT ecosystems*, where sensors, controllers, and cloud services communicate continuously. The *FastAPI framework* acts as the digital bridge, translating user actions over the web into direct commands that Arduino interprets instantly via the serial port.  

This activity not only highlights the merging of hardware control with web technology but also lays the groundwork for *networked automation*, *remote monitoring*, and **smart device synchronization**—key features in the expanding Internet of Things landscape.  

***

### II. Objectives  
1. To implement *Arduino Serial communication* for dynamic hardware control.  
2. To utilize *Python* and *FastAPI* to design HTTP endpoints for real-time Arduino interaction.  
3. To develop a *bidirectional control system* that links physical hardware actions with web-based commands for synchronized LED management.  

***

### III. Concepts Applied  
This experiment combines both embedded system design and web development concepts, bridging the two domains through a unified communication framework.  

- *Arduino–Python Serial Communication* – Data exchange through USB using Serial read and write functions.  
- *Digital Input Handling* – Push button states detected through digital pins.  
- *Edge Detection* – Identifies new button presses to prevent redundant toggles.  
- *Digital Output Control* – Manages LED on/off states through Arduino pins.  
- *HTTP Server Implementation (FastAPI)* – Hosts interactive endpoints for remote LED control.  
- *Mapping Web Requests to Serial Commands* – Relays specific API calls to corresponding LED toggles.  
- *State Synchronization* – Ensures LED states remain consistent between physical and software inputs.  

The project demonstrates how IoT systems function as multi-layer architectures, seamlessly blending local hardware logic with network-level services.  

***

### IV. System Behavior  

#### A. Hardware Configuration  
*Components Used:*  
- 3 LEDs (Red, Green, Blue)  
- 3 Push Buttons (one for each LED)  

*Pin Assignments:*  
| Component | Arduino Pin | Function |
|------------|--------------|-----------|
| Red LED | 5 | Output |
| Green LED | 6 | Output |
| Blue LED | 7 | Output |
| Button 1 | 10 | Input |
| Button 2 | 11 | Input |
| Button 3 | 12 | Input |

The buttons serve as local input devices for toggling LEDs, while the serial connection enables fast, synchronized data exchange with the FastAPI application.  

***

#### B. Arduino Sketch Behavior  
On the hardware side, the Arduino continuously performs two parallel tasks:  

1. *Reading button inputs* and toggling the associated LED whenever a new press is detected.  
2. *Listening for serial commands* transmitted by the Python FastAPI server and updating LED states accordingly.  

Each received serial character corresponds to a specific LED or global state control:  
- 'r' → Toggle Red  
- 'g' → Toggle Green  
- 'b' → Toggle Blue  
- '1' → Turn all LEDs ON  
- '0' → Turn all LEDs OFF  

Arduino ensures that LED states remain *consistent* even when triggered through mixed input methods—manual button presses or software requests.  

***

#### C. FastAPI Application Behavior  
The *FastAPI server*, running locally on Python, acts as the system’s command hub. It defines HTTP endpoints for direct LED interaction:  
- /led/red → Toggle Red LED  
- /led/green → Toggle Green LED  
- /led/blue → Toggle Blue LED  
- /led/on → Turn all LEDs ON  
- /led/off → Turn all LEDs OFF  

When a user accesses any of these routes (for example, using a browser or a mobile device), the server instantly *sends the corresponding serial command* to Arduino via the *PySerial* library.  

This allows LEDs to be controlled physically through the buttons or *remotely* over Wi-Fi or a web interface—showcasing real-time IoT synchronization.  

***

### V. Circuit Diagram and Wiring  

| Component | Pin | Type | Connection |
|------------|------|------|-------------|
| Red LED | 5 | Output | Through 220Ω resistor to GND |
| Green LED | 6 | Output | Through 220Ω resistor to GND |
| Blue LED | 7 | Output | Through 220Ω resistor to GND |
| Button 1 | 10 | Input | With pull-down or internal pull-up resistor |
| Button 2 | 11 | Input | With pull-down or internal pull-up resistor |
| Button 3 | 12 | Input | With pull-down or internal pull-up resistor |
| USB Port | — | — | Provides both power and Serial communication |

The *USB connection* acts as both a power source and a serial gateway between the *Arduino Uno* and *FastAPI server*, achieving real-time responsiveness between physical buttons and API endpoints.  

***

### VI. System Insight  
This final laboratory exercise transitions the Arduino from a closed-loop controller into a *network-enabled intelligent device*, forming a key building block of IoT infrastructure. The successful integration of *FastAPI web services* with hardware control demonstrates how local devices can be expanded into *internet-ready systems*, capable of being managed from anywhere.  

With this, the lab series evolves from blinking LEDs to a scalable, web-controllable hardware platform—embodying the essence of connected innovation.  

***
