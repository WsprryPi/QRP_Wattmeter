# QRP RF Wattmeter: *A compact RF power meter designed for QRP transmitters.*

This project provides hardware and firmware for measuring RF output power and displaying the result digitally. The hardware is designed as a **carrier board (shield-style daughterboard)** that accepts an ESP32 module as a plug‑in controller.

The current reference controller board is the **Heltec WiFi LoRa 32 V3**, although this project does **not use WiFi, Bluetooth, or LoRa**.  
The module is used strictly as a convenient ESP32 microcontroller platform with integrated USB power and programming support.

---

## Project Overview

This repository contains a complete RF wattmeter system for low‑power transmitters.

The system consists of:

- RF sampling network
- RF power detector stage
- Analog conditioning amplifier
- ESP32 microcontroller interface
- Digital power display

The measurement front end converts RF power into a DC voltage that is read by the ESP32 ADC.  
Firmware then converts this value into calibrated RF power measurements.

---

## Hardware Architecture

The hardware implements the following signal chain:

RF input → sampling network → RF detector → analog scaling → ESP32 ADC

The detector stage converts RF power to a logarithmic DC voltage.  
An analog amplifier conditions this voltage so that the ESP32 ADC can measure it with good resolution.

The ESP32 then performs:

- ADC sampling
- calibration compensation
- power calculation
- display output

---

## ESP32 Controller Board

This design is intended to use the [Heltec WiFi LoRa 32 V3](https://heltec.org/project/wifi-lora-32-v3/) module as the controller board.

The module plugs into the wattmeter carrier board and provides:

- ESP32 microcontroller
- USB power and programming
- GPIO access
- ADC input

For this project:

- WiFi is not used
- Bluetooth is not used
- LoRa is not used

The board simply provides a convenient ESP32 platform.

---

## Hardware Features

- RF sampling tap for transmitter output
- RF power detection stage
- analog filtering and scaling
- ESP32 ADC interface
- calibration support
- test points for measurement and debugging
- plug‑in ESP32 controller module

The design is intended for **QRP transmitters up to approximately 1 W**.

---

## Documentation

Full documentation is available in the `docs/` directory and is designed to build with **Sphinx**.

The documentation covers:

- hardware overview
- schematic explanation
- PCB layout notes
- firmware architecture
- RF design details
- calibration procedure

---

## Calibration

Calibration is performed in software using known RF power levels.

Typical calibration procedure:

1. Connect a known RF source and dummy load
2. Apply known RF power levels
3. Record ADC values
4. Store calibration constants in firmware

The firmware then converts ADC readings into power values.

---

## Intended Use

This project is intended for:

- QRP transmitters
- amateur radio experiments
- RF measurement tools
- embedded firmware projects

---

## License

See the [LICENSE](LICENSE.md) file in this repository.

---

## Contributing

Pull requests, improvements, and suggestions are welcome.

<!-- Future Additions:

	•	schematic preview image
	•	project block diagram
	•	badges (RTD, license, build status)
	•	rendered directory tree
	•	calibration example plots
 -->
