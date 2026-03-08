# Arduino Ultrasonic Radar 📡

A functional radar system developed using an **Arduino Uno**, an **HC-SR04** ultrasonic sensor, and a servo motor. The project includes a custom-built Graphical User Interface (GUI) created in **Processing IDE** to visualize detected objects in real-time.

## 🚀 Overview
The radar scans a 150-degree area (from 15° to 165°) and detects objects within a 40cm range. The data is sent via Serial communication to the Processing application, which renders a classic radar display with a motion-blur effect.

![Radar in Action](radar.gif) 

## 🛠️ Hardware Components
* **Microcontroller:** Arduino Uno
* **Sensor:** HC-SR04 Ultrasonic Sensor
* **Actuator:** SG90 Servo Motor
* **Other:** Breadboard, Jumper wires

## 💻 Software & Technologies
* **C++ (Arduino):** Handles sensor data acquisition, servo control, and Serial data transmission.
* **Processing (Java-based):** Manages the GUI, real-time data parsing, and coordinate transformation (Polar to Cartesian).
* **Git:** Version control and project documentation.

## 🧠 Key Learnings
* **Serial Communication:** Implemented a custom data protocol (`angle,distance.`) to synchronize hardware and software.
* **Trigonometry:** Applied `sin()` and `cos()` functions to map sensor data onto a 2D coordinate system.
* **UI/UX Design:** Created a "motion blur" effect in Processing by using semi-transparent rectangles to simulate a real radar sweep.

## 📂 Project Structure
* `Arduino_Code/`: Contains the `.ino` file for the microcontroller.
* `Processing_Code/`: Contains the `.pde` sketch and necessary assets (fonts).
* `Media/`: Images and GIFs demonstrating the project.

## ⚙️ Setup Instructions
1. **Arduino:** Upload the code from `Arduino_Code/` to your board.
2. **Wiring:** Connect the components according to the pin definitions in the code (Trig: 10, Echo: 11, Servo: 12).
3. **Processing:** Open the sketch in `Processing_Code/`. 
4. **Port Configuration:** Ensure the `Serial.list()` or COM port in the Processing code matches your Arduino's port (e.g., `COM3`).
5. **Run:** Click the "Run" button in Processing to start the visualization.
