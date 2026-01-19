Final Project – MAXINO – COSC 111B

--------------------------------------------------------------------------------------------------------------------------------------------

📘Course Overview

This repository contains all laboratory activities and exams for COSC 111B – CS Elective 3 (Internet of Things).
It showcases hands-on work using Arduino, Python, FastAPI, sensors, LEDs, and serial communication—progressing from basic digital outputs to full IoT-style systems.

--------------------------------------------------------------------------------------------------------------------------------------------

📂Project Structure

🧪Midterm Activities

Lab Act #1 – Digital signals: Running light LEDs

Lab Act #2 – Analog signals and PWM LED brightness

Lab Act #3 – Sensor-based fire detection (Thermistor + LDR)

Lab Act #4 – Serial monitoring and control with photoresistor

Midterms Lab Exam – Smart lighting system with manual and automatic modes

--------------------------------------------------------------------------------------------------------------------------------------------

🧪Final Activities

Lab Act #5 – Python → Arduino serial LED control

Lab Act #6 – Bidirectional Arduino–Python button and LED control

Lab Act #7 – FastAPI + Arduino web-controlled LEDs

Finals Lab Exam – Arduino-to-Python client triggering a remote LED API

--------------------------------------------------------------------------------------------------------------------------------------------

📌Each folder includes the source code and supporting files needed to run the corresponding activity.

📁 ##Common Files per Lab
File / Asset	Description
main.ino	Main Arduino sketch for the activity
main.py	Python script for serial or API interaction (when applicable)
main_functions.h	Header file containing reusable Arduino functions
breadboard_diagram.png	Wiring diagram or hardware schematic

⚠️ Not all labs include every file—only files relevant to the activity are provided.

--------------------------------------------------------------------------------------------------------------------------------------------

🛠️Tools & Technologies

Arduino IDE (for compiling and uploading sketches)

Python (with pyserial, requests, and FastAPI as required)

Visual Studio Code or any preferred code editor

Electronic components:

LEDs

Resistors

Push buttons

Thermistor

Photoresistor

Breadboard

Jumper wires

--------------------------------------------------------------------------------------------------------------------------------------------

📝Notes

Each lab is self-contained and should be used only within its respective folder.

Activities are organized into Midterms and Finals for easier navigation.

This repository serves as both a learning record and a project portfolio, demonstrating progression from basic Arduino I/O to IoT-style systems with web APIs.

--------------------------------------------------------------------------------------------------------------------------------------------

▶️How to Use

Open the specific lab folder you wish to run.

For Arduino-based activities:

Open main.ino in the Arduino IDE.

Select the correct board and port.

Upload the sketch.

For Python-enabled activities:

Install the required libraries.

Run main.py from the corresponding folder.

Follow breadboard_diagram.png (or equivalent) for correct hardware wiring.
