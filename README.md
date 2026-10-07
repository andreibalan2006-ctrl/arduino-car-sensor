# Arduino Car Parking Assistant (Distance Sensor)

This repository contains the hardware schematic and code for a Car Parking Assistant built with an Arduino Uno. The system uses an ultrasonic sensor to measure the distance to obstacles and provides visual and auditory warnings, similar to the parking sensors found in modern cars.

## 🚀 Project Overview
The system continuously calculates the distance to the nearest object in front of the ultrasonic sensor. Depending on how close the object is, it triggers different warning levels:
* **Safe Distance:** Green LED is ON.
* **Warning Distance:** Yellow LED is ON, and the buzzer beeps slowly.
* **Danger Distance:** Red LED is ON, and the buzzer emits a continuous/fast warning sound.

## 🛠️ Components Used
Based on the circuit diagram[cite: 8], the following components are required:
* 1x Arduino Uno
* 1x Breadboard
* 1x HC-SR04 Ultrasonic Sensor
* 3x LEDs (1x Red, 1x Yellow, 1x Green)
* 3x Current-limiting Resistors (e.g., 220Ω)
* 1x Piezo Buzzer
* Jumper wires

## ⚡ Circuit Connections
The hardware is wired as follows[cite: 8]:

**Power Supply:**
* Arduino **5V** -> Breadboard Positive (+) Rail
* Arduino **GND** -> Breadboard Negative (-) Rail

**Visual Indicators (LEDs):**
* **Red LED:** Anode to Arduino **Digital Pin 13**, Cathode to GND (via resistor)
* **Yellow LED:** Anode to Arduino **Digital Pin 12**, Cathode to GND (via resistor)
* **Green LED:** Anode to Arduino **Digital Pin 11**, Cathode to GND (via resistor)

**Ultrasonic Sensor (HC-SR04):**
* **VCC:** To 5V Rail
* **TRIG:** To Arduino **Digital Pin 9**
* **ECHO:** To Arduino **Digital Pin 8**
* **GND:** To GND Rail

**Auditory Warning (Buzzer):**
* **Positive Pin (+):** To Arduino **Digital Pin 2**
* **Negative Pin (-):** To GND Rail

## 💻 Code Setup
To run this project, upload the `.ino` file to your Arduino Uno using the Arduino IDE. Make sure the pin definitions in your code match the connections listed above.

## 📄 License
This project is open-source and available under the [MIT License](LICENSE).
