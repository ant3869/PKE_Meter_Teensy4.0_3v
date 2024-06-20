# PKE Meter with Teensy 4.0 and DFRobot Sensors

This project integrates multiple sensors (H2S, CO, VOC, CH4) with visual and audio feedback using LEDs, a servo, and a DFPlayer Mini.

## Table of Contents

- [Introduction](#introduction)
- [Hardware](#hardware)
- [Software](#software)
- [Pin Definitions](#pin-definitions)
- [Features](#features)
- [Setup](#setup)
- [Usage](#usage)
- [Troubleshooting](#troubleshooting)
- [Contributing](#contributing)
- [License](#license)

## Introduction

The PKE Meter is a versatile environmental sensing tool that uses a Teensy 4.0 microcontroller to monitor various gas levels (H2S, CO, VOC, CH4). It provides real-time feedback via an LED array, a servo motor, and sound through a DFPlayer Mini.

## Hardware

### Components

- Teensy 4.0
- DFRobot H2S Sensor
- DFRobot CO Sensor
- DFRobot VOC Sensor
- DFRobot CH4 Sensor
- DFPlayer Mini MP3 Player
- Adafruit ST7789 TFT Display
- Servo Motor
- LEDs (7)
- Various resistors, capacitors, and connectors

### Pin Definitions

- **Servo Pin:** A7
- **Sound Potentiometer Pin:** A1
- **Volume Potentiometer Pin:** A2
- **DFPlayer Mini:** RX (Pin 7), TX (Pin 8)
- **LED Pins:** 0-6
- **H2S Sensor Pin:** A3
- **CO Sensor Pin:** A4
- **VOC Sensor Pin:** A5
- **CH4 Sensor Pin:** A6

### Display (Adafruit ST7789)

- **TFT_CS:** 10
- **TFT_DC:** 9
- **TFT_RST:** 8
- **TFT_SCK:** 13
- **TFT_MOSI:** 11

## Software

### Libraries

This project uses the following libraries:

- `Wire`
- `Servo`
- `Ramp`
- `TimerOne`
- `DFRobotDFPlayerMini`
- `Adafruit_GFX`
- `Adafruit_ST7789`
- `SPI`

### Features

- **Sensor Integration:** Reads values from H2S, CO, VOC, and CH4 sensors.
- **Visual Feedback:** Displays readings on an ST7789 TFT display and uses LEDs for visual indicators.
- **Audio Feedback:** Plays sounds using DFPlayer Mini based on sensor readings.
- **Servo Control:** Moves a servo motor based on sensor data.
- **Debug Mode:** Includes a debug mode for easier troubleshooting and monitoring.

## Setup

1. **Clone the repository:**

    ```sh
    git clone https://github.com/yourusername/PKEMeter.git
    cd PKEMeter
    ```

2. **Install required libraries:**

    Ensure you have all the required libraries installed in your Arduino IDE.

3. **Upload the Sketch:**

    Open the `PKEMeter.ino` file in the Arduino IDE and upload it to your Teensy 4.0.

4. **Connect the Hardware:**

    Follow the pin definitions to connect your sensors, LEDs, display, servo, and DFPlayer Mini.

## Usage

1. **Power the System:**

    Connect the power supply to your Teensy 4.0.

2. **Monitor the Readings:**

    The TFT display will show the sensor readings. LEDs will light up based on the readings, and the servo will move accordingly. The DFPlayer Mini will play sounds based on the sensor data.

3. **Adjust Volume:**

    Use the volume potentiometer to adjust the sound level.

4. **Debug Mode:**

    If debug mode is enabled, use the Serial Monitor to view debug messages.

## Troubleshooting

- **No Display Output:** Check connections to the TFT display and ensure correct pin definitions.
- **No Sound:** Verify connections to the DFPlayer Mini and check if the audio files are correctly loaded on the SD card.
- **Servo Not Moving:** Ensure the servo is properly connected and powered.
- **LEDs Not Lighting Up:** Check LED connections and ensure the correct pin definitions.

## Contributing

Contributions are welcome! Please fork the repository and submit a pull request.

## License

This project is licensed under the MIT License.
