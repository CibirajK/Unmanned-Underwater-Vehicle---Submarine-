
    # AI-Enabled Underwater Surveillance Robot for Lake and Pond Monitoring

[![License: MIT](https.svg)](https://opensource.org/licenses/MIT)

An ECE final year project. This repository contains all the code, hardware designs, and documentation for an autonomous underwater robot (AUV/ROV) designed for environmental monitoring and surveillance of freshwater bodies like lakes and ponds.

[Image or GIF of your finished robot here, once you have one]

## 🎯 Project Overview

The goal of this project is to create an intelligent, cost-effective robotic platform to autonomously patrol and monitor aquatic environments. The robot uses AI-driven computer vision to detect objects (e.g., pollution, debris, aquatic life) and collects real-time water quality data.

This system addresses the need for continuous, automated monitoring to maintain the health of inland water ecosystems.

### ✨ Key Features

* **Autonomous GPS Navigation:** Follows a pre-defined set of GPS waypoints to patrol a given area.
* **AI Object Detection:** On-board camera with a YOLOv8/MobileNet model trained to identify:
    * [Example: Underwater debris/trash]
    * [Example: Specific types of algae blooms]
    * [Example: Fish populations]
* **Real-Time Water Quality Monitoring:** Collects data on:
    * Temperature
    * pH Levels
    * Turbidity (water clarity)
* **Live Data Dashboard:** Transmits sensor data and video feed to a ground station (e.g., via a LoRa/RF link).
* **Obstacle Avoidance:** Uses [Example: ultrasonic sensors or sonar] to avoid collisions.

## 🛠️ Tech Stack & Hardware

This project is built with a combination of embedded systems, robotics, and AI.

### Software & AI
* **Main Controller:** Python (on Raspberry Pi)
* **Autopilot Firmware:** ArduSub (on a Pixhawk/flight controller)
* **Computer Vision:** OpenCV, TensorFlow Lite / PyTorch Mobile
* **Ground Station:** [Example: QGroundControl, or a custom web dashboard]

### Hardware Components
* **Main Computer:** Raspberry Pi 4 (or newer)
* **Flight Controller:** [Example: Pixhawk 4 Mini]
* **Chassis:** [Example: 3D-Printed frame, PVC pipe, or BlueROV components]
* **Propulsion:** 4-6x Brushless Thrusters with ESCs
* **Sensors:**
    * GPS Module (for surface navigation)
    * IMU (Inertial Measurement Unit)
    * [Example: Atlas Scientific pH & Turbidity sensors]
    * Waterproof Camera (e.g., Raspberry Pi Camera in housing)
* **Communication:** [Example: LoRa module or RFD900 for long-range data]

## 🚀 Getting Started

### 1. Hardware Setup

[Describe the main assembly steps. e.g.:]
1.  Assemble the 3D printed chassis (CAD files in `/hardware/cad_files/`).
2.  Mount the thrusters, electronics enclosure, and ballast.
3.  Wire the components according to the circuit diagram in (`/hardware/schematics/`).

### 2. Software Installation

1.  Clone this repository:
    ```bash
    git clone [https://github.com/](https://github.com/)[your-username]/AI-Underwater-Surveillance-Robot.git
    cd AI-Underwater-Surveillance-Robot
    ```
2.  Install required Python libraries:
    ```bash
    pip install -r requirements.txt
    ```
3.  Flash the ArduSub firmware to your flight controller.
4.  [Add other setup steps, like training the AI model]

### 3. Running the Robot

1.  Calibrate all sensors (IMU, GPS, water sensors).
2.  Configure the GPS waypoints in the ground station.
3.  Run the main control script:
    ```bash
    python src/main.py
    ```

## 📖 Project Structure

```
/AI-Underwater-Surveillance-Robot
│
├── 📄 README.md              # You are here!
├── 📄 requirements.txt         # Python libraries
│
├──  hardware/                # Schematics, 3D models, PCB designs
├── src/                     # All source code
│   ├── 1_navigation/          # GPS guidance, obstacle avoidance
│   ├── 2_computer_vision/     # Object detection scripts
│   ├── 3_sensor_integration/  # Water quality sensor code
│   └── ...
├── datasets/                # Sample images for training the AI
└── docs/                    # Final project report, research
```

## Contributors

* **[Your Name]** - Project Lead, Developer

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE) file for details.
