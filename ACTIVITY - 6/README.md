## Laboratory Activity #6 – Bidirectional Control Using Arduino and Python  

### I. Description  
The sixth laboratory activity marks a significant milestone in interactive system design—an experiment where both *hardware and software “speak” to each other*. This exercise demonstrates *bidirectional serial communication* between an *Arduino microcontroller* and a *Python program*, enabling a true two-way dialogue of commands and feedback.  

In this setup, *Arduino* sends button-press data to *Python*, and Python responds by transmitting control commands that toggle LEDs on the Arduino board. Together, they form a *closed feedback loop*, allowing inputs from the physical world to influence digital processes, which then return instructions that affect the physical hardware in real time.  

This kind of responsive collaboration between computer and microcontroller models how intelligent IoT systems operate—continuously gathering, processing, and reacting to data with minimal latency.  

***

### II. Objectives  
1. To understand and implement *Arduino Serial communication* for two-way data transfer.  
2. To use *Python* for serial data reception and real-time control response.  
3. To establish *bidirectional serial communication* that enables reactive, synchronized hardware–software interaction.  

***

### III. Concepts Applied  
This experiment combines crucial principles of data exchange and input/output synchronization:  

- *Serial Communication:* Implements Serial.begin(), Serial.println(), and Serial.readStringUntil() for message handling.  
- *Digital Input Capture:* Uses push buttons connected to digital pins to generate hardware events.  
- *Edge Detection:* Detects discrete button presses, preventing multiple triggers per press.  
- *State-Based Logic:* Manages LED status changes based on received return signals.  
- *Bidirectional Data Flow:* Arduino transmits to Python and listens simultaneously for returning commands.  
- *Python Communication (PySerial):* Reads incoming serial data and sends encoded responses.  
- *Low-Latency Feedback:* Ensures responses cycle in under one second, simulating real-time IoT performance.  

By integrating these elements, the experiment captures both *event-driven hardware reactions* and *responsive data control*, achieving seamless human–machine synchronization.  

***

### IV. System Behavior  

#### Hardware Components  
- *Inputs:* Three push buttons  
- *Outputs:* Three LEDs (Red, Green, Blue)  
- *Interface:* USB serial communication  

#### Outbound Data Flow (Arduino → Python)  
- When *Button 1* is pressed → Arduino sends *“R”*  
- When *Button 2* is pressed → Arduino sends *“G”*  
- When *Button 3* is pressed → Arduino sends *“B”*  

At this stage, Arduino functions purely as a transmitter. It doesn’t act on these signals; instead, it forwards them to Python for interpretation.

#### Inbound Data Flow (Python → Arduino)  
Python continuously listens for characters from Arduino:  
- Upon receiving *“R”*, Python sends back *1*  
- Upon receiving *“G”*, Python sends back *2*  
- Upon receiving *“B”*, Python sends back *3*  

Arduino interprets these numeric codes as LED toggles:  
- *1 → Red LED Toggle*  
- *2 → Green LED Toggle*  
- *3 → Blue LED Toggle*  

#### Real-Time Feedback Loop  
This two-way flow forms a *cyclic communication pipeline**—Arduino detects hardware input, Python interprets and responds, and Arduino enacts corresponding visual feedback. The result is a *real-time control system exhibiting average latency of *under one second*, proving efficient bidirectional synchronization between computing layers.  

***

### V. Circuit Diagram and Wiring  

| Component | Arduino Pin | Type | Description |
|------------|--------------|------|--------------|
| Button 1 | 2 | Input | Sends 'R' when pressed |
| Button 2 | 3 | Input | Sends 'G' when pressed |
| Button 3 | 4 | Input | Sends 'B' when pressed |
| Red LED | 8 | Output | Toggles on ‘1’ response |
| Green LED | 9 | Output | Toggles on ‘2’ response |
| Blue LED | 10 | Output | Toggles on ‘3’ response |
| GND | — | — | Common ground shared among all components |
| USB Port | — | — | Powers Arduino and provides serial connection |

Each push button shares a *common ground*, while each LED connects through a *220Ω resistor* for current protection. The *USB connection* supplies both power and data transfer channels, linking Arduino directly to the *Python interface* running on the host computer.  

***

### VI. System Significance  
This activity brought the laboratory series to its most advanced stage—achieving true interactive feedback between hardware and software. Beyond simple control, this design reflects how modern connected systems—such as environmental monitors, autonomous vehicles, and home automation networks—rely on continuous, coordinated communication to function smartly and safely.  

What began as blinking LEDs has evolved into a dynamic ecosystem of *data-driven, intelligent response*, symbolizing the essence of IoT system design.  

***
