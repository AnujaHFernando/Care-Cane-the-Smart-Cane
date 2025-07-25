# Care-Cane-the-Smart-Cane
Care Cane is a smart cane for the visually impaired that offers obstacle detection, navigation help, fall alerts, and emergency messaging to improve safety and independence.
<img width="2643" height="2141" alt="Care Cane" src="https://github.com/user-attachments/assets/022cb34c-e6b3-480d-9ba1-02fcde996e3d" />


### Care Cane

**“Seeing Beyond Boundaries”**

#### Project Overview

Care Cane is an innovative smart white cane designed to enhance the mobility and safety of visually impaired users. It integrates advanced sensor technologies and wireless communication to provide real-time obstacle detection, navigation assistance, fall detection, and emergency alert functionalities. The cane’s core microcontroller (ESP32) processes sensor data and delivers feedback through vibration, sound, and visual indicators, ensuring users can navigate confidently and independently.

#### Key Features

* **Obstacle Detection & Avoidance**
  The cane uses two ultrasonic sensors strategically positioned to detect obstacles at both low and mid-level heights, covering a wide field to prevent collisions. When an obstacle is detected, the user receives haptic feedback via vibration motors embedded in the handle and auditory alerts from a buzzer, enabling immediate response.

* **Navigation Assistance**
  A GPS module continuously tracks the user’s real-time location. The system connects via Bluetooth to a smartphone app, which interfaces with Google Maps to provide turn-by-turn navigation. Directions are delivered discreetly through a combination of haptic pulses and voice prompts, allowing users to follow routes safely without relying solely on environmental cues.

* **Fall Detection & Emergency Support**
  Equipped with an accelerometer and gyroscope, the cane monitors sudden changes in motion to detect falls or unusual movements. Upon detecting a fall and lack of subsequent movement, the SIM900A GSM module automatically sends an SMS alert containing GPS coordinates and a predefined emergency message to selected contacts. Simultaneously, a buzzer and LED light pattern activate to attract nearby assistance.

* **Environmental Sensing**
  An ambient light sensor measures surrounding light conditions to optimize visual indicators on the cane, improving visibility and user awareness in various lighting environments.

* **Audio Feedback**
  A built-in speaker provides auditory cues for navigation, obstacle alerts, and system status, complementing vibration and visual feedback for comprehensive guidance.

#### Hardware Components

| Component                 | Function                                   |
| ------------------------- | ------------------------------------------ |
| ESP32 module              | Main microcontroller and communication hub |
| GPS module                | Real-time position tracking                |
| SIM900A module            | GSM communication for emergency alerts     |
| Ultrasonic sensors x2     | Detect obstacles at multiple heights       |
| Accelerometer & Gyroscope | Detect falls and motion anomalies          |
| Ambient Light Sensor      | Adjust visual indicators based on lighting |
| Vibration Motors x2       | Provide haptic feedback                    |
| Buzzer                    | Audible alerts                             |
| Speaker                   | Audio feedback                             |

#### System Architecture

* **Sensor Layer:** Ultrasonic sensors, accelerometer, gyro, and ambient light sensor collect environmental and motion data, feeding directly to the ESP32 microcontroller.
* **Processing & Control:** The ESP32 runs dedicated firmware managing sensor data, obstacle detection algorithms, fall detection logic, and communication protocols.
* **Connectivity & Feedback:** GPS and SIM900A modules connect via UART for location tracking and SMS alerts. Bluetooth facilitates data exchange with a smartphone app, which provides map display and voice guidance. User feedback is delivered through vibration motors, buzzer, speaker, and LEDs.

#### PCB & Mechanical Design

* **Custom PCB:** Designed using KiCad/Altium, the single-layer PCB integrates power regulation, sensor connections, and modular slots for GPS and SIM900A modules. Power-saving features extend battery life.
* **Casing & Assembly:** The cane’s ergonomic handle houses vibration motors, buzzer, speaker, and LED indicators within a lightweight ABS casing. A snap-fit design enables tool-free assembly and easy maintenance.
* **Packaging:** Eco-friendly packaging includes foam inserts for protection and comprehensive user manuals with quick-start guides and detailed instructions.

#### Prototype Assembly & Testing

* **PCB Assembly:** Surface-mount and through-hole components are soldered and tested for power integrity.
* **Module Integration:** GPS and SIM900A modules are plugged into headers; sensors are connected to GPIO pins.
* **Housing:** The PCB is inserted into the 3D-printed casing, secured with clips.
* **Testing:** The system is powered on for functional checks including obstacle detection alerts, fall simulation, emergency SMS sending, and smartphone app synchronization.

#### Smartphone Application & Google Maps Integration

* Utilizes the TinyGPS++ library to parse GPS data.
* Bluetooth connectivity (HC-05 or ESP32 BLE) enables communication with an Android app.
* The app displays the user’s real-time position on Google Maps and allows setting destination routes.
* Turn-by-turn directions are translated into haptic and audio cues sent back to the cane, guiding users safely along their path.


